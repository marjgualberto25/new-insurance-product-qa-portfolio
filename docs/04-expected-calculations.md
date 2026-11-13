# Expected Results – Premium & Commission

[← Back to README](../README.md)

Expected values used by the premium and commission test cases. In the Excel version these are live formulas that pull from the rate tables.

## Premium scenarios

| Scenario | Age | Basic SA | PAR SA | Occ. class | CIR SA | Mode | Basic annual | PAR annual | CIR annual | Total annual | Modal factor | Total modal premium |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| C1 | 35 | 1,000,000 | 1,000,000 | 1 | 500,000 | Annual | 24,000.00 | 1,500.00 | 2,500.00 | 28,000.00 | 1.000 | 28,000.00 |
| C2 | 35 | 1,000,000 | 1,000,000 | 1 | 500,000 | Monthly | 24,000.00 | 1,500.00 | 2,500.00 | 28,000.00 | 0.090 | 2,520.00 |
| C3 | 25 | 500,000 | 500,000 | 2 | 250,000 | Quarterly | 9,000.00 | 1,125.00 | 875.00 | 11,000.00 | 0.265 | 2,915.00 |
| C4 | 55 | 2,000,000 | 2,000,000 | 3 | 1,000,000 | Semi-annual | 104,000.00 | 6,000.00 | 13,000.00 | 123,000.00 | 0.520 | 63,960.00 |
| C5 | 45 | 3,000,000 | 0 | – | 0 | Annual | 105,000.00 | 0.00 | 0.00 | 105,000.00 | 1.000 | 105,000.00 |

**Formulas**
- Basic annual = Basic SA ÷ 1,000 × basic rate (age band)
- PAR annual = PAR SA ÷ 1,000 × occupation class rate
- CIR annual = CIR SA ÷ 1,000 × CI rate (age band)
- Total modal premium = (Basic + PAR + CIR) × modal factor, rounded to 2 decimals

## Monthly breakdown – C2 (used by TC-031)

| Component | Monthly amount |
|---|---|
| Basic | 2,160.00 |
| PAR | 135.00 |
| CIR | 225.00 |
| Total | 2,520.00 |

## Commission by policy year – C1 (Annual mode)

| Policy year | Basic premium | Rider premium | Basic rate | Rider rate | Basic commission | Rider commission | Total commission | Payable? |
|---|---|---|---|---|---|---|---|---|
| 1 | 24,000.00 | 4,000.00 | 30% | 20% | 7,200.00 | 800.00 | 8,000.00 | Yes |
| 2 | 24,000.00 | 4,000.00 | 15% | 10% | 3,600.00 | 400.00 | 4,000.00 | Yes |
| 3 | 24,000.00 | 4,000.00 | 10% | 5% | 2,400.00 | 200.00 | 2,600.00 | Yes |
| 4 | 24,000.00 | 4,000.00 | 5% | 5% | 1,200.00 | 200.00 | 1,400.00 | Yes |
| 5 | 24,000.00 | 4,000.00 | 5% | 5% | 1,200.00 | 200.00 | 1,400.00 | Yes |
| 6 | 24,000.00 | 4,000.00 | 0% | 0% | 0.00 | 0.00 | 0.00 | No |
| 7 | 24,000.00 | 4,000.00 | 0% | 0% | 0.00 | 0.00 | 0.00 | No |
| 8 | 24,000.00 | 4,000.00 | 0% | 0% | 0.00 | 0.00 | 0.00 | No |
| 9 | 24,000.00 | 4,000.00 | 0% | 0% | 0.00 | 0.00 | 0.00 | No |
| 10 | 24,000.00 | 4,000.00 | 0% | 0% | 0.00 | 0.00 | 0.00 | No |
| **Total** |  |  |  |  | **15,600.00** | **1,800.00** | **17,400.00** |  |
