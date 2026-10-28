# Review: research-design-halal-etsy-products

Review date: 2026-10-28. Scope: the instructions only. No market study and no product work.

**How the review was done.** Three bounded specialist passes covered research methodology, product design/quality/packaging, and halal/originality/IP. A fourth cross-cutting pass looked at structure and how executable the skill is. The three specialists were forked from one session. They shared the same context, so they are **not fully independent reviewers**, and their agreement is not independent corroboration.

**Access limit.** In this cloud session, `help.etsy.com`, `etsy.com` and `hc.erank.com` were blocked at DNS level. All Etsy and eRank facts below come from **search-result summaries of official pages**. By the skill's own rule, that is snippet-level evidence. Confirm each one on the live page before relying on it. That block is itself the most important finding (N1).

---

## 1. Verdict: Ready after specified material changes

The core safeguards are sound and should stay:
- demand, purchase evidence and entry opportunity kept separate;
- no units inferred from reviews;
- no cutoff rules;
- separate gates;
- suitability statuses;
- licence realism;
- an honest verification log.

The necessary changes are mostly about **when** checks happen and **what to do when a tool or page is unreachable**. Without them, the skill can produce confident-looking rankings from snippets, design a product Etsy will not accept, or mark compatibility checks as passed when they never ran.

**What this verdict does not establish.** It is a review of instructions. It says nothing about sales, profitability, or whether any niche will work. Scenario tests show the skill behaves as written. They do not show commercial results. That needs the live trial in Section 4B.

---

## 2. Prioritised findings

Tags: **[V]** fact from an official source seen as a snippet · **[P]** primary source fetched · **[J]** professional judgement · **[U]** unresolved.

### Necessary

**N1. No access check before research; no defined output when Etsy can't be reached** (Part 1 Evidence discipline; Part 3 Define the comparison)
- **Failure:** Etsy pages are blocked, which happened in this session. The skill falls back to search snippets and third-party summaries, labels them "provisional", and still ranks purchase evidence. It also "verifies" Etsy rules from snippets and treats them as confirmed.
- **Wording:** see the revised *Define the comparison* (Section 5).
- **Test:** run with etsy.com unreachable. Pass if:
  - no purchase-evidence ranking is produced;
  - the output lists exactly which exports, screenshots or pages the user must supply;
  - rule-dependent statements are marked "unverified at source".

**N2. Etsy eligibility and production method are checked too late** (Part 1 gates; Part 5)
- Part 5 verifies the Creativity Standards and AI rules "before finalisation".
- Secondary reports describe two changes [U]:
  - an Oct 2026 Etsy restriction on AI-generated instructional downloads (patterns, recipes, instructions);
  - June 2025 changes to the Creativity Standards.
- **Failure:** a strong-demand candidate built mostly with AI is ranked, briefed and built, then turns out to be ineligible at listing time.
- The AI use recorded in the asset record also never reaches the listing's production attribute or disclosure.
- **Wording:** revised *Apply separate gates* (Suitability), plus additions to Part 5 and the asset record.
- **Test:**
  - an AI-drafted recipe/pattern e-book with strong demand must be flagged at the shortlist;
  - a product with AI cover art must carry matching disclosure into the listing package.

**N3. No default delivery route for spreadsheets; file caps are not planned at brief stage** (Part 4 Package; Part 6 brief)
- **[V]** Etsy digital listings allow up to 5 files, 20 MB each. The listed types include pdf/jpg/png/zip/txt/doc/rtf; XLSX is not shown (the list may be dated) [U].
- **Failure:** the product is built as XLSX, or with 8 deliverables, and the problem is only discovered at upload.
- **Test:** an XLSX brief with 8 deliverables. Pass if the brief contains a file map and a stated delivery route (ZIP or link-in-PDF) before production.

**N4. Verification doesn't record which environment ran each check** (Part 4 Verify; Part 6 log)
- Facts about this sandbox [P]:
  - LibreOffice, pdftoppm, openpyxl and reportlab are installed;
  - no Excel, Google Sheets, Adobe Reader, Goodnotes, Canva or mobile;
  - **no Arabic fonts**.
- **Failures:**
  - XLOOKUP, LET or dynamic arrays pass in LibreOffice and break for buyers in Sheets, or the reverse;
  - Arabic renders as boxes or unjoined letters, or the check is skipped and logged as passed.
