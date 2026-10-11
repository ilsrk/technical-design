# Decision nodes

A tabular list of decisions made, with links to the corresponding decision records.

## Structure

| Field       | Description                                      | Required |
| ----------- | ------------------------------------------------ | -------- |
| ID          | A unique decision node identifier                | true     |
| Title       | Decision node title                              | true     |
| Status      | Current decision status                          | true     |
| Link        | Link to the corresponding solution card          | true     |
| Comments    | User comments                                    | false    |

## Hard constraints

- Each decision node **MUST** reference a solution card.
