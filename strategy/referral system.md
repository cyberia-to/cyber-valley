---
tags: cyberia, cyber valley, strategy, referral
alias: referral system, referral rewards, referral algorithm
crystal-type: pattern
crystal-domain: cyberia
---
# referral system

how cyber valley rewards the people who bring people. two programs run on the same idea — pay for what actually comes in — at two different scales.

## 1. leasehold referrals

a referrer who brings a leaseholder earns 10% of every payment the Company actually receives under that lease, for as long as it pays, one hop only. the terms are on [[leasehold referrals]].

## 2. event and ticket referrals — the on-chain engine

ticket purchases on [cyberia.my](https://cyberia.my) pay referral rewards through the `ReferralRewards` contract. the algorithm:

| step | rule |
|---|---|
| binding | the first purchase with a referrer's link binds the buyer to that referrer for good; one referrer per buyer; a buyer never refers themself; loops within three levels are refused |
| pool | 3% of each purchase forms the referral pool |
| levels | the pool pays up to three levels above the buyer: 60% to the direct referrer, 30% to theirs, 10% to the third |
| reach | a referrer's share scales with how many buyers they brought directly: 1–4 → 50%, 5–24 → 75%, 25 and more → 100% |
| activity | a referrer earns while active — a purchase of their own within the last 30 days |
| payment | rewards are paid in the event token by the event manager at the moment of purchase |

the reward of each referrer on a purchase:

    reward = amount × pool × level × reach

| symbol | meaning |
|---|---|
| reward | what the referrer receives |
| amount | the price of the purchase |
| pool | 3% |
| level | 60%, 30% or 10% by distance from the buyer |
| reach | 50%, 75% or 100% by the referrer's direct buyers |

the Company can adjust pool, levels, reach steps and the activity window on-chain; each change is published.
