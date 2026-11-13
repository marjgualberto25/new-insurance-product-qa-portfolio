# Insurance Product Onboarding – QA Portfolio

A QA package for onboarding a new life insurance product, built the way I'd prepare one on a live insurance account: product rules, user stories with acceptance criteria, test cases, expected-result calculations, and a requirements traceability matrix.

> Fictional product and insurer created for portfolio purposes. No real company data is used.

## The product: LifeAnchor 10 (LA10)

| Attribute | Detail |
|---|---|
| Insurer | Aurora Crest Life Assurance (fictional) |
| Type | Regular-pay traditional life insurance |
| Premium paying term | 10 years |
| Coverage term | 20 years |
| Riders | Personal Accident Rider (PAR), Critical Illness Rider (CIR) – premiums added to the total premium |
| Commission | **Payable for policy years 1–5 only**; years 6–10 earn 0% |
| Currency | PHP |

## What's inside

| # | Document | What it covers |
|---|---|---|
| 1 | [Product Specification](docs/01-product-spec.md) | 20 business rules, rate tables, modal factors, commission schedule |
| 2 | [User Stories & Acceptance Criteria](docs/02-user-stories.md) | 1 epic, 4 user stories, 17 Given/When/Then acceptance criteria |
| 3 | [Test Cases](docs/03-test-cases.md) | 36 test cases – positive, negative and boundary |
| 4 | [Expected Calculations](docs/04-expected-calculations.md) | Worked premium and commission figures behind the calculation tests |
| 5 | [Traceability Matrix](docs/05-traceability-matrix.md) | AC → test case mapping, 100% coverage |
| – | [Excel workbook](excel/LA10_QA_Package.xlsx) | Same package with live formulas and execution tracking |

## Test coverage at a glance

| User story | Focus | ACs | Test cases |
|---|---|---|---|
| US-01 | Product setup & eligibility | 4 | 9 |
| US-02 | Rider attachment, limits & lifecycle | 4 | 14 |
| US-03 | Premium computation & policy schedule | 4 | 8 |
| US-04 | Commission – 5-year cap, late payment, free-look clawback | 5 | 5 |
| **Total** | | **17** | **36** |

## Test design approach

- **Boundary value analysis** on entry ages (17/18, 60/61, 55/56) and sum assured limits (min, max, max + 1)
- **Equivalence partitioning** across age bands, occupation classes and payment modes
- **Negative testing** for every validation rule, checking the exact error message
- **Calculation verification** against independently computed expected results
- **Lifecycle testing** for rider termination on lapse, surrender and cancellation
- **Commission edge cases**: the year 5 → year 6 cutoff, late premiums paid across a policy year boundary, and free-look clawback

## Author

**Marj Gualberto** – Business Analyst / QA with 7+ years in insurance and financial services (policy issuance, underwriting, commissions, agent and channel configuration; credit decisioning and KYC).
