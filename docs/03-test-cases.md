# Test Cases – LifeAnchor 10 (LA10)

[← Back to README](../README.md)

Environment: SIT · Total: **36 test cases** · Status options: Not Run, Pass, Fail, Blocked

## Summary

| TC ID | AC ID | Scenario | Type | Priority | Status |
|---|---|---|---|---|---|
| TC-001 | AC-01.1 | Verify LA10 appears in product list with correct attributes | Positive | High | Not Run |
| TC-002 | AC-01.2 | Accept insured at minimum entry age 18 | Boundary | High | Not Run |
| TC-003 | AC-01.2 | Accept insured at maximum entry age 60 | Boundary | High | Not Run |
| TC-004 | AC-01.2 | Reject insured aged 17 | Negative | High | Not Run |
| TC-005 | AC-01.2 | Reject insured aged 61 | Negative | High | Not Run |
| TC-006 | AC-01.3 | Accept basic SA at minimum (500,000) and maximum (10,000,000) | Boundary | High | Not Run |
| TC-007 | AC-01.3 | Reject basic SA below minimum | Negative | High | Not Run |
| TC-008 | AC-01.3 | Reject basic SA above maximum | Negative | Medium | Not Run |
| TC-009 | AC-01.4 | Verify only regular payment modes are offered | Positive | High | Not Run |
| TC-010 | AC-02.1 | Attach PAR only | Positive | High | Not Run |
| TC-011 | AC-02.1 | Attach CIR only | Positive | High | Not Run |
| TC-012 | AC-02.1 | Attach both PAR and CIR | Positive | High | Not Run |
| TC-013 | AC-02.2 | Accept PAR SA equal to 100% of basic SA | Boundary | Medium | Not Run |
| TC-014 | AC-02.2 | Reject PAR SA above basic SA | Negative | High | Not Run |
| TC-015 | AC-02.2 | Reject PAR SA above 3,000,000 cap | Negative | High | Not Run |
| TC-016 | AC-02.2 | Decline PAR for occupation class 4 | Negative | High | Not Run |
| TC-017 | AC-02.3 | Accept CIR at age 55 with SA at 50% of basic | Boundary | High | Not Run |
| TC-018 | AC-02.3 | Reject CIR for insured aged 56 | Negative | High | Not Run |
| TC-019 | AC-02.3 | Reject CIR SA above 50% of basic SA | Negative | High | Not Run |
| TC-020 | AC-02.3 | Reject CIR SA above 2,000,000 cap | Negative | Medium | Not Run |
| TC-021 | AC-02.4 | Riders terminate when basic plan is surrendered | Positive | High | Not Run |
| TC-022 | AC-02.4 | Riders terminate when basic plan lapses | Positive | High | Not Run |
| TC-023 | AC-02.4 | Block rider issuance without basic plan | Negative | Medium | Not Run |
| TC-024 | AC-03.1 | Basic premium – age band 31–40 | Positive | High | Not Run |
| TC-025 | AC-03.1 | Basic premium – age band 41–50, no riders | Positive | High | Not Run |
| TC-026 | AC-03.2 | PAR class 1 and CIR premium – age 35 | Positive | High | Not Run |
| TC-027 | AC-03.2 | PAR class 3 and CIR premium – age 55 | Positive | High | Not Run |
| TC-028 | AC-03.3 | Total modal premium – Monthly | Positive | High | Not Run |
| TC-029 | AC-03.3 | Total modal premium – Quarterly | Positive | High | Not Run |
| TC-030 | AC-03.3 | Total modal premium – Semi-annual | Positive | Medium | Not Run |
| TC-031 | AC-03.4 | Policy schedule shows premium breakdown | Positive | Medium | Not Run |
| TC-032 | AC-04.1 | Basic commission – policy years 1 to 5 | Positive | High | Not Run |
| TC-033 | AC-04.2 | Rider commission – policy years 1 to 5 | Positive | High | Not Run |
| TC-034 | AC-04.3 | No commission for policy years 6 to 10 | Positive | High | Not Run |
| TC-035 | AC-04.4 | Late year-5 premium paid in year 6 uses year-5 rate | Boundary | High | Not Run |
| TC-036 | AC-04.5 | Clawback on free-look cancellation | Positive | High | Not Run |

## Detailed test cases

### US-01 · Product setup & eligibility

