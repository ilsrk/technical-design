---
name: technical-design-requirements
description: >-
  Gather and record requirements for a technical design through dialogue.
  Propose requirement drafts, confirm with the user, and write them into
  Requirements registers. Use when gathering requirements, filling the
  Requirements section, eliciting FR/NFR/constraints/assumptions, or when
  technical-design continue reaches requirements.
---

# Technical design requirements

## Purpose

- Elicit requirements for the problem through dialogue with the user.
- Propose clear, testable requirement drafts and record confirmed ones.
- Keep each requirement type in its own Requirements register.

## Inputs

Collect before starting. Do not invent defaults.

## Requirement structure

### Types (each type → its own Requirements register)

| Type | Prefix | What it captures | Priority default |
| ---- | ------ | ---------------- | ---------------- |
| Functional | `FR` | Observable behavior the solution must provide | task (high) |
| Non-functional | `NFR` | Quality attributes: performance, reliability, security, scale, UX limits | task (high) |
| Constraint | `CR` | Hard boundary that options must respect (tech, process, legal, deadline) | task (high) unless user marks team |
| Assumption | `AR` | Taken as true for design; risks if false | team (low) unless user marks task |

### ID scheme

`{PREFIX}-{NNN}` — zero-padded, per-type sequence in that register.

Examples: `FR-001`, `NFR-002`, `CR-001`, `AR-003`.

### Quality bar (every proposed requirement)

- Atomic: one obligation per ID.
- Testable: can be checked pass/fail without inventing a solution.
- Solution-free: states *what*, not *how* (no “use Kafka”, unless it is a Constraint).
- Named by ID + title whenever referenced later.

## Steps

1. Resolve the design target and confirm Basic Information exists (Context at least). If Basic Information is empty, ask the user to complete it via `continue` first, then stop.
2. Read existing Requirements registers. Do not invent IDs that collide.
3. Run the dialogue loop (mode `gather`) or a single proposal batch (mode `add`):

   **Propose**
   - Ask one focused question about the problem (goals, actors, must-haves, limits, unknowns).
   - From the user’s answer, draft 1–5 candidate requirements (type, source, Title, Description; Details only if needed).
   - Show candidates as a numbered list with proposed IDs.

   **Confirm**
   - User accepts, edits, rejects, or reclassifies (type/source).
   - Do not write rejected candidates.
   - Unclear items → Open Questions (if that component exists), not fake requirements.

   **Record**
   - Append accepted rows to the matching type’s Requirements register.
   - Never rewrite accepted requirements unless the user explicitly asks to edit them (then use `edit` / explicit revise).

4. Ask whether to continue gathering or finish.
   - Continue → next propose round.
   - Finish → require at least one requirement across all registers.

## Dialogue rules

- **Dialogue only**: do not mine Artifacts, external docs, or the codebase for requirements. The user may paste text into chat; treat that as dialogue input.
- **Propose and record**: always propose before writing; write only after explicit acceptance (or clear “yes / add all / save”).
- Prefer small batches over long dumps.
- Prefer questions that reduce uncertainty (actors, success criteria, hard limits) over open brainstorming.
- If the user states a solution (“we will use Redis”), either:
  - rephrase as a Constraint if they insist it is mandatory, or
  - capture the underlying need as FR/NFR and note the tech choice as optional context in Details — ask which they mean.

## Hard constraints

- **NEVER** write implementation or design solution content into requirements.
- **NEVER** read Artifacts or external sources to invent requirements (dialogue only).
- **NEVER** record a requirement without user confirmation.
- **NEVER** put two types in one register — one register per type.
- **NEVER** modify sections outside Requirements (and State Machine status for that section) during this skill.
- **ALWAYS** use the ID scheme and cite ID + title when referring to requirements.

## Soft constraints

- Keep Title/Description concise; put nuance in Details.
- Use English for IDs and file/register names; requirement prose may follow the user’s language.
- Snake_case English names if creating new register files.

## Outputs

- Updated Requirements register(s) on the design target
- Short summary: counts per type (`FR` / `NFR` / `CR` / `AR`), source mix, open questions filed (if any)
- Suggested next action (`continue`, `edit`, or `validate`)
