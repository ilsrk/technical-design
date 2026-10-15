# Change topic

Change to an existing queue topic.

## Structure

| Field      | Description                          | Required | Type       |
| ---------- | ------------------------------------ | -------- | ---------- |
| Name       | Topic name                           | true     | string     |
| Driver     | Queue driver                         | true     | enum       |
| As is      | Current topic state                  | true     | text       |
| To be      | Target topic state                   | true     | text       |
| Changes    | List of planned changes              | true     | text       |
| Reason     | Why the change is needed             | true     | text       |
| Rationale  | Justification for the chosen approach| true     | text       |
| Comments   | User comments                        | false    | text       |
