# Requirements Traceability Matrix

[← Back to README](../README.md)

**Coverage: 17 of 17 acceptance criteria covered by 36 test cases.**

| Story | AC ID | Acceptance criterion | Linked test cases | # TCs | Coverage | Executed |
|---|---|---|---|---|---|---|
| US-01 | AC-01.1 | Given the LA10 product is configured, when an agent opens New Business > Product List, then LifeAnchor 10 (LA10) is listed as a regular-pay plan with a 10-year PPT and 20-year coverage term. | TC-001 | 1 | Covered | 0 |
| US-01 | AC-01.2 | Given a new proposal for LA10, when the insured's age is outside 18–60, then the system blocks submission and shows 'Insured age is outside the allowed entry age for this plan'. | TC-002, TC-003, TC-004, TC-005 | 4 | Covered | 0 |
| US-01 | AC-01.3 | Given a new proposal for LA10, when the basic SA is below 500,000 or above 10,000,000, then the system blocks submission and shows the allowed SA range. | TC-006, TC-007, TC-008 | 3 | Covered | 0 |
| US-01 | AC-01.4 | Given a new proposal for LA10, when the agent selects a payment mode, then only Annual, Semi-annual, Quarterly and Monthly are available; Single pay is not offered. | TC-009 | 1 | Covered | 0 |
| US-02 | AC-02.1 | Given an LA10 proposal, when the agent opens the Riders section, then PAR and CIR are available as optional riders and can be attached individually or together. | TC-010, TC-011, TC-012 | 3 | Covered | 0 |
| US-02 | AC-02.2 | Given PAR is attached, when the insured is outside age 18–60, the PAR SA exceeds 100% of basic SA or 3,000,000, or the occupation class is 4, then the PAR is rejected with a specific validation message. | TC-013, TC-014, TC-015, TC-016 | 4 | Covered | 0 |
| US-02 | AC-02.3 | Given CIR is attached, when the insured is outside age 18–55 or the CIR SA exceeds 50% of basic SA or 2,000,000, then the CIR is rejected with a specific validation message. | TC-017, TC-018, TC-019, TC-020 | 4 | Covered | 0 |
| US-02 | AC-02.4 | Given an in-force LA10 policy with riders, when the basic plan lapses, is surrendered or is cancelled, then all attached riders terminate on the same date; a rider cannot be issued without the basic plan. | TC-021, TC-022, TC-023 | 3 | Covered | 0 |
| US-03 | AC-03.1 | Given a valid LA10 proposal, when premium is computed, then basic annual premium = basic SA ÷ 1,000 × basic rate for the insured's age band. | TC-024, TC-025 | 2 | Covered | 0 |
| US-03 | AC-03.2 | Given PAR and/or CIR are attached, when premium is computed, then PAR annual premium = PAR SA ÷ 1,000 × class rate and CIR annual premium = CIR SA ÷ 1,000 × CI rate for the age band. | TC-026, TC-027 | 2 | Covered | 0 |
| US-03 | AC-03.3 | Given a payment mode is selected, when premium is computed, then total modal premium = (basic + PAR + CIR annual premium) × modal factor, rounded to 2 decimals. | TC-028, TC-029, TC-030 | 3 | Covered | 0 |
| US-03 | AC-03.4 | Given the policy is issued, when the policy schedule is generated, then it shows basic, PAR and CIR premiums separately and the total modal premium. | TC-031 | 1 | Covered | 0 |
| US-04 | AC-04.1 | Given a basic-plan premium is collected for policy years 1–5, when the commission run executes, then commission = collected basic premium × basic rate for that policy year. | TC-032 | 1 | Covered | 0 |
| US-04 | AC-04.2 | Given a rider premium is collected for policy years 1–5, when the commission run executes, then commission = collected rider premium × rider rate for that policy year. | TC-033 | 1 | Covered | 0 |
| US-04 | AC-04.3 | Given a premium is collected for policy years 6–10, when the commission run executes, then no payable commission is generated (0%), while the premium is still posted to the policy. | TC-034 | 1 | Covered | 0 |
| US-04 | AC-04.4 | Given a premium is due in policy year 5 but paid in policy year 6, when the commission run executes, then commission uses the year-5 rate; no commission is generated for premiums not yet collected. | TC-035 | 1 | Covered | 0 |
| US-04 | AC-04.5 | Given a policy is cancelled within the 15-day free-look period, when the cancellation is processed, then the premium is refunded and 100% of commission paid is clawed back from the agent. | TC-036 | 1 | Covered | 0 |

_Execution counts are live in the Excel version and update from the Status column on the Test Cases tab._
