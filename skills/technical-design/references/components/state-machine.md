# State machine

A status model reflecting the current status of individual sections and the overall technical design status.

## Structure

| Field    | Description                          | Required |
| -------- | ------------------------------------ | -------- |
| Section  | Section name                         | true     |
| Status   | Current status value                 | true     |
| Reason   | Reason for the status change         | false    |
| Comments | User comments                        | false    |

## Conventions

- In Reason, record the reasons for status changes.

## Hard constraints

- If a section was skipped, it **MUST** have a skip reason in Reason.
