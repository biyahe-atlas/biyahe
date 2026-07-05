# BIYAHE - Business Rules

**Version:** 1.0  
**Status:** Draft

---

# Purpose

This document defines all business rules used by Biyahe.

Business Rules determine how the application behaves and how financial calculations are performed.

These rules are based on real operational practices of Filipino ride-hailing drivers and fleet operators.

---

# SECTION A - General Rules

## BR-001

Working Capital is NOT income.

It is temporary business capital used to start operations.

Examples:

- Fuel
- Meals
- Change Fund
- Emergency Cash

---

## BR-002

Grab Net Earnings is the primary source of business income.

Per-trip recording is optional and NOT required for MVP.

---

## BR-003

Every peso entered into the system must have a transaction category.

No uncategorized transactions are allowed.

---

# SECTION B - Working Capital

## BR-004

Working Capital may be added at any time.

Although most drivers receive it every Monday, additional capital may be added during the week.

Example:

Monday

₱1,000

Wednesday

₱500

---

## BR-005

Recovered Working Capital is not considered business profit.

---

# SECTION C - Operating Expenses

## BR-006

Operating Expenses reduce Business Profit.

Examples:

- Fuel
- Meals
- Parking
- Toll
- Car Wash

---

## BR-007

Operating Expenses belong to the business.

They must never be classified as Personal Expenses.

---

# SECTION D - Personal Expenses

## BR-008

Personal Expenses do NOT reduce Business Profit.

Examples:

- Grocery
- Family Allowance
- Shopping
- Personal Cash Withdrawal

These are tracked only for cash reconciliation.

---

# SECTION E - Rental Rules

## BR-009

Rental Policy is configurable.

Each operator may define:

- Daily Rental
- Weekly Settlement
- Sunday Free
- Legal Holiday Free

---

## BR-010

Daily Rental contributes to Weekly Rental Target.

Example

Daily Rental

₱1,350

6 Rental Days

Weekly Rental

₱8,100

---

## BR-011

If Sunday is configured as FREE,

Sunday Rental = ₱0

---

## BR-012

If Legal Holiday is configured as FREE,

Rental for that day = ₱0

Weekly Rental Target is automatically adjusted.

---

## BR-013

Weekly Settlement Day is configurable.

Examples:

Saturday

Sunday

Monday

---

# SECTION F - Rental Deductions

## BR-014

Operator-approved vehicle expenses reduce Rental Due.

Examples:

- Tire Patch
- Wiper Blades
- Bulbs
- Minor Repairs
- Emergency Repairs

---

## BR-015

Rental Deductions do NOT reduce Business Profit.

They reduce only the amount payable to the operator.

---

## BR-016

Every Rental Deduction must include:

- Description
- Amount
- Date
- Operator Approval Status

---

# SECTION G - Cash Management

## BR-017

Cash may exist in multiple locations.

Examples:

- Cash on Hand
- Grab Wallet
- GCash

---

## BR-018

Cash Position equals:

Cash on Hand

+

Grab Wallet

+

GCash

---

## BR-019

Cash Position should reconcile with all recorded transactions.

---

# SECTION H - Weekly Closing

## BR-020

Weekly Closing is the primary financial process.

Daily recording supports Weekly Closing.

---

## BR-021

Weekly Closing calculates:

- Total Earnings
- Total Operating Expenses
- Business Profit
- Rental Due
- Rental Deductions
- Personal Expenses
- Cash Position
- Available Take Home

---

## BR-022

Weekly Closing should require less than five minutes.

---

# SECTION I - Dashboard

## BR-023

Dashboard always displays current week's financial status.

---

## BR-024

Dashboard displays:

- Week Earnings
- Business Profit
- Rental Progress
- Remaining Rental
- Cash Position
- Take Home Estimate

---

## BR-025

Business Health uses three statuses.

🟢 On Track

Rental is on schedule.

🟡 Catch Up

Rental is behind but recoverable.

🔴 At Risk

Rental is significantly behind.

---

# SECTION J - Driver Experience

## BR-026

Daily Closing should take less than one minute.

---

## BR-027

The application should minimize manual calculations.

---

## BR-028

Drivers should never need Excel to determine weekly earnings.

---

## BR-029

Every major calculation should be automatic.

---

## BR-030

Every feature must solve a real driver problem.

If a feature does not improve the driver's weekly business management, it should not be included in the MVP.

---

# Future Rules

The following will be added in later versions:

- Fleet Management
- Multiple Vehicles
- Driver-Owner Loan Tracking
- Maintenance Scheduling
- Operator Dashboard
- AI Financial Insights
- SaaS Billing
- Multi-Currency Support

---

# Decision Log

| Date | Decision | Reason |
|------|----------|--------|
| 2026-07-05 | Weekly Closing is the primary workflow | Based on founder's routine |
| 2026-07-05 | No per-trip recording in MVP | Grab already provides reliable daily totals |
| 2026-07-05 | Rental deductions reduce rental due | Matches real operator practices |
| 2026-07-05 | Working Capital can be added anytime | Reflects real operating scenarios |
| 2026-07-05 | Dashboard focuses on weekly performance | Weekly settlement is the driver's priority |
