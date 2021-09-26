---
description: Cashing out.
---

# 2.3.9.2 - Closing Stakes

A user may close a stake at any time. Depending on the stake’s status \(where the stake is in its lifecycle\), different things will happen:

* Closing a Pending stake – the stake INTR$T shares are destroyed. The entire stake principal is minted back to the user, without interest or penalty.
* Closing an Active \(premature\) stake – the stake shares are destroyed. The stake principal is penalized \(see below\) and minted back to the user along with all INTR$T accumulated thus far.
* Closing a Mature stake – the stake INTR$T shares are destroyed. The entire stake principal and all interest accumulated is minted back to the user.  There are never any penalties for closing a Mature stake, no matter how late.

The penalty deducted from the principal \(stakedSwapp\) when closing an Active stake is as follows:

If the stake is one day long:  
penaltyAmount = stakedSwapp × 0.1

If the stake is two or more days long:  
penaltyAmount = stakedSwapp × \(.1 + .8 × \(\(daysLeft – 1\) / \(stakedDays – 1\)\)\)

Thus, if you close an Active stake that was 100 days long on its final day before maturity, you get a 10% penalty applied to the principal. If you close the same stake on the first day of it being Active, you get a 90% penalty. The penalty scales linearly between those two extremes.

Any such SWAPP penalized from a stake’s return is earmarked for distribution to all active stake shares that day. These penalty distributions are only realized by those stakes’ shares when each of those stakes end.

