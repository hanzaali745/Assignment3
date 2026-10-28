# Evals for research-design-halal-etsy-products

These are five repeatable test cases. Each one turns a scenario first tested by hand on 2026-10-28 into a case that can be re-run (see `skill-review/tests/`).

| Case | Original test | What it checks |
|---|---|---|
| access-check-incomplete-data | A1 | Checks which sources are reachable before researching. Gives no purchase ranking without listing evidence. Labels estimates. Does not count broad keywords as demand for a narrower product. Keeps Etsy eligibility separate from halal suitability. |
| handover-brief-budget-spreadsheet | A7 | Traces each research finding to a design choice and a check. Weights weak evidence as weak. Includes a file map and delivery route, names the test environments, records AI use, and handles zakat carefully. |
| xlookup-spreadsheet-compatibility | A8 | Tests a working XLSX across a range of inputs, names the engine used, and makes honest Excel/Sheets compatibility claims (XLOOKUP is not in older Excel). Does not hide errors. |
| dirty-package-cleanup | A9 | Removes system junk files and finds a promised file that is missing. Leaves the original unchanged, inspects the pages, runs a clean extraction test, and makes no claims about checks it did not run. |
| licensing-ramadan-verse-printable | A10 | Flags translation copyright and the Canva Pro rule against flat-PDF delivery. Permits the OFL-licensed font. Leaves imagery decisions open. Applies the Arabic safeguards. |

## Running them

- **With skill-creator:** run each case with the skill and without it (or against an older snapshot as the baseline), grade the results against `graders/`, then aggregate.
- **With Claude Code:** from the skill folder, run
  `claude plugin eval . --allow-tools Write,Edit,Bash,WebSearch,WebFetch --scaffold`.
  These are real model runs and are billed.

## Results depend on the environment

- **Etsy access:** the assertions are worded so they hold whether or not Etsy is reachable. The first case's assertions only apply when listing pages cannot be retrieved. If Etsy becomes reachable, add a separate case that tests behaviour with real listing access.
- **Not a measure of commercial value:** passing these cases shows that the skill's instructions are followed. It does not show that a product will sell.
- **Test data:** the eRank figures and research notes in the prompts are invented test fixtures.
