# Evidence-Bound PhD Application Skills

Two reusable Codex skills for preparing and writing PhD application materials without turning unsupported assumptions into polished claims.

The workflow separates evidence preparation from document drafting:

1. `phd-application-prep` inventories source material, verifies target requirements, builds a fact bank, audits gaps, and produces an evidence handoff.
2. `phd-application-writer` applies a mandatory applicant-confirmation gate, creates evidence-grounded application documents as Overleaf-compatible LaTeX projects, maintains claim maps, and verifies compiled PDFs.

## Why this workflow exists

Application writing systems can make uncertain or inferred details sound factual. These skills instead require:

- provenance and status labels for consequential claims;
- separation of personal contribution from team outcomes;
- explicit boundaries between completed, unpublished, ongoing, and proposed work;
- applicant confirmation for motivation, ownership, positioning, and disclosure choices;
- target-specific evidence mapping rather than keyword matching;
- auditable claim maps and decision logs outside the submission document;
- compilation and visual inspection of final LaTeX/PDF outputs.

## Repository structure

```text
phd-application-skills/
├── phd-application-prep/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/
└── phd-application-writer/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
```

## Installation

Clone this repository and copy the two skill directories into your Codex skills directory:

```bash
git clone https://github.com/xpxxx/phd-application-skills.git
cp -R phd-application-skills/phd-application-prep ~/.codex/skills/
cp -R phd-application-skills/phd-application-writer ~/.codex/skills/
```

Review every skill before installing it. The workflow is designed for Codex environments that support skills and local workspace files.

## Example use

Preparation:

```text
Use $phd-application-prep to verify this vacancy, inventory my records, and create a target-specific evidence handoff. Do not draft application prose yet.
```

Writing after preparation:

```text
Use $phd-application-writer to create a motivation letter from the approved evidence handoff. Ask me to confirm unresolved motivation and ownership claims before drafting.
```

## Human review and AI disclosure

These skills do not make an application automatically accurate. The applicant remains responsible for supplying records, resolving conflicts, reviewing every claim, complying with institutional AI-use policies, and approving the final submission.

The writer can integrate a separately installed academic-writing humanizer after an evidence-bound draft exists. No third-party humanizer is included in this repository.

## Privacy

Do not commit CVs, transcripts, certificates, recommendation letters, identity documents, fact banks, decision logs, credentials, or target-specific application artifacts to a public repository.

## License

MIT License. See [LICENSE](LICENSE).
