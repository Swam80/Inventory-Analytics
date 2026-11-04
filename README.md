# Inventory Segmentation & Replenishment Planning | Excel

An Excel project using **UCI Online Retail** data to prioritise products through ABC–XYZ classification and explore Safety Stock and Reorder Point scenarios.

## Objective

Identify which products deserve closer planning attention and assess how sales variability, service targets, and changing demand levels affect replenishment decisions.

## Data & Tools

- **Source:** [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Period:** January–November 2011
- **Tools:** Excel 2016, PivotTables, charts, data validation, and formulas
- **Analysed:** 461,414 eligible transaction lines across **3,715 SKUs**

## Approach

- Cleaned transactions using documented exclusion rules for cancellations, invalid quantities/prices, and non-product entries.
- Identified and excluded a **74,215-unit sale matched to an equal cancellation**, preventing an inflated demand signal.
- Analysed monthly sales and classified SKUs using **sales-value ABC** and **monthly coefficient-of-variation XYZ**.
- Built an interactive daily-sales calculator for AX, AY, and AZ examples.
- Compared service targets and two AZ demand scenarios.

```text
CV = Monthly standard deviation / Average monthly units

Safety Stock = Z × Daily standard deviation × √Lead time

ROP = Average daily units × Lead time + Safety Stock
```

## Key Findings

- **816 SKUs—approximately 22% of the range—generated 80% of eligible sales value.**
- Eligible sales totalled **£8.80 million**, with November highest at **£1.46 million**.
- The portfolio included **214 AX** and **273 AZ** products, supporting different planning priorities.

### Replenishment Examples

*Assumed seven-day lead time and 95% cycle service target.*

| SKU | Class | Safety Stock | ROP |
|---|---|---:|---:|
| 22423 | AX | 172 | 410 |
| 47566 | AY | 303 | 679 |
| 22086 | AZ | 518 | 829 |

For AZ SKU **22086**, approximately **91% of units sold occurred in September–November**. Its illustrative ROP changed from **158 units if the uplift fades** to **1,854 if the recent sales level persists**.

This highlighted the need to investigate changing demand before adopting a historical-average stock policy.

## Deliverables

- Excel analysis workbook and summary dashboard
- Interactive replenishment calculator with separate AX, AY, and AZ views
- PowerPoint presentation covering methodology, results, and recommendations

## Assumptions & Limitations

Sales serve as a demand proxy. Lead time and service targets are assumed. Stock balances, supplier performance, and inventory costs are unavailable. Replenishment outputs are illustrative, particularly for trending AZ demand where historical variability includes changes in sales level.

**Author — Swamesh Lotlikar**
