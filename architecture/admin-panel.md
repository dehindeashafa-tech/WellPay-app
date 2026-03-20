
# Admin Panel Architecture

## Overview
The admin panel is a web-based interface used by the WellPay team to manage platform operations and coordinate with financial and healthcare partners.

WellPay acts as an orchestration layer between users, lenders, insurance providers (HMOs), and clinics.

---

## Access Control

- Only users with Role = Admin can access
- Authentication required
- Role-based permissions (future: Ops, Finance, Support)

---

## Core Functions

### 1. Loan Management (Lender Coordination)

- View all credit requests
- Perform basic eligibility checks
- Approve or reject loan requests (based on platform rules)

#### Flow:
User requests credit →  
Admin reviews →  
Request forwarded/validated →  
Lender funds loan →  
Loan marked as Approved  

- Update loan status:
  - Pending → Approved → Repaid

> Note: Loan capital is provided by external lenders, not WellPay.

---

### 2. Insurance Management (HMO Integration)

- Create and manage insurance plans (defined with HMO partners)
- Enroll users into plans
- Track subscription status

#### Flow:
User selects plan →  
Admin/system confirms eligibility →  
User enrolled →  
HMO provides coverage  

> Note: Insurance risk is underwritten by HMOs.

---

### 3. User Management

- View user profiles
- Monitor:
  - Savings behavior
  - Credit usage
  - Insurance status
- Assign or update user roles (Admin/User)

---

### 4. Transaction Monitoring

- View all wallet transactions:
  - Deposits
  - Payments
  - Credit disbursements
  - Repayments

- Track financial flows across:
  - Users
  - Lenders
  - Clinics

---

### 5. Clinic Management

- Add and manage verified clinics
- Ensure clinics are eligible for:
  - Insurance claims
  - Wallet payments
  - Credit payments

---

### 6. Partner Coordination (Critical Layer)

Admin oversees interactions with:

#### Lenders
- Ensure loan requests are valid
- Track disbursement and repayment

#### HMOs
- Ensure correct user enrollment
- Align plans with coverage rules

#### Clinics
- Maintain provider network
- Ensure service delivery alignment

---

## Workflow Example (End-to-End)

User requests credit →  
Admin validates →  
Lender funds →  
Loan becomes active →  
User receives care →  
User repays →  
System updates records  

---

## Security Measures

- Role-based access control
- Restricted admin visibility
- Controlled financial actions
