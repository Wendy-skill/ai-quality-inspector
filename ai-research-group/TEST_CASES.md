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

## v3 — 17-Skill route acceptance cases (not yet executed)

Each case requires a frozen input, evidence/version checks, an expected owner, and an explicit result log. Passing a source-file check is **not** a substitute for running the case.

| Case | Trigger | Expected primary Skill | Routing / acceptance condition |
| --- | --- | --- | --- |
| S01 | 本周卡住，安排开工 | research-monday-start | Plan only, no fictitious execution |
| S02 | 使用 Zotero 读一篇指定全文 | research-reading-mentor | Only claim PDF/full-text access if available |
| S03 | 已知重复次数和不确定度需要实验审查 | engineering-experiment-reviewer | Report experimental evidence; scientific judgement stays Reviewer |
| S04 | 系统综述检索是否完整 | engineering-review-paper-reviewer | Review-specific coverage/selection check |
| S05 | CFD 网格与残差是否支持结论 | simulation-paper-auditor | Numerical credibility without generic rewriting |
| S06 | Fluent 日志和论文 Methods 不一致 | fluent-setting-checker | Real solver evidence required; no guessed settings |
| S07 | 流场机理是否物理上可信 | physics-sanity-check | Plausible does not mean proven |
| S08 | 结论句对应哪张图和哪条数据 | claim-evidence-checker | Map exact claim and evidence, not duplicate final Severity |
| S09 | 对标目标期刊近期论文 | journal-gap-analyzer | Dated identified benchmark; no acceptance prediction |
| S10 | Word 批量修复格式 | paper-format-guardian | Backup + text invariance checked before claiming safe edit |
| S11 | 整体科学严格审稿 | ai-strict-reviewer | Delegate by distinct evidence needs; synthesise scientific Severity |
| S12 | 将复杂论述拆成命题图并重写 | claim-graph-paper-writer | Reconstruct only approved nodes, preserve scientific strength |
| S13 | 检查摘要和结论数值是否一致 | ai-quality-inspector | Compare same-condition values, Impact not Severity, no guessing |
| S14 | 把多个技能压缩以节约上下文 | skill-optimizer | Preserve all prohibitions, source constraints and output requirements |
| S15 | 查文献并核验 DOI | ai-literature-member | Search hit != full-text confirmation; trace bibliographic evidence |
| S16 | 运行已批准数据分析任务 | ai-research-execution | Actual tool run + script/dataset/version log; no unapproved rerun |
| S17 | 修改论文语言而不改变科学含义 | ai-paper-editor | Meaning lock, author confirmation for scientific changes |
| X01 | 同一图表数字在三 Skill 中出现 | Reviewer / Inspector / Execution | Single owner per root issue; cross-referenced ID, no duplicate full audits |
| X02 | 已有旧版 ledger，新数据更新后 | Relevant source owner | Detect version mismatch; reopen only affected claims/checks |
| X03 | 要求‘调用所有17项’但没有安装 | Primary user task owner | Do not claim unavailable calls or fake multi-agent execution |

## Actual execution record

| Case(s) | Environment/model | Input snapshot | Tool/provenance trace | Result | Next action |
| --- | --- | --- | --- | --- | --- |
| S01–S17, X01–X03 | Not run | To be supplied | None | Not assessed | Execute real-world regression cases before performance claims |
