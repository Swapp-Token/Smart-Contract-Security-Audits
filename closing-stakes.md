---
description: Cashing out.
---

# 2.3.6.3 - Closing Stakes

A user may close a stake at any time. Depending on the stake’s status (where the stake is in its lifecycle), different things will happen:

* Closing an Active (premature) stake – The stake principal is penalized (see below) and the user's portion minted back to the user without duration bonus reward.
* Closing a Mature stake – The entire stake principal and all duration bonus rewards that were accumulated are minted back to the user.  There are never any penalties for closing a Mature stake, no matter how late.

The penalty deducted from the principal (stakedSwapp) when closing an Active stake is as follows:

If the stake is one epoch(28days) long, then the user only may un-stake after epoch ends.

If the stake is two or more epochs long:

$$
penaltyAmount = stakedSwapp × ( ((daysLeft – 1) / (stakedDays – 1)))
$$

Thus, if you close an Active stake that was 10 epochs long on its second epoch you would like to cloase then approximately 90% of your principal will be penalty and your duration bonus for that month will be burned; If you close the same stake on the last day of the 10th epoch but before epoch ends you will loose the duration bonus and very small percentage of your principal. **MAKE SURE always the last epoch is complete and your stake is matured before you un-stake even on last epoch.**The penalty scales linearly between those two extremes.

Any such SWAPP penalized from a stake’s return is earmarked for distribution bonus portion to all active stake shares that day but principal portion of penalty gets burned forever. These penalty distributions are only realized by those stakes when each of those stakes end.
