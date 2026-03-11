## PONATECH (HMS)

## Complete Feature Documentation

A modern, web-based Hospital Management System designed for small to mid-size healthcare facilities. Built with enterprise-grade features, real-time workflows, and seamless integrations to digitize every aspect of hospital operations — from patient registration to payroll.

---

## Table of Contents

1. [Patient Management](#1-patient-management)
2. [Visit Workflow & Queue Management](#2-visit-workflow--queue-management)
3. [Clinical Modules](#3-clinical-modules)
4. [Laboratory Management](#4-laboratory-management)
5. [Pharmacy & Dispensing](#5-pharmacy--dispensing)
6. [Dental Module](#6-dental-module)
7. [Ultrasound Module](#7-ultrasound-module)
8. [Billing & Payments](#8-billing--payments)
9. [Insurance Claims](#9-insurance-claims)
10. [Accounting & Financial Management](#10-accounting--financial-management)
11. [Human Resources & Payroll](#11-human-resources--payroll)
12. [Attendance & Shift Management](#12-attendance--shift-management)
13. [Reports & Analytics](#13-reports--analytics)
14. [Settings & Configuration](#14-settings--configuration)
15. [Security & Access Control](#15-security--access-control)
16. [Printing & Documents](#16-printing--documents)
17. [Integrations](#17-integrations)
18. [Technical Overview](#18-technical-overview)

---

## 1. Patient Management

### Patient Registration
- **Multi-step registration form** with 5 organized tabs: Personal Info, Contact & Address, Emergency Contact, Insurance, and Medical Information
- Capture comprehensive demographics: name, gender, date of birth, ID/passport number, marital status, occupation, nationality
- Contact details including phone, email, physical address, and county
- Emergency contact and next of kin recording
- Insurance details: provider, member number, member name, expiry date
- Medical history: blood type, known allergies, chronic conditions, disabilities, clinical notes

### Patient Search & Directory
- Global search accessible from any page (Ctrl+K / Cmd+K)
- Search by patient name, phone number, or patient ID
- Paginated patient list with sorting
- Quick-access patient cards with key information at a glance

### Patient Detail & History
- Complete patient profile with all demographics and medical information
- **Expandable visit history** showing full clinical details per visit:
  - Triage vitals (BP, temperature, heart rate, respiratory rate, SpO2, weight, height)
  - Consultation notes (symptoms, diagnosis, treatment plan, follow-up)
  - Lab orders with test results
  - Prescriptions with medication details
- Direct navigation to full visit records
- Custom fields support for facility-specific data capture

### Patient Card Printing
- Print-ready patient identification cards
- Includes patient photo placeholder, demographics, insurance info, allergies banner, emergency contact
- Hospital-branded with logo and contact details

---

## 2. Visit Workflow & Queue Management

### Visit Creation & Tracking
- Create visits with type selection: Consultation, Dental, Lab Only, Pharmacy Only
- Automatic visit number generation
- Optional consultation fee assignment at visit creation
- Direct lab test selection for Lab Only visits

### Multi-Stage Workflow
Every visit progresses through defined stages:

**REGISTRATION → BILLING → TRIAGE → DOCTOR → LAB → PHARMACY → COMPLETED**

- Visual stage progress bar with color-coded icons
- One-click stage advancement
- Ability to re-add patients to current stage queue
- Manual completion option for any active visit

### Real-Time Queue Management
- **6 queue stations**: Triage, Doctor, Dentist, Lab, Pharmacy, Billing
- Live patient count per station
- Priority-based queue ordering
- Call, serve, and complete actions per queue entry
- Desktop notification alerts when new patients arrive
- Auto-refresh for real-time updates
- Role-specific queue views (each role sees their relevant station)

---

## 3. Clinical Modules

### Triage
- Record vital signs:
  - Blood Pressure (mmHg)
  - Temperature (°C)
  - Heart Rate (bpm)
  - Respiratory Rate (/min)
  - Oxygen Saturation (%)
  - Weight (kg) and Height (cm) with automatic BMI calculation
- Chief complaint documentation
- Priority assessment (Normal, Urgent, Emergency)
- Custom fields for facility-specific triage data
- **"My History" tab** — clinicians can review their own triage records

### Doctor Consultation
Comprehensive clinical documentation:
- **Chief Complaint** — presenting symptoms
- **History of Presenting Illness** — detailed symptom history
- **Review of Systems** — systematic body system review
- **Past Medical & Medication History**
- **Family & Social History**
- **General Examination** — overall clinical findings
- **Systematic Examination** — focused system examination
- **Diagnosis** — clinical diagnosis recording
- **Treatment Plan / Clinical Notes** — management plan
- **Follow-Up Date** — return appointment scheduling
- **Sick-Off Certificate** — generate medical leave certificates with days, dates, reason, and employer details
- Custom fields for specialty-specific documentation
- **"My History" tab** — doctors can review their consultation history

---

## 4. Laboratory Management

### Lab Test Configuration
- Define lab tests with: name, code, category, price, turnaround time
- Organize tests by category for easy ordering
- Price management per test

### Lab Order Workflow
- Order lab tests directly from consultations or as standalone Lab Only visits
- Multi-test ordering in a single order
- Status tracking: PENDING → IN_PROGRESS → COMPLETED
- Result entry with notes per test item
- Performer/technician assignment
- Turnaround time monitoring

### Lab Inventory
- Track lab consumables and reagents
- Stock level monitoring with minimum stock alerts
- Stock adjustment with reason logging (Received, Used, Damaged, Expired, Correction)
- Inventory audit trail

### Lab Results Printing
- Professional lab results report with hospital branding
- Patient details, test results, reference ranges
- Technician and approval signatures

---

## 5. Pharmacy & Dispensing

### Medication Management
- Medication registry: name, generic name, code, category, dosage form
- Dual pricing: selling price and insurance price
- Stock tracking with minimum and maximum levels
- Stock adjustment with reason logging
- Reorder level alerts

### Prescription Workflow
- Create prescriptions linked to patient consultations
- Per-item details: medication, dosage, frequency, duration, quantity, instructions
- Dispensing workflow with stock deduction
- Partial and full dispensing support
- Status tracking: PENDING → DISPENSED

### Prescription Printing
- Print-ready prescription documents
- Patient details, medication list, dosage instructions
- Doctor signature line

---

## 6. Dental Module

*Feature-flagged — can be enabled/disabled per facility*

### Dental Services
- Configure dental procedures with: name, code, category, price, duration
- Organize by service category

### Dental Examination
- Dental-specific consultation workflow
- **Dental chart** with FDI notation (teeth 11-48)
- Clinical findings documentation
- Procedure tracking with quantity and cost
- Dental examination report printing with tooth chart

---

## 7. Ultrasound Module

*Feature-flagged — can be enabled/disabled per facility*

### Scan Configuration
- Define ultrasound scan types: name, code, category, price
- Category-based organization

### Ultrasound Workflow
- Order scans from consultations or directly
- Record findings and clinical impressions
- Performer assignment and status tracking
- **"My History" tab** for sonographers
- Professional ultrasound report printing

---

## 8. Billing & Payments

### Bill Management
- Automatic bill generation from visit services
- Itemized billing: description, category, quantity, unit price, total
- Support for adding/removing bill items
- Cash and insurance price differentiation with configurable markups
- Discount support (percentage or fixed amount)

### Payment Processing
- **Multiple payment methods**:
  - **Cash** — direct cash payments
  - **M-PESA** — mobile money via STK push (see Integrations)
  - **Insurance** — linked to insurance claims
  - **Bank Transfer** — bank payment recording
- Partial payment support with running balance
- Payment status tracking: PENDING → PARTIAL → PAID
- Payment reference and receipt number tracking

### Receipt & Invoice Printing
- **Receipts** — compact payment confirmation with hospital branding
- **Invoices** — detailed itemized invoices for insurance or corporate billing
- Customizable receipt footer message
- Currency formatting (KES default, configurable)

---

## 9. Insurance Claims

*Feature-flagged — can be enabled/disabled per facility*

- Create claims linked to patient bills
- Claim number generation and tracking
- Status workflow: PENDING → SUBMITTED → APPROVED → PAID (or REJECTED)
- Approval amount recording
- Rejection reason documentation
- Claim-to-payment reconciliation

---

## 10. Accounting & Financial Management

*Feature-flagged — can be enabled/disabled per facility*

The accounting module is a full double-entry bookkeeping system with 7 integrated tabs: Dashboard, Chart of Accounts, Journal Entries, Invoices, Vendor Bills, Bank Accounts, and Reports.

### Chart of Accounts
- **Double-entry accounting** with a complete chart of accounts
- Account types: Asset, Liability, Equity, Revenue, Expense
- Sub-type categorization (e.g., Current Asset, Fixed Asset, Administrative Expense, Cost of Sales, etc.)
- Hierarchical parent-child account structure
- Unique account codes and running balances
- System accounts (protected from deletion)
- **Seed default accounts** — one-click setup with standard hospital chart of accounts
- Search and filter by account type
- **CSV export** of the full chart of accounts
- Active/inactive toggle per account

### Journal Entries
- Create multi-line journal entries with automatic debit-credit balancing
- Minimum 2 lines required; real-time balance validation
- Sequential entry numbering (JE-0001, JE-0002, etc.)
- **Status workflow**: DRAFT → POSTED → VOID
- Posting updates linked account balances
- Void posted entries with automatic reversal
- Reference and notes fields for supporting documentation
- Filter by status and date range; search by description or entry number
- **CSV export** with account codes
- Full audit logging on all operations

### Invoices (Accounts Receivable)
- Create customer invoices with line items (quantity, unit price, tax rate)
- Automatic subtotal, tax, and total calculations
- Sequential numbering (INV-0001, INV-0002, etc.)
- **Status workflow**: DRAFT → SENT → PARTIALLY_PAID → PAID (or OVERDUE / VOID)
- **Record partial and full payments** with method tracking (Cash, M-PESA, Bank Transfer, Cheque, Card)
- **Send invoices** to customers via email
- Due date and payment terms (e.g., Net 30)
- Outstanding balance tracking per invoice
- Payment history within invoice detail view
- Filter by status and date range
- **CSV export**
- Linked to Chart of Accounts for revenue recognition

### Vendor Bills (Accounts Payable)
- Create bills from vendors with line items (quantity, unit price, tax rate)
- Sequential numbering (BILL-0001, BILL-0002, etc.)
- **Status workflow**: DRAFT → RECEIVED → PARTIALLY_PAID → PAID (or OVERDUE / VOID)
- Mark bills as received before payment
- **Record partial and full payments** (Cash, M-PESA, Bank Transfer, Cheque)
- Outstanding balance tracking per bill
- Payment history within bill detail view
- Filter by status and date range
- **CSV export**
- Linked to Chart of Accounts for expense tracking

### Bank Accounts & Reconciliation
- Create and manage multiple bank accounts
- Account types: Checking, Savings, Mobile Money
- Multi-currency support (default: KES)
- Track opening balance and current balance
- **Record transactions**: Deposit, Withdrawal, Transfer, Fee, Interest
- Running balance calculation per transaction
- **Bank reconciliation workflow**:
  1. Enter bank statement balance and date
  2. Review unreconciled transactions
  3. Select cleared transactions
  4. System calculates difference between book and statement balance
  5. Mark transactions as reconciled
- Recent transactions display per account
- Transaction flow summary (deposits, withdrawals, interest)

### Accounting Dashboard
- **Key Performance Indicators**:
  - Receivables: Outstanding invoices + unpaid hospital bills, overdue count and amount
  - Payables: Outstanding vendor bills, overdue count and amount
  - Monthly Income: Patient payments + invoice payments, grouped by payment method
  - Monthly Expenses: Operating expenses + payroll costs
  - Net Profit: Income − Expenses − Tax − Discounts (color-coded green/red)
- **Charts & Visualizations**:
  - Income vs Expenses Trend (6-month bar chart)
  - Expense Breakdown by category (pie chart, includes payroll)
  - Income by Payment Method (pie chart)
  - Profit Trend (6-month area chart)
- **Bank Accounts Summary**: Total balance across all accounts with per-account breakdown
- **Recent Transactions Table**: Date, account, description, type, amount (color-coded)
- Selectable month and year for period-based analysis

### Financial Reports

#### Profit & Loss Statement
- Revenue breakdown by payment method (Cash, M-PESA, Insurance, Bank Transfer)
- Less: Discounts
- Operating expenses grouped by category
- Payroll costs (salaries + allowances)
- Tax breakdown: Corporate Tax, VAT on Expenses, PAYE (payroll tax)
- Net income calculation with color coding
- Customizable date range (month/year selector)
- **Printable report** with hospital branding
- **PDF export**

#### Balance Sheet
- **Assets**: Current Assets (Cash & Bank, Accounts Receivable, Inventory), Fixed Assets (Equipment & Machinery)
- **Liabilities**: Current Liabilities (Accounts Payable, Accrued Payroll, Tax Payable), Long-term Liabilities (Loans)
- **Equity**: Retained Earnings (calculated from all-time P&L)
- Balance sheet equation verification: Assets = Liabilities + Equity
- As-of date selector
- **Printable report** with hospital branding
- **PDF export**

#### Cash Flow Statement
- **Operating Activities**: Net income, depreciation adjustments, changes in receivables/payables, vendor payments
- **Investing Activities**: Equipment purchases
- **Financing Activities**: Loan deposits, owner draws
- Net change in cash, beginning and ending cash balances
- Customizable date range
- **Printable report** with hospital branding
- **PDF export**

### Expense Management
- Record expenses with: description, amount, vendor, date, category
- Expense numbering and tracking
- Tax amount recording per expense
- **Approval workflow**: PENDING → APPROVED/REJECTED → PAID
- Approver name and date tracking
- Expense category management

### Fiscal Years
- Define fiscal year periods with start and end dates
- Status: OPEN or CLOSED
- Organize accounting data by fiscal period

### Tax Configuration
- Define multiple tax types: PAYROLL, REVENUE, EXPENSE
- Configurable tax rates and names (e.g., VAT, PAYE, NHIF, NSSF)
- Enable/disable individual tax rules
- Applied automatically in payroll, invoices, and reporting

---

## 11. Human Resources & Payroll

### Staff Management
- User creation with role assignment
- **10 system roles**: Admin, Registration, Billing, Triage, Doctor, Dentist, Lab, Pharmacy, Ultrasound, HR
- Active/inactive staff status management
- Staff profile with contact details, email, phone
- **Salary configuration** per staff member (basic salary)

### Payroll Processing
- **Monthly payroll generation** for all salaried staff
- Automatic calculation:
  - Basic Salary
  - Allowances
  - Deductions
  - Tax (based on configured tax rules)
  - Net Pay
- Payroll status workflow: DRAFT → APPROVED → PAID
- Individual payslip generation
- **Bulk payslip email delivery** — send all payslips in one click
- HR and Admin approval controls

### Payslip
- **Print payslip**: Professional layout with earnings/deductions breakdown, net pay summary, signature lines
- **Email payslip**: Branded HTML email with structured earnings, deductions, net pay box, and calculation summary

---

## 12. Attendance & Shift Management

*Feature-flagged — can be enabled/disabled per facility*

### Clock In/Out
- One-click clock in and clock out
- Automatic timestamp recording
- Shift assignment per attendance record
- Real-time attendance status display

### Shift Management
- Define work shifts: name, start time, end time
- Grace period configuration per shift
- Shift assignment during clock-in

### Attendance Reporting
- **Daily summary**: Present, Late, Absent, On Overtime counts
- Staff-level attendance records
- Monthly attendance history
- Date range filtering
- **CSV export** for payroll integration or external reporting
- Admin view across all staff; individual view for personal records

---

## 13. Reports & Analytics

### Dashboard Analytics
- Patient count statistics
- Visit volume trends
- Revenue summaries
- Queue performance metrics
- Chart visualizations (line, bar, pie)

### Financial Reports
- Revenue by payment method
- Revenue by service category
- Expense reports by category
- Profit & Loss statements (printable, PDF export)
- Balance Sheet reports (printable, PDF export)
- Cash Flow statements (printable, PDF export)
- Payroll cost analysis

### Operational Reports
- Visit volume by type and period
- Lab turnaround times
- Queue wait times
- Attendance summaries

---

## 14. Settings & Configuration

### Hospital Profile
- Hospital name, tagline, address, city, county, country
- Phone numbers (primary and secondary), email, website
- **Logo upload** — displayed across all printed documents and emails
- Receipt footer customization

### Currency & Pricing
- Currency and symbol configuration (default: KES / KSh)
- Cash markup percentage
- Insurance markup percentage

### Service Configuration
- **Consultation Fees** — define fee types with names and prices
- **Lab Tests** — manage test catalog with codes, categories, prices
- **Medications** — manage drug formulary
- **Dental Services** — configure dental procedure catalog
- **Ultrasound Scans** — configure scan type catalog

### Custom Fields
- **Dynamic form fields** for any module (Patient, Triage, Consultation)
- Field types: Text, Textarea, Number, Date, Select/Dropdown, Checkbox
- Organize fields by section with sort ordering
- Mark fields as required or optional
- Custom fields appear in forms, detail views, and printed documents

### Feature Flags
Toggle entire modules on or off per facility:
- Dental, Ultrasound, Laboratory, Pharmacy
- Insurance Claims, Attendance, Accounting
- M-PESA Payments, SMS Notifications, Sick Leave Certificates

### M-PESA Configuration
- **OTP-protected access** — admin must verify via email OTP before viewing or editing M-PESA credentials
- Environment selection (Sandbox / Production)
- Consumer Key and Secret
- Business Shortcode and Passkey
- Callback URL configuration
- Secrets stripped from API responses; only returned after OTP verification
- All credentials stored securely in the database

---

## 15. Security & Access Control

### Authentication
- Email and password login
- **Two-Factor Authentication (2FA)** via OTP:
  - Email OTP delivery
  - SMS OTP delivery
  - 10-minute code expiry
- Password reset via secure email link
- Session management with JWT tokens

### Role-Based Access Control (RBAC)
10 predefined roles with granular page and API access:

| Role | Access |
|------|--------|
| **Admin** | Full system access — all modules, settings, user management |
| **Registration** | Patient registration, visits, queue, attendance |
| **Billing** | Billing, payments, patient lookup, queue |
| **Triage** | Triage assessment, patient lookup, queue |
| **Doctor** | Consultations, lab orders, ultrasound, patient lookup |
| **Dentist** | Dental module, patient lookup, queue |
| **Lab** | Laboratory management, patient lookup, queue |
| **Pharmacy** | Prescription dispensing, patient lookup, queue |
| **Ultrasound** | Ultrasound scanning, patient lookup, queue |
| **HR** | Staff management, payroll, accounting, attendance, reports, settings |

### Admin Impersonation
- Admins can impersonate any staff user for testing or support
- Visual indicator when in impersonation mode
- One-click return to admin account

### Audit Logging
- Track all significant actions: creates, updates, deletes
- Record: action type, entity, user, timestamp, IP address
- Metadata capture for compliance and accountability

---

## 16. Printing & Documents

All documents feature hospital branding (logo, name, address, contact) and are optimized for standard paper sizes.

| Document | Description |
|----------|-------------|
| **Patient Card** | ID-card-sized patient identification with demographics, insurance, allergies |
| **Receipt** | Payment receipt with itemized services and payment details |
| **Invoice** | Detailed billing invoice for insurance or corporate clients |
| **Prescription** | Patient prescription with medication, dosage, and instructions |
| **Lab Results** | Laboratory test results report with reference ranges |
| **Ultrasound Report** | Ultrasound findings and clinical impressions |
| **Doctor Notes** | Complete consultation notes with vitals, examination, diagnosis |
| **Dental Examination** | Dental report with FDI tooth chart and procedure list |
| **Sick-Off Certificate** | Medical leave certificate with dates, reason, and employer details |
| **Payslip** | Employee salary payslip with earnings/deductions breakdown |
| **Profit & Loss** | P&L financial statement for accounting periods |
| **Balance Sheet** | Statement of financial position with assets, liabilities, and equity |
| **Cash Flow Statement** | Cash flow report with operating, investing, and financing activities |

---

## 17. Integrations

### M-PESA Mobile Money
- **STK Push** — initiate payments directly from the billing screen
- Patients receive a payment prompt on their phone
- Automatic payment confirmation via callback
- Transaction status polling for real-time updates
- Support for Sandbox and Production environments
- Configurable credentials via Settings (no code changes needed)

### SMS Notifications
- OTP delivery for two-factor authentication
- Kenyan phone number normalization (07XX, 254XX formats)
- Configurable SMS API integration
- Hospital name dynamically pulled from settings

### Email Communication
- OTP verification emails with branded templates
- Password reset emails with secure token links
- Payslip distribution to all staff
- Configurable SMTP (Gmail, custom mail servers)
- Hospital branding in all email templates (name pulled from settings)

---

## 18. Technical Overview

### Key Technical Features
- **Real-time updates** via React Query polling
- **Responsive design** — works on desktop, tablet, and mobile
- **Print optimization** — all documents use print-specific CSS
- **Modular architecture** — feature flags allow enabling/disabling entire modules
- **Custom fields** — extend any module with facility-specific data without code changes
- **Audit trail** — every significant action is logged for compliance

---

*For detailed feature list and summary, see [FEATURES.md](FEATURES.md).*
