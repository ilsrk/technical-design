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

- Technical design has a title (root) document — the technical design card.
- Technical design is based on a component-based approach.
  - Components are the building blocks of technical design.

## Hard constraints

- Do not write code.
- Do not modify documents outside the technical design working directory.
- **Never** fill in or modify comment fields. These fields must be completed EXCLUSIVELY by the user.

## Process

| Process              | When it runs                                    |
| -------------------- | ----------------------------------------------- |
| `initial` / `import` | Start a new design, or bring in an existing one |
| `continue`           | Design requirements and solutions               |
| `edit`               | Change the design or related components         |
| `validate`           | Check completeness, diagrams, and wording       |
| `review`             | Check that solutions meet the requirements      |
| `realize` / `export` | Write the code, or export the design            |

## Technocal design card

The root component containing the technical design sections 

### Sections

| Section                 | Which groups together                                                                                     | Required |
| ----------------------- | --------------------------------------------------------------------------------------------------------- | -------- |
| `Basic information`     | Description and artifacts: everything that needs to be known before starting the design process           | true     |
| `Requirenmets`          | Requirements for the problem being solved                                                                 | true     |
| `System design`         | System design: which services will be deployed, dependencies between systems, public API contracts, etc   | optional |
| `Application design`    | Application design: components, layers, contracts, and dependencies                                       | optional |
| `Data design`           | Data storage design: the structure of relational and non-relational databases, object storage, etc        | optional |
| `Observability design`  | Observability design: metrics to be collected, processes to be monitored, etc                             | optional |
| `Testing plan`          | Test plan: a document describing how the problem being solved will be tested                              | true     |
| `Implementation plan`   | Implementation plan: breakdown into phases and phases into tasks                                          | true     |
| `State`                 | A technical section reflecting the current state of the technical design                                  | true     |
| `Reviews`               | Technical design reviews                                                                                  | optional |

## Components

| Component                 | What a component contains                                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| `Context`                 | Additional information to help solve the problem more effectively                                                  |
| `Artifacts`               | Links to external documents that must be taken into account and affect the problem being solved                    |
| `Requirenements register` | List of requirements for solving the given problem                                                                 |
| `Decision nodes`          | A tabular list of decisions made, with links to the corresponding decision records                                 |
| `Solution card`           | Design of a decision node, listing options, their evaluations, and the reasons for selecting or rejecting each one |
| `Metrics`                 | Monitoring metrics                                                                                                 |
| `Alerts`                  | Observability alerts                                                                                               |
| `State machine`           | List of requirements for solving the given problem                                                                 |
