# Solution variants

A tabular list of solution variants for a solution node. Each row links to a Solution variant details document. Type selects which extra components that document adds on top of the Solution variant base set.

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
- Type selects extra components from the Solution variant types list in the skill. The details document always includes the Solution variant base components, plus the type's components.

## Soft constraints

- Place variant details in the same file as this register. Split variants into separate files only when the user asks to decompose the solutions. In that case Link points to the separate details document; otherwise Link is an in-file anchor.

## Hard constraints

- Each variant **MUST** have a unique ID.
- Duplicate variants are not allowed.
- There can be only one variant with Status `Selected`.
- A newly added variant **MUST** have Status `Candidate`.
- Each variant **MUST** have a Type.
- The variant details document **MUST** follow the Solution variant component and the chosen Type.
