# Stakeholder Status Update — Evergreen Quote

> Copy to `delivery-leadership-package/status-update.md`. Send it (i.e., paste it in the cohort channel) at the end of the day an inject lands. Target length: ~150 words.

**To:** Lisa Cueva, Project Sponsor
**From:** Angela Jeske, Delivery Lead
**Date:** July 14, 2026

## What shipped today

- Evergreen Quote page fully assembled from provided HTML partials (header, hero, quote form, testimonials, footer)
- Brand theme (theme.css) applied and Bootstrap CONFIG classes configured
- Page verified responsive at 375px mobile width with no horizontal scroll
- Risk register, roadmap, and decision memo drafted and added to delivery-leadership-package/

## What slipped (and why)

- Testimonials section cannot ship — Legal requires signed customer release forms before publication (est. 2-week approval timeline)
- Compare Plans nav link not yet added — Marketing request received at 14:00 via inject, being assessed for Thursday delivery

## What's next (tomorrow)

- Wire quote calculator JavaScript snippet to form (Day 3 priority)
- Add Compare Plans nav link to header navigation
- Hide or replace testimonials section pending Legal clearance
- Enable GitHub Actions CI workflow
- Open PR from delivery/lead to main

## What I need from you

- Confirmation on testimonials: hide section entirely or show placeholder text until Legal approves?
- Exact URL for the Compare Plans destination page for the nav link href
- Confirmation whether Thursday is a hard deadline for the Compare Plans link

## Inject #2 — Leader Response

We have two active issues. First, a customer received a quote of 
$8,950/month for $25,000 of renters coverage — clearly incorrect 
based on our rate logic (expected: ~$10/month). Second, CI on main 
has been failing for 32 minutes with a missing file: 
assets/rates/renters.json — this appears to be connected to a 
recent hotfix commit "adjust renters rate" that likely introduced 
a dependency on a file that was never committed. I am asking the 
engineering team to confirm whether renters.json was intentionally 
added as a required asset and to either commit it or remove the 
CI check. I am holding any further merges to main until CI is 
green. Customer success should inform the affected customer that 
we are investigating and will follow up within the hour.

_Be specific. "Direction on X by 11:00 Wednesday" beats "thoughts welcome."_
