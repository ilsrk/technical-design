# New message

New queue message design.

## Structure

| Field             | Description                    | Required | Type   |
| ----------------- | ------------------------------ | -------- | ------ |
| Topic             | Target topic name              | true     | string |
| Message contract  | Message payload as [JSON contract](../../contracts/json-contract.md) | true     | link   |
| Comments          | User comments                  | false    | text   |
