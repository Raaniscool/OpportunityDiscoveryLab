# Financial scenarios — hypothetical, not forecasts

Each row models a **mature steady-state month**, not year-one sales or an end-of-year forecast. Conservative / moderate / optimistic quantities are 0.4× / 1× / 2× the baseline rounded to whole units. No probability is assigned and none is guaranteed; a zero-sales outcome is possible. R units are paying accounts present throughout the month. O units are monthly one-time sales/leads. A units are thousands of monetized ad impressions/month. Pricing, buyer counts, hosting, CAC and support costs are invented planning assumptions, not measured demand. Model does not infer customers from market size. All values USD.

For each case: gross monthly revenue = price × units; monthly contribution after modeled costs = revenue − fixed operating cost − variable unit cost × units − acquisition spend − payment fees. R assumes 5% account churn/month, with paid acquisitions replacing churn at the stated CAC (fractional customers represent long-run averages). O assumes CAC for every sale; A assumes organic traffic and zero CAC, an especially fragile assumption. Direct payments are modeled at 2.9% + $0.30 per account/sale/lead; Shopify row uses 2.9% only per [S4], under qualifying threshold. A has no card charges. Variable unit costs include support labor at an assumed $30/hour as well as compute/storage; fixed costs cover base hosting/tools. CAC includes ad/partner and sales time. They exclude tax, financing, legal, refunds, additional platform fees, founder management and ongoing product engineering. Thus contribution is **not net profit**. Case quantities are not consistent with any specific growth trajectory; churn and CAC are assumptions, not observed statistics.

Build cost at $75/hour is in the opportunity register; it is a one-off investment excluded below. Annualizing a mature month (×12) assumes it persists for 12 months; it is not expected first-year revenue. Negative contribution is a loss before excluded costs. No annual prepayment or setup fees assumed.

| # | Opportunity | Conservative units: revenue / contribution | Moderate units: revenue / contribution | Optimistic units: revenue / contribution |
|---|---|---:|---:|---:|
| 1 | Agency reporting reconciliation | 10: $1,490 / $814 | 25: $3,725 / $2,304 | 50: $7,450 / $4,789 |
| 2 | Insurance certificate follow-up | 8: $1,592 / $653 | 20: $3,980 / $2,009 | 40: $7,960 / $4,267 |
| 3 | Shopify feed exception monitor | 20: $980 / $532 | 50: $2,450 / $1,539 | 100: $4,900 / $3,218 |
| 4 | AI-built app maintenance | 5: $1,500 / $680 | 12: $3,600 / $1,842 | 24: $7,200 / $3,834 |
| 5 | Offline specialist file converter | 8: $632 / $307 | 20: $1,580 / $888 | 40: $3,160 / $1,856 |
| 6 | Accounting document chase | 10: $990 / $423 | 25: $2,475 / $1,298 | 50: $4,950 / $2,756 |
| 7 | Accessible document QA | 8: $1,032 / $380 | 20: $2,580 / $1,249 | 40: $5,160 / $2,698 |
| 8 | Ecommerce returns reason analyzer | 12: $948 / $371 | 30: $2,370 / $1,197 | 60: $4,740 / $2,575 |
| 9 | Vendor security questionnaire library | 7: $1,043 / $371 | 18: $2,682 / $1,299 | 36: $5,364 / $2,818 |
| 10 | Website accessibility change monitor | 12: $1,068 / $423 | 30: $2,670 / $1,344 | 60: $5,340 / $2,877 |
| 11 | Backup restore verification | 7: $1,393 / $456 | 18: $3,582 / $1,643 | 36: $7,164 / $3,585 |
| 12 | Niche scheduling plugin | 14: $546 / $141 | 35: $1,365 / $562 | 70: $2,730 / $1,265 |
| 13 | Developer webhook replay tool | 16: $464 / $74 | 40: $1,160 / $454 | 80: $2,320 / $1,089 |
| 14 | AI cost and usage attribution | 8: $792 / $147 | 20: $1,980 / $727 | 40: $3,960 / $1,693 |
| 15 | Localized creator caption package | 12: $468 / $-9 | 30: $1,170 / $127 | 60: $2,340 / $354 |
| 16 | Vertical spreadsheet template pack | 8: $472 / $186 | 20: $1,180 / $570 | 40: $2,360 / $1,210 |
| 17 | Professional design plugin | 8: $552 / $180 | 20: $1,380 / $584 | 40: $2,760 / $1,258 |
| 18 | Premium niche puzzle game | 20: $300 / $-15 | 50: $750 / $143 | 100: $1,500 / $406 |
| 19 | Specialist lead marketplace | 12: $720 / $-84 | 30: $1,800 / $59 | 60: $3,600 / $298 |
| 20 | Ad-supported niche reference site | 20: $40 / $-90 | 50: $100 / $-45 | 100: $200 / $30 |

## Worked unit economics and sensitivities

**Agency reconciliation**, moderate: 25 accounts × $149 = $3,725 monthly gross, $805 fixed/variable support ($180 + 25 × $25), $500 replacement acquisition (25 × 5% × $400), and $115.53 payment fees (2.9% × $3,725 + 25 × $0.30). Contribution is $2,304.48/month; $27,653.70 annualized, before the excluded costs above. At 25 accounts, if monthly churn doubles to 10%, acquisition rises by $500 and contribution falls to $1,804.48. If variable cost doubles to $50/account, contribution falls another $625. At 20% monthly churn with unchanged CAC, acquisition is $2,000 and contribution falls to $804.48. These cases hold account count steady by assuming enough replacements are available; that is not guaranteed.

Per-account monthly contribution before acquisition and fixed costs is $149 − $25 − $4.621 = $119.379. Simple CAC payback is $400 / $119.379 = 3.35 months, before fixed costs and churn; approximate gross contribution lifetime at 5% constant churn is $119.379 / 0.05 = $2,387.58, before CAC and fixed costs. This simple geometric model ignores discounting, expansion and cohort variation and must not be treated as measured LTV. Replacing churn at 5% implies break-even at about 2 accounts ($180 / ($119.379 − $20)), ignoring all excluded costs; it is not a living-wage threshold. To cover an additional $6,000/month owner salary and product engineering, roughly 63 accounts are needed: ceiling(($180 + $6,000) / $99.379). Acquisition demand and support capacity at that level are untested.

**Maintenance:** $300/month with $100 variable delivery implies about 3.3 hours of support at $30/hour before any other variable costs; actual support can exceed that. Never promise unlimited changes. At 12 accounts the modeled contribution is positive but cannot automatically support a full-time salary. **One-time purchases:** revenue requires fresh purchases every month; no churn-replacement simplification applies. The game assumption includes $5/unit for channel, refunds and fulfillment, a rough placeholder, not an asserted Steam fee. **Ads:** $2 per thousand monetized impressions is a hypothetical effective yield, not an observed CPM; 50 units = 50,000 monthly monetized impressions, not visitors or pageviews. Traffic acquisition, fill rates and privacy limits may be worse.

For a decision, replace every assumption with pilot evidence, add wages and all overhead, model monthly ramp and cash runway, then assess payback and uncertainty. A contribution surplus alone is not proof of profitability or financing viability.
