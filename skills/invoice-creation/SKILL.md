# Invoice Creation Skill

## Trigger
When user asks to create/make an invoice, bill, or sales invoice.

**Keywords:** "create invoice", "make invoice", "new invoice", "invoice for", "bill for"

## Flow

### Step 1: Gather Information
Reply with exactly three questions:

```
📝 **New Invoice**

1. **Who's it for?** (client name)
2. **What's the invoice subject?** (e.g., "February driving services")
3. **What are the line items?** (description + amount each)
```

### Step 2: Wait for Response
User provides answers. Can be:
- All three in one message
- Partial answers (ask for missing info)
- Voice message with details

### Step 3: Create Invoice
Once all three answered:
1. Navigate to Bean Counter: `http://localhost:3002/sales_invoices/new`
2. Select client from dropdown (match by name)
3. Add line items with descriptions and amounts
4. Submit form
5. Screenshot and send confirmation with invoice number + total

## Clients (Bean Counter)
Known clients in system:
- Racing Car SA
- AkInformatica S.a.s.
- Alberto Duran
- CP Film Productions Ltd
- Challenge Sport & Services
- Duncan Cameron
- FFLaser Msp.
- J H J Racing Team Limited
- Nordstar Partners Ltd
- Rinaldi Automotive GmbH

If client not in list, ask user to confirm or add client first.

## Example Interaction

**User:** Make me an invoice

**Assistant:**
```
📝 **New Invoice**

1. **Who's it for?** (client name)
2. **What's the invoice subject?** (e.g., "February driving services")  
3. **What are the line items?** (description + amount each)
```

**User:** Racing Car SA, Barcelona test day, €5000 driving fee plus €300 travel expenses

**Assistant:** *[Creates invoice, sends screenshot]*
Invoice SI-20260206-003 created for Racing Car SA — €5,300 total.

## Notes
- Default currency: EUR
- Default VAT: 0%
- Default payment terms: 30 days
- Subject goes in Notes field (optional)
