# AI 课题组 | Five Research Member Skills — v3

五个 Skill **可单独安装、单独使用**；只有在相应工具和权限实际可用时，才按需调用其他成员或专项 Skill。

## 文件夹

| Member | Three roles / area | Optional specialist examples |
| --- | --- | --- |
| `ai-literature-member` | Search / Reading / Citation | Research Reading Mentor |
| `ai-research-execution` | Execution / Analysis / Output | Fluent Setting Checker, Physics Sanity Check |
| `ai-paper-editor` | Structure / Terminology / Language | Claim Graph Paper Writer, Paper Format Guardian |
| `ai-strict-reviewer` | Methods / Evidence / Statistics | Experimental, Simulation, Review Paper Reviewer, Claim–Evidence, Physics Sanity |
| `ai-quality-inspector` | Numbers / Figures-References / Requirements | Paper Format Guardian, Fluent Setting Checker |

## Workflow (default, not compulsory)

`文献 → 执行 → 科学审稿 → 编辑 → 质量检查 → 提交`

- 科学审稿发现数据或方法问题：回到文献/执行组员，并由作者决定修改方法。
- 编辑可能改变科学含义：保留原文，等待作者确认。
- 终稿质检发现冲突：验证唯一正确的数据源；不擅自猜值。
- 大改后只复查受影响的环节，避免重复 token 开销。

## 独立安装

把**任意一个成员的完整文件夹**复制到支持 Skill 的环境的相应目录。主入口为该文件夹的 `SKILL.md`。不要只复制主文件后漏掉 `references/`，其中包含按需读取的规则。

五个 `references/coordination-protocol.md`、`references/claim-data-ledger.md`、`references/specialist-routing.md` 是独立包随附的可选参考；不是自动同步数据库，也不意味着已安装其他专项工具。

## 推荐调用

```
调用 AI Strict Reviewer，先检查方法和证据是否支持结论。若检测到实验/数值/物理专项问题，只有对应专项 Skill 实际可用时才调用它；使用统一问题 ID 交接结果，不要重复检查已核实的事项。
```

```
调用 AI Quality Inspector，检查这篇论文数字、图表、公式和引文的一致性。优先复用我提供的共享命题与数据账本，发现冲突不自行选值，报告实际检查范围。
```

## 本次升级

- 继承了五个原 Skill 的全部有效研究规则及专业 reference 文件。
- 新增每位成员专属的专项调用矩阵与中英触发/排除条件。
- 新增统一问题交接、证据状态、可共享命题/数据账本模板。
- 质量检查和严格审稿的长规则分离到按需加载的 reference，主文件更短。
- **结构校验不代表真实论文行为测试**。见 `TEST_CASES.md`，用于后续对不同输入逐项验收。

## 发布状态

**发布信息**：v3 文件发布在本公开仓库的 ai-research-group 专题目录中；严格审稿组员使用独立仓库，质量检查组员使用本仓库根目录。尚未安装到用户设备，也未运行外部专家 Skill。

## GitHub 文件位置

- 文献组员：`ai-research-group/ai-literature-member/`
- 科研执行组员：`ai-research-group/ai-research-execution/`
- 论文编辑组员：`ai-research-group/ai-paper-editor/`
- 严格审稿组员：独立仓库 `Wendy-skill/ai-strict-reviewer`
- 质量检查组员：本仓库根目录 `Wendy-skill/ai-quality-inspector`

## 17个 Skill 的路由和交接（v3）

完整职责分工与按需调用见 [ROUTING_INDEX.md](./ROUTING_INDEX.md)；对应静态检查和拟执行测试见 [TEST_CASES.md](./TEST_CASES.md)。五位组员 + 十二个专项/辅助 Skill 均可独立使用；跨 Skill 交接采用统一问题 ID、证据来源、源文件版本和核实状态，不表示自动安装了其他 Skill，也不等于真正完成了跨应用调用。

**本次状态**：17份主 `SKILL.md` 已加入可选路由入口和按需加载的 reference；尚未执行模型级真实论文回归测试。科研结论的科学 Severity 和终稿一致性 Impact 各自保留，不做统一换算。
