# User Stories & Acceptance Criteria

[← Back to README](../README.md)

**Epic EP-LA10:** Onboard LifeAnchor 10 with Personal Accident and Critical Illness riders.

## US-01

> As a product configuration analyst, I want LifeAnchor 10 set up in the Policy Admin System with its eligibility rules, so that agents can only submit proposals that meet the product's limits.

### Acceptance criteria

**AC-01.1** _(Rule: BR-01–BR-03)_
- **Given** the LA10 product is configured
- **When** an agent opens New Business > Product List
- **Then** LifeAnchor 10 (LA10) is listed as a regular-pay plan with a 10-year PPT and 20-year coverage term.

**AC-01.2** _(Rule: BR-05)_
- **Given** a new proposal for LA10
- **When** the insured's age is outside 18–60
- **Then** the system blocks submission and shows 'Insured age is outside the allowed entry age for this plan'.

**AC-01.3** _(Rule: BR-06)_
- **Given** a new proposal for LA10
- **When** the basic SA is below 500,000 or above 10,000,000
- **Then** the system blocks submission and shows the allowed SA range.

**AC-01.4** _(Rule: BR-04)_
- **Given** a new proposal for LA10
- **When** the agent selects a payment mode
- **Then** only Annual, Semi-annual, Quarterly and Monthly are available; Single pay is not offered.

## US-02

> As an agent, I want to attach a Personal Accident rider and a Critical Illness rider to LifeAnchor 10, so that my client gets extra protection under one policy and one premium.

### Acceptance criteria

**AC-02.1** _(Rule: BR-07–BR-11)_
- **Given** an LA10 proposal
- **When** the agent opens the Riders section
- **Then** PAR and CIR are available as optional riders and can be attached individually or together.

**AC-02.2** _(Rule: BR-07–BR-09)_
- **Given** PAR is attached
- **When** the insured is outside age 18–60, the PAR SA exceeds 100% of basic SA or 3,000,000, or the occupation class is 4
- **Then** the PAR is rejected with a specific validation message.

**AC-02.3** _(Rule: BR-10–BR-11)_
- **Given** CIR is attached
- **When** the insured is outside age 18–55 or the CIR SA exceeds 50% of basic SA or 2,000,000
- **Then** the CIR is rejected with a specific validation message.

**AC-02.4** _(Rule: BR-12)_
- **Given** an in-force LA10 policy with riders
- **When** the basic plan lapses, is surrendered or is cancelled
- **Then** all attached riders terminate on the same date; a rider cannot be issued without the basic plan.

## US-03

> As a policyholder, I want my total premium to include the basic plan and attached riders at the correct rates for my chosen payment mode, so that I am billed the right amount.

### Acceptance criteria

**AC-03.1** _(Rule: BR-13)_
- **Given** a valid LA10 proposal
- **When** premium is computed
- **Then** basic annual premium = basic SA ÷ 1,000 × basic rate for the insured's age band.

**AC-03.2** _(Rule: BR-14–BR-15)_
- **Given** PAR and/or CIR are attached
- **When** premium is computed
- **Then** PAR annual premium = PAR SA ÷ 1,000 × class rate and CIR annual premium = CIR SA ÷ 1,000 × CI rate for the age band.

**AC-03.3** _(Rule: BR-16)_
- **Given** a payment mode is selected
- **When** premium is computed
- **Then** total modal premium = (basic + PAR + CIR annual premium) × modal factor, rounded to 2 decimals.

**AC-03.4** _(Rule: BR-13–BR-16)_
- **Given** the policy is issued
- **When** the policy schedule is generated
- **Then** it shows basic, PAR and CIR premiums separately and the total modal premium.

## US-04

> As a sales operations officer, I want commission on LifeAnchor 10 paid only for policy years 1 to 5, so that agent compensation follows the approved commission schedule.

### Acceptance criteria

**AC-04.1** _(Rule: BR-17)_
- **Given** a basic-plan premium is collected for policy years 1–5
- **When** the commission run executes
- **Then** commission = collected basic premium × basic rate for that policy year.

**AC-04.2** _(Rule: BR-18)_
- **Given** a rider premium is collected for policy years 1–5
- **When** the commission run executes
- **Then** commission = collected rider premium × rider rate for that policy year.

**AC-04.3** _(Rule: BR-17–BR-18)_
- **Given** a premium is collected for policy years 6–10
- **When** the commission run executes
- **Then** no payable commission is generated (0%), while the premium is still posted to the policy.

**AC-04.4** _(Rule: BR-19)_
- **Given** a premium is due in policy year 5 but paid in policy year 6
- **When** the commission run executes
- **Then** commission uses the year-5 rate; no commission is generated for premiums not yet collected.

**AC-04.5** _(Rule: BR-20)_
- **Given** a policy is cancelled within the 15-day free-look period
- **When** the cancellation is processed
- **Then** the premium is refunded and 100% of commission paid is clawed back from the agent.

---

**Out of scope:** claims processing, underwriting medical requirements, policy loans, reinstatement processing (except its effect on commission year).
