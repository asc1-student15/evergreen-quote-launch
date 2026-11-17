# Risk Register

> Copy to `delivery-leadership-package/risk-register.md`. At least 5 rows. **No boilerplate**; your peers will grade you on whether these are real.

| # | Risk | Owner | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation | Trigger to escalate |
|---|---|---|---|---|---|---|
| R1 | The page renders while the client/API contract is quietly wrong, so the demo "works" until a field goes missing | Dev Lead | M | H | Run `npm run type-check` and `npm test` after every wiring step, not just before merge | One or both checks are still red at 16:00 on Thursday = no merge |
| R2 | There's a mismatch in quotes displayed when the page is loaded and checked against the database | Dev Team | M | M | Wire the client to use the API data so that the client site quote list matches the API's database records | Mismatch still occurs after Monday |
| R3 | The estimate quote displayed and the saved quote in the list for the same entry do not match | Dev Team | M | M | Check the rate table to ensure the local client and the sponsor's expected standardized rates for the API match | This scenario is still occurring after Tuesday |
| R4 |  |  |  |  |  |  |
| R5 |  |  |  |  |  |  |

## How I'll use this register

_One short paragraph. When will you re-read it? Who else can see it? What's the cadence?_
