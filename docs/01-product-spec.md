# Product Specification – LifeAnchor 10 (LA10)

[← Back to README](../README.md)

> Fictional product and insurer created for portfolio purposes. No real company data is used.

Age = age last birthday at policy issue date. All amounts in PHP.

## Business rules

| Rule ID | Area | Rule | Value / Limit |
|---|---|---|---|
| BR-01 | Product | Product code / name | LA10 – LifeAnchor 10 |
| BR-02 | Product | Premium paying term (PPT) | 10 years |
| BR-03 | Product | Coverage term | 20 years |
| BR-04 | Product | Allowed payment modes | Annual, Semi-annual, Quarterly, Monthly (Single pay not allowed) |
| BR-05 | Basic | Entry age – insured | 18 to 60 |
| BR-06 | Basic | Basic sum assured (SA) | Min 500,000 / Max 10,000,000 |
| BR-07 | PAR | PA rider entry age | 18 to 60 |
| BR-08 | PAR | PA rider SA | Up to 100% of basic SA, max 3,000,000 |
| BR-09 | PAR | Occupation class | Classes 1–3 accepted; Class 4 declined for PAR |
| BR-10 | CIR | CI rider entry age | 18 to 55 |
| BR-11 | CIR | CI rider SA | Up to 50% of basic SA, max 2,000,000 |
| BR-12 | Riders | Rider dependency | Riders cannot exist without the basic plan; riders terminate when the basic plan lapses, is surrendered or is cancelled |
| BR-13 | Premium | Basic annual premium | Basic SA ÷ 1,000 × basic rate for the insured's age band |
| BR-14 | Premium | PAR annual premium | PAR SA ÷ 1,000 × rate for occupation class (not age-rated) |
| BR-15 | Premium | CIR annual premium | CIR SA ÷ 1,000 × CI rate for the insured's age band |
| BR-16 | Premium | Total modal premium | (Basic + PAR + CIR annual premium) × modal factor, rounded to 2 decimals |
| BR-17 | Commission | Basic plan commission rates by policy year | Y1 30% · Y2 15% · Y3 10% · Y4 5% · Y5 5% · Y6–Y10 0% |
| BR-18 | Commission | Rider commission rates by policy year (PAR and CIR) | Y1 20% · Y2 10% · Y3 5% · Y4 5% · Y5 5% · Y6–Y10 0% |
| BR-19 | Commission | Commission basis | Commission is computed on premium actually collected, at the rate of the policy year the premium is due for (not the year it is paid) |
| BR-20 | Commission | Free-look | 15 calendar days from policy delivery. Cancellation within free-look refunds premium and claws back 100% of commission paid |

## Rate tables

Rates are annual premium per 1,000 sum assured.

### Basic plan

| Age band | Rate per 1,000 |
|---|---|
| 18–30 | 18.00 |
| 31–40 | 24.00 |
| 41–50 | 35.00 |
| 51–60 | 52.00 |

### Critical Illness rider

| Age band | Rate per 1,000 |
|---|---|
| 18–30 | 3.50 |
| 31–40 | 5.00 |
| 41–50 | 8.50 |
| 51–55 | 13.00 |

### Personal Accident rider

| Occupation class | Rate per 1,000 |
|---|---|
| 1 | 1.50 |
| 2 | 2.25 |
| 3 | 3.00 |
| 4 | Declined |

### Modal factors

| Payment mode | Factor |
|---|---|
| Annual | 1.000 |
| Semi-annual | 0.520 |
| Quarterly | 0.265 |
| Monthly | 0.090 |

### Commission schedule

| Policy year | Basic plan | Riders (PAR & CIR) |
|---|---|---|
| 1 | 30% | 20% |
| 2 | 15% | 10% |
| 3 | 10% | 5% |
| 4 | 5% | 5% |
| 5 | 5% | 5% |
| 6 | 0% | 0% |
| 7 | 0% | 0% |
| 8 | 0% | 0% |
| 9 | 0% | 0% |
| 10 | 0% | 0% |