#### TC-001 – Verify LA10 appears in product list with correct attributes

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.1 |
| Module | Product Setup |
| Type / Priority | Positive / High |
| Preconditions | LA10 deployed to SIT; agent user has LA10 licence |
| Test data | Product code: LA10 |

**Steps**

1. Log in to PAS as agent.
2. Go to New Business > Product List.
3. Search 'LA10'.

**Expected result:** LifeAnchor 10 is listed; plan type = Regular Pay; PPT = 10 years; coverage term = 20 years; currency = PHP.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-002 – Accept insured at minimum entry age 18

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| Module | Eligibility |
| Type / Priority | Boundary / High |
| Preconditions | Agent logged in |
| Test data | Age 18; basic SA 500,000; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Proposal passes age validation; no error shown.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-003 – Accept insured at maximum entry age 60

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| Module | Eligibility |
| Type / Priority | Boundary / High |
| Preconditions | Agent logged in |
| Test data | Age 60; basic SA 1,000,000; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Proposal passes age validation; basic rate 52.00 applied (age band 51–60).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-004 – Reject insured aged 17

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| Module | Eligibility |
| Type / Priority | Negative / High |
| Preconditions | Agent logged in |
| Test data | Age 17; basic SA 500,000; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Submission blocked. Message: 'Insured age is outside the allowed entry age for this plan'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-005 – Reject insured aged 61

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| Module | Eligibility |
| Type / Priority | Negative / High |
| Preconditions | Agent logged in |
| Test data | Age 61; basic SA 500,000; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Submission blocked. Message: 'Insured age is outside the allowed entry age for this plan'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-006 – Accept basic SA at minimum (500,000) and maximum (10,000,000)

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.3 |
| Module | Eligibility |
| Type / Priority | Boundary / High |
| Preconditions | Agent logged in |
| Test data | Run 1: SA 500,000<br>Run 2: SA 10,000,000<br>Age 35; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Both proposals pass SA validation.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-007 – Reject basic SA below minimum

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.3 |
| Module | Eligibility |
| Type / Priority | Negative / High |
| Preconditions | Agent logged in |
| Test data | SA 499,999; Age 35; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Submission blocked. Message shows allowed range 500,000 – 10,000,000.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-008 – Reject basic SA above maximum

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.3 |
| Module | Eligibility |
| Type / Priority | Negative / Medium |
| Preconditions | Agent logged in |
| Test data | SA 10,000,001; Age 35; Annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Submission blocked. Message shows allowed range 500,000 – 10,000,000.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-009 – Verify only regular payment modes are offered

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.4 |
| Module | Payment Mode |
| Type / Priority | Positive / High |
| Preconditions | Agent logged in |
| Test data | LA10 proposal |

**Steps**

1. Create LA10 proposal.
2. Open Payment Mode dropdown.

**Expected result:** Dropdown lists exactly: Annual, Semi-annual, Quarterly, Monthly. 'Single' is not listed.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-02 · Riders

#### TC-010 – Attach PAR only

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| Module | Riders |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal (age 35, SA 1,000,000) |
| Test data | PAR SA 1,000,000; Occ. class 1 |

**Steps**

1. Open Riders section.
2. Add PAR with test data.
3. Save.

**Expected result:** PAR is attached; CIR is not required; proposal saves.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-011 – Attach CIR only

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| Module | Riders |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal (age 35, SA 1,000,000) |
| Test data | CIR SA 500,000 |

**Steps**

1. Open Riders section.
2. Add CIR with test data.
3. Save.

**Expected result:** CIR is attached; PAR is not required; proposal saves.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-012 – Attach both PAR and CIR

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| Module | Riders |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal (age 35, SA 1,000,000) |
| Test data | PAR SA 1,000,000 class 1; CIR SA 500,000 |

**Steps**

1. Open Riders section.
2. Add PAR and CIR.
3. Save.

**Expected result:** Both riders are attached and listed under the policy.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-013 – Accept PAR SA equal to 100% of basic SA

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| Module | Riders – PAR |
| Type / Priority | Boundary / Medium |
| Preconditions | Valid LA10 proposal (SA 2,000,000) |
| Test data | PAR SA 2,000,000; class 2 |

**Steps**

Add PAR, then Validate.

**Expected result:** PAR passes validation.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-014 – Reject PAR SA above basic SA

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| Module | Riders – PAR |
| Type / Priority | Negative / High |
| Preconditions | Valid LA10 proposal (SA 1,000,000) |
| Test data | PAR SA 1,000,001; class 1 |

**Steps**

