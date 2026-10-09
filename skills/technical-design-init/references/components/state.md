# State

The technical design status displays a list of all main and nested sections of the technical design.

## Sections list

1. Context
2. Requirenments register
3. System design
4. Infrastructure design
5. Application design
6. Observability design
7. Test plan
8. Implementation plan
9. Review register

## Sections State Machine

Sections **MUST** have one of the following statuses:
  - INITED
  - NOT PRESENT
  - IN PROGRESS
  - SKIPPED
  - CLOSED
  - DONE

**Initial statuses:** INITED, NOT PRESENT

**In-progress statuses:** IN PROGRESS, SKIPPED

**Final statuses:** DONE, CLOSED

Intial statuses => In-progress statuses => Final statuses

## Structure

Each requirement in the list **MUST** have:
  - Sequence number
  - Name
  - Status
  - Details

Each requirement in the list **MUST** have:
  - Comments

## Requirenments

- The objects in the status component **MUST** be numbered in ascending order.
- The list of sections **MUST NOT** be modified, even if the user requests a change.

## Constraints

- The requirements register **MUST** contain **AT LEAST** one requirement.
