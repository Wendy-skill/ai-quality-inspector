# Optional specialist routing — Quality Inspector

## Activation

Trigger on 终稿质检 / 图表编号 / 数字与章节一致性 / 提交清单, or final QA / numerical consistency / reference checks. Avoid activating for novelty, validity, scientific plausibility or pure language polishing.

## Task → optional Skill

| Need | Optional specialist | When useful / safeguard |
| --- | --- | --- |
| Batch-fix Word style/caption/format against supplied template | `paper-format-guardian` | Only when fixes are authorised; make backup, compare content before/after, report deviations; QA still verifies resulting cross-references |
| Cross-check manuscript solver values with actual Fluent inputs | `fluent-setting-checker` | Only if the actual configuration/logs exist; missing evidence stays unverified |
| Bibliographic identity or DOI beyond manuscript text | `ai-literature-member` (member handoff) | Literature Member owns external reference identification; Inspector checks in-manuscript citation consistency |

## Escalation

- Conflicting values with unknown truth → author/Research Execution; no automatic 'latest value' rule.
- Science-changing interpretation or insufficient evidence → Strict Reviewer.
- Safe terminology/grammar clean-up after source resolved → Paper Editor.
- Do not recompute full scientific adequacy or claim a formatting change was applied without editing tool evidence.
