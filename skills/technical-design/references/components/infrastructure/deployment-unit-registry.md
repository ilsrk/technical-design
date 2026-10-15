# Deployment unit registry

Detailed description of the deployment unit

## Structure

| Field       | Description      | Required | Type              |
| ----------- | ---------------- | -------- | ----------------- |
| ID          | Unit ID          | true     | string            |
| Name        | Unit name        | true     | string            |
| Type        | Unit type        | true     | enum              |
| Description | Unit description | true     | text              |
| Attributes  | Unit attributes  | true     | list of Attribute |
| Comments    | User comments    | false    | text              |

## Complex data types

- For Unit Attributes type use Attribute component

## Enums

Type:
  - service
  - account
  - config