Add PAR, then Validate.

**Expected result:** PAR rejected. Message: 'PA rider SA cannot exceed 100% of basic SA'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-015 – Reject PAR SA above 3,000,000 cap

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| Module | Riders – PAR |
| Type / Priority | Negative / High |
| Preconditions | Valid LA10 proposal (SA 5,000,000) |
| Test data | PAR SA 3,000,001; class 1 |

**Steps**

Add PAR, then Validate.

**Expected result:** PAR rejected. Message: 'PA rider SA cannot exceed 3,000,000'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-016 – Decline PAR for occupation class 4

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| Module | Riders – PAR |
| Type / Priority | Negative / High |
| Preconditions | Valid LA10 proposal (SA 1,000,000) |
| Test data | PAR SA 500,000; class 4 |

**Steps**

Add PAR, then Validate.

**Expected result:** PAR rejected. Message: 'PA rider not available for occupation class 4'. Basic plan remains valid.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-017 – Accept CIR at age 55 with SA at 50% of basic

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| Module | Riders – CIR |
| Type / Priority | Boundary / High |
| Preconditions | Valid LA10 proposal (age 55, SA 2,000,000) |
| Test data | CIR SA 1,000,000 |

**Steps**

Add CIR, then Validate.

**Expected result:** CIR passes validation; CI rate 13.00 applied.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-018 – Reject CIR for insured aged 56

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| Module | Riders – CIR |
| Type / Priority | Negative / High |
| Preconditions | Valid LA10 proposal (age 56, SA 1,000,000) |
| Test data | CIR SA 500,000 |

**Steps**

Add CIR, then Validate.

**Expected result:** CIR rejected. Message: 'Insured age is outside the allowed entry age for the CI rider'. Basic plan remains valid.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-019 – Reject CIR SA above 50% of basic SA

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| Module | Riders – CIR |
| Type / Priority | Negative / High |
| Preconditions | Valid LA10 proposal (SA 1,000,000) |
| Test data | CIR SA 500,001 |

**Steps**

Add CIR, then Validate.

**Expected result:** CIR rejected. Message: 'CI rider SA cannot exceed 50% of basic SA'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-020 – Reject CIR SA above 2,000,000 cap

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| Module | Riders – CIR |
| Type / Priority | Negative / Medium |
| Preconditions | Valid LA10 proposal (SA 6,000,000) |
| Test data | CIR SA 2,000,001 |

**Steps**

Add CIR, then Validate.

**Expected result:** CIR rejected. Message: 'CI rider SA cannot exceed 2,000,000'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-021 – Riders terminate when basic plan is surrendered

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.4 |
| Module | Riders – Lifecycle |
| Type / Priority | Positive / High |
| Preconditions | In-force LA10 policy with PAR and CIR |
| Test data | Surrender effective date: today |

**Steps**

1. Log in as policy servicing user.
2. Process full surrender of basic plan.
3. View policy coverage list.

**Expected result:** Basic, PAR and CIR all show status 'Terminated' with the same termination date; no further rider premium is billed.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-022 – Riders terminate when basic plan lapses

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.4 |
| Module | Riders – Lifecycle |
| Type / Priority | Positive / High |
| Preconditions | In-force LA10 policy with PAR and CIR; premium unpaid past grace period |
| Test data | Run lapse batch |

**Steps**

1. Run lapse batch job.
2. View policy coverage list.

**Expected result:** Basic, PAR and CIR all show status 'Lapsed' on the same date.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-023 – Block rider issuance without basic plan

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.4 |
| Module | Riders – Lifecycle |
| Type / Priority | Negative / Medium |
| Preconditions | Agent logged in |
| Test data | Attempt to create PAR-only proposal |

**Steps**

1. Start new proposal.
2. Try to add PAR before selecting a basic plan.

**Expected result:** System prevents it. Message: 'Select a basic plan before adding riders'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-03 · Premium computation

