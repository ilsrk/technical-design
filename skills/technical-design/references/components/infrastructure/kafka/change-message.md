# Change message

Change to an existing Kafka message.

## Structure

| Field      | Description                          | Required | Type   |
| ---------- | ------------------------------------ | -------- | ------ |
| Topic      | Topic name                           | true     | string |
| Message    | Message identifier or name           | true     | string |
| As is      | Current message state                | true     | text   |
| To be      | Target message state                 | true     | text   |
| Changes    | List of planned changes              | true     | text   |
| Reason     | Why the change is needed             | true     | text   |
| Rationale  | Justification for the chosen approach| true     | text   |
| Comments   | User comments                        | false    | text   |
