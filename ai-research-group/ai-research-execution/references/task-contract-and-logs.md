# Execution templates

## Task Contract

```yaml
Task_ID: <identifier>
Research_type: <field or task type>
Research_question: <user-supplied or not applicable>
Task: <requested execution>
Method: <user-confirmed approach>
Inputs: <paths/identifiers>
Constraints: <time/cost/safety/integrity>
Fixed_parameters: <list>
Variable_parameters: <list>
Outputs_expected: <list>
Tools_required: <list>
Success_criteria: <measurable>
Stop_conditions: <conditions>
Primary_owner: Research Execution Member
Secondary_checker: <optional>
Human_approval_needed: <decisions>
Approval_status: <approved/not confirmed>
```

Do not treat placeholders as real task data.

## Execution Log

| Field | Record |
| --- | --- |
| Task ID, time | Actual task/run identifier and time when known |
| Input filenames/hashes | Source paths/versions; check hashes if feasible |
| Environment | Tool/software version and configuration |
| Fixed/variable settings | Explicit values, units and deviations |
| Actual operations | Commands / tool invocations / digital workflow |
| Exclusions and changes | Reason, authority and affected outputs |
| Attempt status | Completed / Partially completed / Failed / Blocked / Not run |
| Outputs | Actual file paths/IDs and checks performed |
| Limitations | Missing inputs or unverified steps |

## Progress status

Never infer Completed merely from a plan, a returned draft script, or a promise to run. If verification was not performed, state `output exists but not independently checked` only when existence was actually established.
