# Changelog

## 2026-10-28 — Five necessary changes (review: skill-review/research-design-halal-etsy-products-review.md)

The five changes below are all that changed. All other wording is preserved from the baseline.

### N1 — Access check before research and rule statements

- Part 1 Evidence discipline: new first bullet. Test whether Etsy is reachable before researching or quoting any Etsy rule. Mark snippet-only rules "unverified at source".
- Part 3 Define the comparison:
  - The access-check result is recorded with the other access limits.
  - No purchase-evidence ranking is made when listing pages or reviews can't be retrieved.
  - In that case the skill names the screenshots or exports the user should supply.

### N2 — Etsy eligibility and production method at shortlist

- Part 1 gate 3:
  - Record the production method and check it against Etsy's current rules before shortlisting.
  - If those rules can't be read on Etsy's own pages, eligibility is "unverified" and the candidate cannot be marked "Suitable".
- Part 5: the Creativity, IP and AI rules are now checked at shortlisting, not only "before finalisation". AI disclosure is carried into the listing.
- Part 4 listing: production attribute and AI-disclosure text added.
- Part 6: production method and eligibility added to the suitability record; AI-generated category and disclosure column added to the asset record.

### N3 — Delivery route and file limits planned in the brief

- Part 1 gate 4: Etsy file count, file size and file type are now part of feasibility.
- Part 4 brief: customer file map and delivery route added.
- Part 4 package: three separate upload-verification sentences consolidated into one rule. It applies before production and again before packaging, with ZIP or link-in-PDF as the fallback route.
- Part 6 brief: file map line added.

### N4 — Verification environment recorded

- Part 4 Select tools: record the environment for each format, prefer functions every named app supports, and add an Arabic-font gate.
- Part 4 "All formats": no compatibility claims from a different application; a check that couldn't run is "blocked".
- Part 6:
  - brief now lists the environments;
  - verification log gains an Environment/engine column and a "blocked" status.

### N5 — Marketplace Insights scope and equal tool budgets

- Part 3 Define the comparison: each candidate gets the same query budget within verified free quotas.
- Part 3 Collect demand evidence: verify Marketplace Insights scope before use; don't treat it as country-specific or seasonal without support.
- Part 6 Evidence register: query budget per candidate recorded.

### Not applied (recommended, pending owner decision)

R1–R8 and O1–O4 from the review.

## 2026-10-28 — Fixes from test A1 (skill-review/tests/A1-access-check-2026-10-28.md)

- **G1 (Part 3, Collect demand evidence):** demand is now ranked only on keywords that match the candidate. A broader parent keyword is reported as context, and the candidate's own demand is marked unknown.
- **G2 (Part 1, gate 3):** when eligibility is unverified, Etsy eligibility is recorded separately from the halal status, and neither Suitable status may be given overall.

## 2026-10-29 — Browser-based Etsy rule checks

- **Part 1, new section "Verify Etsy rules in the user's browser":**
  - When a tool that acts in the user's own browser is available (such as Claude in Chrome), use it to read Etsy's own pages for:
    - file limits and file types;
    - Creativity Standards;
    - AI disclosure rules;
    - image requirements;
    - title and tag limits;
    - fees.
  - Rules read this way count as verified at source.
  - Read-only by default: no sign-in, setting changes, listing edits, purchases or messages unless the user asks.
