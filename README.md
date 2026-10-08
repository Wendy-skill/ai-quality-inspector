# AI Quality Inspector

**科研论文与学位论文的最终一致性检查 Skill**  
A consistency and quality-assurance Skill for scientific manuscripts and theses.

适用于 SCI / 科研论文、硕士论文、博士论文，以及投稿前和修订后的质量检查。

## 能检查什么

- **数字与结果**：摘要、结果、讨论、结论、图表中的数值、百分比、样本量、单位等是否一致。
- **图表与公式**：编号、标题、图注、公式符号、正文交叉引用是否匹配。
- **引用与参考文献**：文内引文和文末条目是否对应，是否存在编号或元数据不一致。
- **全文一致性**：术语、缩写、研究问题、研究目标、贡献与最终结论是否对应。
- **提交要求**：依据用户提供的学校、期刊规范检查缺漏。
- **长篇论文**：先建立全文索引，分章扫描，再做跨章节比对。

## 核心原则

> 找出不一致，并标注位置与证据；**不知道哪个值正确时，不擅自选择或修改**。

本 Skill 专注文档质量检查，**不替代科学审稿**。研究方法、因果推断、结论是否科学成立，应交由科学审稿流程判断。

对于百分比、比值、均值、单位换算等需要计算的核对，要求使用可用的计算工具；若未计算，必须明确注明未验证。

## 检查模式

| 模式 | 适用场景 |
| --- | --- |
| `Quick QA` | 投稿前快速排查明显错误 |
| `Full Consistency Audit` | 全文一致性系统检查 |
| `Thesis Final Check` | 硕士、博士论文最终检查 |
| `Submission Checklist` | 根据学校或期刊要求逐项核对 |
| `Revision Consistency Check` | 大幅修订后检查旧数字、旧编号与残留内容 |

## 如何使用

本仓库的核心文件是 [SKILL.md](./SKILL.md)。

**支持 Skills 的 AI 工作环境：** 将本仓库文件夹放到该环境认可的 Skills 目录，按环境规则启用。

**ChatGPT Project：** 把 `SKILL.md` 上传到项目文件，并在项目指令中写入：

```text
When checking manuscripts or theses for internal consistency,
read and follow the uploaded AI Quality Inspector SKILL.md.
Report detected issues with locations and evidence.
Do not silently revise the manuscript.
```

这属于项目文件加项目指令的使用方式，不表示原生 Skill 已安装。

### 示例指令

**论文投稿前：**

```text
调用 AI Quality Inspector。
模式：Quick QA。
检查这篇论文中的数字、图表、公式、引用和单位是否一致。
先列出问题与具体位置，不要修改原稿。
```

**完整学位论文：**

```text
调用 AI Quality Inspector。
模式：Thesis Final Check。
先建立全文检查索引，再分章节检查并核对摘要、结果、结论之间的一致性。
涉及计算的核对请使用可用的计算工具。
只报告实际完成的检查范围，不要擅自修改原稿。
```

## 输入类型

支持按材料情况检查 `LaTeX`、`DOCX`、`PDF` 及图片/截图。不同格式可验证的信息不同：例如 PDF 无法直接验证 Word 的内部域；缺少图像时无法宣称已经核对图片内容。

## 输出方式

每个问题说明：

`Issue → Location → Type → Status → Impact → Evidence → Required action`

状态区分：`Confirmed inconsistency`、`Probable inconsistency`、`Needs verification`、`No issue found`。

仅对**实际检查过的范围**给出完成结论。

---

**作者/仓库：** [Wendy-skill](https://github.com/Wendy-skill)

> 本项目为辅助检查工具，任何审查结果都需要研究者根据原始数据和适用规范确认。
