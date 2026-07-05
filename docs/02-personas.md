# BIYAHE - User Personas

**Version:** 1.0  
**Status:** Draft

---

# Purpose

This document defines the primary users of Biyahe.

Every feature, screen, and workflow must solve a real problem experienced by at least one of these personas.

---

# Persona 1 - The Part-Time Driver (Primary Persona)

## Profile

Jason works full-time during the day and drives during his free time to earn additional income for his family.

He treats Grab driving as a small business rather than simply earning extra cash.

## Goals

- Earn additional family income
- Stay on track with weekly rental
- Avoid suspension due to unpaid rental
- Know the actual weekly take-home income
- Monitor business performance

## Current Process

- Wife provides working capital every Monday.
- Drives after office hours.
- Records daily Grab net earnings.
- Records daily fuel and expenses.
- Monitors rental progress mentally.
- Every Sunday reviews everything in Excel with his wife.

## Pain Points

- Manual calculations
- Difficult weekly reconciliation
- Unsure where missing money went
- Hard to determine actual profit
- Time-consuming weekly review

## Success

"I want to know my real earnings without opening Excel."

---

# Persona 2 - Full-Time Driver

## Profile

A driver whose primary source of income comes from ride-hailing.

Drives 8-14 hours every day.

## Goals

- Reach daily earning targets
- Complete weekly rental
- Maximize take-home income
- Control fuel expenses

## Pain Points

- Cash flow uncertainty
- Poor daily earnings
- Unexpected vehicle expenses
- Difficulty monitoring rental progress

## Success

"I want to know if I'm still on track this week."

---

# Persona 3 - Fleet Operator

## Profile

Owns one or more vehicles and assigns them to drivers under a rental arrangement.

## Goals

- Monitor rental collections
- Track driver balances
- View vehicle profitability
- Monitor maintenance expenses

## Pain Points

- Manual rental monitoring
- Drivers forgetting deductions
- Inconsistent records
- Difficult weekly reconciliation

## Success

"I want to know which drivers are behind on rental."

---

# Persona 4 - Driver's Spouse / Family Auditor

## Profile

Helps manage the family's finances and verifies the driver's weekly income.

Often responsible for budgeting and savings.

## Goals

- Verify weekly earnings
- Ensure rental is complete
- Understand household income
- Monitor family cash flow

## Pain Points

- Manual Excel checking
- Missing transactions
- Confusing calculations
- Difficult reconciliation

## Success

"I want to trust the weekly report without recalculating everything."

---

# Persona 5 - Driver-Owner (Future Version)

## Profile

Owns the vehicle personally and pays a monthly bank amortization instead of daily rental.

## Goals

- Monitor vehicle profitability
- Track loan payments
- Manage maintenance costs
- Grow income

## Pain Points

- No clear vehicle financial records
- Unexpected repair costs
- Difficulty tracking long-term profitability

## Success

"I want to know if my vehicle is making money."

---

# Persona Relationships

Driver
│
├── Drives Vehicle
│
├── Pays Operator
│
├── Records Daily Business
│
└── Shares Weekly Report
     │
     └── Family

Operator
│
└── Manages Multiple Drivers

Driver-Owner
│
└── Manages Own Vehicle

---

# MVP Focus

Version 1 focuses on:

✅ Part-Time Driver

✅ Full-Time Driver

✅ Driver's Spouse

Fleet Operators and Driver-Owners will be expanded in later releases.

---

# Product Design Principles

Every feature must satisfy at least one of these questions:

### Driver

"Am I still making money?"

### Family

"How much can we safely use this week?"

### Operator

"Is the rental complete?"

### Driver-Owner

"Is my vehicle profitable?"

If a feature does not answer one of these questions, it should not be included in the MVP.

---

# Decision Log

| Date | Decision | Reason |
|------|----------|--------|
| 2026-07-05 | Primary persona is the Part-Time Driver | Based on the founder's real experience |
| 2026-07-05 | Family member included as a persona | Weekly financial review is part of the workflow |
| 2026-07-05 | Fleet Operator deferred to later versions | Keep MVP focused |
| 2026-07-05 | Driver-Owner added for future expansion | Supports long-term product vision |

---

# Persona 6 - New Driver (First 90 Days)

## Profile

A newly registered ride-hailing driver who is still learning how the business works.

Most new drivers focus only on daily earnings and often underestimate operating expenses, rental obligations, and working capital requirements.

They usually have no financial monitoring system and rely on memory or handwritten notes.

## Goals

- Understand if driving is profitable
- Learn proper financial discipline
- Build confidence during the first few months
- Avoid falling behind on rental
- Learn how to separate business money from personal money

## Current Process

- Checks only the Grab daily earnings.
- Estimates fuel expenses mentally.
- Spends available cash without tracking.
- Doesn't know the real weekly take-home income.
- Has no structured weekly review.

## Pain Points

- Doesn't know how much capital is needed to start each week.
- Doesn't understand where the money goes.
- Gets surprised during weekly settlement.
- Confuses revenue with profit.
- Doesn't know if the business is sustainable.

## Success

"I want to know if I'm really earning money and how to manage my driving business properly."

---

# Product Opportunities

To support new drivers, Biyahe can provide guided onboarding and educational insights.

Examples:

### Recommended Starting Capital

Based on previous driving history, Biyahe can suggest:

- Fuel Budget
- Meal Budget
- Emergency Cash
- Change Fund

---

### Weekly Business Health

Instead of only showing numbers, Biyahe explains what they mean.

Example:

🟢 Excellent

Your rental is fully covered and your business is profitable this week.

---

🟡 Attention

Your rental is covered, but your operating expenses are higher than normal.

---

🔴 Action Needed

You are behind on your rental target and should monitor your expenses closely.

---

### Financial Tips (Future Feature)

Examples:

- Separate business money from personal money.
- Recover working capital before spending profits.
- Complete your rental obligation before taking your weekly earnings.
- Set aside money for future maintenance.
- Monitor fuel as your largest operating expense.

These tips help drivers develop healthy financial habits from their first week on the road.

---

# Why This Persona Matters

Many drivers leave ride-hailing because they believe they are not earning enough.

In many cases, the real issue is not income—it is the lack of financial visibility and planning.

By teaching drivers how to manage their business from the beginning, Biyahe can become more than a tracking app.

It becomes a financial companion that helps drivers build a sustainable driving business.

---

# Decision Log

| Date | Decision | Reason |
|------|----------|--------|
| 2026-07-05 | Added "New Driver" persona | Opportunity to teach good financial habits and increase long-term user retention |
