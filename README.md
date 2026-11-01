# Fashion Business Dashboard

A portfolio project using fictional data for an Indian fashion maker and wholesaler founded in 2018.

The dashboard uses an ink-navy, warm-ivory and copper theme. Its data ends on 28 October 2026, so October is partial and 2026 totals are year-to-date. It helps an owner or operations lead review sales, margin, returns, markets and factory output. It has date and business filters, saved views, shareable filtered links, a reset button, charts with hover details, and click-to-filter drill-through to order lines.

“Ask this dashboard” answers supported questions with local calculations and shows the period, filters and calculation. It uses fixed patterns, not an AI model. Unsupported questions are declined. The sample has no live database connection.

## Metrics

- **Net sales:** shipped units × list price, less discounts and modeled returns.
- **Gross profit:** net sales − estimated cost of shipped units.
- **Return rate:** returned units ÷ ordered units.
- **Good units:** produced units − recorded defects.

## About the sample

All businesses, orders, products, customers, costs and exchange rates are fictional. Production is simulated per month and SKU at 7–15% above shipped units. The records do not reconcile to an ERP: there are no work orders, inventory roll-forward or return reasons. City-level sales and reliable restock recommendations are also out of scope because those fields are missing.

## Quality checks

The core evaluation scores **30/30**, checking month-by-month values, ranking order and values, plus calculation and filter evidence. A separate 12-question development set initially scored 9/12; after using its three misses to fix the assistant, it scores 12/12 as a regression check. It is no longer an untouched blind test. See [core results](qa_results.html) and [the 12-question report](heldout_results.html). The original prototype’s 28/30 used different data and looser checks, so it is not directly comparable.

Built with AI assistance. The assistant itself is deterministic, runs in the browser and sends no data to an AI service.
