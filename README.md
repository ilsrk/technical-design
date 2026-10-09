# About

Agent skill for a component-based technical design. It creates a design directory and a root document, then walks requirements, solution cards, review, and validation before implementation.

# Process map

```mermaid
flowchart TD
  start([Start]) --> entry{New or existing?}
  entry -->|new| initial[initial]
  entry -->|existing| import[import]
  initial --> continue[continue]
  import --> continue
  continue --> needEdit{Need changes?}
  needEdit -->|yes| edit[edit]
  edit --> continue
  needEdit -->|no| validate[validate]
  validate --> review[review]
  review --> finish{Code or export?}
  finish -->|code| realize[realize]
  finish -->|export| export[export]
  realize --> done([Done])
  export --> done
```


| Process              | When it runs                                    |
| -------------------- | ----------------------------------------------- |
| `initial` / `import` | Start a new design, or bring in an existing one |
| `continue`           | Design requirements and solutions               |
| `edit`               | Change the design or related components         |
| `validate`           | Check completeness, diagrams, and wording       |
| `review`             | Check that solutions meet the requirements      |
| `realize` / `export` | Write the code, or export the design            |




# Quick Start

```
npm install -g @ilsrk/technical-design@latest

```

