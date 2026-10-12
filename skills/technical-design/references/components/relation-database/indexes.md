# Indexes

List of indexes to be designed.

## Structure

| Field       | Description                         | Required |
| ----------- | ----------------------------------- | -------- |
| Name        | Index name                          | true     |
| Table       | Target table name                   | true     |
| Columns     | Indexed columns                     | true     |
| Type        | Index type (btree, hash, gin, etc.) | false    |
| Unique      | Whether the index is unique         | false    |
| Comments    | User comments                       | false    |
