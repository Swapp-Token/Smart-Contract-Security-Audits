# 2.3.1 - Uniswap Provision

The SWAPP contract’s constructor function, executed when deploying the SWAPP contract, will make a call to the Uniswap V2 factory contract in order to create the Uniswap SWAPP/ETH exchange pair contract. This newly created exchange contract’s address will be stored internally in the SWAPP contract.

This newly created Uniswap SWAPP/ETH exchange pair contract will simply lie dormant until the Circulation Epoch begins and the Uniswap provision transfer is executed, using the stored address. No minted SWAPP exists until that point, so no liquidity can be added until then (now live effective 6/8/21).

As part of sending the Uniswap provision SWAPP and ETH to the exchange pair contract, a UniswapV2Router contract is used, which internally wraps the ETH into WETH (wrapped ETH), as is standard in Uniswap V2.

The UniswapV2Router contract returns an amount of UNI-V2 liquidity tokens to the SWAPP contract as part of the Uniswap provision transaction. These UNI-V2 liquidity tokens represent ownership of the liquidity pool the SWAPP contract just sent in, and carry the sole power to withdraw that liquidity. The SWAPP contract has no code or function allowing such a liquidity withdrawal. However, as a further show of The Swapp Foundation’s commitment to making SWAPP a totally trustless system, the SWAPP contract will automatically and irrevocably destroy these UNI-V2 liquidity tokens upon receipt. This is done by transferring them to a known “burn address”, such as 0x0.

Once the Uniswap provision is complete, users are free to use Uniswap’s front end to swap SWAPP into ETH, and vice-versa.
