# AI Literature Member | AI 文献组员

用于文献检索、初筛、全文深读、引用元数据核对、证据整理与文献综合。可独立使用，不需要安装其他四位组员。

三个内部角色：`Search`、`Reading`、`Citation`。这些是分工规则；运行环境没有多智能体功能时顺序执行，不声称实际启动子智能体。

## 安装

将包含 `SKILL.md` 和 `references/` 的整个 `ai-literature-member` 文件夹放入支持 Skills 的工具指定目录，或在 ChatGPT Project 上传文件并指明以此 Skill 为操作规则。

## 示例

> 调用 AI Literature Member。请围绕 [研究问题] 执行 Search + Triage，列出 10 篇候选文献和核验状态。暂时不要深读或合成结论。

> 调用 AI Literature Member。只读我上传的 3 篇论文，逐篇生成 Reading Card，重要结果标注页码或图表位置，不要补充未提供论文的信息。

所有输出应区分来源访问级别和未核实内容。
