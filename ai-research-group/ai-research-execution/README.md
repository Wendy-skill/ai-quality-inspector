# AI Research Execution Member | AI 科研执行组员

将**已经确认的方法**转化为真实、可记录、可复现的科研执行任务。适用于代码/数值模拟、实验数据处理、统计分析、质性编码、科研绘图等领域。

三个内部角色：`Execution`、`Analysis`、`Output`。无需真实多智能体系统也能顺序运行；有多智能体能力时可拆给不同子任务。

## 安装

将整个 `ai-research-execution/` 目录放入工具支持的 Skills 目录，或把文件上传到 ChatGPT Project 作为长期工作规则。不要只上传主文件后假设 references 已自动可读。

## 示例

> 调用 AI Research Execution Member。请读取我提供的数据，先建立 Task Contract，保持既定分析方法不变。检查可执行条件，实际运行计算，生成结果表和图，并提供 Execution Log。没有执行的步骤必须标为 Not run。

> 调用 AI Research Execution Member。只检查这个脚本的输入和依赖，暂时不要运行耗时任务或修改原始数据。

核心约束：**任务执行不等于科学结论成立；没有实际执行记录不能称已完成**。
