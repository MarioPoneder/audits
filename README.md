# Public Findings

For more info, visit: https://decentra.vision/

## Index
- [Team Engagements](#team-engagements)
- [Solo Engagements](#solo-engagements)
- [Shieldify](#shieldify)
- [Code4rena](#code4rena)
- [Cantina](#cantina)
- [Sherlock](#sherlock)
- [Hats Finance (Bug Bounty)](./HatsFinance_BugBounties)

---

## Team Engagements

| Begin month | Project | Category | Provider | Duration | Platform |
| :---: | :--- | :---  | :--- | :---: | :--- |
| 2024-09 | To be disclosed | AMM, DEX | Spearbit | 4.0 weeks | Solidity / EVM |
| 2024-08 | To be disclosed | Stablecoin, Liquid staking, Futures | Pashov Audit Group | 1.0 weeks | Solidity / EVM |
| 2024-08 | Aurora BTC Light Client | Bitcoin client, Relay | AuditOne | 1.0 weeks | Rust / NEAR |
| 2024-07 | To be disclosed | Proof of Liquidity, Staking, Voting | Spearbit | 3.0 weeks | Solidity / EVM |
| 2024-06 | Undisclosed | Cross-chain, Liquidity, Messaging | Oak Security | 3.0 weeks | Rust / Solana |
| 2024-06 | [Out GCC](https://github.com/oak-security/audit-reports/blob/main/Out/2024-09-24%20Audit%20Report%20-%20Out%20GCC.pdf) | Tokenization, Marketplace | Oak Security | 1.0 weeks | Rust / Solana |
| 2024-06 | [Sharwa Finance](https://github.com/pashov/audits/blob/master/team/pdf/SharwaFinance-security-review.pdf) | Margin trading, Options | Pashov Audit Group | 1.0 weeks | Solidity / EVM |
| 2024-06 | Undisclosed | Cross-chain, Airdrop | Pashov Audit Group | 0.4 weeks | Solidity / EVM |
| 2024-05 | [Pendle Finance](https://github.com/spearbit/portfolio/blob/master/pdfs/Pendle-Spearbit-Security-Review-July-2024.pdf) | Tokenization, Yield trading | Spearbit | 3.0 weeks | Solidity / EVM |
| 2024-04 | Undisclosed | Game, Infrastructure | Oak Security | 1.1 weeks | Rust / Substrate |

## Solo Engagements

| Begin month | Project | Category | Provider | Duration | Platform |
| :---: | :--- | :--- | :--- | :---: | :--- |
| 2024-07 | [Possum Core](https://gist.github.com/MarioPoneder/abfae63a5b456a1edf683d55266bbbaf) ([ref](https://possum-labs.gitbook.io/docs/security/audits)) | Governance, Staking | Decentra Vision | 0.8 weeks | Solidity / EVM |
| 2024-06 | [Proportionalized Contracts](https://gist.github.com/MarioPoneder/dd1e90a40364bbefce24a1141b729017) | Fee token, Staking | Decentra Vision | 0.8 weeks | Solidity / EVM |
| 2024-05 | [Yeet Cup](https://github.com/shieldify-security/audits-portfolio/blob/main/reports/Yeet-Security-Review.pdf)  | Game, Yield | Shieldify | 0.8 weeks | Solidity / EVM |
| 2024-03 | [Olas Lockbox v2 - Mitigation review](https://github.com/valory-xyz/lockbox-solana/blob/13859c034d4be1286b3f2f0458aed435adef9c19/lockbox2/doc/External_Audit_LockboxV2.pdf) | Liquidity bonding | Cantina | 0.4 weeks | Rust / Solana |

---

## [Shieldify](https://www.shieldify.org/)

### 2024-03: [Possum Labs Portals v2](https://github.com/shieldify-security/audits-portfolio/blob/main/reports/PossumLabs-V2-Security-Review.pdf)  :2nd_place_medal:

| Risk | Title | Finding in report |
| :---: | :--- | :---: |
| 🟨<br>Medium | Investors could earn 10x more than intended | M-01 |
| 🟦<br>Low | Cannot revoke permit of MintBurnToken | L-02 |

### 2024-02: [Ion Protocol](https://github.com/shieldify-security/audits-portfolio/blob/main/reports/Ion-Security-Review.pdf)  :1st_place_medal:

| Risk | Title | Finding in report |
| :---: | :--- | :---: |
| 🟨<br>Medium | Unsafe downcast truncation in UniswapOracleLibrary leading to invalid price data | M-01 |

## [Code4rena](https://code4rena.com/)

### Judging

* **2024-07**: [BendDAO Invitational](https://code4rena.com/audits/2024-07-benddao-invitational)
* **2024-05**: [Lavarage Appellate Court](https://github.com/code-423n4/2024-04-lavarage-findings/discussions/36)
* **2024-03**: [Neobase Invitational](https://code4rena.com/audits/2024-03-neobase-invitational)
* **2024-02**: [Code4rena Blue](https://code4rena.com/blog/introducing-code4rena-blue-more-than-just-bug-bounties) Bug Bounty submissions (undisclosed)
* **2024-02**: [UniStaker Infrastructure](https://code4rena.com/audits/2024-02-unistaker-infrastructure)
* **2023-12**: [Revolution Protocol ](https://code4rena.com/audits/2023-12-revolution-protocol)
* **2023-11**: [Canto Application Specific Dollars and Bonding Curves for 1155s](https://code4rena.com/audits/2023-11-canto-application-specific-dollars-and-bonding-curves-for-1155s)
* **2023-10**: [The Wildcat Protocol](https://code4rena.com/audits/2023-10-the-wildcat-protocol)

### 2024-03: [Acala](https://code4rena.com/audits/2024-03-acala)
<sup>Rust / Substrate</sup>

| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟨<br>Medium | [Incentive accumulation can be sandwiched with additional shares to gain advantage over long-term depositors](https://github.com/code-423n4/2024-03-acala-findings/issues/88) | [M-02](https://code4rena.com/reports/2024-03-acala#m-02-incentive-accumulation-can-be-sandwiched-with-additional-shares-to-gain-advantage-over-long-term-depositors) |

### 2024-03: [Canto Invitational](https://code4rena.com/audits/2024-03-canto-invitational) :2nd_place_medal:

| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [Native gas tokens can become stuck in ASDRouter contract](https://github.com/code-423n4/2024-03-canto-findings/issues/6) | [H-01](https://code4rena.com/reports/2024-03-canto#h-01-native-gas-tokens-can-become-stuck-in-asdrouter-contract) |
| 🟥<br>High | [Dual transaction nature of composed message transfer allows anyone to steal user funds](https://github.com/code-423n4/2024-03-canto-findings/issues/5) | [H-02](https://code4rena.com/reports/2024-03-canto#h-02-dual-transaction-nature-of-composed-message-transfer-allows-anyone-to-steal-user-funds) |
| 🟨<br>Medium | [Removing token from the whitelist may cause DoS due to limited USDC amount](https://code4rena.com/reports/2024-03-canto#m-03-removing-token-from-the-whitelist-may-cause-dos-due-to-limited-usdc-amount) |  |
| 🟦<br>Low | [Low Risk and Non-Critical Issues](https://github.com/code-423n4/2024-03-canto-findings/issues/9) | [QA](https://code4rena.com/reports/2024-03-canto#low-risk-and-non-critical-issues) |

### 2024-03: [Phat Contract Runtime](https://code4rena.com/audits/2024-03-phat-contract-runtime) :3rd_place_medal:
<sup>Rust / Substrate</sup>

<details>
<summary><b>Related tweet</b></summary>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Awards have been announced for the $60,500 USDC <a href="https://twitter.com/PhalaNetwork?ref_src=twsrc%5Etfw">@PhalaNetwork</a> audit! 🥳<br><br>Top 5:<br>🥇 <a href="https://twitter.com/DadeKuma?ref_src=twsrc%5Etfw">@DadeKuma</a> - $15,937.95 USDC<br>🥈 zhaojie - $15,225.87 USDC<br>🥉 <a href="https://twitter.com/MarioPoneder?ref_src=twsrc%5Etfw">@MarioPoneder</a> - $12,619.42 USDC<br>🏅 Koolex - $2,606.45 USDC<br>🏅 Cryptor - $994.09 USDC <a href="https://t.co/C15fmXxxJ2">pic.twitter.com/C15fmXxxJ2</a></p>&mdash; Code4rena (@code4rena) <a href="https://twitter.com/code4rena/status/1774840564347007466?ref_src=twsrc%5Etfw">April 1, 2024</a></blockquote>
</details>

| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟨<br>Medium | [Limited availability of balance_of(...) method](https://github.com/code-423n4/2024-03-phala-network-findings/issues/50) | [M-01](https://code4rena.com/reports/2024-03-phala-network#m-01-limited-availability-of-balance_of-method) |

### 2024-01: [Opus](https://code4rena.com/audits/2024-01-opus) :3rd_place_medal:
<sup>Rust / Starknet</sup>

<details>
<summary><b>Related tweet</b></summary>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Rounding out the Top 3 was <a href="https://twitter.com/MarioPoneder?ref_src=twsrc%5Etfw">@MarioPoneder</a>! 🥉<br><br>Rank: #3 (#86 All-time) <br>Medium-risk findings: 2 (2 solo) <a href="https://t.co/vCgs0GlnQY">pic.twitter.com/vCgs0GlnQY</a></p>&mdash; Code4rena (@code4rena) <a href="https://twitter.com/code4rena/status/1765461990728708298?ref_src=twsrc%5Etfw">March 6, 2024</a></blockquote>
</details>

| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟨<br>Medium | [Collateral cannot be withdrawn from trove once yang is suspended](https://github.com/code-423n4/2024-01-opus-findings/issues/48) | [M-07](https://code4rena.com/reports/2024-01-opus#m-07-collateral-cannot-be-withdrawn-from-trove-once-yang-is-suspended) |
| 🟨<br>Medium | [Unhealthy troves with LTV > 90% cannot always be absorbed as intended](https://github.com/code-423n4/2024-01-opus-findings/issues/11) | [M-09](https://code4rena.com/reports/2024-01-opus#m-09-unhealthy-troves-with-ltv--90-cannot-always-be-absorbed-as-intended) |
| 🟦<br>Low | [Low Risk and Non-Critical Issues](https://github.com/code-423n4/2024-01-opus-findings/issues/85) | [QA](https://code4rena.com/reports/2024-01-opus#low-risk-and-non-critical-issues) |

### 2023-12: [Olas](https://code4rena.com/audits/2023-12-olas)
| Risk | Title |
| :---: | :--- | 
| 🟥<br>High | [Bonds created in year cross epoch’s can lead to lost payouts](https://code4rena.com/reports/2023-12-autonolas#h-04-bonds-created-in-year-cross-epochs-can-lead-to-lost-payouts-) |

### 2023-10: [zkSync Era](https://code4rena.com/audits/2023-10-zksync-era)
| Risk | Title |
| :---: | :--- | 
| 🟨<br>Medium | [Incorrect max precompile address](https://code4rena.com/reports/2023-10-zksync#m-04-incorrect-max-precompile-address) |
| 🟦<br>Low | [EIP-1559 transactions can be invoked from kernel space accounts due to missing assertion in bootloader](https://github.com/code-423n4/2023-10-zksync-findings/issues/224) |
| 🟦<br>Low | [EIP-712 transactions via custom accounts do not comply with EIP-3607 and could therefore fail](https://github.com/code-423n4/2023-10-zksync-findings/issues/322) |
| 🟦<br>Low | [State changes are preserved on failed L2 transactions using custom account abstraction](https://github.com/code-423n4/2023-10-zksync-findings/issues/469) |
| 🟦<br>Low | [Users can avoid paying fees for failed L2 transactions](https://github.com/code-423n4/2023-10-zksync-findings/issues/520) |

### 2023-09: [Maia DAO - Ulysses](https://code4rena.com/contests/2023-09-maia-dao-ulysses)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [All tokens can be stolen from VirtualAccount due to missing access modifier](https://github.com/code-423n4/2023-09-maia-findings/issues/885) |[H-01](https://code4rena.com/reports/2023-09-maia#h-01-all-tokens-can-be-stolen-from-virtualaccount-due-to-missing-access-modifier) |

### 2023-09: [Venus Prime](https://code4rena.com/contests/2023-09-venus-prime)
| Risk | Title |
| :---: | :--- |
| 🟥<br>High | [Prime contract incompatible with currently deployed / active markets (vToken) with 8 decimals](https://github.com/code-423n4/2023-09-venus-findings/issues/85) |
| 🟥<br>High | [Prime contract incompatible with underlying assets differing from 18 decimals](https://github.com/code-423n4/2023-09-venus-findings/issues/91) |

### 2023-08: [Chainlink Staking v0.2](https://code4rena.com/audits/2023-08-chainlink-staking-v02)
Findings under NDA, requires [Code4rena backstage access](https://docs.code4rena.com/roles/certified-contributors/backstage-wardens#to-request-+backstage-access).
| Risk | Title |
| :---: | ---: |
| 🟨<br>Medium | #223 |

### 2023-08: [Dopex](https://code4rena.com/contests/2023-08-dopex)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟨<br>Medium | [Change of fundingDuration causes "time travel" of PerpetualAtlanticVault.nextFundingPaymentTimestamp()](https://github.com/code-423n4/2023-08-dopex-findings/issues/850) |[M-10](https://code4rena.com/reports/2023-08-dopex#m-10-change-of-fundingduration-causes-time-travel-of-perpetualatlanticvaultnextfundingpaymenttimestamp) |
| 🟦<br>Low | [RdpxV2Core.removeAssetFromtokenReserves(...) irrecoverably breaks reserve token handling](https://github.com/code-423n4/2023-08-dopex-findings/issues/717) |  |

### 2023-08: [Arbitrum Security Council Election System](https://code4rena.com/contests/2023-08-arbitrum-security-council-election-system)
| Risk | Title |
| :---: | :--- |
| 🟨<br>Medium | [SecurityCouncilNomineeElectionGovernorTiming.electionToTimestamp(...) can create unsupported/invalid dates](https://github.com/code-423n4/2023-08-arbitrum-findings/issues/11) |

### 2023-07: [Tapioca DAO](https://code4rena.com/contests/2023-07-tapioca-dao)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [User can give himself approval for all assets held by MagnetarV2 contract](https://github.com/code-423n4/2023-07-tapioca-findings/issues/832) |[H-49](https://code4rena.com/reports/2023-07-tapioca#h-49-user-can-give-himself-approval-for-all-assets-held-by-magnetarv2-contract) |
| 🟥<br>High | [MagnetarMarketModule.depositRepayAndRemoveCollateralFromMarket(...) can be invoked with other user's tokens](https://github.com/code-423n4/2023-07-tapioca-findings/issues/650) | |
| 🟨<br>Medium | [Double accounting of action value in MagnetarV2.burst(...)](https://github.com/code-423n4/2023-07-tapioca-findings/issues/793) |  |
| 🟦<br>Low | [Multicall3 ignores allowFailure leading to DoS](https://github.com/code-423n4/2023-07-tapioca-findings/issues/816) |  |

### 2023-07: [Axelar Network](https://code4rena.com/contests/2023-07-axelar-network)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟨<br>Medium | [Insufficient support for tokens with different decimals on different chains lead to loss of funds on cross-chain bridging](https://github.com/code-423n4/2023-07-axelar-findings/issues/52) |[M-08](https://code4rena.com/reports/2023-07-axelar#m-08-insufficient-support-for-tokens-with-different-decimals-on-different-chains-lead-to-loss-of-funds-on-cross-chain-bridging) |

### 2023-05: [Maia DAO Ecosystem](https://code4rena.com/contests/2023-05-maia-dao-ecosystem)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [UlyssesToken asset ID accounting error](https://github.com/code-423n4/2023-05-maia-findings/issues/275) | [H-25](https://code4rena.com/reports/2023-05-maia#h-25-ulyssestoken-asset-id-accounting-error) |
| 🟥<br>High | [Ulysses Omnichain support for tokens with other than 18 decimals is fundamentally flawed](https://github.com/code-423n4/2023-05-maia-findings/issues/498) |  |
| 🟨<br>Medium | [RootBridgeAgent.redeemSettlement can be front-run using RootBridgeAgent.retrySettlement causing redeem DoS](https://github.com/code-423n4/2023-05-maia-findings/issues/869) | [M-03](https://code4rena.com/reports/2023-05-maia#m-03-rootbridgeagentredeemsettlement-can-be-front-run-using-rootbridgeagentretrysettlement-causing-redeem-to-dos) |
| 🟨<br>Medium | [Maia Governance token balance dilution in vMaia vault is breaking the conversion rate mechanism](https://github.com/code-423n4/2023-05-maia-findings/issues/473) | [M-22](https://code4rena.com/reports/2023-05-maia#m-22-maia-governance-token-balance-dilution-in-vmaia-vault-is-breaking-the-conversion-rate-mechanism) |
| 🟨<br>Medium | [Claiming outstanding utility tokens from vMaia vault DoS on pbHermes<>bHermes conversion rate > 1](https://github.com/code-423n4/2023-05-maia-findings/issues/470) | [M-23](https://code4rena.com/reports/2023-05-maia#m-23-claiming-outstanding-utility-tokens-from-vmaia-vault-dos-on-pbhermesbhermes-conversion-rate--1) |
| 🟨<br>Medium | [UlyssesToken.setWeights(...) can cause user loss of assets on vault deposits/withdrawals](https://github.com/code-423n4/2023-05-maia-findings/issues/281) | [M-34](https://code4rena.com/reports/2023-05-maia#m-34-ulyssestokensetweights-can-cause-user-loss-of-assets-on-vault-depositswithdrawals) |
| 🟨<br>Medium | [Withdrawal from vMaia vault only on first Tuesday of the month is not strictly enforced](https://github.com/code-423n4/2023-05-maia-findings/issues/396) |  |
| 🟦<br>Low | [Payable method RootBridgeAgent.retrySettlement can lead to loss of funds for users](https://github.com/code-423n4/2023-05-maia-findings/issues/811) |  |

### 2023-05: [Chainlink Cross-Chain Services: CCIP and ARM Network](https://code4rena.com/contests/2023-05-chainlink-cross-chain-services-ccip-and-arm-network)
Findings under NDA, requires [Code4rena backstage access](https://docs.code4rena.com/roles/certified-contributors/backstage-wardens#to-request-+backstage-access).
| Risk | Title |
| :---: | ---: |
| 🟥<br>High | #164 |
| 🟨<br>Medium | #95 |
| 🟨<br>Medium | #307 |

### 2023-05: [Ajna Protocol](https://code4rena.com/contests/2023-05-ajna-protocol)
| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [Position NFT can be spammed with insignificant positions by anyone until rewards DoS](https://github.com/code-423n4/2023-05-ajna-findings/issues/488) | [H-03](https://code4rena.com/reports/2023-05-ajna#h-03-position-nft-can-be-spammed-with-insignificant-positions-by-anyone-until-rewards-dos) |
| 🟥<br>High | [Permanent loss of rewards on temporary underfunding of RewardsManager contract](https://github.com/code-423n4/2023-05-ajna-findings/issues/114) ||

### 2023-04: [EigenLayer](https://code4rena.com/contests/2023-04-eigenlayer-contest) :1st_place_medal:
<details>
<summary><b>Related tweet</b></summary>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Awards have been announced for the $90,500 USDC <a href="https://twitter.com/eigenlayer?ref_src=twsrc%5Etfw">@eigenlayer</a> audit 🤝<br><br>Top 5:<br>🥇 <a href="https://twitter.com/MarioPoneder?ref_src=twsrc%5Etfw">@MarioPoneder</a> - $13,081.90 USDC<br>🥈 volodya - $12,193.66 USDC<br>🥉 windowhan001 - $5,031.50 USDC<br>🏅 <a href="https://twitter.com/CyfrinAudits?ref_src=twsrc%5Etfw">@CyfrinAudits</a> - $3,177.34 USDC<br>🏅 <a href="https://twitter.com/QiuhaoLi?ref_src=twsrc%5Etfw">@QiuhaoLi</a> - $2,972.95 USDC </p>&mdash; Code4rena (@code4rena) <a href="https://twitter.com/code4rena/status/1667379760614502402?ref_src=twsrc%5Etfw">June 10, 2023</a></blockquote>
</details>

| Risk | Title | Selected for report |
| :---: | :--- | :---: |
| 🟥<br>High | [Slot and block number proofs not required for verification of withdrawal (multiple withdrawals possible)](https://github.com/code-423n4/2023-04-eigenlayer-findings/issues/388) | [H-01](https://code4rena.com/reports/2023-04-eigenlayer#h-01-slot-and-block-number-proofs-not-required-for-verification-of-withdrawal-multiple-withdrawals-possible) |

### 2023-04: [Rubicon v2](https://code4rena.com/contests/2023-04-rubicon-v2)
Findings under NDA, requires [Code4rena backstage access](https://docs.code4rena.com/roles/certified-contributors/backstage-wardens#to-request-+backstage-access).
| Risk | Title |
| :---: | ---: |
| 🟥<br>High | #1214 |
| 🟥<br>High | #1265 |

### 2023-04: [Caviar Private Pools](https://code4rena.com/contests/2023-04-caviar-private-pools)
| Risk | Title |
| :---: | :--- |
| 🟥<br>High | [Owner of PrivatePool can steal any NFTs and tokens that the pool has approval for](https://github.com/code-423n4/2023-04-caviar-findings/issues/63) |
| 🟨<br>Medium | [PrivatePool creation can be front-run](https://github.com/code-423n4/2023-04-caviar-findings/issues/92) |

### 2023-02: [Ethos Reserve](https://code4rena.com/contests/2023-02-ethos-reserve-contest)
| Risk | Title |
| :---: | :--- |
| 🟨<br>Medium | [Strategy emergency exit (guardian privileges) harvest amount can be reduced with strategist privileges](https://github.com/code-423n4/2023-02-ethos-findings/issues/262) |
| 🟨<br>Medium | [Inconsistent support of ERC20 tokens that deduct transaction fee](https://github.com/code-423n4/2023-02-ethos-findings/issues/477) |
| 🟦<br>Low | [Strategy contract upgrade can be prevented by lower privileged roles](https://github.com/code-423n4/2023-02-ethos-findings/issues/359) |

---

## [Cantina](https://cantina.xyz/)

### 2024-02: [3DNS](https://cantina.xyz/code/cdb738fd-0e7f-4a6b-9073-2b8629bfc1c3/README.md)

| Risk | Title |
| :---: | :--- |
| 🟥<br>High | [Anyone can drain the whole ETH balance of ThreeDNSRegControl when making a commitment](https://cantina.xyz/code/cdb738fd-0e7f-4a6b-9073-2b8629bfc1c3/findings/1517fb44-4b0c-400f-a0ec-5e0520852ae5) |
| 🟨<br>Medium | [Safe transfers of registrations to ERC-721 receiver contracts which also have a fallback method will always fail](https://cantina.xyz/code/cdb738fd-0e7f-4a6b-9073-2b8629bfc1c3/findings/d64dc4d0-897c-47c5-af64-940270315c9a) |
| 🟨<br>Medium | [Batch transfers of registrations to contracts will always fail due to an invalid selector check](https://cantina.xyz/code/cdb738fd-0e7f-4a6b-9073-2b8629bfc1c3/findings/f3740093-04e2-4717-ad14-8b8d70451b21) |

### 2024-01: [Olas Lockbox](https://cantina.xyz/competitions/829164bf-7fba-4b84-a6b8-76652205bd97) 🥈
<sup>Rust / Solana</sup>

<details>
<summary><b>Related tweet</b></summary>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Congratulations to our resident rustaceans on an excellent job during the <a href="https://twitter.com/autonolas?ref_src=twsrc%5Etfw">@autonolas</a> security competition.<br><br>Here are your top 3 placements:<br><br>🥇: <a href="https://twitter.com/99Crits?ref_src=twsrc%5Etfw">@99crits</a> - $22,275.61<br>🥈: <a href="https://twitter.com/MarioPoneder?ref_src=twsrc%5Etfw">@MarioPoneder</a> - $8,590.35<br>🥉: <a href="https://twitter.com/meltedblocks?ref_src=twsrc%5Etfw">@meltedblocks</a> - $6,682.68<br><br>Full Results Below! <a href="https://t.co/Cr5ATXONbQ">pic.twitter.com/Cr5ATXONbQ</a></p>&mdash; Cantina 🪐 (@cantinaxyz) <a href="https://twitter.com/cantinaxyz/status/1769846698514231628?ref_src=twsrc%5Etfw">March 18, 2024</a></blockquote>
</details>

| Risk | Title |
| :---: | :--- |
| 🟨<br>Medium | [Attacker can create token account for NFT position to cause deposit DoS](https://cantina.xyz/code/829164bf-7fba-4b84-a6b8-76652205bd97/findings/94fb8f14-7aaf-4d87-9001-84b9e2ca856e) |
| 🟨<br>Medium | [DoS on simultaneous deposit due to id restriction](https://cantina.xyz/code/829164bf-7fba-4b84-a6b8-76652205bd97/findings/a00c4470-fe01-4172-8f21-df12ad6c2e71) |
| 🟦<br>Low | [Missing mutable constraint leads to withdrawal DoS due to read-only signer](https://cantina.xyz/code/829164bf-7fba-4b84-a6b8-76652205bd97/findings/7f40f7ec-a1da-4dd7-b40f-90664389b586) |
| 🟦<br>Low | [Attacker can frontrun lockbox initialization to provide own fee token accounts](https://cantina.xyz/code/829164bf-7fba-4b84-a6b8-76652205bd97/findings/e92ec89f-9397-4c3a-839a-162fed09c2b9) |

### 2023-11: [Superform](https://cantina.xyz/competitions/2cd0b038-3e32-4db6-b488-0f85b6f0e49f)
| Risk | Title |
| :---: | :--- |
| 🟨<br>Medium | [Insufficient support for fee-on-transfer tokens](https://cantina.xyz/code/2cd0b038-3e32-4db6-b488-0f85b6f0e49f/findings/cdee2f91-6ad6-4326-8ca9-7c1a2cce4233) |
| 🟦<br>Low | [ArrayCastLib.castToMultiVaultData(...) does not preserve values of hasDstSwap and retain4626](https://cantina.xyz/code/2cd0b038-3e32-4db6-b488-0f85b6f0e49f/findings/5cf83a4f-397f-428a-846f-7777db33c676) |
| 🟦<br>Low | [Timing overlap of dispute/finalizeRescueFailedDeposits(...) methods](https://cantina.xyz/code/2cd0b038-3e32-4db6-b488-0f85b6f0e49f/findings/11c3eed3-9cc2-4fa2-987a-41d2764bd921) |

### 2023-11: [Morpho Blue](https://cantina.xyz/competitions/d86b7f95-e574-4092-8ea2-78dcac2f54f1)
| Risk | Title |
| :---: | :--- |
| 🟦<br>Low | [Interest/fee accrual can be suppressed in regular markets with low-decimal loan tokens](https://cantina.xyz/code/d86b7f95-e574-4092-8ea2-78dcac2f54f1/findings/4e7fb083-542d-4e9b-8da4-1799cea8ee26) |
| 🟦<br>Low | [Oracles should be whitelisted to avoid theft by direct price manipulation](https://cantina.xyz/code/d86b7f95-e574-4092-8ea2-78dcac2f54f1/findings/c6dc5ae3-4081-4406-a1ee-2aa85fbde59c) |

---

## [Sherlock](https://app.sherlock.xyz/)
Note that I am also listing issues here which were labeled as `Excluded` due to the strict `High`/`Medium` only policy at Sherlock.  
However, those issues are still valid & valuable for the sponsor and most of them contain a coded PoC, therefore they might be a good read for new aspiring auditors.

### 2023-07: [Perennial V2](https://audits.sherlock.xyz/contests/106)
| Risk | Title |
| :---: | :--- |
| 🟦<br>Low | [DSU token balance of MultiInvoker contract can be drained by anyone](https://github.com/sherlock-audit/2023-07-perennial-judging/issues/67) |

### 2023-06: [Tokemak](https://audits.sherlock.xyz/contests/101)
| Risk | Title |
| :---: | :--- |
| 🟥<br>High | [Rewards can be drained due to incorrect handling of userRewardPerTokenPaid accounting](https://github.com/sherlock-audit/2023-06-tokemak-judging/issues/270) |
| 🟥<br>High | [LiquidationRow.liquidateVaultsForToken(...) will always revert due to missing token transfers](https://github.com/sherlock-audit/2023-06-tokemak-judging/issues/509) |
| 🟦<br>Low | [LMPVaultRouter mint and deposit entry-points can be blocked by anyone](https://github.com/sherlock-audit/2023-06-tokemak-judging/issues/241) |

### 2023-06: [Index Update](https://audits.sherlock.xyz/contests/91)
| Risk | Title |
| :---: | :--- |
| 🟦<br>Low | [New auction rebalance can be started before previous one concluded or duration elapsed](https://github.com/sherlock-audit/2023-06-Index-judging/issues/22) |
| 🟦<br>Low | [Insufficient validation of auction execution price adapter config data](https://github.com/sherlock-audit/2023-06-Index-judging/issues/24) |
| 🟦<br>Low | [SetToken can be indefinitely locked by AuctionRebalanceModule](https://github.com/sherlock-audit/2023-06-Index-judging/issues/25) |

