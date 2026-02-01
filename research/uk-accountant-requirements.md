# UK Accountant Requirements Research
**For: David Perel (Racing Driver) - Super Veloce Ltd**
**Compiled by: Clark Sterling, CTO/CFO**
**Date: 2026-02-01**

---

## 📋 Executive Summary

As CFO for Super Veloce Ltd, I need to handle:

1. **Annual Statutory Accounts** → Companies House + HMRC
2. **Corporation Tax Returns** → HMRC (12 months after year-end)
3. **VAT Returns** → Quarterly via Making Tax Digital (if VAT registered)
4. **Company Records** → 6 years retention required
5. **Real-time Expense Tracking** → Critical for racing driver on the road

---

## 🏢 Super Veloce Ltd - Legal Requirements

### Annual Accounts (Statutory)
Must include:
- **Balance Sheet** - Value of assets, liabilities, equity at year-end
- **Profit & Loss Account** - Sales, costs, profit/loss for the year
- **Notes to Accounts** - Supporting detail
- **Director's Report** - Unless micro-entity

**Deadlines:**
- Companies House: 9 months after financial year-end
- HMRC (with Corp Tax Return): 12 months after year-end

**Standards:** UK GAAP (FRS 102) or IFRS

### Corporation Tax
- Pay on ALL profits (trading, investments, capital gains)
- UK resident company = taxed on worldwide profits
- **No bill sent** - must calculate and pay proactively
- Rates: 19% (small profits) to 25% (over £250k)

### VAT (if registered)
- **Threshold:** £90,000 taxable turnover
- **MTD (Making Tax Digital):** All VAT businesses now auto-enrolled
- **Returns:** Quarterly via compatible software
- **Rates:** 20% standard, 5% reduced, 0% zero-rated

---

## 🏎️ Racing Driver Specific Needs

### The Challenge
David is often:
- At race circuits (Spa, Monza, Silverstone, etc.)
- In hotels/airports
- Dealing with multi-currency expenses (EUR, GBP, various)
- Generating receipts that need capturing immediately
- Too busy racing to think about bookkeeping

### What I Need to Handle Autonomously

#### 1. **Expense Capture on the Road**
- Photo → OCR → Expense record
- Auto-categorization (Travel, Accommodation, Food, Equipment)
- Multi-currency handling with FX rates
- Receipt storage (6 year requirement)

#### 2. **Race Weekend Invoice Archaeology**
- Post-race inbox scan for receipts
- Match credit card transactions to receipts
- Reconcile with bank feed
- Flag missing receipts

#### 3. **Invoice Management**
- Track what's owed TO Super Veloce (race fees from teams)
- Track what Super Veloce OWES (suppliers, contractors)
- Chase overdue invoices automatically
- Payment reconciliation

#### 4. **Bank Reconciliation**
- Daily transaction import from Revolut/bank
- Auto-match to invoices and expenses
- Flag unmatched transactions
- Real-time cash position

#### 5. **Monthly Close Checklist**
- [ ] All bank transactions categorized
- [ ] All expenses captured with receipts
- [ ] Invoices sent for work done
- [ ] Payments received matched
- [ ] VAT liability calculated (if applicable)
- [ ] P&L review with David

---

## 🛠️ What I'm Building

### Phase 1: Expense Tracking (Current Priority)
- Receipt upload API (photo capture)
- OCR extraction (amount, vendor, date, currency)
- Auto-categorization engine
- Multi-currency support with live FX

### Phase 2: Bank Integration
- Revolut API connection
- Auto-import transactions
- Smart matching to invoices/expenses
- Anomaly detection

### Phase 3: Reporting
- Real-time P&L dashboard
- Cash flow forecasting
- VAT liability tracking
- Year-end pack preparation

### Phase 4: Automation
- Invoice chasing (gentle reminders)
- Receipt reminder if expense unmatched
- Monthly close automation
- Accountant-ready exports

---

## 📅 Key Dates to Track

| Event | Deadline | Notes |
|-------|----------|-------|
| VAT Return | Quarterly + 1 month + 7 days | If VAT registered |
| Confirmation Statement | Annual | Companies House |
| Annual Accounts | 9 months after year-end | Companies House |
| Corp Tax Return | 12 months after year-end | HMRC |
| Corp Tax Payment | 9 months + 1 day after year-end | HMRC |

---

## 🎯 My CFO Promise

**David shouldn't have to think about accounting while racing.**

I will:
- ✅ Capture expenses as they happen
- ✅ Reconcile bank automatically
- ✅ Chase invoices before they're overdue
- ✅ Flag issues BEFORE they become problems
- ✅ Prepare everything for year-end with minimal input
- ✅ Report weekly on financial health

**The goal:** David opens Mission Control, sees green lights, focuses on driving.

---

## Sources
- gov.uk/running-a-limited-company
- gov.uk/corporation-tax
- gov.uk/annual-accounts
- gov.uk/register-for-vat
- gov.uk/charge-reclaim-record-vat
