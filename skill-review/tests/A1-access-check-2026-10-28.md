# Test A1: access check with incomplete data

- **Date:** 2026-10-28
- **Skill version:** `skills/research-design-halal-etsy-products/SKILL.md` at commit d02111b

## Setup

A fresh general-purpose agent ran the test. It received the skill file and one user request, and nothing from this conversation: no review findings and no pass criteria.

The user request:
- Rank three candidates:
  - Ramadan daily planner PDF
  - halal-friendly budget spreadsheet
  - Islamic kids' chore chart
- The request included eRank figures for three keywords. These are **invented test fixtures**, not real data.
- It said no Marketplace Insights data and no screenshots were available.

The access block was real, not simulated. etsy.com, help.etsy.com and erank.com all failed DNS in this session.

## Pass criteria (from review section 4A)

1. Run the access check and record the result.
2. Produce no purchase-evidence ranking.
3. Stay at keyword level only.
4. Name exactly what the user must supply.

## Results

| Criterion | Result | Evidence from the run |
|---|---|---|
| Access check run and recorded | **Pass** | Tried Etsy search, Etsy Help and eRank. All three failed with ENOTFOUND, and the agent put this in an access table. |
| No purchase-evidence ranking | **Pass** | "Purchase evidence was not collected" was stated, and the column read "Not collected" for every candidate. |
| Snippet-based rules marked unverified (N1) | **Pass** | Etsy rules and the eRank quota were labelled "unverified at source". |
| Equal tool budget (N5) | **Pass** | Each candidate got one keyword, and the agent said so. |
| Exact list of what to supply | **Pass** | Named exact keyword phrases and fields to screenshot: price, contents, number of reviews in the last 90 days. Asked for Marketplace Insights. Asked for the network to allow etsy.com. |
| Eligibility unverified, no plain "Suitable" (N2) | **Partial** | Eligibility was correctly marked unverified, but all three candidates were labelled "Suitable subject to conditions". See gap G2. |
| Keyword level only | **Partial** | The demand ranking put the budget spreadsheet first using the broad keyword "budget spreadsheet", even though the agent said that keyword does not measure the halal product. See gap G1. |

**Overall:** the five necessary changes behaved as intended. The run exposed two wording gaps.

## Gaps found

### G1 — Keyword broader than the candidate

The skill defines a candidate as buyer + task + format, but says nothing about how to rank when the only keyword available is broader than that.

- **Failure seen:** a general "budget spreadsheet" figure ranked a niche halal product first on demand.
- **Proposed wording** (Part 3, Collect demand evidence):

  > Rank demand only on keywords that match the candidate definition. When only broader parent keywords are available, report them as context, mark candidate-specific demand unknown, and do not place the candidate in the ordinal demand ranking on that basis.

- **Retest:** rerun A1. Pass if the budget spreadsheet is shown as "candidate-specific demand unknown", not ranked first.

### G2 — "Do not assign 'Suitable'" is ambiguous

Gate 3 says not to assign "Suitable" when eligibility is unverified. The agent read this as forbidding only the plain "Suitable under recorded requirements" status, so it used "Suitable subject to conditions".

- **Proposed wording** (Part 1, gate 3), replacing the last sentence:

  > If those cannot be read at source, record Etsy eligibility as "unverified" separately from the halal status, and do not assign either Suitable status overall until eligibility is verified.

- **Retest:** rerun A1. Pass if the output shows the halal status and Etsy eligibility separately, and gives no overall Suitable status.

## Minor observations (no change proposed)

- The agent asked for about 5 screenshots per idea, against the skill's guide of about 20 listings across 10 shops, and did not flag the difference. This is a reasonable first ask, and the skill already treats the numbers as ranges.
- The agent gave a provisional pick at low confidence. This matches the skill's rule to "deliver the provisional shortlist and smallest useful validation step".
- Ramadan 2027 dates were taken from news sources and labelled as expected dates.

## Limits of this test

- One run with invented eRank figures.
- The agent is the same underlying model family as the reviewer.
- A pass shows the instruction is followed in this scenario. It does not show the research is commercially correct.
