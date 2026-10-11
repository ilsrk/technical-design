---
name: technical-design
description: Technical design management: creation, updates, authoring, validation, import, export.
---

# Technical design

## Glossary

**Technical design** is the in-depth design of a solution to a given problem before coding begins.

**The technical design card** is the root document of the technical design, containing all information related to it.

**A technical design sections** is a logically grouped set of blocks that address specific design problems. Examples include a system design block, an application design block, a task context block, a testing block, and so on.

**Decision nodes (points, areas)** is a list of areas where decisions must be made to meet the requirements of the given task.

## Purpose

- Design a solution to the given problem.
- Reduce uncertainty in decision-making.

## Conventions

- Technical design is primarily intended to be read by humans and reviewed by the team
- The more requirements are considered, the fewer options remain at each decision point.
- The IT team may supplement the task with its own requirements (constraints, assumptions, etc.), but these requirements must be considered lower priority.
- The technical design must contain at least one decision to be made. A technical design that does not solve the stated problems has no reason to exist.
- When referencing requirements, always specify the requirement ID and title.
- Whenever you reference something, use Markdown links in the [text](URL) format. ALWAYS verify that links are reachable.

## Structure

- Technical design has a title (root) document — [the technical design card](./references/roots/design-card.md).
- Technical design is based on a component-based approach.
- Components are the building blocks of technical design.
- Technical design consists of individually analyzed [solution nodes](./references/roots/solution-card.md).

## Hard constraints

- Do not write code.
- Do not modify documents outside the technical design working directory.
- **Never** fill in or modify comment fields. These fields must be completed EXCLUSIVELY by the user.

## Process

| Process              | When it runs                                    | Link |
| -------------------- | ----------------------------------------------- | ---- |
| `initial`            | Start a new design, or bring in an existing one | [link](./references/process/init.md) |
| `import`             | Start a new design, or bring in an existing one | [link](./references/process/import.md) |
| `continue`           | Design requirements and solutions               | [link](./references/process/continue.md) |
| `edit`               | Change the design or related components         | [link](./references/process/edit.md) |
| `validate`           | Check completeness, diagrams, and wording       | [link](./references/process/vilidate.md) |
| `review`             | Check that solutions meet the requirements      | [link](./references/process/review.md) |
| `realize`            | Write the code, or export the design            | [link](./references/process/realize.md) |
| `export`             | Write the code, or export the design            | [link](./references/process/export.md) |

## Technocal design card

The root component containing the technical design sections 

### Section list

| Section                 | Which groups together                                                                                     | Link |
| ----------------------- | --------------------------------------------------------------------------------------------------------- | ---- |
| `Basic information`     | Description and artifacts: everything that needs to be known before starting the design process           | [link](./references/sections/basic-information.md) |
| `Requirenmets`          | Requirements for the problem being solved                                                                 | [link](./references/sections/requirenments.md) |
| `System design`         | System design: which services will be deployed, dependencies between systems, public API contracts, etc   | [link](./references/sections/system-design.md) |
| `Application design`    | Application design: components, layers, contracts, and dependencies                                       | [link](./references/sections/application-design.md) |
| `Data design`           | Data storage design: the structure of relational and non-relational databases, object storage, etc        | [link](./references/sections/data-design.md) |
| `Observability design`  | Observability design: metrics to be collected, processes to be monitored, etc                             | [link](./references/sections/obserability-design.md) |
| `Testing plan`          | Test plan: a document describing how the problem being solved will be tested                              | [link](./references/sections/testing-plan.md) |
| `Implementation plan`   | Implementation plan: breakdown into phases and phases into tasks                                          | [link](./references/sections/implementation-plan.md) |
| `State`                 | A technical section reflecting the current state of the technical design                                  | [link](./references/sections/state-machine.md) |
| `Reviews`               | Technical design reviews                                                                                  | [link](./references/sections/reviews.md) |

## Component list

| Component                 | What a component contains                                                                                          | Link |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------ | ---- |
| `Context`                 | Additional information to help solve the problem more effectively                                                  | [link](./references/components/context.md) |
| `Artifacts`               | Links to external documents that must be taken into account and affect the problem being solved                    | |
| `Requirenements register` | List of requirements for solving the given problem                                                                 | [link](./references/components/requrenments-register.md) |
| `Decision nodes`          | A tabular list of decisions made, with links to the corresponding decision records                                 | [link](./references/sections/solution-design.md) |
| `Solution card`           | Design of a decision node, listing options, their evaluations, and the reasons for selecting or rejecting each one | [link](./references/roots/solution-card.md) |
| `Metrics`                 | Monitoring metrics                                                                                                 | [link](./references/sections/metrics.md) |
| `Alerts`                  | Observability alerts                                                                                               | [link](./references/sections/alertings.md) |
| `State machine`           | List of requirements for solving the given problem                                                                 | [link](./references/components/state-machine.md) |
