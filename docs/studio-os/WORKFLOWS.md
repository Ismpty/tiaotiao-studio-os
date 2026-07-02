# WORKFLOWS — TiaoTiao Studio OS Workflows Guide（工作流使用指南）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件定义 TiaoTiao Studio OS 中所有 Workflow Templates 的使用方式。

它的目标是让 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具能够快速理解：

- 当前有哪些 Workflow
- 每个 Workflow 负责什么
- 每个 Workflow 应该什么时候被调用
- 每个 Workflow 会读取哪些文件
- 每个 Workflow 会调用哪些 Agents
- 每个 Workflow 应该输出什么结果
- Workflow 与 Commands、Agents、Database Records、Knowledge Nodes 的关系

## English

This file defines how Workflow Templates should be used inside TiaoTiao Studio OS.

It helps AI tools understand available workflows, execution order, required source files, agent usage, expected outputs and workflow boundaries.

---

# Core Principle（核心原则）

Workflow 是 TSOS 的执行顺序层。

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
Workflows 负责规定任务怎么执行。  
Agents 负责完成具体创作步骤。

---

# Current Workflows（当前工作流）

当前 TSOS 已定义以下 4 个核心工作流：

```text
WORKFLOW-001 — Jump After Work Production Workflow
WORKFLOW-002 — Short Video Prompt Workflow
WORKFLOW-003 — Storyboard to Video Workflow
WORKFLOW-004 — Publishing Workflow
```

---

# Workflow Index（工作流索引）

| Workflow | Name | Primary Use |
|---|---|---|
| WORKFLOW-001 | Jump After Work Production Workflow | 完整生产流程 |
| WORKFLOW-002 | Short Video Prompt Workflow | 短视频 Prompt 生成 |
| WORKFLOW-003 | Storyboard to Video Workflow | 分镜转视频生成包 |
| WORKFLOW-004 | Publishing Workflow | 发布包生成 |

---

# WORKFLOW-001 — Jump After Work Production Workflow

## File

```text
workflows/WORKFLOW-001.md
```

## 中文说明

WORKFLOW-001 是《跳跳下班啦》的完整生产工作流。

它用于把 TSOS 中已经建立的 Knowledge Nodes、Database Records 和 AI Agents 串联起来，形成一套可重复执行的短视频生产流程。

它覆盖从项目启动到发布规划的完整链路。

## When to Use（什么时候使用）

当用户说：

```text
完整做一条《跳跳下班啦》
从分镜到发布全部生成
启动完整生产流程
做一个完整项目包
Run Jump After Work Production
```

应该使用：

```text
WORKFLOW-001
```

通常由以下命令调用：

```text
COMMAND-001
```

## Required Records

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
AGENT-002 — Prompt Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

## Execution Stages

```text
1. Project Setup
↓
2. Storyboard Planning
↓
3. Prompt Generation
↓
4. Cinematography Planning
↓
5. Script Writing
↓
6. Editing Planning
↓
7. Publishing Planning
↓
8. Final Consistency Check
```

## Expected Output

```text
1. Project Brief
2. Storyboard Output
3. Prompt Output
4. Cinematography Output
5. Script Output
6. Editing Output
7. Publishing Output
8. Final Consistency Checklist
```

---

# WORKFLOW-002 — Short Video Prompt Workflow

## File

```text
workflows/WORKFLOW-002.md
```

## 中文说明

WORKFLOW-002 是短视频提示词生成工作流。

它用于把 Project、Storyboard、Character、Environment、Camera、Lighting、Motion、Asset 和 Knowledge Nodes 转化为可直接用于 AI 图片 / 视频生成的 Prompt。

它不重新设计角色，也不改写故事。

它只负责生成稳定、清晰、可复制、可执行的提示词。

## When to Use（什么时候使用）

当用户说：

```text
生成视频 Prompt
生成 Kling Prompt
生成 Veo Prompt
生成 Runway Prompt
生成图片 Prompt
生成封面 Prompt
生成角色一致性 Prompt
```

应该使用：

```text
WORKFLOW-002
```

通常由以下命令调用：

```text
COMMAND-002
```

