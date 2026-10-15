---
name: technical-design
description: >-
  Technical design management: creation, updates, authoring, validation, and
  realization. Use when creating, continuing, editing, validating, or realizing
  a technical design. For import or export, use technical-design-converter.
  For review, use technical-design-review.
---

# Technical design

## Glossary

**Technical design** is the in-depth design of a solution to a given problem before coding begins.

**The technical design card** is the root document of the technical design, containing all information related to it.

**A technical design section** is a logically grouped set of blocks that address specific design problems. Examples include a system design block, an application design block, a task context block, a testing block, and so on.

**Solution nodes (points, areas)** are a list of areas where solutions must be made to meet the requirements of the given task.

**A solution card** is a detailed design of a single solution node, including a comprehensive description of all available variants and the rationale behind the solution made.

**Solution variants** are a tabular list of solution variants for a solution node, each with an ID, title, type, status, and link.

**A solution variant** is the details document for one row in Solution variants.

## Purpose

- Design a solution to the given problem.
- Reduce uncertainty in solution-making.

## Steps

1. Determining the Technical Design Working Directory
  - Based on the context of the data provided by the user, determine whether a technical design needs to be created, continued, modified, validated, or implemented.
  - If the user needs to import or export a design, apply [`technical-design-converter`](../technical-design-converter/SKILL.md) instead of a process in this skill.
  - If the user needs to review a design, apply [`technical-design-review`](../technical-design-review/SKILL.md) instead of a process in this skill.
2. Apply the appropriate process based on the list of processes in the `Process` section of this document.

## Conventions

- Technical design is primarily intended to be read by humans and reviewed by the team
- The more requirements are considered, the fewer variants remain at each solution point.
- The IT team may supplement the task with its own requirements (constraints, assumptions, etc.), but these requirements must be considered lower priority.
- The technical design must contain at least one solution to be made. A technical design that does not solve the stated problems has no reason to exist.
- When referencing requirements, always specify the requirement ID and title.
- Whenever you reference something, use Markdown links in the [text](URL) format. ALWAYS verify that links are reachable.

## Structure

- Technical design has a title (root) document — [the technical design card](./references/roots/design-card.md).
- Technical design is based on a component-based approach.
- Components are the building blocks of technical design.
- Technical design consists of individually analyzed [solution nodes](./references/roots/solution-card.md).

## Hard constraints

- **Never** write code, except during the `realize` process.
- **Never** modify documents outside the technical design working directory.
- **Never** fill in or modify comment fields. These fields must be completed EXCLUSIVELY by the user.
- **Never** add comments or your own text blocks outside the component structure.
- **Never** design solutions on behalf of the consumer. Ask, prompt, and record; do not invent, choose, or fill in solutions, variants, or selected decisions for them.

## Soft constraints (can be overridden)

- Use snake_case for file and directory naming.
- Name directories and files ONLY in English.
- Name the root directory of the technical design using the task ID followed by a short task description in English.
- Name the root technical design document `index.md`.
- Place solution variant details in the same file as the Solution variants register, unless the user asks to decompose the solutions.

## Process

| Process    | When it runs                              | Link                                     |
| ---------- | ----------------------------------------- | ---------------------------------------- |
| `initial`  | Start a new technical design              | [link](./references/process/init.md)     |
| `continue` | Design requirements and solutions         | [link](./references/process/continue.md) |
| `edit`     | Change the design or related components   | [link](./references/process/edit.md)     |
| `validate` | Check completeness, diagrams, and wording | [link](./references/process/validate.md) |
| `realize`  | Implement the design in code              | [link](./references/process/realize.md)  |


## Section list

| Section                | Which groups together                                                                                   | Link                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| `Basic information`    | Description and artifacts: everything that needs to be known before starting the design process         | [link](./references/sections/basic-information.md)    |
| `Requirements`         | Requirements for the problem being solved                                                               | [link](./references/sections/requirements.md)         |
| `System design`        | System design: which services will be deployed, dependencies between systems, public API contracts, etc | [link](./references/sections/system-design.md)        |
| `Application design`   | Application design: components, layers, contracts, and dependencies                                     | [link](./references/sections/application-design.md)   |
| `Data design`          | Data storage design: the structure of relational and non-relational databases, object storage, etc      | [link](./references/sections/data-design.md)          |
| `Observability design` | Observability design: metrics to be collected, processes to be monitored, etc                           | [link](./references/sections/observability-design.md) |
| `Solution design`      | Design of a solution node: variants, evaluations, and reasons for accepting or rejecting each variant   | [link](./references/sections/solution-design.md)      |
| `Testing plan`         | Test plan: a document describing how the problem being solved will be tested                            | [link](./references/sections/testing-plan.md)         |
| `Implementation plan`  | Implementation plan: breakdown into phases and phases into tasks                                        | [link](./references/sections/implementation-plan.md)  |
| `Service`              | A service section for managing the technical design process: statuses, logs, tracking, etc              | [link](./references/sections/service.md)              |
| `Support`              | Support for technical design. History of changes, reviews, etc                                          | [link](./references/sections/support.md)              |

