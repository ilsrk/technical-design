# Solution nodes

A tabular list of solution nodes, with links to the corresponding solution cards and the selected option after card design is complete.

## Structure

| Field                    | Description                                                                 | Required |
| ------------------------ | --------------------------------------------------------------------------- | -------- |
| ID                       | A unique solution node identifier                                           | true     |
| Title                    | Solution node title                                                         | true     |
| Subject                  | Essence of the decision to be made                                          | true     |
| Status                   | Current solution status                                                     | true     |
| Link                     | Link to the corresponding solution card                                     | true     |
| Selected solution        | ID and short description of the chosen option                               | true     |
| Related solutions        | Links to related solution nodes                                             | false    |
| Comments                 | User comments                                                               | false    |

## Conventions

- In Subject, keep only the shortest possible statement of the decision essence.
- Fill Selected solution only after the solution card design is complete: record the chosen option ID and a short description (for example, `OPT-2: Store sessions in Redis`).
- Leave Selected solution empty while the solution card is still in progress.

## Hard constraints

- Each solution node **MUST** reference a solution card.
- When a solution card is marked complete, Selected solution **MUST** contain the chosen option ID and a short description.
