# Accounting Skill

## Apps
- **Accounting Rails**: localhost:3002 | `/Users/shiftbot/.openclaw/workspace/accounting-rails/`
- **Xero Client**: `/Users/shiftbot/.openclaw/workspace/clarks-proving-ground/xero-client.js`
- **Tokens**: `/Users/shiftbot/.openclaw/workspace/clarks-proving-ground/.xero-tokens.json`

## Xero API
```javascript
const xero = require('./xero-client');
// Get 2025+ transactions
const txns = await xero.get('/BankTransactions?where=Date>=DateTime(2025,01,01)');
```

## Cross-Reference Logic
Fuzzy match: date ±2 days, amount ±10%
```javascript
const match = xeroList.find(x => {
  const dayDiff = Math.abs(x.date - expDate) / (1000*60*60*24);
  const amtDiff = Math.abs(x.amount - expAmt) / expAmt;
  return dayDiff <= 2 && amtDiff <= 0.10;
});
```

## Import Expenses
```bash
cd /Users/shiftbot/.openclaw/workspace/accounting-rails
eval "$(rbenv init - bash)"
bundle exec rake expenses:import[/path/to/file.csv]
```

## Data Cleanup Rules
- Delete crypto transfers (vendor contains "→ BTC", "→ SOL")
- Fix NULL amount_gbp: set to amount
- Fix crazy fx_rates (amount_gbp > 50000): reset to amount

## Categories
- EQUIPMENT: tech, accessories, motorsport gear
- FOOD: restaurants, cafes
- TRAVEL: car rental, hotels, flights, parking
- PROFESSIONAL-SERVICES: photography, consulting
- ENTRY-FEES: race entries, events
- MEDICAL: doctors, health
- SOFTWARE: Xero, subscriptions
- OTHER: unclassified

## Businesses
- **Super Veloce Ltd**: Racing driver expenses
- **Speed Capital Ltd**: Coach Dave Delta, SimGrid

## Cron Jobs
- Xero token refresh: every 20 min (gpt-4o-mini)
- Bug fix patrol: hourly (sonnet)
