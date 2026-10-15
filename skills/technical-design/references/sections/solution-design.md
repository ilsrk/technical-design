# Solution design

Main section for solution design.

## Components

| Component           | Required |
| ------------------- | -------- |
| `Solution variants` | true     |

## Conventions

- Each solution variant must be considered separately.

## Hard constraints

- Variant details **MUST** use a type from [`references/variants`](../variants/). Do not invent variant structure outside those types.
- The section is complete only when one variant has Status `Selected` with recorded reasons for the choice, and every other variant has Status `Rejected` with recorded rejection reasons.
- If Solution variants contains no variants, the section **MUST NOT** be considered complete.

