# New topic

New queue topic design.

## Structure

| Field          | Description                          | Required | Type       |
| -------------- | ------------------------------------ | -------- | ---------- |
| Name           | Topic name                           | true     | string     |
| Driver         | Queue driver                         | true     | enum       |
| Partitions     | Number of partitions                 | true     | number     |
| Partition key  | Key used to route messages           | true     | string     |
| Producers      | Services that produce to the topic   | true     | list       |
| Consumers      | Services that consume from the topic | true     | list       |
| Comments       | User comments                        | false    | text       |
