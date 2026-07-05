# BIYAHE - Database Design

**Version:** 1.0
**Status:** Draft

---

# Purpose

This document defines the core data model for Biyahe.

The database is designed around the business operations of ride-hailing drivers rather than application screens.

This allows the platform to support future features without major database redesign.

---

# Database Overview

Version 1.0 consists of the following core entities:

1. Users
2. Vehicles
3. Operators
4. Driver Settings
5. Weekly Cycles
6. Daily Closings
7. Transactions
8. Expense Categories
9. Rental Deductions

---

# Entity Relationship

User

↓

Vehicle

↓

Weekly Cycle

↓

Daily Closing

↓

Transactions

↓

Dashboard

---

# Table: Users

Stores driver account information.

Fields

- id
- full_name
- email
- mobile_number
- profile_photo
- created_at
- updated_at

---

# Table: Operators

Stores fleet operator information.

Fields

- id
- operator_name
- contact_person
- mobile_number
- remarks

---

# Table: Vehicles

Stores vehicle information.

Fields

- id
- user_id
- operator_id
- plate_number
- vehicle_model
- vehicle_type
- ownership_type
- created_at

Ownership Type

- Rental
- Owned
- Bank Loan

---

# Table: Driver Settings

Stores configurable business rules.

Fields

- id
- user_id
- daily_rental
- weekly_settlement_day
- sunday_free
- legal_holiday_free
- currency

---

# Table: Weekly Cycles

Represents one operating week.

Fields

- id
- user_id
- week_start
- week_end
- rental_target
- rental_paid
- business_profit
- cash_position
- status

Status

- Active
- Closed

---

# Table: Daily Closings

One record per driving day.

Fields

- id
- weekly_cycle_id
- closing_date
- grab_net_earnings
- cash_on_hand
- grab_wallet
- gcash
- notes

---

# Table: Transactions

Every money movement is stored here.

Fields

- id
- daily_closing_id
- transaction_type
- category
- amount
- remarks
- created_at

Transaction Types

- Income
- Working Capital
- Operating Expense
- Personal Expense
- Rental Payment
- Rental Deduction

---

# Table: Expense Categories

System categories.

Examples

Operating

- Fuel
- Meals
- Parking
- Toll
- Car Wash

Personal

- Grocery
- Family
- Shopping

Rental Deduction

- Tire Patch
- Wiper Blades
- Bulbs
- Minor Repair

---

# Table: Rental Deductions

Stores operator-approved deductions.

Fields

- id
- daily_closing_id
- description
- amount
- approved
- approved_by

---

# Dashboard Calculations

Dashboard values are generated automatically from:

- Weekly Cycle
- Daily Closings
- Transactions
- Rental Deductions

No dashboard values are entered manually.

---

# Future Tables

The following tables will be added in future versions:

- Fleet Drivers
- Fleet Vehicles
- Maintenance
- Loan Payments
- Notifications
- Subscription
- Audit Logs
- Cloud Backup
- Reports

---

# Database Design Principles

## Single Source of Truth

Every financial value must originate from a recorded transaction.

---

## No Duplicate Data

The same information should never be stored twice.

---

## Automatic Calculations

Dashboard values should always be computed from transactions.

---

## Configurable

Operator policies must be configurable instead of hardcoded.

---

## Scalable

The design must support:

- Individual Drivers
- Fleet Operators
- Multiple Vehicles
- SaaS Platform

without redesigning the database.

---

# Decision Log

| Date | Decision | Reason |
|------|----------|--------|
| 2026-07-05 | Weekly Cycle introduced | Weekly settlement is the core workflow |
| 2026-07-05 | Transactions table stores all money movements | Single source of truth |
| 2026-07-05 | Rental Deductions stored separately | Different business behavior from expenses |
| 2026-07-05 | Driver Settings stores business rules | Configurable operator policies |
