---
description: Terminology and other stuff you might want to know about.
---

# 7.0 - Appendix

[**Appendix A**](https://swapp.org/whitepaper#sec-7-1) **Source Code Audits**

The Swapp Foundation has obtained a paid, professional audit of the SWAPP contract Solidity source code from [RD Auditors](https://drive.google.com/file/d/1-xDfof9K4JEi-AdFqZJijbxt\_YOfy6dp/view?usp=sharing), [Chainsulting](https://drive.google.com/file/d/1BOv-yoYwtdXHij0eQPxLhAJ1JJPuvlVz/view?usp=sharing)1, [Chainsulting2](https://drive.google.com/file/d/1ChCYYDbVsSKLvx0kI6Bo6CtMKfQQrHSn/view?usp=sharing), and the Certik(coming soon), all reputable auditing firms. The full audit report is included below.

RD Findings: The auditors’ conclusion was, _“We have used all possible tests based on the given object. We found no critical, high, \[or] medium level issues so it is good to go for production. Security state of reviewed contract is “secured”._

[**Appendix B**](https://swapp.org/whitepaper#sec-7-2) **Coding Standards**

* The SWAPP contract is written entirely in Solidity and compiled with solc 0.7.2.
* The code should adhere to the formats prescribed by the [style guide](https://solidity.readthedocs.io/en/v0.7.2/style-guide.html) section of in the official [Solidity 0.7.2 documentation](https://solidity.readthedocs.io/en/v0.7.2/).
* All public interfaces (at a minimum) should be annotated using the [NatSpec format](https://solidity.readthedocs.io/en/v0.7.2/natspec-format.html).
* Unit tests should provide 100% coverage of the source code. All conceivable edge and corner cases should be covered.
* Function and variable names should convey their purpose and usage as clearly and tersely as possible, in plain English. Avoid using digits, unnecessary abbreviations, acronyms, shorthand, or slang.
* Functions should be as short as is practical. They should do what their name implies, and not much else. A good rule of thumb is that a function should try to be viewable in its entirety on a typical monitor, at a typical font size, if at all possible.

[**Appendix C**](https://swapp.org/whitepaper#sec-7-3) **Terminology**

* SWAPP — the utility token and smart contract described here.
* TESLA— the base unit of the SWAPP token, similar to wei for ETH, or satoshi for BTC. One SWAPP equals one quintillion TESLA (1,000,000,000,000,000,000).
* [Stake](https://swapp.org/whitepaper#sec-2-3-5) — a time locked deposit of SWAPP which earns interest over time.
* [Auction Phase](liquidity-transformer-epoch.md) — the first thirty(30) days of the contract’s existence, during which users may deposit ETH to reserve part of the initial supply of SWAPP.
* [Circulation Epoch](https://swapp.org/whitepaper#sec-2-3) — the epoch immediately following the end of the LT Epoch, during which users may mint their tokens reserved in the LT Epoch, transfer tokens, stake tokens, etc.
* Uniswap — a decentralized, non-custodial ERC-20 token and ETH exchange on the Ethereum blockchain. The SWAPP contract is integrated directly with Uniswap. General info on Uniswap is [here](https://uniswap.org), Uniswap exchange stats are [here](https://uniswap.info), and the main exchange is [here](https://app.uniswap.org).
* ERC-20 — a standard interface for Ethereum smart contract tokens. ERC stands for “Ethereum Request for Comment”. The original EIP (Ethereum Improvement Proposal) describing ERC-20 tokens can be found [here](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md).

**References**

Adams, H. (2020, February). _Uniswap whitepaper._ [https://hackmd.io/@Uniswap/HJ9jLsfTz](https://hackmd.io/@Uniswap/HJ9jLsfTz)

Adams, H., Zinsmeister, N., Robinson, D. (2020, March). _Uniswap v2 core._ [https://uniswap.org/whitepaper.pdf](https://uniswap.org/whitepaper.pdf)

Mushegian, N., Brockman, D., Brockman, M. (2018, February 6). _Reference implementation of the decentralized DAI stablecoin issuance system._ [https://makerdao.com/purple/](https://makerdao.com/purple/)

Oraclize. (n.d.). _A scalable architecture for on-demand, untrusted delivery of entropy._ Retrieved March 22, 2020, from [https://provable.xyz/papers/random\_datasource-rev1.pdf](https://provable.xyz/papers/random\_datasource-rev1.pdf).

Provable Things. (n.d.). _Security deep dive._ Provable docs. Retrieved March 22, 2020, from [https://docs.provable.xyz/#security-deep-dive](https://docs.provable.xyz/#security-deep-dive)

Vogelsteller, F., & Buterin, V. (2015, November). _EIP-20: ERC-20 token standard._ [https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md)

Wood, G. (2019, October 20). _Ethereum: A secure decentralized generalized transaction ledger: Byzantium version 7e819ec._ [https://ethereum.github.io/yellowpaper/paper.pdf](https://ethereum.github.io/yellowpaper/paper.pdf)

Zhang, Y., Chen, X., & Park, D. (2018, October). _Formal specification of constant product (x × y = k) market maker model and implementation._ [https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf](https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf)

Copyright © Swapp Protocol 2021
