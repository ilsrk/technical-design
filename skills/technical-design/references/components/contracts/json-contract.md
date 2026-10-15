# JSON contract

JSON payload contract as JSON Schema.

## Structure

| Field    | Description                                              | Required | Type   |
| -------- | -------------------------------------------------------- | -------- | ------ |
| Title    | Contract name                                            | true     | string |
| Schema   | JSON Schema document (embedded fenced `json`)            | true     | json   |
| Example  | Example JSON payload matching the schema                 | false    | json   |
| Comments | User comments                                            | false    | text   |

## Conventions

- Set `$schema` to `https://json-schema.org/draft/2020-12/schema`.
- Write the full schema in a fenced `json` block under the Schema section.
- If Example is filled, it must be a valid payload for that schema.
