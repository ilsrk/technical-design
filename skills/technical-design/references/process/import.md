# Import technical design

## Steps

1. Determine the technical design working directory or prompt the user to create one.
2. Copy the technical design from the external source, converting it to the internal format.

## Hard constraints

- **NEVER** modify any artifacts in the imported technical design.
- **NEVER** leave the working directory of the imported technical design. Reading nested articles is allowed, but reading parent articles is prohibited.
- **NEVER** perform any analysis; only copy the technical design.
- **ALWAYS** ask the user for permission before reading any artifact in the imported technical design.

## Constraints

- Technical design formats may vary. Follow the component format defined in the current repository. Adapt components from external technical designs while preserving their underlying concepts.
  - If any components cannot be copied or a conflict arises, consult the user before proceeding.

## Inputs

- Link to the external technical design to be imported.

## Outputs

- Link to the imported technical design.