## Component list

| Component                  | What a component contains                                                                                          | Link                                                                 |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| `Context`                  | Additional information to help solve the problem more effectively                                                  | [link](./references/components/context.md)                           |
| `Artifacts`                | Links to AS IS external documents (schemas, released solutions) that affect the problem  | [link](./references/components/artifacts.md)                         |
| `Glossary`                 | Domain and project terms used in the technical design, with their meanings                                         | [link](./references/components/glossary.md)                          |
| `User stories`             | List of user stories that describe the problem from the user's perspective                                         | [link](./references/components/user-stories.md)                      |
| `Requirements register`    | List of requirements for solving the given problem                                                                 | [link](./references/components/requirements-register.md)             |
| `Solution nodes`           | A tabular list of solution nodes, with links to cards and the selected variant once the card is complete           | [link](./references/components/solution-nodes.md)                    |
| `Solution variants`        | A tabular list of solution variants for a solution node, with type, status, and links                              | [link](./references/components/solution-variants.md)                 |
| `Solution variant`         | Details of one solution variant: base components plus type-specific components                                     | [link](./references/components/solution-variant.md)                  |
| `Solution card`            | Design of a solution node; variants carry type-specific component sets                                             | [link](./references/roots/solution-card.md)                          |
| `Observing`                | What is planned to be observed                                                                                     | [link](./references/components/observability/observing.md)           |
| `Metrics`                  | Monitoring metrics                                                                                                 | [link](./references/components/observability/metrics.md)             |
| `Alerts`                   | Observability alerts                                                                                               | [link](./references/components/observability/alerts.md)              |
| `Tables`                   | Created and modified relational tables                                                                             | [link](./references/components/relation-database/tables.md)          |
| `Table`                    | Single table design: columns and attributes                                                                        | [link](./references/components/relation-database/table.md)           |
| `Indexes`                  | Indexes for relational tables                                                                                      | [link](./references/components/relation-database/indexes.md)         |
| `Partitions`               | Partitions for relational tables                                                                                   | [link](./references/components/relation-database/partitions.md)      |
| `Attributes`               | Object attributes                                                                                                  | [link](./references/components/attributes.md)                        |
| `JSON contract`            | JSON payload contract as JSON Schema                                                                               | [link](./references/components/contracts/json-contract.md)            |
| `Deployment unit registry` | List of deployment units: servers, systems, users, connections, packages, etc.                                     | [link](./references/components/infrastructure/deployment-unit-registry.md) |
| `Deployment unit`          | Detailed description of the deployment unit                                                                        | [link](./references/components/infrastructure/deployment-unit.md)    |
| `New service`              | New service design                                                                                                 | [link](./references/components/infrastructure/services/new-service.md) |
| `Change service`           | Change to an existing service                                                                                      | [link](./references/components/infrastructure/services/change-service.md) |
| `New connection`           | New connection design                                                                                              | [link](./references/components/infrastructure/connections/new-connection.md) |
| `Change connection`        | Change to an existing connection                                                                                   | [link](./references/components/infrastructure/connections/change-connection.md) |
| `New topic`                | New queue topic design                                                                                             | [link](./references/components/infrastructure/queue/new-topic.md)    |
| `New message`              | New queue message design                                                                                           | [link](./references/components/infrastructure/queue/new-message.md)  |
| `Change topic`             | Change to an existing queue topic                                                                                  | [link](./references/components/infrastructure/queue/change-topic.md) |
| `Change message`           | Change to an existing queue message                                                                                | [link](./references/components/infrastructure/queue/change-message.md) |
| `State machine`            | A status model reflecting the current status of individual sections and the overall technical design status        | [link](./references/components/state-machine.md)                     |
| `Reviews`                  | Technical design reviews and review history                                                                        | [link](./references/components/reviews.md)                           |
| `Open Questions`           | Unanswered questions, areas of uncertainty, difficulties, and doubts                                               | [link](./references/components/open-questions.md)                    |
| `Migration plan`           | Strategy, steps, rollback, and risks for the refactoring migration                                                 | [link](./references/components/refactoring/migration-plan.md)        |

## Solution variant types

Use these as the Type of a row in Solution variants. They add components on top of the Solution variant base set.

| Type             | When to use                                                | Link                                          |
| ---------------- | ---------------------------------------------------------- | --------------------------------------------- |
| `Observability`  | When designing an observability solution                   | [link](./references/variants/observability.md)  |
| `System design`  | When designing services, deployment units, and connections | [link](./references/variants/system-design.md)  |
| `Refactoring`    | When designing a refactoring of existing code or system    | [link](./references/variants/refactoring.md)    |