- **Test:**
  - an XLOOKUP spreadsheet must produce either a caveat or a function swap, with the engine named;
  - an Arabic printable in this sandbox must log "blocked: no Arabic font", not "pass".

**N5. Marketplace Insights scope and free-tool quotas are not handled** (Part 1; Part 3 demand)
- Third-party reports of Marketplace Insights [U]:
  - a ~30-day window;
  - no country filter;
  - ~15 searches/week on the free tier.
- **[V]** eRank Free allows 5 keyword lookups and 5 listing audits per day.
- **Failures:**
  - a global 30-day count gets recorded as UK demand, or as sustained demand;
  - 12 candidates get unequal tool coverage, quietly breaking the skill's own comparable-scope rule.
- **Test:**
  - a UK target plus pasted Insights data must not be labelled UK-specific or seasonal;
  - 12 candidates against a 5/day cap must lead to narrowing or an equal, disclosed allocation.

### Recommended

| ID | Section | Change | Test |
|---|---|---|---|
| R1 | Part 3 Sample listings | Classify on-page signals as follows. The bestseller badge [V: Etsy says "high sales volume in past 6 months", threshold undisclosed] is opaque corroboration. "In X carts" is a display nudge, not purchase evidence. Hidden or rounded shop sales are **unknown**, not zero. | A badge, "20+ in carts" and hidden sales are never converted into units or a rank on their own. |
| R2 | Part 6 Demand ranking | Add the columns *Evidence window* and *Coverage complete/partial*, and record source/geography/window for searches. | Candidates with 30-day and 180-day windows produce a visible mismatch and a tie or narrowed comparison. |
| R3 | Part 1 gate 5; Part 3 economics | Itemise fees with retrieval dates: listing, transaction, payment processing (by country), currency conversion, regulatory, and Offsite Ads (reported as 15%, or 12% above $10k/yr, capped at $100/order) [V]. Add a support/refund assumption: digital items can't be returned, but "not as described" and non-delivery cases still apply [V]. | Economics output shows a per-sale net figure with an Offsite Ads scenario and a support/refund line. |
| R4 | Part 5 sacred text | Record the Arabic source, the translation's copyright holder or licence, and the font licence for Qur'an/hadith text [J]. | A verse-of-the-day printable records the translation licence before production. |
| R5 | Part 5 fonts | State the OFL 1.1 position [P]: embedding and bundling are allowed with the licence text; selling the font on its own is not. | An editable DOCX with an OFL font bundles the font and its licence instead of refusing. |
| R6 | Part 5 / gate 4 | If a licence permits only platform-link delivery (Canva Pro, per secondary reports [U]), carry that into Feasibility, buyer requirements and the package. | A Canva Pro brief avoids a flattened PDF and discloses that a Canva account is required. |
| R7 | Parts 2 and 5 | Define how "Requires qualified review" gets resolved: who decided, the date and the scope. Claude presents sourced positions but never decides. Until a decision is recorded, keep the neutral alternative. | A figurative-illustration question stays open, the draft stays neutral, and nothing is finalised. |
| R8 | Part 4 listing | Verify Etsy's current listing-image requirements for digital items before making previews. A newer Etsy article exists but could not be read [U]. | Preview plan cites the requirement and its retrieval date. |

### Optional

- **O1. Google Trends:** use broader parent terms and say it measures Google, not Etsy. Long-tail "no data" means unknown, which is already partly covered.
- **O2. Title length:** "140 characters is a limit, not a target." Etsy's own pages conflict (one checklist suggests about 40), so the existing "concise, front-loaded" wording is correct.
- **O3. Repetition:** Part 4 tells the agent to verify upload limits three times, and the no-publish rule appears in four places. Consolidating saves context, but changes no behaviour. Only do it if the skill is otherwise being edited.
- **O4. Packaging:** move Parts 3–6 into reference files loaded on demand, keeping Parts 1–2 in the main skill file. This loads less context per task. It changes no behaviour.

---

## 3. Capability and execution check

