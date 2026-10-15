# Continue technical design

## Hard constraints

- Does not write code.

## Steps

### 1. Determine the current state

- Determine the current state of the technical design based on the State Machine component in the Service section of the technical design card.

### 2. Display a list of the design statuses

- Display a list of the design statuses for all sections and prompt the user to continue designing an incomplete section.

### 3. Start describing the Basic Information section.

- Prompt the user to provide the task context.
- Suggest that the user fill in the task artifacts.
- Ask the user if they would like to add anything else to the task's basic information.
- Record in the Technical Design State component that the Basic Information section has been completed.

### 4. Start filling in the Requirements section.

- Suggest that the user add a requirement.
- Ask the user if they want to finish gathering requirements.
- Record the requirements-gathering status in the Technical Design State component.

### 5. Start filling in the System Design section.

- Ask the user where system-level solutions need to be made, and continue until they finish filling out the system solutions register.
- Suggest that the user start designing the system solution cards.
- Complete the System Design section once all solution nodes in the solution register have selected options and links to completed solution cards.

### 6. Start filling in the Infrastructure Design Solutions section.

- Ask the user which deployment units they intend to design.
- Keep asking until the user explicitly asks you to stop.
- Record everything in the Infrastructure Solutions Register.
- Suggest that the user start designing infrastructure solutions in the solution cards.
- Complete the system design once all solutions in the solution register have selected options and corresponding solution cards.

### 7. Start filling in the Application Design section.

- Ask which solutions need to be made and record them in the Solution Register.
- Keep asking until the user explicitly asks you to stop.
- Suggest that the user start designing the solution cards.
- Complete the Application Design section once all solutions in the Application Design Solution Register have selected options and links to their corresponding solution cards.

### 8. Start designing the Data Storage Design section.

- Ask the user which data needs to be designed and which solutions need to be made.
- Record all solutions in the Solution Register.
- Keep asking the user until they explicitly ask you to stop.
- Suggest starting to design the solution cards.
- Complete the design once all solutions have selected options and links to their corresponding solution cards.

### 9. Start designing the Test Plan section.

### 10. Start designing the Implementation Plan section.

### 11. Collect reviews.

- Apply [`technical-design-review`](../../../technical-design-review/SKILL.md).

## Output

- List of technical design section statuses (technical design status)
-