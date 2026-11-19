# Go / No-Go: Launch Decision
This is the call for Friday's launch demo. Make it **from** the CI result, not in spite of it.

**Date / time:** 11/18/26
**Decision:** x GO   ☐ NO-GO   ☐ GO WITH CONDITIONS

## CI evidence
- Latest run on `delivery/lead` (both jobs): Green ·  link: https://github.com/asc1-student15/evergreen-quote-launch/actions/runs/44360661705
- Workflow file: `.github/workflows/ci.yml`
- What the workflow actually checked: 
Test the API
Type-check and Build the Client

## What "GO" would mean
- Merge `delivery/lead` → `main`, squash, delete branch.
- Tag the merge commit `launch`.
- `main` branch has two green CI runs

## What "NO-GO" would mean
- Hold the merge until: Issues are resolved around pod restarts and the 'cleanups' are revisited
- Owner of that condition: Dev Team
- Re-evaluate at: Thursday morning check in

## My call
We will move forward with the live demo on Friday provided that the renaming of the DB variable is reverted and the demo environment is operational with 3 started pods and 1 started Mongo DB by 9am Thursday. CI runs should both stay Green as well.