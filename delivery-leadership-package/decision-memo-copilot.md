# Decision Memo: Copilot Usage
Target length: ~250 words. Write for a non-technical reader. Name the options you **rejected**, not just the one you picked.

**Date:** 11/18/26
**Author:** Tina Matthys
**Decision area:** Copilot usage for adding seed data to the Mongo DB

## Context
Copilot was asked to "add another quote to this list for renters using believable data and the rating files to calculate the correct monthlyPremium value", followed by "add another quote for any type". It produced the following:
`Added a new Renters quote (q7) to seed.js.

Age: 32
Coverage: $30,000
Monthly premium: $120.00
Premium calculated using calculatePremium()
Syntax validation passed.`
`Added a Life quote (q8) to seed.js.

Age: 45
Coverage: $150,000
Monthly premium: $1,050.00
Calculated using calculatePremium("life", 45, 150000)
Syntax validation passed.`

## Options considered
1. **Option A: Don't use the proposed quotes in seeding - DECLINED** 
N/A
2. **Option B: Use the proposed quotes in seeding - ACCEPTED**
Quotes were created in the right schema, with accurate data and correctly calculated premiums

## Recommendation and Why
We will select Option B and use the data provided by Copilot since all updates were valid and the schema validation passed when running 'npm run seed'

## What would change my mind
If 'npm run seed' had produced any errors, I would question the use of this data
