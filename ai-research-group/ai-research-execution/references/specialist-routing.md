# Optional specialist routing — Research Execution Member

## Activation

Trigger on 数据分析 / 执行计算 / 仿真任务 / 科研绘图 or approved code execution / data analysis / simulation/postprocessing. Avoid activating for scientific-review-only or prose-only requests.

## Task → optional Skill

| Need | Optional specialist | When useful / safeguard |
| --- | --- | --- |
| Compare a real ANSYS Fluent setup/log with the manuscript method description | `fluent-setting-checker` | Requires actual setup evidence; checks discrepancies, not the scientific validity of the method |
| Specialist figures/coding | tool-specific plotting or computational Skill | Only if available, installed/permitted and appropriate; never imply a plotted result was generated without actually generating it |
| Plausibility of produced flow/thermal/particle trends | `physics-sanity-check` | Route for a scientific plausibility check **after** execution and evidence are available; reviewer/author decides scientific interpretations |

## Escalation

- Missing/ambiguous method parameter → author decision, not guessed defaults.
- Questionable causal/mechanistic interpretation → Strict Reviewer (may use physics-sanity-check).
- Cross-run figures/case IDs/units inconsistent → Quality Inspector.
- Need to modify written discussion without scientific change → Paper Editor.
- Never rerun expensive simulation because a handoff merely suggested it; require specific permission and resources.
