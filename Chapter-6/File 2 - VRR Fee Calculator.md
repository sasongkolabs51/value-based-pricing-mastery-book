## File 2: VRR Fee Calculator (.xlsx)

**Filename:** `VRR-Calculator.xlsx`

Create a new Excel workbook with two sheets: **VRR Calculator** and **Example**.

### Sheet 1: VRR Calculator

| A                                                                        | B                                               | C                                                                         | D   |
| ------------------------------------------------------------------------ | ----------------------------------------------- | ------------------------------------------------------------------------- | --- |
| **VALUE REALIZATION RATE (VRR) CALCULATOR**                              |                                                 |                                                                           |     |
|                                                                          |                                                 |                                                                           |     |
| **Step 1: Outcome Significance (OS)**                                    |                                                 |                                                                           |     |
| Client's At-Risk Value (Low End)                                         | $[enter]                                        |                                                                           |     |
| Client's At-Risk Value (High End)                                        | $[enter]                                        |                                                                           |     |
| **OS Midpoint**                                                          | =(B5+B6)/2                                      |                                                                           |     |
|                                                                          |                                                 |                                                                           |     |
| **Step 2: Risk Absorption (RA)**                                         |                                                 |                                                                           |     |
| Risk Level (Low/Medium/High)                                             | [enter]                                         |                                                                           |     |
| RA Percentage                                                            | [enter %]                                       | (Guidance: Low=1%, Medium=2-3%, High=4-5%)                                |     |
| **RA Value (OS × RA)**                                                   | =B7*B11                                         |                                                                           |     |
|                                                                          |                                                 |                                                                           |     |
| **Step 3: Judgment Intensity (JI)**                                      |                                                 |                                                                           |     |
| Judgment Requirement Score (from Ch 4: 1=highly durable, 5=commoditized) | [enter 1-5]                                     |                                                                           |     |
| Risk Transfer Score (1=highly durable, 5=commoditized)                   | [enter 1-5]                                     |                                                                           |     |
| Average Score                                                            | =AVERAGE(B14,B15)                               |                                                                           |     |
| **JI Multiplier**                                                        | =IF(B16<=2,1,IF(B16<=3,0.8,IF(B16<=4,0.6,0.4))) | (Auto-calculated: 1.0 for avg 1-2; 0.8 for 2-3; 0.6 for 3-4; 0.4 for 4-5) |     |
|                                                                          |                                                 |                                                                           |     |
| **VRR FEE CALCULATION**                                                  |                                                 |                                                                           |     |
| **VRR Fee = (OS Midpoint × RA) × JI**                                    | **=B12*B17**                                    |                                                                           |     |
|                                                                          |                                                 |                                                                           |     |
| **Sense Check**                                                          |                                                 |                                                                           |     |
| Old Model Hourly Estimate                                                | $[enter]                                        |                                                                           |     |
| VRR Fee as % of At-Risk Midpoint                                         | =B19/B7                                         | (Target: 1-5% of at-risk value)                                           |     |
| VRR Fee vs. Old Model                                                    | =B19/B21                                        | (Target: 3-10x for high-stakes work)                                      |     |

### Sheet 2: Example

Pre-populate with the pharma example from the book:

| A | B |
|---|---|
| Client's At-Risk Value (Low End) | $50,000,000 |
| Client's At-Risk Value (High End) | $80,000,000 |
| OS Midpoint | $65,000,000 |
| Risk Level | High |
| RA Percentage | 3% |
| RA Value | $1,950,000 |
| Judgment Requirement Score | 2 |
| Risk Transfer Score | 2 |
| Average Score | 2.0 |
| JI Multiplier | 1.00 |
| **VRR Fee** | **$1,950,000** |

Protect the sheets so only the input cells (those with `[enter]` prompts) are editable. All other cells are locked formulas.