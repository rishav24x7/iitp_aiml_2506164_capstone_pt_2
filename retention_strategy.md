# Retention Strategy & Where to Spend (Part 2)

I split all 2,400 customers into segments using RFM plus a few behavioural signals, then worked out what to do with each group and where a limited budget should go first. For context the overall 60-day churn rate is 47%. Important: I built the segments WITHOUT ever looking at the churn label — the churn column below is only there to check the segments actually separate risk.

## What to do with each segment

| Segment | Customers | Churn % | Avg monetary (INR) | Priority | Play | What that means in practice |
|---|---|---|---|---|---|---|
| At-Risk High-Value | 376 | 70.7 | 1,530 | High | Win-back, high touch | Personal outreach + modest targeted offer; highest priority save. |
| Loyal Customers | 595 | 28.2 | 1,207 | Low | Deepen & cross-sell | Replenishment reminders, bundle nudges into new categories. |
| High-Value but Unhappy | 193 | 24.4 | 2,257 | High | Resolve, then retain | Service recovery (resolve open ticket/refund) BEFORE any offer. |
| Need Attention | 226 | 42.5 | 752 | Medium | Nurture / re-engage | Content + low-cost reactivation email before they go dormant. |
| Champions | 288 | 9.4 | 2,417 | Low | Reward & advocate | Early access, loyalty perks, referral asks. NO discount needed. |
| Discount-Dependent | 194 | 53.1 | 588 | Medium | Wean off discounts | Shift to value framing, bundles; cap discount depth. |
| Dormant | 459 | 88.2 | 148 | Low | Low-cost win-back only | Cheap automated win-back; do not over-invest. |
| New / Promising | 69 | 21.7 | 665 | Medium | Onboard to 2nd purchase | Welcome series, category education, small 2nd-order incentive. |

## Where the budget should go

I ranked segments by **revenue at risk** — customers x churn rate x average spend — which comes to about INR 983,998 in total. The point is to chase recoverable revenue, not just high churn percentages. With limited money, I'd fund them in this order:

1. **At-Risk High-Value** — about INR 407,066 at risk (376 customers, 70.7% churn).
2. **Loyal Customers** — about INR 202,747 at risk (595 customers, 28.2% churn).
3. **High-Value but Unhappy** — about INR 106,066 at risk (193 customers, 24.4% churn).
4. **Need Attention** — about INR 72,171 at risk (226 customers, 42.5% churn).
5. **Champions** — about INR 65,261 at risk (288 customers, 9.4% churn).
6. **Discount-Dependent** — about INR 60,584 at risk (194 customers, 53.1% churn).
7. **Dormant** — about INR 60,123 at risk (459 customers, 88.2% churn).
8. **New / Promising** — about INR 9,980 at risk (69 customers, 21.7% churn).

## The thinking behind it
- **High-value-at-risk comes first.** At-Risk High-Value and High-Value but Unhappy hold the most money we can actually save per customer, so they earn the first and most personal outreach.
- **Fix the problem before sending an offer.** For High-Value but Unhappy, a coupon on top of an unresolved complaint just burns cash — resolve the issue first, then talk retention.
- **Don't pay Champions and Loyal customers to stay.** They were going to stay anyway; spending on them is money we could have used on someone genuinely wavering.
- **Keep Dormant cheap.** Churn is ~88% and their spend is low, so anything here should be automated and low-cost — don't pour budget into a group that's mostly gone.
- **Move Discount-Dependent customers off discounts.** Shifting them toward value and bundles protects margin instead of training them to wait for the next deal.