# Delivery Goal: Evergreen Quote
One sentence. Read it back to yourself. Then to your pair. Then to someone who wasn't in the room. If they can repeat it, it's good.

## Goal
A functional Evergreen Quote application is launched after a green CI build and merged PR, including connected marketing page, React app, API with database, and scaling provided by containerization.


## "Done" looks like

- The quote page loads its recent quotes from the API, and a saved quote survives a reload.
- The estimate on screen and the saved premium agree, at the launch rates.
- `npm test` (API) and `npm run type-check` + `npm run build` (client) pass; both CI jobs on the merge commit are **green**.
- The containerized API serves the wired app, and the cluster demo shows three API pods behind one Service.
- The landing page carries the launch banner and points at the app.
- A reviewed PR is merged, branch deleted.
- `delivery-leadership-package/` is complete and committed.

## Out of scope (this week)
- No authentication, no payments, no real rate engine.
- No AWS Account with actual spend - this work is done locally.