| Dependency in the skill | Reality in a typical Claude session | Fallback, and what it does **not** give you |
|---|---|---|
| Browsing Etsy search, listings, reviews and Help | May be blocked; it was here. Anti-bot pages are common. | User-supplied screenshots, saved pages or CSV of named listings. Gives a smaller, user-selected sample with possible selection bias. Snippets alone must not rank purchase evidence. |
| Marketplace Insights and Shop Manager | Only the seller can access them. Claude can't. | User pastes or exports results. Reported as global and ~30 days, so they give no country split or seasonality. |
| eRank Free | Needs an account; 5 lookups/day [V]. | User runs the lookups. The quota limits candidate breadth, and figures are third-party estimates. |
| Google Trends / Pinterest Trends | Often reachable; long-tail terms are thin. | Use parent terms. Neither measures Etsy search or sales. |
| Independent specialist agents | Forks share context; fresh agents need the full brief. | Separate passes, disclosed. Agreement between them is not corroboration. |
| Excel, Google Sheets, Adobe Reader, Goodnotes, Canva, iOS/Android | Not available in this sandbox. | LibreOffice recalculation and pdftoppm rendering. This is **not** Excel or Sheets compatibility. Name the engine and list untested apps. |
| Arabic rendering | No Arabic font installed here. | Install an OFL Arabic font (e.g. Noto Naskh/Amiri) if the network allows; otherwise block the Arabic part. Rendering is still not a scholarly proofread. |
| Image generation | Not guaranteed to be available. | Vector/programmatic previews of the real product, which are often better for truthful listings anyway. |
| Persistent memory and scheduled re-observation | Not assumed; scheduling needs authorisation. | Continuation record plus a user-triggered rerun. |
| Physical printing; Windows/macOS extraction | Not available. | Render-based checks; Linux unzip only. Disclose the rest. |

---

## 4. Focused validation plan

### A. Instruction tests (cheap; run before the live trial)

Each task is a short prompt with planted conditions. Score pass or fail against the stated criterion.

1. **Incomplete data:** etsy.com unreachable, plus an eRank screenshot for 3 keywords. Pass: keyword clusters only; no purchase ranking; an exact list of what the user should supply. (N1, N5)
2. **Comparable vs incomparable:** candidate A has a 30-day review window across 8 shops; candidate B has 180 days across 3 shops plus a pasted Insights count. Pass: tie, narrowed comparison or qualitative finding; window mismatch visible in the table. (R2)
3. **Seasonal:** a Ramadan planner observed in August with no recent reviews. Pass: labelled seasonal/historical with an uncertainty check, not rejected. (existing rule)
4. **New-seller entry:** two shops under a year old show recent reviews, but product launch dates are unknown. Pass: entrant evidence is qualified and launch date is marked unknown. (existing rule)
5. **Economics:** $6 price, UK buyer, US seller. Pass: itemised fees with dates, an Offsite Ads scenario, and a support/refund line; no invented forecast. (R3)
6. **Eligibility timing:** an AI-drafted crochet-pattern e-book with the strongest demand. Pass: flagged at the shortlist. (N2)
7. **Handover:** turn a provisional shortlist into a brief for a budgeting spreadsheet. Pass: evidence IDs linked to acceptance checks, a file map within caps, a delivery route, and named target apps. (N3)
8. **Functionality:** build a small spreadsheet that uses XLOOKUP. Pass: input tests logged with the engine named; Sheets/Excel marked untested or the function swapped. (N4)
9. **Packaging/setup:** the zip contains `.DS_Store` and `__MACOSX`, and the start guide references a missing file. Pass: both are caught and fixed, and the clean-copy buyer task is logged.
10. **Licensing/suitability:** a Canva Pro element, an OFL font, a copyrighted Qur'an translation, and an unresolved imagery question. Pass: link-only delivery is disclosed, the OFL font is bundled with its licence, the translation is flagged, and the imagery stays neutral and open. (R4–R7)

### B. Live end-to-end trial (the only real evidence of business value)

One complete run on a single real candidate:
- the user sets country and currency and provides any first-party exports;
- research, then brief, then the built product, then the full verification log, then the listing package;
- publish only with authorisation;
- record dated observations of visits, favourites and sales at around 2, 4 and 8 weeks, run when the user asks;
- set continue/revise/stop criteria in advance.

This tests the skill's usefulness. A single listing's outcome cannot validate the method statistically.

---

## 5. Revised sections

Sections not listed here stay **verbatim**. Text marked *(new)* is inserted. Everything else in each block is the current wording, kept as is.

### Part 1 — Evidence and tool discipline: add as the first bullet *(new)*

- Before collecting evidence or stating any Etsy rule, test access to Etsy search results, listing pages, listing reviews and Etsy Help, and record which were reachable. Treat Etsy rules seen only in search snippets or third-party summaries as "unverified at source" until read on Etsy's own page or confirmed by the user from the live seller form.

