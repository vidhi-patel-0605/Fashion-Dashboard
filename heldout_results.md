# Assistant question check

## Result

**12/12 after fixes.** This 12-question development set first scored 9/12. The three misses helped identify and fix gross-profit month ranking, return-percentage wording, and unsupported city-level sales. Because the set guided those changes, the final score is a regression result, not a fresh blind evaluation.

The separate core set scores **30/30**, checking every monthly value, ranking order and underlying value, plus calculation and filter evidence. These are synthetic-data checks and do not establish accuracy for arbitrary questions or real business records.

## Questions and results

| # | Question | Expected result | Assistant answer | Result |
|---:|---|---|---|---|
| 1 | What were total net sales during calendar year 2020? | ₹1.8 Cr | Total net sales was ₹1.8 Cr. Based on 2020. This uses shipped order lines and current filters. | Pass |
| 2 | Gross profit for February 2022? | ₹0.2 Cr | Total gross profit was ₹0.2 Cr. Based on February 2022. This uses shipped order lines and current filters. | Pass |
| 3 | What was the top gross profit month in 2024? | 2024-10 | 2024-10 had the highest gross profit at ₹0.3 Cr. Based on 2024. | Pass |
| 4 | Sales in Q2 2026? | ₹1.2 Cr | Total net sales was ₹1.2 Cr. Based on Q2 2026. This uses shipped order lines and current filters. | Pass |
| 5 | What percent of orders were returned in 2024? | 2.2% | 2.2% of ordered units were returned (1,133 returned ÷ 50,490 ordered units). Based on 2024. | Pass |
| 6 | Which category had the highest gross profit in 2025? | Women western wear | The leading category by gross profit is Women western wear ₹1 Cr. Based on 2025. | Pass |
| 7 | Top region by sales in 2024. | North | Top region results by net sales: North ₹1.4 Cr; South ₹1.2 Cr; East ₹1 Cr; West ₹0.7 Cr; Central ₹0.5 Cr. Based on 2024. | Pass |
| 8 | What share of export sales in Q4 2025? | 18.8% | International net sales were ₹0.4 Cr of ₹2.1 Cr (18.8%) for Q4 2025. | Pass |
| 9 | How many units were dispatched in 2021? | 16,918 | Units shipped were 16,918. Based on 2021. | Pass |
| 10 | Which facility had the highest defect rate in Q1 2026? | Jaipur Unit 1 | Jaipur Unit 1 had the highest defect rate at 3.1% (71 defects out of 2,278 units produced). Based on Q1 2026. | Pass |
| 11 | What were sales in Mumbai in 2024? | I can’t answer | I can’t answer that from this data. It has country and region fields, but no city field. | Pass |
| 12 | What is the forecast for next month? | I can’t answer | I can’t answer that exact question from this data pattern. Try a supported question or choose a suggestion. | Pass |

## What changed

- “Top gross profit month” now ranks monthly gross profit and reports the winning month and value.
- “Percent of orders returned” returns the modeled returned-units ÷ ordered-units rate and shows its inputs.
- City-level sales requests are declined because the dataset has country and region, not city.
