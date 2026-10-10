---
name: technical-design-init
description: Create the technical design directory and root artifact. Use when initiating a new technical design.
---

# Technical Design Init

Initialize the technical design working directory and create a technical design card in it.

Does not write code, perform analysis, design solutions, or gather requirements.

## Artifacts

Read the [glossary](./references/glossary.md) to clarify the terminology used in this document.
Read the [global](./references/constraits.md) constraints and never perform any of the prohibited actions.
Read the [technical design card design guidelines](./references/card.md).

## Instructions

1. Validate the Input Data.
2. Create a Working Directory.
3. Initialize the technical design card.
3. Suggest that the user proceed with the technical design.

## Constraints

- The working directory name **MUST** include the task ID and a short description of the task.

## Input

- Unique task identifier
- Task title
- Task description
- Working directory

## Output

- Link to the technical design card
