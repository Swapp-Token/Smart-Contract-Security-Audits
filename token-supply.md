# 2.1.0 - Token Supply

The contract has no set token supply. The total initial supply minted by users through the launch phase deposit functionality will fall within a defined range, determined partially by confined randomness. A total of 130M SWAPP tokens was released during the launch phase.

This total supply released during the launch phase was matched by a minted batch \(an additional 130M\) that is then [sent permanently to Uniswap](liquidity-transformer-epoch.md).

The total token supply may increase as referral bonus tokens are minted. Some of the new tokens will be minted directly to stakers upon each monthly epoch ending and/or when [closing a stake](closing-stakes.md). 

If no stakes are closed on a given day, and no stakes scrape interest on that day, no new tokens are actually minted that day, though they are earmarked to be minted later. Once a stake is closed, all tokens the stake had earmarked to it for all past days are then minted at once.

