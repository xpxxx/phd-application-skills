# Application preparation artifact schema

Read this reference when creating an inventory, fact bank, gap audit, target brief, or evidence handoff. Adapt the fields to the task; do not create empty tables merely to satisfy the schema.

## Recommended artifact set

```text
application-prep/
|-- source-inventory.md
|-- fact-bank.md
|-- gap-audit.md
|-- targets/
|   `-- <institution-or-position>.md
`-- handoffs/
    `-- <institution>-<document>.md
```

The location and filenames are conventions, not requirements. Preserve an existing project structure when one already exists.

## Status vocabulary

| Status | Meaning | Permitted use |
|---|---|---|
| `verified` | Supported by a supplied primary record or authoritative external source | May appear as fact |
| `user-stated` | Explicitly supplied by the applicant but not independently documented | May appear with care; retain provenance |
| `inferred` | Reasonable interpretation derived from evidence | Use as analysis, not biography |
| `conflicting` | Two or more sources disagree | Do not draft until resolved or transparently qualified |
| `unknown` | Needed information is absent | Ask or omit |

## Source inventory

For each item capture:

| Field | Guidance |
|---|---|
| `source_id` | Stable short ID such as `SRC-CV-01` |
| `path_or_url` | Exact local path or authoritative URL |
| `type` | Transcript, CV, letter, certificate, paper, code, report, webpage, etc. |
| `version_or_date` | Visible date, revision, or `unknown` |
| `originality` | Original, derived extract, render, summary, or earlier draft |
| `coverage` | Facts this item can support |
| `limitations` | Missing pages, OCR errors, self-authored claim source, stale content, etc. |

## Fact bank

Use atomic rows. One row should normally support one independently editable claim.

| Field | Guidance |
|---|---|
| `fact_id` | Stable ID such as `EDU-03` or `EXP-YORK-07` |
| `claim` | Minimal factual statement |
| `status` | One label from the status vocabulary |
| `source_locator` | `source_id` plus page, section, line, cell, commit, or URL |
| `confidence` | High, medium, or low; explain non-high ratings |
| `personal_contribution` | What the applicant personally did, if relevant |
| `outcome` | Output or result, kept separate from contribution |
| `safe_wording` | Strongest wording the evidence supports |
| `risk_or_conflict` | Exaggeration, ambiguity, privacy, timeline, attribution, etc. |
| `relevant_to` | CV, RP, letter, statement, interview, eligibility, or multiple |

## Gap audit

Prioritize rather than merely list.

| Field | Guidance |
|---|---|
| `priority` | Blocking, high, medium, or low |
| `gap` | Missing fact, document, verification, explanation, or decision |
| `why_it_matters` | Eligibility, credibility, fit, narrative, or formatting consequence |
| `needed_evidence` | Exact record or answer that resolves it |
| `owner` | Applicant, referee, institution, or researcher |
| `deadline` | Known date or `unknown` |
| `status` | Open, waiting, resolved, or intentionally omitted |

## Target brief

Record target facts before recommending a strategy:

- program, position, department, supervisor, funding model, deadline, and application route;
- binding eligibility and document requirements with authoritative sources and access dates;
- supervisor or project's current research themes, methods, and concrete recent work;
- criterion-to-evidence map;
- fit strengths, fit gaps, and disqualifying uncertainties;
- recommended narrative route and rejected routes with reasons;
- questions worth asking the program or supervisor.

Use this mapping vocabulary: `strong`, `partial`, `transferable`, `unsupported`, `uncertain`, `not applicable`.

## Evidence handoff

A handoff should give a separate writer enough verified material to begin without reopening every source, while remaining auditable:

1. Target and document constraints.
2. Candidate positioning for this target.
3. Intended reader takeaway.
4. Approved evidence blocks with fact IDs.
5. Suggested order and emphasis.
6. Keep / omit / verify / explain decisions.
7. Claims that must not appear.
8. Open questions.
9. Source locators.

Do not turn the handoff into prose for submission. Drafting remains outside this skill even if it is requested in the same conversation.
