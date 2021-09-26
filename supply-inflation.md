---
description: How annual inflation works.
---

# 2.3.4 - Supply Inflation

The total circulating supply of SWAPP inflates at a variable rate of approximately 4% per year to accommodate staking pool rewards and referral bonuses. At the end of every day of the Circulation Epoch, the contract calculates how many new SWAPP will need to be minted for that day in order to achieve that rate of inflation.

totalSwappSupply = circulatingSwapp + stakedSwapp  
dailyInflationRate = \(1.04 ^ \(1 / 365\) – 1\)  
dailyInflationRate =~ 0.0001074597820279

newSwappToday = totalSwappSupply × dailyInflationRate

