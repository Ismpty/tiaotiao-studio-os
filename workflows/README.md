# Workflows — Workflow Templates Index（工作流模板索引）

> Navigation Index（导航索引）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 `workflows/` 目录的索引文件。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- 当前有哪些 Workflow Templates
- 每个 Workflow 负责什么
- 每个 Workflow 应该什么时候使用
- 每个 Workflow 会调用哪些 Agents
- 每个 Workflow 会读取哪些 Database Records
- 每个 Workflow 的标准输出是什么
- Workflow 与 Commands、Agents、Database Records、Knowledge Nodes 的关系

## English

This file is the index for the `workflows/` directory.

It helps AI tools understand available workflow templates, workflow routing, related commands, related agents, required records and expected outputs.

---

# Workflow Layer Role（工作流层作用）

Workflows 是 TSOS 的执行顺序层。

```text
Command
↓
Workflow
↓
Agent
↓
Database Records
↓
Knowledge Nodes
↓
Output
```

Commands 负责启动任务。  
Workflows 负责规定执行顺序。  
Agents 负责执行具体创作职责。

---

# Current Workflows（当前工作流）

```text
WORKFLOW-001 — Little Security Guard Production Workflow
WORKFLOW-002 — Short Video Prompt Workflow
WORKFLOW-003 — Storyboard to Video Workflow
WORKFLOW-004 — Publishing Workflow
```

---

# Workflow Index（工作流索引）

| Workflow | Name | File | Primary Use |
|---|---|---|---|
| WORKFLOW-001 | Little Security Guard Production Workflow | WORKFLOW-001.md | 完整生产流程 |
| WORKFLOW-002 | Short Video Prompt Workflow | WORKFLOW-002.md | 视频 Prompt Package 生成 |
| WORKFLOW-003 | Storyboard to Video Workflow | WORKFLOW-003.md | 分镜转视频生成包 |
| WORKFLOW-004 | Publishing Workflow | WORKFLOW-004.md | 发布包生成 |

---

# WORKFLOW-001 — Little Security Guard Production Workflow

## File

```text
workflows/WORKFLOW-001.md
```

## 中文说明

WORKFLOW-001 是《小保安和他的古人朋友们》的完整生产工作流。

它用于把 TSOS 中已经建立的 Knowledge Nodes、Database Records 和 AI Agents 串联起来，形成一套可重复执行的短视频生产流程。

## Use When（使用场景）

当用户需要：

```text
完整做一条《小保安和他的古人朋友们》
从项目到分镜、Prompt、脚本、剪辑、发布全部生成
启动完整生产流程
生成完整生产包
```

使用：

```text
WORKFLOW-001
```

通常由以下命令调用：

```text
COMMAND-001
```

## Required Database Records

```text
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
PROJ-001
```

## Required Agents

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Engineer Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

## Execution Stages

```text
1. Project Setup
2. Storyboard Planning
3. Prompt Generation
4. Cinematography Planning
5. Script Writing
6. Editing Planning
7. Publishing Planning
8. Final Consistency Check
```

## Expected Output

```text
Project Brief
Storyboard Output
Prompt Output
Cinematography Output
Script Output
Editing Output
Publishing Output
Final Consistency Checklist
```

---

# WORKFLOW-002 — Short Video Prompt Workflow

## File

```text
workflows/WORKFLOW-002.md
```

## 中文说明

WORKFLOW-002 是短视频提示词生成工作流。

它用于把 TSOS 中的 Project、Storyboard、Character、Environment、Camera、Lighting、Motion、Asset 和 Knowledge Nodes 转化为模型可读的视频提示词包。

## Use When（使用场景）

当用户需要：

```text
生成视频 Prompt
生成 Identity Card Prompt
生成 Storyboard Prompt
生成 Universal Video Prompt
生成模型可读视频提示词包
生成 Jimeng / Veo / Runway 视频执行 Prompt
```

使用：

```text
WORKFLOW-002
```

通常由以下命令调用：

```text
COMMAND-002
```

## Required Database Records

```text
CHAR-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
PROJ-001
```

## Required Agent

```text
AGENT-002 — Prompt Engineer Agent
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-003 Cinematography Output
AGENT-004 Script Output
AGENT-005 Editing Output
```

## Execution Stages

```text
1. Prompt Task Setup
2. Source Record Collection
3. Identity Card Prompt
4. Storyboard Prompt
5. Universal Video Prompt
6. Model-readable Check
7. COMMAND-005 Review
8. Final Prompt Package
```

## Expected Output

```text
Prompt Purpose
Source References
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
Usage Notes
```

## Required Rule

WORKFLOW-002 必须始终包含：

```text
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
```

---

# WORKFLOW-003 — Storyboard to Video Workflow

## File

```text
workflows/WORKFLOW-003.md
```

## 中文说明

WORKFLOW-003 是分镜到视频生成工作流。

它用于把已经完成的 Storyboard Output 转化为可执行的视频镜头生成包。

它覆盖：

```text
镜头拆分
视频提示词
摄影增强
动作连续性
灯光一致性
负面提示词
片段检查
视频组装备注
```

## Use When（使用场景）

当用户需要：

```text
把分镜转成视频 Prompt
把 Storyboard 做成 Kling 片段
拆成逐镜头视频生成包
把分镜转成 AI 视频生产包
生成每个镜头的视频提示词
```

使用：

```text
WORKFLOW-003
```

通常配合以下命令使用：

```text
COMMAND-003
COMMAND-002
COMMAND-005
```

## Required Database Records

```text
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
PROJ-001
```

