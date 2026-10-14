# Solution nodes

A tabular list of solutions made, with links to the corresponding solution records.

## Structure

| Field       | Description                                      | Required |
| ----------- | ------------------------------------------------ | -------- |
| ID          | A unique solution node identifier                | true     |
| Title       | Solution node title                              | true     |
| Status      | Current solution status                          | true     |
| Link        | Link to the corresponding solution card          | true     |
| Comments    | User comments                                    | false    |

## Hard constraints

- Each solution node **MUST** reference a solution card.
