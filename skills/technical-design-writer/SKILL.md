---
name: technical-design-writer
description: >-
  Writing rules for technical design prose: ban AI/machine-text patterns
  (em dashes, clipped phrases, boilerplate, empty contrasts, and similar).
  Use whenever drafting or editing text inside a technical design, solution
  card, requirements register, review, open question, or any component field.
  Also use when technical-design continue/edit/validate touches wording.
---

# Technical design writer

## Purpose

- Keep design prose readable for humans and reviewers.
- Stop the model from writing in machine-text patterns while filling components.

## Voice

- Prefer full sentences with a clear subject and verb.
- Be concrete: name the system, actor, constraint, or requirement ID.
- Prefer verbs over noun stacks.
- One idea per sentence when the sentence starts to nest clauses.

## Dash rule (strict)

1. Search the draft for `—`, `–`, and ` - `.
2. Keep only: numeric ranges (`NFR latency 50–100 ms`) and in-word hyphens.
3. Everywhere else rebuild the sentence without a dash.

Wrong: `The worker — a long-running consumer — owns retries.`
Right: `The worker is a long-running consumer and owns retries.`

## Phrase-length rule (strict)

Do not shorten phrases into machine staccato. Technical design text is for the team: keep grammar complete.

Wrong: `Auth via gateway. Tokens short-lived. Refresh separate.`
Right: `The gateway authenticates requests. Access tokens are short-lived. Refresh tokens are issued separately.`

Lists and tables remain lists and tables. Inside cells and bullets, still write readable clauses, not keyword debris.

## Allowed in this domain

- Requirement IDs (`FR-001`), file paths, API names, code identifiers.
- Tables, Mermaid, JSON Schema, and other structured blocks (style rules apply
  to surrounding prose, not to schema keys or diagram node ids).
- Honest uncertainty recorded as Open Questions, not as padded hedging.

## Checklist before saving prose

- [ ] No `—` / `–` / dash-like ` - ` outside ranges and hyphens
- [ ] No clipped slogan stacks or one-word sentence runs
- [ ] No boilerplate openers, formulaic closers, or chatbot shell
- [ ] Claims name actors, systems, or requirement IDs where possible
- [ ] Terms for one entity stay stable across the paragraph

## Hard constraints

- **NEVER** add machine-text patterns listed above when writing design prose.
- **NEVER** “polish” by inserting dashes, triplet slogans, or empty contrasts.
- **NEVER** change meaning, requirement IDs, or selected variants to satisfy style.
- **ALWAYS** rewrite a sentence that needs a dash instead of swapping in a hyphen.

## Outputs

- Prose that passes the checklist
- On validate: wording findings as concrete quotes + the ban they hit
