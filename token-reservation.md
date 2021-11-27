# 2.2.1 - Initial Token Release (ENDED)

On any given day of the Launch Phase Epoch, users may choose to send ETH (or any ERC-20 token traded on Uniswap V2) to the contract and assign it to any of the Auction Phase Epoch days that have not yet concluded. We call this action a “token reservation”.

For example, during day 12, users may send and assign ETH to any of the days 12–30, but not to days 1–11, since those days have already concluded.

Each token reservation is assigned to a single day, but users may make as many such reservations as they wish, to as many different days as they wish.

The SWAPP contract front end will also include the ability for a user to spread a single reservation amount of ETH (or ERC-20) evenly across all remaining Auction Phase days. This “dollar cost averaging” feature saves gas for the user who wishes to reserve an equal part of each Auction Phase day.

Reservations can be made with ETH, but also with any ERC-20 token that’s traded on Uniswap V2. This is done via direct integration with Uniswap, which swaps the ERC-20 for ETH as part of the reservation transaction. This is functionally the same as the users themselves swapping the ERC-20 for ETH on Uniswap, and then later sending the ETH to the SWAPP contract for a token reservation. The benefit of using the SWAPP reservation interface to do this is that it saves the user some gas fees and time.

Each single token reservation must be of a minimum ETH amount, to make spam attacks cost-prohibitive. The specific minimum amount will be finalized at a later date, closer to launch. This is because the price of ETH may change significantly between the time of this writing and the contract launch. The minimum will likely be approximately $10 of ETH.

The contract will provide public interfaces for viewing the total amount of ETH currently assigned to each Auction Phase Epoch day across all users, as well as the total SWAPP available for each day (where that supply has been determined, in the case of random days). For days where the supply has not yet been finalized, the min/max range will also be retrievable from the contract.
