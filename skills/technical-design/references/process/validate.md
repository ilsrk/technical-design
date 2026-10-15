# Validate technical design

## Steps

1. Open the State machine component on the validation object (design card or solution card).
2. Determine which sections and components should be reviewed from the card's section list and each section's component list.
3. Run the checks below. Apply [`technical-design-writer`](../../../technical-design-writer/SKILL.md) when reviewing prose in component fields.
4. Prompt the user to fix the errors. Do not invent fixes for solutions, variants, or selected decisions.

## Checklist

### Structure and completeness

- [ ] Every required section on the card is present.
- [ ] Every required component inside each present section is present.
- [ ] Required fields in each component Structure table are filled.
- [ ] Comment fields were not filled or modified by the agent.
- [ ] Skipped sections have a skip reason in the State machine Reason field.

### Solution nodes and variants

- [ ] Each Solution nodes row that claims a completed card has a reachable Link and a filled Selected solution (chosen variant ID and short description).
- [ ] Each solution card has Solution variants with at least one variant.
- [ ] Exactly one variant has Status `Selected` when the card is complete; every other variant has Status `Rejected`.
- [ ] Each variant has a Type from Solution variant types in the skill.
- [ ] Each variant details document includes all required base Solution variant components plus all required components of its Type.
- [ ] Selected and Rejected rows have recorded reasons for the choice or rejection.

### Links and references

- [ ] Markdown links use `[text](URL)` and resolve to existing paths or reachable URLs.
- [ ] Requirement references include requirement ID and title.
- [ ] Artifacts link only to AS IS schemas and solutions already in a release; no TO BE or not-yet-released designed solutions.

### Wording

- [ ] Prose in component fields passes the technical-design-writer checklist (no banned dashes, clipped slogan stacks, or boilerplate shell).

## Outputs

- Validation results: a brief summary if everything is valid; otherwise a list of errors with file path and what failed.
