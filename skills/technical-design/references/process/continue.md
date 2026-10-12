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

- Ask the user where system-level decisions need to be made, and continue until they finish filling out the system decisions register.
- Suggest that the user start designing the system decision cards.
- Complete the System Design section once all decision nodes in the decision register have selected options and links to completed decision cards.

### 6. Start filling in the Infrastructure Design Decisions section.

- Ask the user which deployment units they intend to design.
- Keep asking until the user explicitly asks you to stop.
- Record everything in the Infrastructure Decisions Register.
- Suggest that the user start designing infrastructure decisions in the decision cards.
- Complete the system design once all decisions in the decision register have selected options and corresponding decision cards.

### 7. Start filling in the Application Design section.

- Ask which decisions need to be made and record them in the Decision Register.
- Keep asking until the user explicitly asks you to stop.
- Suggest that the user start designing the decision cards.
- Complete the Application Design section once all decisions in the Application Design Decision Register have selected options and links to their corresponding decision cards.

### 8. Start designing the Data Storage Design section.

- Ask the user which data needs to be designed and which decisions need to be made.
- Record all decisions in the Decision Register.
- Keep asking the user until they explicitly ask you to stop.
- Suggest starting to design the decision cards.
- Complete the design once all decisions have selected options and links to their corresponding decision cards.

### 9. Start designing the Test Plan section.

### 10. Start designing the Implementation Plan section.

### 11. Collect reviews.

## Output

- List of technical design section statuses (technical design status)
-