# Solution variant

Details document for a single solution variant. Linked from a row in Solution variants.

## Components

| Component        | Required |
| ---------------- | -------- |
| `Context`        | true     |
| `Open Questions` | false    |
| `State machine`  | true     |

## Conventions

- Base components above are always present on every solution variant.
- Additional components come from the variant Type in [`references/variants`](../variants/). Add only those components that the chosen type defines.

## Hard constraints

- Every solution variant **MUST** include all required base components.
- Type-specific components **MUST** come from the matching type in [`references/variants`](../variants/).
