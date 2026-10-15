# Migration plan

Steps and strategy for moving from the current state to the target state.

## Structure

| Field    | Description                                       | Required | Type |
| -------- | ------------------------------------------------- | -------- | ---- |
| Strategy | Migration strategy (incremental, strangler, etc.) | true     | text |
| Steps    | Ordered migration steps                           | true     | text |
| Rollback | Rollback approach if something goes wrong         | true     | text |
| Risks    | Key risks and mitigations                         | true     | text |
| Comments | User comments                                     | false    | text |
