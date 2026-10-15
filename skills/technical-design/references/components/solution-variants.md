# Solution variants

A tabular list of solution variants for a solution node. Each variant has a type that defines which components its details document contains.

## Structure

| Field    | Description                              | Required |
| -------- | ---------------------------------------- | -------- |
| ID       | A unique solution variant identifier     | true     |
| Title    | Solution variant title                   | true     |
| Type     | Variant type (defines component set)     | true     |
| Status   | Current variant status                   | true     |
| Link     | Link to the variant details document     | true     |
| Comments | User comments                            | false    |

## Conventions

- Status is one of: `Selected`, `Candidate`, `Rejected`.
- New variants default to `Candidate`.
- `Selected` is set only when the user asks to choose and finalize a solution. Once this is done, the solution card is considered complete.
- `Candidate` marks variants still being evaluated.
- `Rejected` marks variants that were considered and declined.
- Type selects the variant definition from the Solution variant types list in the skill. The variant details document **MUST** follow that type's component set.
- If no listed type fits the problem, ask the user which components the variant needs and record them in the variant details document.

## Hard constraints

- Each variant **MUST** have a unique ID.
- Duplicate variants are not allowed.
- There can be only one variant with Status `Selected`.
- A newly added variant **MUST** have Status `Candidate`.
- Each variant **MUST** have a Type.
- The variant details document **MUST** include only components allowed by its Type (or by the user when no type fits).
