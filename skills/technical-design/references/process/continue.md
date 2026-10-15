# Continue technical design

## Hard constraints

- Does not write code.
- **Never** design solutions on behalf of the consumer. Ask, prompt, and record; do not invent, choose, or fill in solutions, variants, or selected decisions for them.

## Conventions

- After each solution card is complete, set Status `Selected` on the chosen row in Solution variants, then record Selected solution on the corresponding solution node: the chosen variant ID and a short description.
- When adding a variant, ask which Type fits the problem (see Solution variant types). Build the variant details from that type's components in the same file as the Solution variants register, unless the user asks to decompose the solutions.
- Record section progress in the State machine component in the Service section of the technical design card.

## Steps

### 1. Determine the current state

- Determine the current state of the technical design based on the State machine component in the Service section of the technical design card.

### 2. Display a list of the design statuses

- Display a list of the design statuses for all sections and prompt the user to continue designing an incomplete section.

### 3. Start describing the Basic Information section

- Prompt the user to provide the task context.
- Suggest that the user fill in the task artifacts.
- Ask the user if they would like to add anything else to the task's basic information.
- Record in the State machine that the Basic Information section has been completed.

### 4. Start filling in the Requirements section

- Apply [`technical-design-requirements`](../../../technical-design-requirements/SKILL.md).
- Record the requirements-gathering status in the State machine after that skill finishes.

### 5. Start filling in the System Design section

- Ask the user where system-level solutions need to be made, and continue until they finish filling out Solution nodes for this section.
- When a system solution involves deployment units, services, or connections, prefer variant Type `System design`.
- Suggest that the user start designing the system solution cards.
- Complete the System Design section once all solution nodes have Selected solution filled and links to completed solution cards.
- Record completion in the State machine.

### 6. Start filling in the Application Design section

- Ask which solutions need to be made and record them in Solution nodes for this section.
- Keep asking until the user explicitly asks you to stop.
- Suggest that the user start designing the solution cards.
- Complete the Application Design section once all solution nodes have Selected solution filled and links to their corresponding solution cards.
- Record completion in the State machine.

### 7. Start designing the Data Design section

- Ask the user which data needs to be designed and which solutions need to be made.
- Record all solutions in Solution nodes for this section.
- Keep asking the user until they explicitly ask you to stop.
- Suggest starting to design the solution cards. Use Tables, Table, Indexes, and Partitions on the section or inside variants when the chosen design needs them.
- Complete the section once all solution nodes have Selected solution filled and links to their corresponding solution cards.
- Record completion in the State machine.

### 8. Start filling in the Observability Design section

- Ask the user where observability solutions need to be made, and record them in Solution nodes for this section.
- Prefer variant Type `Observability` for those solution cards.
- Complete the section once all solution nodes have Selected solution filled and links to completed solution cards.
- Record completion in the State machine.

### 9. Start designing the Testing Plan section

- Ask the user which checks are needed to verify the solution against the requirements.
- Record each check in the Testing plan structure (ID, Title, Type, Description).
- Keep asking until the user explicitly asks you to stop or confirms the plan is complete.
- Record completion in the State machine.

### 10. Start designing the Implementation Plan section

- Ask the user how to break the work into phases and tasks.
- Record each task in the Implementation plan structure (Phase, Task ID, Title, and optional Description and Dependencies).
- Keep asking until the user explicitly asks you to stop or confirms the plan is complete.
- Record completion in the State machine.

## Output

- List of technical design section statuses (technical design status)