### Part 1 — Apply separate gates (full replacement)

Do not use an arbitrary weighted total to hide a failed requirement:

1. Demand: relevant Etsy searches and/or recent purchase signals, with gaps labelled.
2. Entry: plausible buyer-specific advantage and competition assessment.
3. Suitability: halal screen, asset provenance and Etsy eligibility. Before shortlisting, record the intended production method (original, licensed, AI-assisted, AI-generated) and check it against Etsy's current Creativity Standards, AI rules and listing-image requirements for that product type. If those cannot be read at source, mark eligibility "unverified" and do not assign "Suitable".
4. Feasibility: ability to produce and test the actual promised formats in the available environments, within current Etsy file-count, file-size and file-type limits, including any delivery method a licence requires (for example template-link-only assets).
5. Economics: realistic prices; itemised, dated fees (listing, transaction, payment processing for the seller's country, currency conversion, regulatory, and an Offsite Ads scenario); support effort; an assumption for refunds and "not as described" cases; other stated assumptions.

For complete requests, select the strongest supported candidate and explain the trade-off.

If evidence cannot support selection, deliver the provisional shortlist and smallest useful validation step.

Build an explicitly unvalidated prototype only when authorised; never call it a validated winner.

### Part 3 — Define the comparison (full replacement)

Record:
- Research date.
- Market.
- Language.
- Currency.
- Timeframe.
- Access limits, including the result of the access check: which of Etsy search, listing pages, reviews, Etsy Help, and user-supplied first-party data were available.
- Halal requirements.

If listing pages or reviews cannot be retrieved, do not rank purchase evidence from snippets or third-party summaries. Request user-supplied screenshots, saved pages or exports for named listings, deliver keyword discovery labelled "purchase evidence not collected", and continue other accessible work.

Before broad discovery, compare the planned queries per candidate against the verified free quotas of each tool. Give every candidate being ranked the same query budget. If quotas prevent equal coverage, reduce candidates or split work across user-run sessions and record the split. Do not rank candidates measured with different tool budgets.

Define each candidate as:

Buyer + task + format + software/print requirements.

Separate printable planners, tablet planners and spreadsheets.

Group colour variants as one offer family unless evidence supports a distinct use.

For broad discovery, scan roughly 10–15 product families, then deepen a small shortlist.

For a specified niche or candidate comparison, investigate the requested scope directly.

Treat ranges as planning aids, not statistical guarantees.

Avoid limiting discovery to previously suggested categories.

Screen unsuitable and Etsy-ineligible products early.

### Part 3 — Collect demand evidence: insert after "Prefer Etsy first-party search data when available." *(new)*

Treat Etsy Marketplace Insights, run by the user and shared, as first-party search data. Before use, verify its current geography, window and quota on Etsy Help. Record the geography as reported and the window. Do not treat it as country-specific, or as evidence of seasonality or persistence, without dated repeat pulls or a longer-period source.

### Part 3 — Collect demand evidence: replace "Use Google Trends for long-term interest and seasonality." with

Use Google Trends for long-term interest and seasonality, using broader parent terms when long-tail terms return no data. It measures Google web search, not Etsy search.

### Part 3 — Sample listings consistently: insert after "Label shop-wide lifetime figures separately." *(new)*

Record Etsy's bestseller badge as a first-party but opaque signal (verify Etsy's current definition; the threshold is undisclosed), useful only as corroboration. Record "in carts" or similar urgency messages as display observations, not purchase evidence. Record shop sales counts as shop-wide, lifetime and possibly rounded. Hidden counts are unknown, not zero.

### Part 4 — Select tools and formats: append *(new)*

Before production, record the verification environment for each promised format: for example, the spreadsheet engine, PDF renderer or reader, and installed fonts. Prefer spreadsheet functions that exist in every application the listing will name, or list the unsupported applications. Before Arabic production, confirm an Arabic-capable font is installed and its licence permits embedding or redistribution. If none is available, stop the Arabic portion and record it as blocked.

### Part 4 — Verify actual deliverables: add under "All formats" *(new)*

- Record the engine, reader or environment that produced each result. Do not claim Excel, Google Sheets, Adobe Reader, Goodnotes, Canva or mobile compatibility from a different application's result.

### Part 4 — Package and prepare the listing: replace the three separate upload-verification sentences with one

Before production, and again before packaging, verify Etsy's current digital-listing file count, per-file size and supported file types on Etsy's official help or the live listing form. If a needed type (for example XLSX) is not supported, deliver it inside a ZIP or through a verified link in a delivered PDF. Record the route used.

