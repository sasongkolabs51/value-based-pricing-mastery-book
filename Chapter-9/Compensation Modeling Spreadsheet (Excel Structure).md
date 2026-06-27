## 2. Compensation Modeling Spreadsheet (Excel Structure)

Create an Excel workbook with two sheets: **Input Dashboard** and **Margin Comparison**.

#### Sheet 1: Input Dashboard

| A                                   | B                              | C                              | D                                            |
| ----------------------------------- | ------------------------------ | ------------------------------ | -------------------------------------------- |
| **Engagement/Service Line**         | **Old Hourly Model**           | **New Post‑Pyramid Model**     | **Notes**                                    |
| Name of engagement                  |                                |                                |                                              |
| Projected/Actual Fee                | $[enter]                       | $[enter VRR fee]               |                                              |
| Delivery Team                       |                                |                                |                                              |
| – Partner hours                     | [hours]                        | [hours]                        |                                              |
| – Senior/Manager hours              | [hours]                        | [hours]                        |                                              |
| – Associate/Junior hours            | [hours]                        | [hours]                        |                                              |
| Blended Hourly Cost (fully loaded)  | $[enter]                       | $[enter]                       | Use internal cost rates, not billable rates. |
| **Total Delivery Cost**             | =SUMPRODUCT(hours, cost rates) | =SUMPRODUCT(hours, cost rates) |                                              |
| AI Tool Costs (annual/subscription) | $0                             | $[enter]                       |                                              |
| Other Direct Costs                  | $[enter]                       | $[enter]                       |                                              |
| **Total Cost**                      | sum                            | sum                            |                                              |
| **Gross Margin ($)**                | Fee – Total Cost               | Fee – Total Cost               |                                              |
| **Gross Margin (%)**                | Gross Margin / Fee             | Gross Margin / Fee             |                                              |
| **Margin Uplift**                   | –                              | New Margin % – Old Margin %    | Conditional formatting: green if positive.   |

#### Sheet 2: Margin Comparison Chart

Use the data from Sheet 1 to create a simple bar chart comparing old hourly margin vs. new post‑pyramid margin for each service line. Add a line for target margin.