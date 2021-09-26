# 2.3.9 - Earn INTR$T on Stakes

When a stake is opened, its SWAPP principal is burned and converted into theoretical "INTR$T". These LP tokens represent the stake size and length as well as, indirectly, how early the stake was opened. The amount of INTR$T a newly opened stake gets is determined by the SWAPP contract, as well as a percentage bonus based on the length of the stake \(for Pool3\). The earlier the users get into the pool, the more interest-earning potential they are given.

Stakes earn interest daily through the SWAPP supply inflation, as well as from other [stakes’ penalties](staking.md) paid. Depending on the length of the stake, a bonus amount of shares will be generated on top of the amount determined by the staked amount of SWAPP and current share price.

The share price starts at some predetermined value denominated in SWAPP per share. Whenever any stake is closed, the contract calculates a ratio of that stake’s total return \(principal + interest – penalty\) to its shares. If this ratio is greater than the current share price, then the share price is immediately set to this new, increased value.

