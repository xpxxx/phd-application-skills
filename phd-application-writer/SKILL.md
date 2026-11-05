---
name: phd-application-writer
description: Generate or revise evidence-grounded PhD application documents as Overleaf/LaTeX projects after preparation is complete. Use for a CV, research proposal or statement, motivation/application letter, or related submission document when a phd-application-prep fact bank or target brief is available. Requires applicant confirmation before drafting, uses academic-humanizer where appropriate, and compiles and checks the LaTeX output. Do not use for initial evidence collection or target verification.
---

# PhD Application Writer

Create target-specific application documents from an audited evidence base without filling gaps by assumption. Treat the applicant's confirmation as part of authorship, not as a final proofreading step.

## Required upstream material

Use the outputs of `phd-application-prep`: the relevant fact bank, target brief, gap audit, and evidence handoff when present. Read source records only to verify a locator or resolve an inconsistency; do not silently rebuild or override the preparation audit.

If the preparation artifacts are absent, materially stale, or labeled **Not ready**, invoke `phd-application-prep` first. Finish or update the relevant preparation artifacts before starting this workflow.

## Mandatory confirmation gate

Before generating submission prose, read [references/confirmation-gate.md](references/confirmation-gate.md) and apply it. The gate is mandatory for:

- unresolved `conflicting` or consequential `unknown` items;
- `user-stated` claims selected for prominent use when ownership, dates, metrics, publication status, or role boundaries lack documentary support;
- personal motivation, reasons for choosing the target or direction, career goals, and explanations of sensitive timelines;
- the proposed positioning, narrative route, omissions, and disclosure choices;
- any interpretation that could be mistaken for a biographical fact.

Ask focused questions in small batches and explain what each answer unlocks. Do not draft around a missing answer by inventing a plausible bridge. If the applicant declines to confirm an item, omit it, qualify it transparently, or retain a visible placeholder in a review draft. Never place placeholders in a document presented as final.

Persist confirmed decisions in a target-specific decision log so later revisions do not ask the same question again without cause.

## Document mode

After the confirmation gate passes, read the relevant section of [references/document-playbooks.md](references/document-playbooks.md):

- CV or academic CV;
- research proposal, research statement, or statement of research interests;
- application, motivation, or cover letter.

Respect the target's actual requested document type. Do not turn a motivation letter into an unsolicited research proposal or present proposed work as completed experience.

## Overleaf-first authoring

All submission documents produced by this skill must be authored as Overleaf-compatible LaTeX projects. Before creating or editing a project, read [references/overleaf-workflow.md](references/overleaf-workflow.md).

- Prefer the applicant's existing Overleaf project or approved template. Do not select a CV, letter, or proposal design without confirmation.
- Use one Overleaf project per deliverable by default because CVs, letters, and proposals normally require different document classes and independent compilation. Combine them only when the applicant explicitly prefers that structure.
- Keep the auditable local `.tex`, bibliography, and asset sources in the application workspace even when editing through the Overleaf browser.
- Keep internal fact IDs, claim maps, decision logs, and review notes outside the uploadable Overleaf project.
- Compile after substantive edits and inspect the PDF for layout, overflow, missing references, font problems, page limits, and accidental exposure of internal notes.
- Do not create an Overleaf project, upload files, replace an existing project, use Git credentials, or push changes until the intended account and project are confirmed.

## Evidence-bound drafting

1. Build a private claim plan from approved fact IDs, target facts, and confirmed decisions.
2. Draft for the requested reader, length, language, and format. Keep claims at or below their approved `safe wording`.
3. Separate personal contribution from team outcomes and prior results from future plans.
4. Preserve exact dates, numbers, names, publication states, citations, and qualifications.
5. Create or update a claim map beside the draft. The clean submission document must not contain internal fact IDs.
6. When revising an existing document, audit every newly introduced or strengthened claim; prior polished wording is not evidence.

## Academic-humanizer integration

Load and follow `academic-humanizer` after the evidence-bound draft exists, not before.

- For research proposals, research statements, and technical research narratives, apply its full applicable academic/proposal workflow: audit first, then rewrite, then report changes.
- For CVs and personal application letters, do not impose paper-style third-person or funding-proposal conventions. Use only the compatible safeguards: claim-evidence discipline, removal of unsupported hype and generic AI phrasing, concise sentence structure, and author/venue voice matching.
- If an authentic applicant writing sample is available, use it only for voice characteristics, never as independent factual proof.
- After humanization, compare the text against the claim plan. Reject any new fact, stronger verb, altered number, changed citation, invented motivation, or erased qualification.
- Never use humanization to evade an AI-use disclosure requirement. Prepare the disclosure from the actual workflow when the target requests one.

## Output and validation

Keep source files untouched. Store drafts and their sidecar audit files in the user's chosen workspace. Before calling a document final, read [references/final-quality-gates.md](references/final-quality-gates.md).

Return:

- the requested clean document or revision;
- a concise change report;
- unresolved items that were omitted or left for the applicant;
- confirmation that every consequential claim is traceable and that humanization did not alter facts, numbers, citations, or publication status.

The default final package is the Overleaf-compatible LaTeX source plus its compiled PDF and sidecar claim map. Produce `.docx` only when a target explicitly requires it or the applicant separately requests an export.
