---
name: technical-design-converter
description: >-
  Convert a technical design between the internal component markdown format and
  an external format or repository. Use when importing or exporting a technical
  design, mapping Confluence/wiki pages to local design files, adapting foreign
  design structure to local components, or migrating a design between formats.
---

# Technical design converter

## Purpose

- Bring an existing design from an external source into the internal format (`to-internal`).
- Export a local design to an external source (`to-external`).
- Preserve underlying concepts while adapting structure to the target format’s components.

## When to use

- User asks to import, export, convert, or migrate a technical design.
- Formats differ between local markdown components and an external wiki/repo.
- `technical-design` routes import/export work here (no separate import/export process).

## Directions

| Direction | Source | Target | User wording |
| --------- | ------ | ------ | ------------ |
| `to-internal` | External design | Local technical design working directory | import |
| `to-external` | Local technical design | External working directory | export |

## Required inputs

Collect before starting. Do not invent defaults.

| Input | Direction | Description |
| ----- | --------- | ----------- |
| Direction | both | `to-internal` or `to-external` |
| Source link | both | Root of the design to read (`to-internal`: external design; `to-external`: local design root) |
| Target working directory | both | Where to write (`to-internal`: local path; `to-external`: external root link) |
| External formatting style | `to-external` | Link to the technical design formatting style in the external source |

If any required input is missing, ask the user and stop until provided.

## Steps

### Shared

1. Confirm direction and required inputs.
2. Read the target format rules:
   - `to-internal`: component and section specs from the `technical-design` skill.
   - `to-external`: the user-provided formatting style link.
3. Map source structure to target structure (sections → components / pages).
4. Copy content. Adapt shape; preserve underlying concepts and identifiers where possible.
5. If any component cannot be mapped or a conflict arises, consult the user before proceeding.
6. Return the link/path to the written root document and a short mapping summary.

### `to-internal` (import)

1. Determine the local technical design working directory, or prompt the user to create one.
2. Walk the external design from the given root. Nested articles are allowed; parent articles outside that root are prohibited.
3. **ALWAYS** ask the user for permission before reading any artifact of the imported technical design.
4. Produce local files matching internal components/sections. Prefer `index.md` as the root design card.
5. Follow the component format from `technical-design`. Adapt external components while preserving their underlying concepts.
6. Do not analyze quality, completeness, or correctness — conversion only.

### `to-external` (export)

1. Determine the local technical design working directory (source).
2. Determine the working directory in the external source (target).
3. Ask the user for a link to the technical design formatting style in the external source if not already provided.
4. **ALWAYS** ask for permission before creating or modifying files in the external repository.
5. Write the design into the external tree following that style.
6. **NEVER** leave the working directory in the external repository.

## Mapping rules

- Prefer one-to-one mapping to known components from `technical-design` (Context, Requirements register, Solution nodes, Solution card, etc.).
- If the external doc has no matching component, either:
  - place content in the closest existing component (not in user Comments), or
  - ask the user which component to use.
- Keep requirement IDs, solution node IDs, and variant IDs stable across conversion when present.
- Use Markdown links `[text](URL)`; verify reachability when linking back to originals.
- Diagrams: keep source text (Mermaid/PlantUML) when the target supports it; otherwise link to the original artifact.
- Technical design formats may differ between local and external repositories — that is expected.

## Hard constraints

- **NEVER** modify any artifacts of the source design (read-only source). On `to-internal`, that means the external imported design; on `to-external`, the local design.
- **NEVER** leave the agreed working directory:
  - `to-internal`: stay inside the external design root while reading (nested OK, parents forbidden); write only into the local working directory.
  - `to-external`: stay inside the external working directory while writing.
- **ALWAYS** ask permission before creating or modifying files in an external repository.
- **ALWAYS** ask permission before reading any artifact when importing.
- **NEVER** perform design analysis, validation, or review during conversion — only copy and adapt format.
- **NEVER** fill or modify user `Comments` fields.
- **NEVER** write application/implementation code.

## Soft constraints

- Snake_case English names for new local files and directories.
- Root local directory: `{task_id}_{short_english_description}` when creating a new import target.
- Root local document name: `index.md`.

## Outputs

| Direction | Output |
| --------- | ------ |
| `to-internal` | Link/path to the imported technical design root |
| `to-external` | Link/path to the exported root in the external source |
| both | Short mapping summary: what was converted, what was skipped, what needs user decision |

## Related

- Format specs: `technical-design` (components, sections, roots)
- Sibling: `technical-design-review` (critical review — not used during conversion)
