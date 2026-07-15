# Delivery Review — Evergreen Quote

> Copy to `delivery-leadership-package/delivery-review-outline.md`. Five slides OR one page. Target: 5 minutes spoken, then 3 minutes of questions.

# Delivery Review — Evergreen Quote
**Presenter:** Angela Jeske, Delivery Lead
**Date:** July 15, 2026

## Slide 1 — Delivery goal & did we hit it?

- **Goal:** By Thursday EOD, an assembled, themed, responsive 
  Evergreen Quote app with the wired quote calculator is merged 
  to main via a reviewed PR with a green CI run.
- Hit? ☑ Yes
- We delivered all five required sections, applied the brand theme, 
  verified responsive at 375px, wired the quote calculator, enabled 
  CI, and merged via a reviewed PR with a green CI run.

## Slide 2 — What shipped

- Screenshot of assembled Evergreen Quote app see Live Server at http://127.0.0.1:5500/index.htmlL
- Link to merged PR: https://github.com/asc1-student02/aj-capstone-1-evergreen-quote/pull/8
- Link to green CI run: https://github.com/asc1-student02/aj-capstone-1-evergreen-quote/actions

## Slide 3 — Two key decisions

- **Decision 1:** Prioritized required Bootstrap CONFIG classes 
  over optional "About" nav link challenge.
  Why it mattered: ensured responsive layout met done criteria 
  before attempting optional enhancements.

- **Decision 2:** Held all merges to main during Inject #2 
  (NO-GO call) when CI was red and customer received incorrect 
  quote of $8,950/month for $25k renters coverage.
  Why it mattered: shipping broken rate logic would have been 
  a customer trust and compliance risk.

## Slide 4 — Risks & injects

- **Top risk we tracked:** Quote calculator JS not wired (Day 3 
  dependency) — mitigated by placeholder comment in HTML on Day 2 
  and wired successfully on Day 3.

- **Inject #1 (Tue):** Legal placed a hold on testimonials — 
  signed customer release forms required before publication 
  (est. 2-week approval). Re-prioritized by keeping testimonials 
  in codebase but holding from release. Added Compare Plans nav 
  link request from Marketing to the backlog.

- **Inject #2 (Wed):** Customer received incorrect quote 
  ($8,950/month for $25k renters). CI on main failing 32 minutes 
  — missing assets/rates/renters.json from hotfix commit. 
  Decision: NO-GO — held all merges to main, routed to engineering 
  team, held until CI green and rate logic confirmed correct.

## Slide 5 — What I'd do differently next round

- Get Legal sign-off on customer-facing content (testimonials) 
  before build starts, not after assembly is complete.
- Require a file checklist review before any rate hotfix is 
  committed — would have caught missing renters.json before 
  it broke CI and customer quotes.
- Fix HTML void element self-closing tags earlier — caught by 
  CI validator, non-breaking but should be clean code from the start.
- Build in a buffer day before final merge for QA verification 
  and stakeholder review.

## Q&A prep — likely questions

**Q: Why didn't you fix the HTML validator errors?**
A: The 7 warnings were non-breaking — the page rendered and 
functioned correctly. CI still passed. I documented them as 
a known issue for a follow-on PR rather than risk destabilizing 
the build before the Thursday EOD deadline.

**Q: What happened with the testimonials?**
A: Legal flagged missing signed release forms during Inject #1. 
The section remains in the codebase but is not live. Clearance 
is estimated at 2 weeks.

**Q: How did you handle the production incident in Inject #2?**
A: I made a NO-GO call, held all merges to main, routed the 
issue to the engineering team, and communicated status to the 
project sponsor. I did not attempt to fix the code myself.

- _e.g., "Why didn't you ship X?"_
- _e.g., "If you ran this week again with 3 engineers, what's the first thing you'd ask them?"_
