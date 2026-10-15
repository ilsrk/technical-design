# Solution card

The root document of the solution record. It describes the solution node, available options, the evaluation of each option, and the reasons for accepting or rejecting each option.

## Sections

| Section             | Required |
| ------------------- | -------- |
| `Basic information` | true     |
| `Requirements`      | true     |
| `Solution design`   | true     |
| `Testing plan`      | false    |
| `Service`           | true     |
| `Support`           | false    |

## Conventions 

- Each solution node has: a Selected solution, Preferred solution, and Alternative solution.
- The Selected solution is filled in only when the user asks to choose and finalize a solution. Once this is done, the technical design of the solution card is considered complete.
- Preferred solutions are the most suitable options.
- Alternative solutions include all remaining options.

## Hard constraints

- The header of the solution card must include the solution node ID and a short title.
- The order of the sections must not be changed, even if the user requests otherwise.
- There can be only one Selected Decision.
- Each decision option has a unique identifier.
- All decisions must be unique; duplicates are not allowed.

## Templates

Each Solution Card has a different component structure. Use the base component template in the `Solution design` section. Refer to the table for the templates.