## Required Records

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
AGENT-002 — Prompt Agent
```

## Optional Agent Inputs

```text
AGENT-001 — Storyboard Output
AGENT-003 — Cinematography Output
AGENT-004 — Script Output
AGENT-005 — Editing Output
```

## Execution Stages

```text
1. Prompt Task Setup
↓
2. Source Record Collection
↓
3. Shot Context Extraction
↓
4. Prompt Variable Mapping
↓
5. Base Prompt Generation
↓
6. Model Adaptation
↓
7. Negative Prompt Generation
↓
8. Consistency Check
↓
9. Final Prompt Package
```

## Expected Output

```text
1. Prompt Purpose
2. Target Model
3. Source Records
4. Base Prompt
5. Model-Specific Prompt
6. Negative Prompt
7. Consistency Checklist
8. Usage Notes
```

## Important Rule

WORKFLOW-002 必须始终包含：

```text
ASSET-001
Negative Prompt
Consistency Checklist
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

它不重新写故事，也不重新设计角色。

## When to Use（什么时候使用）

当用户说：

```text
把分镜转成视频 Prompt
把 Storyboard 做成 Kling 片段
拆成逐镜头视频生成包
把分镜转成 AI 视频生产包
生成每个镜头的视频提示词
```

应该使用：

```text
WORKFLOW-003
```

通常配合以下命令使用：

```text
COMMAND-003
COMMAND-002
COMMAND-005
```

## Required Records

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
AGENT-002 — Prompt Agent
AGENT-003 — Cinematography Agent
AGENT-005 — Editing Agent
```

## Execution Stages

```text
1. Storyboard Input Review
↓
2. Shot Segmentation
↓
3. Video Prompt Generation
↓
4. Cinematography Enhancement
↓
5. Motion Continuity Setup
↓
6. Lighting and Style Lock
↓
7. Negative Prompt Setup
↓
8. Video Clip Generation Package
↓
9. Clip Review
↓
10. Assembly Notes
```

## Expected Output

```text
1. Storyboard Review Result
2. Video Shot Units
3. Shot-by-Shot Video Prompts
4. Cinematography-Enhanced Video Prompts
5. Motion Continuity Map
6. Lighting and Style Lock Notes
7. Shot Negative Prompt Set
8. Video Clip Generation Package
9. Clip Review Notes
10. Video Assembly Notes
```

## Important Rule

WORKFLOW-003 必须逐镜头输出，不得只输出一条总 Prompt。

每个镜头都必须包含：

```text
Shot ID
Duration
Start State
Action
End State
Camera
Motion
Lighting
Negative Prompt
Continuity Notes
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

它不重新创作视频内容，也不修改 Jump 角色设定。

它只负责发布层内容。

## When to Use（什么时候使用）

当用户说：

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

应该使用：

```text
WORKFLOW-004
```

通常由以下命令调用：

```text
COMMAND-004
```

## Required Records

```text
EP-001
STORY-001
PROMPT-001
ASSET-001
PROJ-001
```

