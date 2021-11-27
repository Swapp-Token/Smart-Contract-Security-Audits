# 2.2 - The Launch Phase (ENDED)

The launch of the SWAPP contract will kick off an initial **30 day** phase during which users may send ETH (or any ERC-20 token traded on Uniswap V2) to the SWAPP contract in order to receive SWAPP tokens. The tokens reserved can be [minted by the users](minting-tokens.md) immediately following the end of the "launch phase", i.e. the **start of day 31**.

Each day of the launch phase will have a certain amount of SWAPP tokens that can be reserved by all those who deposit ETH to the platform on that day. Most days will have exactly five million SWAPP available, but the other days will have their available SWAPP amount randomly set within a predefined range. These random amounts will be determined by the contract shortly after the end of each random day, by leveraging the [Provable](https://provable.xyz) (formerly called “Oraclize”) smart contract’s Random Datasource interface. The generated randomness is delivered on-chain in a trustless and provably cryptographically secure way.

Each day’s available SWAPP tokens end up getting split among the users who deposited ETH to that day, in direct proportion. In other words, a user that made a reservation on a particular auction day will later be able to mint the fraction of that day’s available SWAPP that equals the fraction of the day’s total ETH they personally sent in.
