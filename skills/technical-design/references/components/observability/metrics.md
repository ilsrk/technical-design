# Metrics

Monitoring metrics collected for the designed solution.

## Validation

Valid metric types: counter, histogram, gauge, log

## Structure

| Field      | Description                        | Required |
| ---------- | ---------------------------------- | -------- |
| Name       | Metric name                        | true     |
| Group      | Metric group name                  | false    |
| ID         | Metric ID in the logs              | true     |
| Type       | Metric type                        | true     |
| Attributes | Metric additional attributes       | false    |
| Trigger    | What triggers the metric?          | true     |
| Source     | Where the metric is collected from | true     |
| Comments   | User comments                      | false    |
