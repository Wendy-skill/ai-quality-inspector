# AI Paper Editor｜AI 论文编辑组员（第三位）

一个**可单独使用**的论文编辑 Skill，面向 SCI 论文、会议论文、硕博学位论文、研究计划和审稿回复。

## 负责什么

- **Structure Editor（结构编辑）**：章节逻辑、段落顺序、过渡、重复、表达组织。
- **Terminology Editor（术语编辑）**：术语、缩写、变量、单位、拼写规范的一致性。
- **Language Editor（语言编辑）**：语法、表达清晰度、冗余、学术语言。

核心规则：**科学含义可能改变时，必须先让作者确认**。不擅自改变数据、研究方法、结论强度，不伪造引用。**它不替代科学审稿和最终质量检查。**

## 安装

将整个 `ai-paper-editor` 文件夹放到支持 Agent Skills 的环境所要求的 Skills 目录，或上传 ZIP（如果你的环境支持上传技能包）。保留 `references/` 子目录，不要只复制主文件而遗漏其引用文件。

在 ChatGPT 中，也可以把 `SKILL.md` 及必要的 `references/` 文件上传到专门 Project，然后在项目指令中要求按该规则处理论文；这不是原生 Skill 安装。

## 直接使用

**审查而不改文：**

```text
调用 AI Paper Editor，对这篇论文做 Diagnostic Review。
重点检查 Structure、Terminology 和 Language。
只报告编辑问题及具体位置，不要改写科学结论。
```

**直接改一段：**

```text
调用 AI Paper Editor，按 Targeted Edit 模式修改这段英文论文。
保持数据、引文、公式和科学含义不变。
如果某项修改会影响结论强度，先单独列出让我确认。
```

**编辑整篇论文：**

```text
调用 AI Paper Editor，按 Full Manuscript Edit 模式分章节处理。
先建立结构和术语索引，再依次检查结构、术语和语言。
每章记录修改清单；科学含义相关修改必须先经我确认。
```

## 与第四、第五位组员的区别

- 第三位 **Paper Editor**：怎么写得清楚、统一、自然。
- 第四位 **Strict Reviewer**：科学方法、证据和结论是否站得住。
- 第五位 **Quality Inspector**：数字、图表、引用等是否前后一致。

本 Skill 可以不依赖其他组员独立使用。如果外部组员不存在，会列出需要后续人工处理的任务，不声称已完成交接。
