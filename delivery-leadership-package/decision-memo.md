# Decision Memo: Duplicate Premium Retrieval
Target length: ~250 words. Write for a non-technical reader. Name the options you **rejected**, not just the one you picked.

**Date:** 11/17/26
**Author:** Tina Matthys
**Decision area:** Premium Calculations are duplicated in the Client and API

## Context
The premium calculations for the application live in two places, the Client and the API. Updates would need to be made in both places to keep the quotes to the customer consistent.

## Options considered

1. **Option A: Revert to prior code where only the Client holds the calculation - DECLINED.** 
This would allow the user to instantly create a quote, but we would lose the opportunity to save it.
2. **Option B: Revert to prior code where only the API holds the calculation - DECLINED.**
This would allow only a backend user with access to the DB the opportunity to save quotes.
3. **Option C: Keep updated premium calculations synced between Cient and API - ACCEPTED.**
This allows both customers and back end users access to the same quoting strategy and functionality. Keeping everything up to date is a little more effort, but it will be worth the extra time and network calls.

## Recommendation and Why
Option C was accepted so that all user types operate off the same premium calculations and are able to retrieve consistent quotes after saving.

## What would change my mind
If a defect was found with an inconsistency between the Client and API code, it would need to be mitigated before release.
