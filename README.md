# Coverage matrix — Delegation for Agentic AI in OAuth-Based Architectures

Companion data for the Internet-Draft **draft-cea-list-vaultys-oauth-agent-deleg-reqs-gaps**
(*Delegation for Agentic AI in OAuth-Based Architectures: Requirements and Gap Analysis*).

The draft states 15 architectural requirements (R0–R14), refined into 111 sub-requirements, that a
delegation model for agentic AI systems must satisfy, and evaluates each sub-requirement against
41 mechanisms: 18 published RFCs, 11 Internet-Drafts and 12 non-IETF specifications included as
informative prior art. This repository holds the full evaluation: one verdict per (sub-requirement,
mechanism) pair, with the verbatim quotation and section reference supporting every positive verdict.

* `coverage-matrix.xlsx` — the matrix (12 sheets, described below).
* `csv/` — one CSV per sheet, for diffing and scripting.
* `CHANGELOG.md` — version history.

Tags: each tag named after a draft revision (`draft-00`, `draft-01`, …) is the exact matrix cited by
that revision. The draft cites the tag URL, never a branch. Each tag is also archived on Zenodo with a DOI.

## How to read the symbols

**Published RFCs (normative baseline)**

| Symbol | Meaning |
|---|---|
| ✓ | Covered — a published RFC defines the property with normative language (MUST/SHALL) |
| ◐ | Partial — a published RFC addresses the property in part, or only informatively |
| ✗ | RFC gap — no published RFC defines the property |

**Internet-Drafts (non-normative — RFC adoption required)**

| Symbol | Meaning |
|---|---|
| ◉ | Draft-complete — the draft defines the property with normative language and fully covers it |
| ◑ | Draft-partial — the draft addresses the property in part or only informatively |
| – | Not covered |

**Prior art / non-IETF (informative only)**

| Symbol | Meaning |
|---|---|
| ● | Full (informative) |
| ◐ | Partial (informative) |
| – | Not covered |

**Combined coverage (column J of "Full Coverage")** — computed from the three families: RFC ✓ → Covered;
RFC ◐ → Partial (◑·◉ when a draft is complete); RFC ✗ with a complete draft → Draft-complete; with a partial
draft → Draft-partial; with prior art only → Partial (informative); otherwise → Unaddressed in the evaluated corpus.

**Requirement-level symbol (sheet "Coverage Matrix")** — a mechanism is *full* on a requirement only if at
least half of its sub-requirements are full and none is uncovered; *partial* if at least one sub-requirement
is credited; otherwise not covered.

## Evaluation rules

1. One verdict per (sub-requirement, mechanism). Every positive verdict carries at least one section
   reference and one verbatim quotation (10–60 words) that can be found by text search in the cited version.
2. No inference: only what the text says is credited. Delegation to another specification is not coverage.
3. Sub-requirements about multi-hop chains need text about depth ≥ 2.
4. R13 concerns human oversight *during* execution, not consent at authorization time.
5. A security consideration that merely warns about a risk earns at most a partial symbol.
6. Each mechanism is evaluated at one frozen version, stated in sheet "Coverage Matrix" (row 5) and in
   the draft's Table 6-1. Newer revisions are not evaluated until the next matrix tag.

## Sheets

| Sheet | Content |
|---|---|
| Coverage Matrix | 15 requirements × 41 mechanisms, requirement-level symbols; row 5 gives the frozen version of each mechanism |
| Sub-Req Coverage | 111 sub-requirements, RFC-only baseline: covering RFC(s), symbol, justification |
| Sub-Req Summary / Gap Summary | RFC-only counts per requirement; for each requirement, which sub-requirements are RFC gaps |
| ✗ Gaps Only | the 48 sub-requirements with no RFC coverage |
| Full Coverage (All Mechs) | 111 sub-requirements × three families: RFC, drafts, prior art, combined verdict, remaining gap, primary/derived nature, corroboration columns |
| Full Sub-Req Summary (All) / Full Gap Summary (All) | counts per requirement across the three families |
| ✗ True Gaps (All Mechs) | sub-requirements unaddressed by any evaluated mechanism (none at this tag) |
| Scores (long) | one row per positive (sub-requirement, mechanism) verdict — plus all 41 verdicts for the two rows added last (R6.9, R10.6) — with section, rationale and verbatim quotation. This is the evidence behind every verdict. |
| Justifications | one paragraph per (requirement, mechanism) pair summarizing its requirement-level symbol (615 rows) |
| C8 Corroboration | for each RFC gap, how many mechanisms independent of the two AIP drafts cover it (fragile / limited / corroborated) |

## Headline figures at tag `draft-00`

* 111 sub-requirements; 41 mechanisms.
* RFC-only baseline: 39 covered, 24 partial, **48 RFC gaps (43 %)**.
* Of the 48 RFC gaps: 33 have Draft-complete coverage, 13 Draft-partial, 2 prior-art only; 0 unaddressed.
* Corroboration of the 48 gaps: 10 fragile (AIP drafts only), 6 limited (one independent mechanism), 32 corroborated.

## Method and limits

Every positive verdict was checked against the source text of the frozen version; quotations were
verified mechanically. Known limitations are listed in `CHANGELOG.md`. Corrections are welcome as issues or pull requests; a correction
accepted after a tag is published appears in the next tag and in the next draft revision, never by
rewriting a published tag.

## Citation

Abdallah, R., Thoorens, F.-X., Boitier, W., Williamson, J., Souihi, S. *Coverage matrix for
draft-cea-list-vaultys-oauth-agent-deleg-reqs-gaps-00*, tag `draft-00`, 2026. DOI: 10.5281/zenodo.24530432

## License

The matrix and its exports are released under the Creative Commons Attribution 4.0 International
license (CC BY 4.0). Quotations from RFCs, Internet-Drafts and third-party specifications remain the
property of their authors and are reproduced for the purpose of citation.