### Part 4 — Package and prepare the listing: add to the listing checklist *(new)*

- The Etsy production attribute and AI-disclosure text required by current Etsy guidance, consistent with the asset record.
- Verify Etsy's current listing-image requirements for digital items before preparing previews.
- Treat the title character cap as a limit, not a target.

### Part 5 — insert after "Commercial use does not automatically permit redistributing fonts, stock assets or editable templates." *(new)*

Record each font's licence. SIL OFL fonts may be embedded or bundled with the licence text included, but not sold on their own or renamed when modified under a reserved name. For other licences, check the terms for embedding, editable-file delivery and app use. If a licence permits only platform-link delivery, record it as a feasibility limit, a buyer requirement and the delivery method.

For Qur'an or hadith text, record the Arabic source, the translation and its copyright holder or licence, and the font licence. Use public-domain, licensed or owner-written translations only.

### Part 5 — insert after "Seek qualified guidance for material unresolved questions before inclusion." *(new)*

Record who resolved each question (the owner, or a reviewer the owner named), the date and the scope. Claude may present sourced positions but does not decide the question. Without a recorded decision, keep the neutral alternative and finalise nothing that depends on it.

### Part 6 — Rankings: Demand (replace header)

Product + buyer | Searches (source, geography, window) | Recent purchase evidence | Evidence window | Sample and coverage (complete/partial) | Sustained/seasonal/emerging/historical | Confidence | Contradiction | Sources

### Part 6 — Asset record (replace header)

Asset/component | Creator/source | Original/licensed/AI-assisted/AI-generated | Licence and acquisition date if relevant | Permitted customer distribution/editing/delivery method | Required attribution/disclosure | Etsy production attribute/AI disclosure and where shown | Verification or unresolved restriction

### Part 6 — Design brief: add *(new)*

- Customer file map: file, then contents, then estimated size, then delivery route, checked against current Etsy limits.
- Verification environments per format, and the target applications to be named in the listing.

### Part 6 — Verification log (replace header)

Artifact/version | Check | Environment/engine | Input/page | Expected result | Actual result | Pass/fail/blocked | Correction | Untested limitation

---

## 6. Next action

Run instruction test A1 (incomplete data, with Etsy unreachable) against the revised skill, then fix whatever it exposes. It exercises the highest-risk finding (N1) together with N5, and it costs minutes. After that, start the live trial (4B) once you have set the target country and currency and can supply first-party exports.

---

## Sources (retrieved 2026-10-28; Etsy pages via search snippets only)

- Etsy Help:
  - [Manage Digital Listings](https://help.etsy.com/hc/en-us/articles/115015628347)
  - [Create a Listing](https://help.etsy.com/hc/en-us/articles/115015628707)
  - [Tags](https://help.etsy.com/hc/en-us/articles/360000336307)
  - [Image requirements](https://help.etsy.com/hc/en-us/articles/44297885802647)
  - [Fees](https://help.etsy.com/hc/en-us/articles/115014483627)
  - [Finding items / Bestseller](https://help.etsy.com/hc/en-in/articles/4409221032599)
  - [Marketplace Insights](https://help.etsy.com/hc/en-us/articles/35122361353239)
- Etsy policy pages:
  - [Fees & Payments Policy](https://www.etsy.com/legal/fees/)
  - [Cases Policy](https://www.etsy.com/legal/policy/cases-policy/243306189901)
  - [House Rules](https://www.etsy.com/help/article/4511)
  - [Keywords 101](https://www.etsy.com/seller-handbook/article/keywords-101-everything-you-need-to-know/382774281517)
- eRank: [Plans](https://erank.com/plans) · [Free plan](https://help.erank.com/blog/eranks-free-plan/)
- Fetched directly: [SIL OFL 1.1](https://opensource.org/license/ofl/)
- Secondary sources [U]:
  - [Value Added Resource — AI patterns](https://www.valueaddedresource.net/etsy-bans-ai-patterns/)
  - [Value Added Resource — Creativity Standards June 2025](https://www.valueaddedresource.net/etsy-creativity-standards-update-june-2025/)
  - [Value Added Resource — Marketplace Insights](https://valueaddedresource.net/etsy-marketplace-insights-tool/)
  - [Alura — Marketplace Insights](https://www.alura.io/vs/etsy-marketplace-insights)
