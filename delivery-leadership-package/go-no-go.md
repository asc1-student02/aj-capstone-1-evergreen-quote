# Go / No-Go — Merge Decision

> Copy to `delivery-leadership-package/go-no-go.md`. Make this call **from** the CI result, not in spite of it.

# Go / No-Go — Merge Decision

**Date / time:** July 14, 2026 / ~14:00
**Decision:** ☐ GO   ☑ NO-GO   ☐ GO WITH CONDITIONS

## CI evidence

- Latest run on `delivery/lead`: red · link: 
  https://github.com/asc1-student02/aj-capstone-1-evergreen-quote/actions
- Workflow file: `.github/workflows/ci.yml`
- What the workflow actually checked:
  - ✓ Check out the code
  - ✓ Set up Node
  - ✓ Validate HTML (html-validate)
  - ✗ Smoke-check required files — missing: assets/rates/renters.json
  - ✓ Lint JS syntax

## What "GO" would mean

- Merge `delivery/lead` → `main`, squash, delete branch.
- Tag the merge commit `week-1`.

## What "NO-GO" would mean

- Hold the merge until: assets/rates/renters.json is committed 
  to the repo OR the CI check is updated to remove the reference 
  to that file, AND CI returns green on delivery/lead.
- Owner of that condition: Engineering team lead.
- Re-evaluate at: 15:30 today.

## My call

NO-GO. The one thing that drove this decision is CI failing on 
the Smoke-check step due to a missing file (assets/rates/renters.json) 
introduced by the "adjust renters rate" hotfix — the same commit 
that appears connected to a customer receiving a wildly incorrect 
quote of $8,950/month for $25,000 of renters coverage. This will 
flip to GO when CI is green and engineering confirms the rate 
calculation is correct.

_2–3 sentences. State the call. Name the *one* thing that drove it. Name what would flip it._
