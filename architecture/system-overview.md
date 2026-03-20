
# System Overview

## Introduction
WellPay is a health financing platform that combines savings, insurance, and credit to enable access to healthcare for informal workers.

The platform operates as an orchestration layer connecting users to financial and healthcare service providers.

---

## Core Components

### 1. Mobile App (User Interface)
- Built with Adalo
- Used by customers to:
  - Save money (Health Wallet)
  - Request credit
  - Access insurance
  - Find clinics

---

### 2. Admin Web App
- Used by internal team
- Manages:
  - Loan approvals
  - Insurance plans
  - User activity
  - Clinics and transactions

---

### 3. Backend Database
- Stores:
  - Users
  - Wallet balances
  - Credit records
  - Insurance subscriptions
  - Transactions

Acts as the single source of truth.

---

### 4. Financial Partners

#### a. Lenders (Credit Providers)
- Provide capital for health credit
- WellPay performs:
  - User onboarding
  - Credit scoring
  - Loan request handling
- Lenders fund approved loans

#### b. Insurance Providers (HMOs)
- Underwrite insurance plans
- Manage claims and coverage rules
- WellPay handles:
  - User enrollment
  - Premium collection
  - Plan presentation

---

### 5. Healthcare Providers (Clinics)
- Deliver medical services
- Receive payments via:
  - Insurance
  - Wallet
  - Credit

---

## Key Modules

- Health Wallet (user savings)
- Insurance System
- Health Credit Engine
- Clinic Directory
- Learn & Earn (engagement layer)

---

## Data Flow

User → Mobile App → Platform Database  

Platform → Lenders (for credit funding)  
Platform → HMOs (for insurance coverage)  
Platform → Clinics (for service delivery)

Admin → Web App → Database  

---

## System Interaction

1. User saves money → builds wallet balance  
2. User requests credit → platform evaluates → lender funds  
3. User subscribes to insurance → HMO provides coverage  
4. User visits clinic → payment via wallet, credit, or insurance  

---

## Platform Role

WellPay does NOT directly:

- Underwrite insurance  
- Provide loan capital  

Instead, it acts as:

- Aggregator  
- Orchestrator  
- Access layer for underserved users  

---

## Future Integrations

- Payment gateways (Flutterwave, Paystack)
- Telecom APIs (for credit scoring)
- USSD for feature phone users
- EHR / clinic systems integration
