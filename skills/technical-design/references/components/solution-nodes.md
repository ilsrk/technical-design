# Solution nodes

A tabular list of solutions made, with links to the corresponding solution records.

## Structure

| Field                    | Description                             | Required |
| ------------------------ | --------------------------------------- | -------- |
| ID                       | A unique solution node identifier       | true     |
| Title                    | Solution node title                     | true     |
| Subject                  | Essence of the decision to be made      | true     |
| Status                   | Current solution status                 | true     |
| Link                     | Link to the corresponding solution card | true     |
| Related solutions        | Links to related solution nodes         | false    |
| Comments                 | User comments                           | false    |

## Conventions

- In Subject, keep only the shortest possible statement of the decision essence.

## Hard constraints

- Each solution node **MUST** reference a solution card.
