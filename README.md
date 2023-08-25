# Public Audit Findings

Being unable to publicly share my past proprietary development work and [Immunefi](https://immunefi.com/) findings, I am glad that I've started to participate in decentralized audits which allows me to publish my bug reports once they are judged.

## [Code4rena](https://code4rena.com/)

### 2023-08: [Arbitrum Security Council Election System](https://code4rena.com/contests/2023-08-arbitrum-security-council-election-system)
Findings not available yet.

### 2023-07: [Tapioca DAO](https://code4rena.com/contests/2023-07-tapioca-dao)
Findings not available yet.

### 2023-07: [Axelar Network](https://code4rena.com/contests/2023-07-axelar-network)
Findings not available yet.

### 2023-05: [Maia DAO Ecosystem](https://code4rena.com/contests/2023-05-maia-dao-ecosystem)
Findings not available yet.

### 2023-05: [Chainlink Cross-Chain Services: CCIP and ARM Network](https://code4rena.com/contests/2023-05-chainlink-cross-chain-services-ccip-and-arm-network)
Findings under NDA, requires [Code4rena backstage access](https://docs.code4rena.com/roles/certified-contributors/backstage-wardens#to-request-+backstage-access).
| Risk | Title |
| :--- | ---: |
| High | #164 |
| Medium | #95 |
| Medium | #307 |

### 2023-05: [Ajna Protocol](https://code4rena.com/contests/2023-05-ajna-protocol)
| Risk | Title | Included in report |
| :--- | :--- | :---: |
| High | [Permanent loss of rewards on temporary underfunding of RewardsManager contract](https://github.com/code-423n4/2023-05-ajna-findings/issues/114) ||
| High | [Position NFT can be spammed with insignificant positions by anyone until rewards DoS](https://github.com/code-423n4/2023-05-ajna-findings/issues/488) | [H-03](https://code4rena.com/reports/2023-05-ajna#h-03-position-nft-can-be-spammed-with-insignificant-positions-by-anyone-until-rewards-dos) |

### 2023-04: [EigenLayer](https://code4rena.com/contests/2023-04-eigenlayer-contest) :1st_place_medal:
<details>
<summary><b>Related tweet</b></summary>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Awards have been announced for the $90,500 USDC <a href="https://twitter.com/eigenlayer?ref_src=twsrc%5Etfw">@eigenlayer</a> audit 🤝<br><br>Top 5:<br>🥇 <a href="https://twitter.com/MarioPoneder?ref_src=twsrc%5Etfw">@MarioPoneder</a> - $13,081.90 USDC<br>🥈 volodya - $12,193.66 USDC<br>🥉 windowhan001 - $5,031.50 USDC<br>🏅 <a href="https://twitter.com/CyfrinAudits?ref_src=twsrc%5Etfw">@CyfrinAudits</a> - $3,177.34 USDC<br>🏅 <a href="https://twitter.com/QiuhaoLi?ref_src=twsrc%5Etfw">@QiuhaoLi</a> - $2,972.95 USDC </p>&mdash; Code4rena (@code4rena) <a href="https://twitter.com/code4rena/status/1667379760614502402?ref_src=twsrc%5Etfw">June 10, 2023</a></blockquote>
</details>

| Risk | Title | Included in report |
| :--- | :--- | :---: |
| High | [Slot and block number proofs not required for verification of withdrawal (multiple withdrawals possible)](https://github.com/code-423n4/2023-04-eigenlayer-findings/issues/388) | [H-01](https://code4rena.com/reports/2023-04-eigenlayer#h-01-slot-and-block-number-proofs-not-required-for-verification-of-withdrawal-multiple-withdrawals-possible) |

### 2023-04: [ENS](https://code4rena.com/contests/2023-04-ens-contest)
Findings not available yet.

### 2023-04: [Frankencoin](https://code4rena.com/contests/2023-04-frankencoin)
| Risk | Title |
| :--- | :--- |
| Medium | [Successful minter application can be prevented by front-runner](https://github.com/code-423n4/2023-04-frankencoin-findings/issues/477) |
| Medium | [Denial of service in checkQualified() method of Equity contract](https://github.com/code-423n4/2023-04-frankencoin-findings/issues/635) |

### 2023-04: [Rubicon v2](https://code4rena.com/contests/2023-04-rubicon-v2)
Findings not available yet.

### 2023-04: [Caviar Private Pools](https://code4rena.com/contests/2023-04-caviar-private-pools)
| Risk | Title |
| :--- | :--- |
| High | [Owner of PrivatePool can steal any NFTs and tokens that the pool has approval for](https://github.com/code-423n4/2023-04-caviar-findings/issues/63) |
| Medium | [PrivatePool creation can be front-run](https://github.com/code-423n4/2023-04-caviar-findings/issues/92) |

### 2023-02: [Ethos Reserve](https://code4rena.com/contests/2023-02-ethos-reserve-contest)
| Risk | Title |
| :--- | :--- |
| Medium | [Strategy emergency exit (guardian privileges) harvest amount can be reduced with strategist privileges](https://github.com/code-423n4/2023-02-ethos-findings/issues/262) |
| Medium | [Inconsistent support of ERC20 tokens that deduct transaction fee](https://github.com/code-423n4/2023-02-ethos-findings/issues/477) |
| QA | [Strategy contract upgrade can be prevented by lower privileged roles](https://github.com/code-423n4/2023-02-ethos-findings/issues/359) |


## [Sherlock](https://app.sherlock.xyz/)

### 2023-07: [Perennial V2](https://audits.sherlock.xyz/contests/106)
| Risk | Title |
| :--- | :--- |
| Medium | [DSU token balance of MultiInvoker contract can be drained by anyone](https://github.com/sherlock-audit/2023-07-perennial-judging/issues/67) |

### 2023-06: [Index Update](https://audits.sherlock.xyz/contests/91)
| Risk | Title |
| :--- | :--- |
| Medium | [New auction rebalance can be started before previous one concluded or duration elapsed](https://github.com/sherlock-audit/2023-06-Index-judging/issues/22) |
| Medium | [Insufficient validation of auction execution price adapter config data](https://github.com/sherlock-audit/2023-06-Index-judging/issues/24) |
| Medium | [SetToken can be indefinitely locked by AuctionRebalanceModule](https://github.com/sherlock-audit/2023-06-Index-judging/issues/25) |

