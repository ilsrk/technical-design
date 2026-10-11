# Solution card

The root document of the decision record. It describes the decision node, available options, the evaluation of each option, and the reasons for accepting or rejecting each option.

## Sections

| Section                 | Which groups together                                                                                     | Required |
| ----------------------- | --------------------------------------------------------------------------------------------------------- | -------- |
| `Basic information`     | Description and artifacts: everything that needs to be known before starting the design process           | true     |
| `Requirenmets`          | Requirements for the problem being solved                                                                 | true     |
| `Solution design`       | Application design: components, layers, contracts, and dependencies                                       | true     |
| `State`                 | A technical section reflecting the current state of the technical design                                  | true     |
| `Reviews`               | Technical design reviews                                                                                  | optional |

The header of the technical design card must include the technical design ID and a short task description.

The technical design card must contain the following technical design sections:
  - Context
  - Requirenments
  - State

## Constraints 

- The order of the sections must not be changed, even if the user requests otherwise.
