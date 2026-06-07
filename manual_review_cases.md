# Manual Review Cases (Part 2)

Twelve real customers where the automated segment is not the whole story and a human retention decision is needed. Feature values are as of the 2025-09-30 snapshot; the churn outcome is shown only in hindsight to sanity-check the reasoning (it was NOT used to decide).

## CUST00030 — segment: High-Value but Unhappy
- R/F/M = 5/5/5 | recency 5d | monetary INR 2,820 | returns 0% | neg-ticket 100% (2 tickets) | manual bucket: medium
- **Decision:** Textbook Champion (R5F5M5, INR 2,820) yet has 2 tickets, both negative. DECISION: proactive service check-in, no discount — protect a top customer before sentiment sours. (Did not churn.)

## CUST00006 — segment: High-Value but Unhappy
- R/F/M = 3/5/5 | recency 51d | monetary INR 2,990 | returns 25% | neg-ticket 100% (2 tickets) | manual bucket: medium
- **Decision:** High value (INR 2,990, F5) but 25% returns AND fully negative tickets, recency 51d. DECISION: service recovery + quality feedback loop; hold offers until resolved. (Did not churn.)

## CUST00071 — segment: High-Value but Unhappy
- R/F/M = 4/1/5 | recency 32d | monetary INR 2,062 | returns 0% | neg-ticket 100% (1 tickets) | manual bucket: high
- **Decision:** Single large order (INR 2,063, F1) but flagged manual_priority=high and 100% negative ticket. DECISION: high-touch save — this one DID churn; a timely resolution call was the right bet.

## CUST00027 — segment: High-Value but Unhappy
- R/F/M = 3/1/5 | recency 70d | monetary INR 2,128 | returns 100% | neg-ticket 0% (1 tickets) | manual bucket: medium
- **Decision:** 100% return rate on a high-value buyer (INR 2,128), neutral sentiment, 18 days since visit. DECISION: investigate WHY returns are total — sizing/quality? Fix root cause, not a coupon. (Did not churn.)

## CUST00067 — segment: Loyal Customers
- R/F/M = 3/3/4 | recency 63d | monetary INR 1,246 | returns 50% | neg-ticket 0% (1 tickets) | manual bucket: medium
- **Decision:** Mid RFM (3/3/4), 50% returns, recency 63d — DID churn. DECISION: borderline; a small reactivation offer + return-reason survey was warranted but missed.

## CUST00134 — segment: Loyal Customers
- R/F/M = 4/3/4 | recency 35d | monetary INR 1,527 | returns 50% | neg-ticket 0% (0 tickets) | manual bucket: low
- **Decision:** Manual bucket=low yet M4, 50% returns, active (visit 4d ago). DECISION: CRM label underrates them; reclassify to Need-Attention and monitor returns. (Did not churn.)

## CUST00053 — segment: High-Value but Unhappy
- R/F/M = 4/5/5 | recency 25d | monetary INR 2,064 | returns 0% | neg-ticket 100% (1 tickets) | manual bucket: medium
- **Decision:** Champion-like (R4F5M5) but 46% avg discount AND negative tickets. DECISION: retain via value/bundles not deeper discounts; resolve ticket. Margin risk. (Did not churn.)

## CUST00050 — segment: Loyal Customers
- R/F/M = 5/3/5 | recency 0d | monetary INR 2,027 | returns 50% | neg-ticket 0% (0 tickets) | manual bucket: low
- **Decision:** Just ordered (recency 0) but 50% returns, no recent tickets, bucket=low. DECISION: watch returns; no spend now — very recent activity makes near-term churn unlikely. (Did not churn.)

## CUST00086 — segment: High-Value but Unhappy
- R/F/M = 4/5/4 | recency 21d | monetary INR 1,741 | returns 0% | neg-ticket 100% (1 tickets) | manual bucket: medium
- **Decision:** Engaged Champion (visit today, F5) with a negative ticket. DECISION: quick resolution + thank-you, no discount. Cheapest possible retention. (Did not churn.)

## CUST00139 — segment: High-Value but Unhappy
- R/F/M = 4/3/4 | recency 28d | monetary INR 1,715 | returns 0% | neg-ticket 100% (2 tickets) | manual bucket: medium
- **Decision:** M4, F3, fully negative tickets (2), no campaign ever sent, 10d since visit. DECISION: first-touch service outreach — untouched by CRM and at risk. (Did not churn.)

## CUST00026 — segment: High-Value but Unhappy
- R/F/M = 3/5/5 | recency 72d | monetary INR 3,561 | returns 33% | neg-ticket 100% (1 tickets) | manual bucket: medium
- **Decision:** Highest spender here (INR 3,561) but recency 72d, 26d since visit, 33% returns, negative tickets, never campaigned. DECISION: top win-back priority with personal outreach. (Did not churn — outreach likely pays off.)

## CUST00096 — segment: Loyal Customers
- R/F/M = 3/3/4 | recency 61d | monetary INR 1,415 | returns 50% | neg-ticket 0% (0 tickets) | manual bucket: medium
- **Decision:** Mid RFM, 50% returns, 15d since visit, bucket=medium. DECISION: ambiguous drift case — low-cost reactivation email + return survey; reassess in 30 days. (Did not churn.)