#### TC-024 – Basic premium – age band 31–40

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.1 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc scenario C1: age 35, SA 1,000,000 |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Basic annual premium = 24,000.00 (see Expected Calc C1).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-025 – Basic premium – age band 41–50, no riders

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.1 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc scenario C5: age 45, SA 3,000,000 |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Basic annual premium = 105,000.00; rider premiums = 0 (see Expected Calc C5).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-026 – PAR class 1 and CIR premium – age 35

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.2 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc C1: PAR 1,000,000 class 1; CIR 500,000 |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** PAR annual premium = 1,500.00; CIR annual premium = 2,500.00.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-027 – PAR class 3 and CIR premium – age 55

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.2 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc C4: PAR 2,000,000 class 3; CIR 1,000,000 |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** PAR annual premium = 6,000.00; CIR annual premium = 13,000.00.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-028 – Total modal premium – Monthly

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.3 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc C2 (C1 data, Monthly) |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Total modal premium = 2,520.00 (28,000.00 × 0.09).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-029 – Total modal premium – Quarterly

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.3 |
| Module | Premium |
| Type / Priority | Positive / High |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc C3: age 25, SA 500,000, PAR 500,000 class 2, CIR 250,000, Quarterly |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Total modal premium = 2,915.00 (11,000.00 × 0.265).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-030 – Total modal premium – Semi-annual

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.3 |
| Module | Premium |
| Type / Priority | Positive / Medium |
| Preconditions | Valid LA10 proposal |
| Test data | Expected Calc C4, Semi-annual |

**Steps**

1. Log in to PAS as agent.
2. Create new proposal for LA10.
3. Enter test data.
4. Click Validate / Compute Premium.

**Expected result:** Total modal premium = 63,960.00 (123,000.00 × 0.52).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-031 – Policy schedule shows premium breakdown

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.4 |
| Module | Policy Schedule |
| Type / Priority | Positive / Medium |
| Preconditions | Policy issued using Expected Calc C2 data |
| Test data | Policy issued, Monthly |

**Steps**

1. Issue policy.
2. Generate policy schedule PDF.
3. Review premium section.

**Expected result:** Schedule shows Basic 2,160.00, PAR 135.00, CIR 225.00 and Total 2,520.00 per month; amounts match PAS.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-04 · Commission (years 1–5 only)

#### TC-032 – Basic commission – policy years 1 to 5

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.1 |
| Module | Commission |
| Type / Priority | Positive / High |
| Preconditions | Policy from Expected Calc C1 issued, Annual; agent assigned |
| Test data | Collect annual premium for years 1–5 |

**Steps**

1. Post premium for each year 1–5.
2. Run commission batch after each.
3. Check agent commission statement.

**Expected result:** Basic commission: Y1 7,200.00; Y2 3,600.00; Y3 2,400.00; Y4 1,200.00; Y5 1,200.00 (see Expected Calc commission table).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-033 – Rider commission – policy years 1 to 5

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.2 |
| Module | Commission |
| Type / Priority | Positive / High |
| Preconditions | Same policy as previous test |
| Test data | Collect annual premium for years 1–5 |

**Steps**

1. Post premium for each year 1–5.
2. Run commission batch.
3. Check rider commission lines.

**Expected result:** Rider commission (PAR + CIR): Y1 800.00; Y2 400.00; Y3 200.00; Y4 200.00; Y5 200.00.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-034 – No commission for policy years 6 to 10

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.3 |
| Module | Commission |
| Type / Priority | Positive / High |
| Preconditions | Same policy, years 1–5 premiums paid |
| Test data | Collect annual premium for years 6–10 |

**Steps**

1. Post premium for each year 6–10.
2. Run commission batch.
3. Check agent statement and policy premium history.

**Expected result:** Premiums for years 6–10 are posted to the policy (28,000.00 each). No commission line is generated for basic or riders for years 6–10. Total lifetime commission = 17,400.00.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-035 – Late year-5 premium paid in year 6 uses year-5 rate

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.4 |
| Module | Commission |
| Type / Priority | Boundary / High |
| Preconditions | Policy C1; year-5 premium unpaid at year-6 anniversary, still within grace period |
| Test data | Pay year-5 premium 10 days after year-6 anniversary |

**Steps**

1. Post year-5 premium with payment date in year 6.
2. Run commission batch.

**Expected result:** Commission generated at year-5 rates: basic 1,200.00 + riders 200.00 = 1,400.00.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-036 – Clawback on free-look cancellation

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.5 |
| Module | Commission |
| Type / Priority | Positive / High |
| Preconditions | Policy C1 issued; Y1 commission 8,000.00 already paid; policy delivered 10 days ago |
| Test data | Free-look cancellation request |

**Steps**

1. Process free-look cancellation.
2. Run commission batch.
3. Check agent statement.

**Expected result:** Policy status 'Cancelled – Free Look'; full premium refunded; clawback line of -8,000.00 posted to the agent.

**Actual result:** _Not yet executed_ · **Status:** Not Run
