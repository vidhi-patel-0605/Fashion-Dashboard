# Ask this dashboard: core evaluation

## Results

**Current in-sample set: 30/30.** Scalar answers are compared with independent calculations. Month-by-month answers must match all 12 displayed month/value pairs. Ranking questions must match the complete order and underlying values in the assistant's evidence. Every response must also show calculation and filter details.

**12-question development set: 12/12 after fixes.** It first scored 9/12; its three misses guided the targeted fixes, so this is now a regression set, not a fresh blind result. See the [question report](heldout_results.html).

The first prototype scored **28/30** under an earlier, looser check on a different sample. The data and scoring rules changed, so that historical result is not directly comparable.

The assistant uses fixed question patterns and local calculations. This curated evaluation does not establish accuracy for arbitrary wording or real operational data.

## Product changes

- The assistant compares return rate across full months and explains that the sample has no return reasons to establish cause. The current comparison: September 2026 was below August 2026.
- It refuses restock questions because stock on hand, stockouts and supplier lead times are missing.
- Production is generated at 7–15% above shipped volume for each month and SKU.
- Weekly summaries became monthly comparisons. Alerts now require minimum order, return, sales and line volumes.

## Questions and results

Each expected result is calculated independently from the embedded synthetic data.

| # | Question | Expected result | Assistant answer | Detail checked | Result |
|---:|---|---|---|---|---|
| 1 | What were net sales in 2025? | ₹6.3 Cr | Total net sales was ₹6.3 Cr. Based on 2025. This uses shipped order lines and current filters. | calculation and filter evidence | Pass |
| 2 | What was gross profit in 2025? | ₹3.1 Cr | Total gross profit was ₹3.1 Cr. Based on 2025. This uses shipped order lines and current filters. | calculation and filter evidence | Pass |
| 3 | What was gross margin in 2025? | 50.0% | Gross margin was 50.0% (gross profit ₹3.1 Cr divided by net sales ₹6.3 Cr). Based on 2025. | calculation and filter evidence | Pass |
| 4 | What were net sales in December 2023? | ₹0.5 Cr | Total net sales was ₹0.5 Cr. Based on December 2023. This uses shipped order lines and current filters. | calculation and filter evidence | Pass |
| 5 | What was gross profit in December 2023? | ₹0.2 Cr | Total gross profit was ₹0.2 Cr. Based on December 2023. This uses shipped order lines and current filters. | calculation and filter evidence | Pass |
| 6 | How many units were shipped in December 2023? | 3,681 | Units shipped were 3,681. Based on December 2023. | calculation and filter evidence | Pass |
| 7 | What was the return rate in December 2023? | 2.2% | The return rate was 2.2% (110 returned units out of 4,908 ordered). Based on December 2023. | calculation and filter evidence | Pass |
| 8 | How many returned units in 2024? | 1,133 | There were 1,133 returned units. Based on 2024. | calculation and filter evidence | Pass |
| 9 | How many active buyers were there in 2025? | 118 | There were 118 active buyers. Based on 2025. | calculation and filter evidence | Pass |
| 10 | What was the average line value in 2025? | ₹1,01,519 | Average net sales per order line were ₹1,01,519. Based on 2025. | calculation and filter evidence | Pass |
| 11 | Which month had the highest net sales in 2025? | 2025-11 | 2025-11 had the highest net sales at ₹0.8 Cr. Based on 2025. | calculation and filter evidence | Pass |
| 12 | Which month had the lowest gross profit in 2024? | 2024-08 | 2024-08 had the lowest gross profit at ₹0.2 Cr. Based on 2024. | calculation and filter evidence | Pass |
| 13 | Show net sales month by month in 2023. | ₹0.2 Cr | net sales by month: 2023-01 ₹0.2 Cr; 2023-02 ₹0.2 Cr; 2023-03 ₹0.5 Cr; 2023-04 ₹0.3 Cr; 2023-05 ₹0.4 Cr; 2023-06 ₹0.3 Cr; 2023-07 ₹0.3 Cr; 2023-08 ₹0.2 Cr; 2023-09 ₹0.5 Cr; 2023-10 ₹0.5 Cr; 2023-11 ₹0.7 Cr; 2023-12 ₹0.5 Cr. Based on 2023. | 12/12 monthly values and labels checked | Pass |
| 14 | Show gross profit month by month in 2024. | ₹0.2 Cr | gross profit by month: 2024-01 ₹0.2 Cr; 2024-02 ₹0.2 Cr; 2024-03 ₹0.2 Cr; 2024-04 ₹0.2 Cr; 2024-05 ₹0.2 Cr; 2024-06 ₹0.2 Cr; 2024-07 ₹0.2 Cr; 2024-08 ₹0.2 Cr; 2024-09 ₹0.2 Cr; 2024-10 ₹0.3 Cr; 2024-11 ₹0.3 Cr; 2024-12 ₹0.3 Cr. Based on 2024. | 12/12 monthly values and labels checked | Pass |
| 15 | Compare net sales in 2024 and 2025. | ₹5.3 Cr | net sales was ₹5.3 Cr in 2024 and ₹6.3 Cr in 2025 (+19.6% change). | calculation and filter evidence | Pass |
| 16 | Compare gross profit in 2023 and 2024. | ₹2.4 Cr | gross profit was ₹2.4 Cr in 2023 and ₹2.6 Cr in 2024 (+10.8% change). | calculation and filter evidence | Pass |
| 17 | Which category had the most net sales? | Women western wear | The leading category by net sales is Women western wear ₹10 Cr. Based on the selected date range. | ranking order and all 5 values checked | Pass |
| 18 | Which category had the highest return rate? | Men apparel | Men apparel had the highest return rate at 2.5% (1,258 of 49,686 ordered units). Based on the selected date range. | ranking order and all 5 values checked | Pass |
| 19 | Which category had the highest gross margin? | Women ethnic wear | Category gross margins: Women ethnic wear 53.7% on ₹2.3 Cr; Men apparel 53.3% on ₹7.1 Cr; Women western wear 51.0% on ₹10 Cr; Kidswear 48.4% on ₹5.8 Cr; Home textiles 46.7% on ₹5 Cr. Based on the selected date range. | ranking order and all 5 values checked | Pass |
| 20 | Show net sales by category in 2025. | Women western wear | Top category results by net sales: Women western wear ₹2.1 Cr; Men apparel ₹1.4 Cr; Kidswear ₹1.2 Cr; Home textiles ₹0.9 Cr; Women ethnic wear ₹0.5 Cr. Based on 2025. | ranking order and all 5 values checked | Pass |
| 21 | Top region by sales in 2025. | North | Top region results by net sales: North ₹1.6 Cr; East ₹1.3 Cr; South ₹1 Cr; West ₹0.8 Cr; Central ₹0.4 Cr. Based on 2025. | ranking order and all 5 values checked | Pass |
| 22 | Which country had the most sales in Q3 2026? | India | The leading country by net sales is India ₹1.2 Cr. Based on Q3 2026. | ranking order and all 5 values checked | Pass |
| 23 | Show gross profit by product in 2025. | Lotus Shirt 14 | Top product results by gross profit: Lotus Shirt 14 ₹0.2 Cr; Indigo Kids Set 07 ₹0.2 Cr; Monsoon Top 13 ₹0.1 Cr; Monsoon Dress 39 ₹0.1 Cr; Kashmir Shirt 04 ₹0.1 Cr. Based on 2025. | ranking order and all 5 values checked | Pass |
| 24 | How many units were shipped in 2023? | 32,066 | Units shipped were 32,066. Based on 2023. | calculation and filter evidence | Pass |
| 25 | How many good units were produced last quarter? | 9,731 | Good units were 9,731. Based on the last complete quarter in this dataset (2026-07-01 to 2026-09-30). Good units equal produced units less recorded defects. | calculation and filter evidence | Pass |
| 26 | How many units were produced in 2024? | 38,732 | Units produced were 38,732. Based on 2024. | calculation and filter evidence | Pass |
| 27 | What was the defect rate in 2025? | 3.0% | The defect rate was 3.0% (1,369 defects out of 46,301 units produced). Based on 2025. | calculation and filter evidence | Pass |
| 28 | Show good units by facility in 2024. | Jaipur Unit 1 | Good units by facility: Jaipur Unit 1 10,904; Jaipur Unit 2 9,461; Surat Unit 8,880; Tiruppur Unit 8,323. Based on 2024. | ranking order and all 4 values checked | Pass |
| 29 | Why did returns go up last month? | did not go up | The return rate did not go up in the latest complete month. It was 2.4% in September 2026 versus 2.8% in August 2026. I compared returned units ÷ ordered units. The data has no return-reason field, so it cannot explain causes. | calculation and filter evidence | Pass |
| 30 | Which category should I restock? | I can’t answer that from this data | I can’t answer that from this data. There are no stock-on-hand, stockout, lead-time or purchase-order fields. I can show sales and margin as context, but those alone are not a restock recommendation. | calculation and filter evidence | Pass |

## Guardrail notes

The restock question is intentionally refused because the dataset has no inventory or replenishment fields. The returns question describes category contribution as a place to investigate; it does not claim that category caused the change. Month and year answers include the selected period and calculation details in the dashboard.
