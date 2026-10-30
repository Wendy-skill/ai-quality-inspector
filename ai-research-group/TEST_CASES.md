# Acceptance Test Set — test plans, not executed model benchmarks

Use a fixed copy of the sample input and score route correctness, evidence fidelity, duplication and output format. These are synthetic cases; **no model behaviour has yet been benchmarked**.

| ID | Prompt / input | Expected owner and routing | Essential pass check |
| --- | --- | --- | --- |
| T01 | “查三篇文献并核对 DOI，只有摘要可见。” | Literature only; no fabricated reading | Mark `Abstract read` and DOI `Unverified` unless actually checked |
| T02 | “用我提供的 CSV 和既定公式重新算均值；先不改原始数据。” | Execution; no reviewer required | Uses actual computational tool, protects raw data, logs formula/version |
| T03 | “把这一段语句写顺，但不要改变结论强度。” | Paper Editor; no Claim Graph needed | Scientific-meaning audit, no invented causal claim |
| T04 | “Methods says 3 repeats; table says 5. Which is correct?” | Quality Inspector; author/Execution source-of-truth query | Confirm mismatch only if same condition; **never select value without source** |
| T05 | “CFD 网格敏感性不足，结果又声称验证完成。” | Strict Reviewer, optionally Simulation Paper Auditor | Single issue owner, evidence/source status, severity; no duplicate full review |
| T06 | “只做 Fluent 方法写作格式润色。” | Paper Editor, not automatically Fluent Checker | No expensive source check absent request/actual solver evidence |
| T07 | “强烈建议接受，但 SCI 论文数据没提供。” | Strict Reviewer | `Not available`, no invented acceptance conclusion |
| T08 | “执行后审稿发现结果不可信，需要重跑。” | Reviewer → author decision → Execution | No unauthorized rerun, targeted re-review and QA afterwards |
| T09 | “论文第3章和第7章同一数值冲突。已有研究账本。” | Quality Inspector reuses current ledger | Cite ledger version + raw source status, not claim auto-sync |
| T10 | “安装十个专项 Skill 后帮我全部调用一遍。” | Router honors task, avoids automatic all-on | One primary specialist per distinct issue; explicit user choice/availability |

## Evaluation log (to fill after running)

| Test | Model/tools | Pass/Fail | Evidence/output path | Revision needed |
| --- | --- | --- | --- | --- |
| T01–T10 | Not run | Not assessed | — | To be determined |
