# Overleaf workflow

Use this workflow only after the evidence and applicant-confirmation gate has passed for the relevant content. Account access does not replace factual approval.

## Choose an access mode

### Browser mode

Use browser mode when the applicant has a normal Overleaf account, wants to work directly in the web editor, or does not have Git integration.

1. Ask the applicant to identify the intended project or approve creation of a new project.
2. Open Overleaf in the Codex built-in browser, or use an applicant-provided Chrome tab when the existing Chrome login session is needed.
3. The applicant signs in and completes passwords, passkeys, CAPTCHA, and multi-factor authentication personally. Never ask for credentials in chat and never record them in project files.
4. Confirm the visible account and project title before editing.
5. Preserve the existing template and unrelated project content. Preview broad replacements before applying them.
6. Compile in Overleaf after substantive edits. Download or otherwise preserve the final `.tex` project and PDF in the local application workspace when permitted.

Browser login is a website session, not a permanent connected-app authorization. The built-in browser has its own cookies and login state; an applicant's existing Chrome session requires the browser extension or a shared Chrome tab.

### Git integration mode

Use Git mode only when the applicant has access to Overleaf Git integration and provides the intended project URL. Overleaf Cloud Git integration may require a premium entitlement.

1. Confirm the exact project and local destination before cloning.
2. Use the project's Overleaf Git URL. Never embed a token in the remote URL, shell history, `.git/config`, a skill file, or the conversation.
3. The applicant creates the Overleaf Git authentication token and enters it only through the credential prompt or an appropriate system credential manager.
4. Pull and inspect the current project before editing. Preserve unrelated changes and do not overwrite an active collaborator's work.
5. Keep local commits scoped to the requested document changes. Do not rewrite remote history, force-push, create unsupported branch workflows, or assume that Overleaf comments and tracked changes will survive Git operations.
6. Show the compiled result and change summary before the first push or any push that materially replaces existing content. Push only to the confirmed Overleaf remote.
7. Pull again before a later push when collaborators may have edited the online project.

## Project structure

Adapt an existing project rather than reorganizing it without need. For a new project, use the smallest structure that fits:

```text
main.tex
sections/          optional for a longer RP
references.bib     only when citations are required
assets/            only applicant-approved figures or marks
```

Do not upload:

- fact banks, gap audits, decision logs, or claim maps;
- source certificates, transcripts, identity records, or unrelated application files;
- temporary renders, extracted text, credentials, or hidden review notes.

Store audit material beside, not inside, the Overleaf source directory. A conventional local layout is:

```text
application-writing/<target>/
|-- decision-log.md
|-- claim-maps/
`-- overleaf/
    |-- cv/
    |-- motivation-letter/
    `-- research-proposal/
```

Create only the deliverables the target requests.

## Template confirmation

Before inserting prose into a new project, show or describe the proposed template choices that affect content: document class, page size, margins, typography, section order, bibliography style, and whether a photo or personal fields are present. The applicant must approve choices that are not dictated by the target.

Do not use a decorative or ATS-hostile CV template merely because it is available on Overleaf. Do not add a photo, birth date, nationality, marital status, signature image, or other personal field unless the applicant explicitly requests it and it is appropriate for the target.

## Compilation and verification

After substantive revisions:

1. Compile with the project's intended engine and resolve actual errors.
2. Check missing citations/references, overfull boxes, clipped content, blank pages, incorrect glyphs, and unexpected font substitution.
3. Confirm the final page count and target limits.
4. Render and visually inspect every page of the final PDF.
5. Verify that PDF text is selectable/searchable unless the template necessarily contains an image element.
6. Ensure the PDF and `.tex` contain no internal evidence labels, comments, credentials, placeholders, or hidden instructions.
7. Keep the local source synchronized with the version delivered through Overleaf.

## Stopping conditions

Stop and ask the applicant when:

- the browser is signed into the wrong account;
- the project or template is ambiguous;
- a login, CAPTCHA, passkey, or multi-factor challenge appears;
- an upload, synchronization, or push would overwrite material not created in this workflow;
- the Overleaf project contains collaborator changes that conflict with the local draft;
- compilation requires changing content, claims, citations, or layout decisions beyond the approved scope.
