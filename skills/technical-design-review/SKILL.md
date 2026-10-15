---
name: technical-design-review
description: >-
  Critical review of a technical design or solution card against requirements.
  Use when reviewing a technical design, checking that solutions meet
  requirements, or writing an AI review into the Reviews component.
---

# Technical design review

## Purpose

- Check that chosen solutions actually satisfy the stated requirements.
- Surface gaps, weak rationale, and unresolved uncertainty before realize or export.
- Record an independent AI review in the `Reviews` component.

## When to use

- User asks to review a technical design, a section, or a solution card.
- After `validate`, before `realize` or export via `technical-design-converter`.
- `technical-design` routes review work here (no separate review process).

## Required inputs

Collect before starting. Do not invent defaults.

| Input | Description |
| ----- | ----------- |
| Review target | Path or link to the technical design card, or to a single solution card |
| Scope | `full` (entire design) or `solution` (one solution card / node) |

If either input is missing, ask the user and stop until provided.

## Steps

1. Determine the review scope (an individual solution or the entire technical design) and resolve the review target.
2. Find the `Reviews` component in the review target (Support section, or the target’s own Reviews component).
3. Read only what is needed for this review:
   - Requirements that apply to the target
   - Solution nodes / solution cards in scope
   - Related open questions (if present)
4. Perform the review using the checklist below. Apply critical thinking throughout.
5. Record the review in the `Reviews` component, authored by AI: append one new row. Do not edit existing rows.
6. Summarize the outcome for the user (verdict + key findings). Do not paste other authors’ reviews.

## Review checklist

Evaluate each item. Mark as pass, fail, or not applicable. Failures must appear in the Review text.

### Requirements coverage

- [ ] Every in-scope requirement is addressed by at least one solution (cite requirement ID + title).
- [ ] No accepted option contradicts a higher-priority requirement.
- [ ] Team-added constraints are treated as lower priority than task requirements.

### Solution quality

- [ ] Each solution node has Selected solution filled (option ID + short description) and explicit rationale on the solution card.
- [ ] Rejected options have reasons, not silence.
- [ ] Evaluations refer to requirements by ID, not vague claims.
- [ ] Chosen options are implementable given the documented context and artifacts.

### Completeness and risk

- [ ] Critical open questions that block the solution are flagged (or none remain).
- [ ] Missing sections that the target requires are called out.
- [ ] External links cited as evidence are reachable; note broken links.

### Independence

- [ ] Conclusions follow from your own reading of the design, not from agreement with the author by default.

## Recording the review

Write a new entry in the `Reviews` component:

| Field | Value |
| ----- | ----- |
| Author | Name and version of the model used for this review |
| Review | Verdict and findings (see format below) |
| Comments | Comma-separated list of skills used when writing the review (include `technical-design-review`) |

### Review field format

```markdown
Verdict: Approve | Approve with comments | Request changes

Findings:
- [Critical] <finding> — refs: <requirement IDs / solution node IDs>
- [Major] ...
- [Minor] ...

Coverage: <N>/<M> in-scope requirements addressed
```

Severity:

- **Critical** — blocks realize/export; requirement unmet or contradiction.
- **Major** — weak rationale, missing evaluation, or material gap.
- **Minor** — clarity, wording, or non-blocking incompleteness.

## Hard constraints

- **NEVER** read reviews by other authors. Your review must not mention or reference other authors’ reviews or any other reviews outside the subject being reviewed.
- **ALWAYS** approach every review through the lens of critical thinking.
- **NEVER** agree with the author unless your own reasoning supports their position.
- **NEVER** fill or modify user `Comments` fields on other components.
- **NEVER** modify design content during review except appending to `Reviews`.
- **NEVER** write implementation code.

## Soft constraints

- Prefer short findings with concrete references over long essays.
- If scope is `full`, review section-by-section; if `solution`, stay inside that card and its linked requirements.

## Outputs

- Updated `Reviews` component on the review target
- Short user-facing summary: verdict, critical/major counts, next suggested action (`edit`, `continue`, `realize`, or `technical-design-converter`)

## Related

- Format specs: `technical-design` (components, sections, roots) — especially `Reviews`
- Sibling: `technical-design-converter` (format import/export — not used during review)