## Required Knowledge

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
↓
2. Platform Selection
↓
3. Title Generation
↓
4. Caption / Description Generation
↓
5. Hashtag Generation
↓
6. Cover Text Planning
↓
7. Publishing Time Planning
↓
8. Pre-Publish Checklist
↓
9. Publish Record Setup
↓
10. Post-Publish Review
```

## Expected Output

```text
1. Publish Asset Review Result
2. Platform Strategy
3. Title Options
4. Caption / Description
5. Hashtag Set
6. Cover Text Suggestions
7. Publishing Time Suggestion
8. Pre-Publish Checklist
9. Publishing Record
10. Post-Publish Review Template
```

## Important Rule

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
| 生成短视频 Prompt | WORKFLOW-002 |
| 生成图片 Prompt | WORKFLOW-002 |
| 生成视频 Prompt | WORKFLOW-002 |
| 分镜转视频片段 | WORKFLOW-003 |
| 分镜转 Kling / Veo / Runway 包 | WORKFLOW-003 |
| 生成发布包 | WORKFLOW-004 |
| 生成标题、正文、标签 | WORKFLOW-004 |
| 发布前检查 / 发布后复盘 | WORKFLOW-004 |

---

# Workflow and Command Mapping（工作流与命令映射）

| Command | Workflow |
|---|---|
| COMMAND-001 | WORKFLOW-001 |
| COMMAND-002 | WORKFLOW-002 |
| COMMAND-003 | WORKFLOW-001 / WORKFLOW-003 |
| COMMAND-004 | WORKFLOW-004 |
| COMMAND-005 | Checks outputs from all workflows |

---

# Workflow and Agent Mapping（工作流与智能体映射）

| Workflow | Agents |
|---|---|
| WORKFLOW-001 | AGENT-001, AGENT-002, AGENT-003, AGENT-004, AGENT-005, AGENT-006 |
| WORKFLOW-002 | AGENT-002 |
| WORKFLOW-003 | AGENT-001, AGENT-002, AGENT-003, AGENT-005 |
| WORKFLOW-004 | AGENT-006 |

---

# Standard Workflow Execution Rule（标准工作流执行规则）

执行任何 Workflow 时，必须遵守：

```text
1. Read Workflow file
2. Read required Command if invoked by Command
3. Read required Agent files
4. Read required Database Records
5. Read required Knowledge Nodes
6. Execute stages in order
7. Output required package
8. Run consistency check when needed
```

---

# Workflow Source of Truth Rule（工作流事实来源规则）

Workflow 只能规定执行顺序。

Workflow 不得覆盖：

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

# Required Workflow Checks（工作流必须检查）

任何正式 Workflow 输出前，必须检查：

```text
[ ] 是否读取正确 Workflow
[ ] 是否读取正确 Agents
[ ] 是否读取 required Database Records
[ ] 是否读取 required Knowledge Nodes
[ ] 是否按阶段执行
[ ] 是否输出规定格式
[ ] 是否没有新增未确认设定
[ ] 是否没有跳过 ASSET-001
[ ] 是否没有跳过 Negative Prompt
[ ] 是否可以进入下一阶段
```

---

# Workflow Failure Handling（工作流失败处理）

如果 Workflow 缺少必要输入，必须输出：

```text
Missing Input:
[缺少内容]

Required Source:
[需要读取的文件]

Action:
Cannot complete workflow until required source is provided or loaded.
```

如果用户要求跳过关键流程，必须输出：

```text
Issue Found:
This request skips a required TSOS workflow stage.

Required Workflow:
WORKFLOW-XXX

Suggested Action:
Run the required stage before continuing.
```

---

# Workflow Safety Rules（工作流安全规则）

所有 Workflow 都不得：

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

# Workflow Output Standard（工作流输出标准）

所有 Workflow 输出必须：

```text
[ ] 可执行
[ ] 可复制
[ ] 可追溯
[ ] 有明确来源
[ ] 有阶段结构
[ ] 有输出格式
[ ] 有检查项
[ ] 不空泛
[ ] 不脱离 TSOS Source of Truth
```

---

# Workflow Examples（工作流示例）

## Example 1 — Full Production

User：

```text
运行 COMMAND-001。
```

Runtime：

```text
COMMAND-001
↓
WORKFLOW-001
↓
AGENT-001
↓
AGENT-002
↓
AGENT-003
↓
AGENT-004
↓
AGENT-005
↓
AGENT-006
↓
COMMAND-005
```

Output：

```text
Complete production package.
```

---

## Example 2 — Storyboard to Video

User：

```text
把这个分镜转成 Kling 视频生成包。
```

Runtime：

```text
WORKFLOW-003
↓
AGENT-002
↓
AGENT-003
↓
Continuity Check
```

Output：

```text
Shot-by-shot video generation package.
```

---

## Example 3 — Publishing

User：

```text
生成小红书发布包。
```

Runtime：

```text
COMMAND-004
↓
WORKFLOW-004
↓
AGENT-006
↓
Brand Safety Check
```

Output：

```text
Platform-ready publishing package.
```

---

# Relationship to Docs（与文档关系）

Workflow 使用时应该参考：

```text
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
```

其中：

```text
RUNTIME.md
```

定义整体运行逻辑。

```text
CODEX.md
```

定义 Codex 如何读取和执行。

```text
COMMANDS.md
```

定义命令入口。

```text
WORKFLOWS.md
```

定义执行流程。

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial workflows guide |