## Required Agents

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Engineer Agent
AGENT-003 — Cinematography Agent
AGENT-005 — Editing Agent
```

## Execution Stages

```text
1. Storyboard Input Review
2. Shot Segmentation
3. Storyboard Verification
4. Universal Video Prompt Setup
5. Shot Execution Plan
6. Clip Generation Package
7. Clip Review with COMMAND-005
8. Iteration Notes
9. Assembly Notes
```

## Expected Output

```text
Storyboard Review Result
Identity Card Verification Result
Storyboard Verification Result
Universal Video Prompt Verification Result
Shot Execution Plan
Clip Generation Package
COMMAND-005 Clip Review Result
Iteration Notes
Video Assembly Notes
```

## Required Rule

WORKFLOW-003 必须使用上传身份卡、上传故事板和 Universal Video Prompt 逐镜头执行。

每个镜头执行单元必须包含：

```text
Uploaded Identity Card
Uploaded Storyboard
Universal Video Prompt
Current Shot Number and Name
Target Model
Duration
Continuity Notes
COMMAND-005 Review Status
```

---

# WORKFLOW-004 — Publishing Workflow

## File

```text
workflows/WORKFLOW-004.md
```

## 中文说明

WORKFLOW-004 是发布工作流。

它用于把完成的视频、脚本、字幕、封面、剪辑方案和品牌规范转化为可直接发布到不同平台的发布包。

## Use When（使用场景）

当用户需要：

```text
生成发布包
生成小红书发布文案
生成抖音标题
生成视频号正文
生成 YouTube Shorts 标题
生成标签和封面文案
发布前检查
发布后复盘模板
```

使用：

```text
WORKFLOW-004
```

通常由以下命令调用：

```text
COMMAND-004
```

## Required Database Records

```text
EP-001
STORY-001
PROMPT-001
ASSET-001
PROJ-001
```

## Required Knowledge Nodes

```text
BRAND-001
STORYFORMULA-001
EMOTION-001
MUSIC-001
STYLE-001
COLOR-001
```

## Required Agent

```text
AGENT-006 — Publishing Agent
```

## Execution Stages

```text
1. Publish Asset Review
2. Platform Selection
3. Title Generation
4. Caption / Description Generation
5. Hashtag Generation
6. Cover Text Planning
7. Publishing Time Planning
8. Pre-Publish Checklist
9. Publish Record Setup
10. Post-Publish Review
```

## Expected Output

```text
Publish Asset Review Result
Platform Strategy
Title Options
Caption / Description
Hashtag Set
Cover Text Suggestions
Publishing Time Suggestion
Pre-Publish Checklist
Publishing Record
Post-Publish Review Template
```

## Required Rule

WORKFLOW-004 必须避免：

```text
标题党
焦虑表达
强营销腔
虚假承诺
无关标签
```

---

# Workflow Routing Table（工作流路由表）

| User Request | Workflow |
|---|---|
| 完整生产流程 | WORKFLOW-001 |
| 从分镜到发布全部生成 | WORKFLOW-001 |
| 生成视频 Prompt Package | WORKFLOW-002 |
| 生成身份卡 + 故事板 + 通用视频 Prompt | WORKFLOW-002 |
| 生成 Jimeng / Veo / Runway 视频执行 Prompt | WORKFLOW-002 |
| 分镜转视频片段 | WORKFLOW-003 |
| 分镜转 Jimeng / Veo / Runway 片段生成包 | WORKFLOW-003 |
| 生成发布包 | WORKFLOW-004 |
| 生成标题、正文、标签 | WORKFLOW-004 |
| 发布前检查 / 发布后复盘 | WORKFLOW-004 |

---

# Workflow and Command Mapping（工作流与命令映射）

| Workflow | Command |
|---|---|
| WORKFLOW-001 | COMMAND-001 |
| WORKFLOW-002 | COMMAND-002 |
| WORKFLOW-003 | COMMAND-003 / COMMAND-002 / COMMAND-005 |
| WORKFLOW-004 | COMMAND-004 |

---

# Workflow and Agent Mapping（工作流与智能体映射）

| Workflow | Agents |
|---|---|
| WORKFLOW-001 | AGENT-001, AGENT-002, AGENT-003, AGENT-004, AGENT-005, AGENT-006 |
| WORKFLOW-002 | AGENT-002 |
| WORKFLOW-003 | AGENT-001, AGENT-002, AGENT-003, AGENT-005 |
| WORKFLOW-004 | AGENT-006 |

---

# Standard Workflow Execution Rule（标准执行规则）

执行任何 Workflow 时，必须遵守：

```text
1. Read Workflow file
2. Read related Command if invoked by Command
3. Read required Agent files
4. Read required Database Records
5. Read required Knowledge Nodes
6. Execute stages in order
7. Output required package
8. Run consistency check when needed
```

---

# Source of Truth Rule（事实来源规则）

Workflows 只能规定执行顺序。

Workflows 不得覆盖：

```text
Character Rules
World Rules
Brand Rules
Knowledge Nodes
Database Records
```

如果 Workflow 与 Source of Truth 冲突，优先级为：

```text
Knowledge Nodes
+
Database Records
>
Workflow instructions
```

---

# Workflow Safety Rules（工作流安全规则）

所有 Workflows 都不得：

```text
修改 Jump 核心身份
修改 TiaoTiao Universe 世界观
修改 Brand Language
绕过 Knowledge Nodes
绕过 Database Records
绕过 ASSET-001
省略一致性检查
临时新增未确认设定
改变文件命名规则
改变目录结构
```

---

# Required Runtime Docs（相关运行文档）

执行 Workflows 时应参考：

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/WORKFLOWS.md
```

---

# Related Directories（相关目录）

```text
workflows/
commands/
agents/
database/
knowledge/
examples/
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial workflows index |
