<div align="center">

# Review Writing Skill

### 从阅读文献，到形成有证据的综述论证

![Format](https://img.shields.io/badge/Format-SKILL.md-2563eb)
![Language](https://img.shields.io/badge/Language-中文%20%7C%20English-0f766e)
![Focus](https://img.shields.io/badge/Focus-Literature%20Synthesis-7c3aed)

**问题统领 · 主题组织 · 证据比较 · 综合判断 · 持续扩展**

[快速开始](#快速开始) · [功能介绍](#功能介绍) · [使用示例](#使用示例) · [扩展规则](#持续扩展) · [English](README.en.md)

</div>

---

一套用于学术综述写作的 Codex Skill，将文献整理推进到科学解释、研究比较和有依据的综合判断。适合从文献、阅读笔记或提纲起草综述，也适合已经明确授权的整体重写。

技能的核心是让文章回答一个明确问题：已有研究共同说明了什么，差异来自哪里，这些认识如何影响后续研究或技术选择。

## 功能介绍

| 能力 | 具体作用 |
|---|---|
| 明确问题与范围 | 定义核心问题、读者需求、工作定义、文献边界与文章贡献 |
| 组织文献 | 按概念、机制或共同任务建立结构，连接不同研究之间的关系 |
| 形成综合论证 | 解释共识、分歧及研究意义，合理安排核心研究与背景文献的详略 |
| 支撑技术比较 | 围绕相同任务分析不同方法的路径、适用条件、瓶颈与代价 |
| 保持证据准确 | 区分直接观测、模型推断与作者综合，使引文对应具体论点 |
| 判断数据可比性 | 交代指标定义、参照、时间窗口、系统范围及关键试验条件 |
| 提炼明确结论 | 对已有证据直接作出判断，同时保留影响结论成立的具体条件 |
| 设计图表和使用公式 | 使图表、模型与正文论证相连，保留来源、假设和实际用途 |
| 形成具体展望 | 从前文问题提出所需实验、测量或比较及其判断用途 |
| 持续积累经验 | 使用 W01–W13 核心编号和限定范围的补充条目维护新要求 |

## 写作思路

```text
明确问题与边界
       ↓
收集文献 ↔ 整理主题 ↔ 评价贡献与分歧
       ↓
综合判断 → 图表与公式支撑 → 条件性结论与具体展望
```

流程允许往返。章节与段落结构依学科、综述类型和证据成熟度调整。

## 快速开始

需要支持本地 `SKILL.md` 的 Codex 环境。此仓库提供提示词与工作规则，本身不包含文献数据库、联网检索、PDF 获取或 Word 渲染引擎；相应任务由宿主环境中可用的工具完成。

将仓库克隆到技能目录，文件夹名使用技能名 `review-writing`。

**Windows PowerShell**

```powershell
$reviewSkillRoot = if ($env:CODEX_HOME) { Join-Path $env:CODEX_HOME 'skills' } else { Join-Path $HOME '.codex\skills' }
New-Item -ItemType Directory -Path $reviewSkillRoot -Force | Out-Null
git clone https://github.com/borin9Wang/review-writing-skill.git (Join-Path $reviewSkillRoot 'review-writing')
```

**macOS / Linux**

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/borin9Wang/review-writing-skill.git "${CODEX_HOME:-$HOME/.codex}/skills/review-writing"
```

若已经安装同名技能，请先合并自己的新增规则，避免覆盖个性化内容。在能识别该技能的会话中，用 `$review-writing` 明确调用。

## 使用示例

**从文献起草综述**

```text
使用 $review-writing，根据这个文件夹中的文献和阅读笔记，
先明确综述的核心问题与贡献，再组织提纲并起草正文。
关键判断要有原文依据，未获取全文的部分如实说明。
```

**比较两类技术**

```text
使用 $review-writing，比较 A 和 B 完成同一任务的不同路径。
围绕共同问题组织章节，解释性能差异及适用条件，
不要根据不同试验中的最高值直接排名。
```

**整体重写已有草稿**

```text
使用 $review-writing，依据现有稿件和已核实的文献整体重写。
重点形成各节的综合判断，保留正确数据、公式和来源。
```

## 持续扩展

可以直接告诉助手：

> 把这条加入综述写作 Skill：讨论分歧时，先检查研究对象和测量定义是否一致。

> 修改 W09：保留必要的物理条件，同时压缩重复的保留性表达。

> 这条要求只适用于当前项目，作为补充规则保存。

| 文件 | 维护内容 |
|---|---|
| [SKILL.md](SKILL.md) | 跨项目适用的核心写作规则 |
| [references/additions.md](references/additions.md) | 项目、期刊或作者偏好，以及适用范围和来源 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 新规则的归类、合并、编号与提交方式 |

已有规则优先完善，新增规则使用稳定编号。一次性任务指令不会自动成为永久要求。仓库保留了源项目的少量补充示例，只有任务符合其范围时才适用。

## 与修改 Skill 配合

| 任务 | 选择 |
|---|---|
| 从文献、笔记或提纲起草新综述 | 本仓库：`review-writing` |
| 已明确要求全文重构或整体重写 | 本仓库，可结合修改 Skill 保留原稿成果 |
| 依据指定稿件、导师批注或审稿意见修订 | [review-fixing-skill](https://github.com/borin9Wang/review-fixing-skill)，调用名 `review-revision` |

## 仓库结构

```text
review-writing-skill/
├── SKILL.md
├── agents/openai.yaml
├── references/additions.md
├── README.md
├── README.en.md
├── CONTRIBUTING.md
└── .github/ISSUE_TEMPLATE/rule-request.md
```

## 方法来源

规则来自实际综述写作与多轮修订经验，并吸收 Karen V. Fernandez（2019）的教程 [Critically reviewing literature: A tutorial for new researchers](https://doi.org/10.1016/j.ausmj.2019.05.001) 中的问题统领、收集—整理—评价、主题组织、综合陈述与研究机会识别方法。

工程指标、图表、公式和交付方面的具体规则是项目实践中的归纳。仓库不包含原教程全文、研究论文 PDF 或未公开稿件。
