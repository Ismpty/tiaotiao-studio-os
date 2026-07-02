# TiaoTiao Studio OS Architecture

## Architecture

```
Studio OS

├── Documentation

├── Database

├── Knowledge

├── Production

├── AI Agents

├── Skills

├── Templates

├── Archive
```

---

# Phase 4–8 Architecture Update（Phase 4–8 架构更新）

> Version：1.0  
> Status：Active  
> Scope：Agents / Workflows / Commands / Runtime Docs / Navigation Index

---

# Architecture Summary（架构总结）

## 中文

经过 Phase 4–8，TiaoTiao Studio OS 已经从一个基础知识库和生产数据库，升级为一套可运行的 AI Native Studio Operating System。

当前系统不只是保存角色、故事、镜头和 Prompt，而是具备：

- AI Agents
- Workflow Templates
- Operating Commands
- Runtime Docs
- Examples
- Navigation Index

这意味着 TSOS 已经可以被 ChatGPT、Codex、Cursor、Claude 等 AI 工具读取、理解、调用和执行。

## English

After Phase 4–8, TiaoTiao Studio OS has evolved from a knowledge and production database into an executable AI Native Studio Operating System.

It now includes agents, workflows, commands, runtime docs, examples and navigation indexes.

---

# Current System Architecture（当前系统架构）

TSOS 当前系统结构为：

```text
knowledge/
↓
database/
↓
agents/
↓
workflows/
↓
commands/
↓
docs/studio-os/
↓
examples/
```

---

# Layer 1 — Knowledge Layer（知识层）

## Path

```text
knowledge/
```

## Role

Knowledge Layer 定义长期稳定的创作规则。

它负责：

- 世界观
- 视觉风格
- 色彩系统
- 情绪系统
- 镜头语言
- 动作语言
- 服装系统
- 音乐语言
- 故事公式
- 品牌语言

## Core Principle

```text
Knowledge Nodes define rules.
```

Knowledge Nodes 是长期规则，不应该被临时任务随意修改。

---

# Layer 2 — Production Database（生产数据库层）

## Path

```text
database/
```

## Role

Production Database 定义具体可生产对象。

它负责：

- 角色
- 剧集
- 故事
- 环境
- 动作
- 镜头
- 灯光
- Prompt
- 资产
- 项目

## Core Records

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

## Core Principle

```text
Database Records define production entities.
```

Database Records 应引用 Knowledge Nodes，而不是重复制造规则。

---

# Layer 3 — AI Agents（AI 智能体层）

## Path

```text
agents/
```

## Role

AI Agents 定义执行角色。

它负责回答：

```text
谁来完成这个任务？
```

## Current Agents

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

## Directory Structure

```text
agents/
├── README.md
├── director/
│   └── AGENT-001.md
├── prompt-engineer/
│   └── AGENT-002.md
├── cinematographer/
│   └── AGENT-003.md
├── writer/
│   └── AGENT-004.md
├── editor/
│   └── AGENT-005.md
└── publisher/
    └── AGENT-006.md
```

## Core Principle

```text
Agents perform creative tasks.
```

Agents 只能执行任务，不能修改 Source of Truth。

---

# Layer 4 — Workflow Templates（工作流层）

## Path

```text
workflows/
```

## Role

Workflows 定义执行顺序。

它负责回答：

```text
任务应该按什么流程完成？
```

## Current Workflows

```text
WORKFLOW-001 — Jump After Work Production Workflow
WORKFLOW-002 — Short Video Prompt Workflow
WORKFLOW-003 — Storyboard to Video Workflow
WORKFLOW-004 — Publishing Workflow
```

## Core Principle

```text
Workflows define execution order.
```

Workflows 不定义角色规则，也不覆盖 Knowledge / Database。

---

# Layer 5 — Operating Commands（操作命令层）

## Path

```text
commands/
```

## Role

Commands 是用户调用 TSOS 的操作入口。

它负责回答：

```text
用户一句话应该触发哪个系统流程？
```

## Current Commands

```text
COMMAND-001 — Run Jump After Work Production
COMMAND-002 — Generate Short Video Prompt
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

## Core Principle

```text
Commands trigger operations.
```

Commands 是入口，不是自由发挥提示词。

---

# Layer 6 — Runtime Docs（运行文档层）

## Path

```text
docs/studio-os/
```

## Role

Runtime Docs 定义 TSOS 如何被 AI 工具读取和运行。

## Current Runtime Docs

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
```

## Core Principle

```text
Runtime Docs explain how to operate TSOS.
```

---

# Layer 7 — Examples（示例层）

## Path

```text
examples/
```

## Role

Examples 展示标准输出格式。

## Current Examples

```text
examples/COMMAND-001-output.md
examples/COMMAND-002-prompt.md
examples/COMMAND-003-storyboard.md
```

## Core Principle

```text
Examples show expected outputs.
```

Examples 只作为格式参考，不覆盖 Source of Truth。

---

# Source of Truth Architecture（事实来源架构）

TSOS 的事实来源规则：

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

## GitHub Owns（GitHub 负责）

```text
Knowledge Nodes
Database Records
Agents
Workflows
Commands
Runtime Docs
Examples
Architecture
Changelog
```

## Notion Owns（Notion 负责）

```text
Visual management
Database view
Production record browsing
Workflow visibility
```

## Important Rule

Notion 不覆盖 GitHub。

如果 Notion 和 GitHub 内容冲突，以 GitHub 为准。

---

# Notion Sync Architecture（Notion 同步架构）

当前 Notion 只同步 Production Database Records：

```text
Character DB
Episode DB
Story DB
Environment DB
Motion DB
Camera DB
Lighting DB
Prompt DB
Asset DB
Project DB
```

以下内容暂不进入 Notion：

```text
Agents
Workflows
Commands
Runtime Docs
Examples
```

原因：

```text
Agents, Workflows, Commands and Runtime Docs are operating instructions.
GitHub is the source of truth for runtime behavior.
```

---

# Runtime Execution Architecture（运行执行架构）

TSOS 标准执行链路：

```text
User Request
↓
Command Routing
↓
Workflow Execution
↓
Agent Behavior
↓
Database References
↓
Knowledge Constraints
↓
Output Generation
↓
Consistency Check
```

---

# Command-to-Workflow Architecture（命令与工作流关系）

| Command | Workflow |
|---|---|
| COMMAND-001 | WORKFLOW-001 |
| COMMAND-002 | WORKFLOW-002 |
| COMMAND-003 | WORKFLOW-001 / WORKFLOW-003 |
| COMMAND-004 | WORKFLOW-004 |
| COMMAND-005 | Checks outputs from all workflows |

---

# Workflow-to-Agent Architecture（工作流与智能体关系）

| Workflow | Agents |
|---|---|
| WORKFLOW-001 | AGENT-001, AGENT-002, AGENT-003, AGENT-004, AGENT-005, AGENT-006 |
| WORKFLOW-002 | AGENT-002 |
| WORKFLOW-003 | AGENT-001, AGENT-002, AGENT-003, AGENT-005 |
| WORKFLOW-004 | AGENT-006 |

---

# Agent Responsibility Architecture（智能体职责架构）

| Agent | Responsibility |
|---|---|
| AGENT-001 | Storyboard planning |
| AGENT-002 | Prompt generation |
| AGENT-003 | Cinematography planning |
| AGENT-004 | Script writing |
| AGENT-005 | Editing planning |
| AGENT-006 | Publishing planning |

---

# Default Production Architecture（默认生产架构）

当前默认生产项目：

```text
PROJ-001 — Jump After Work Pilot Project
```

默认生产链路：

```text
CHAR-001
+
EP-001
+
STORY-001
+
ENV-001
+
MOT-001
+
CAM-001
+
LGT-001
+
PROMPT-001
+
ASSET-001
=
PROJ-001
```

默认执行链路：

```text
PROJ-001
↓
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

---

# Navigation Architecture（导航架构）

Phase 8 增加了索引层，帮助 AI 工具快速定位文件。

当前导航入口：

```text
docs/studio-os/INDEX.md
commands/README.md
workflows/README.md
agents/README.md
examples/README.md
database/README.md
```

推荐读取顺序：

```text
1. README.md
2. ARCHITECTURE.md
3. CHANGELOG.md
4. docs/studio-os/INDEX.md
5. docs/studio-os/RUNTIME.md
6. docs/studio-os/CODEX.md
7. docs/studio-os/COMMANDS.md
8. docs/studio-os/WORKFLOWS.md
9. docs/studio-os/AGENTS.md
```

---

# Safety Architecture（安全架构）

任何 AI 工具不得：

```text
change Jump's core identity
change TiaoTiao Universe worldbuilding
change Brand Language
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
invent unapproved canon
treat Notion as the source of truth
```

正式输出前，应调用：

```text
COMMAND-005 — Run Consistency Check
```

---

# Phase 4–8 Completed Layers（Phase 4–8 已完成层）

| Phase | Layer | Status |
|---|---|---|
| Phase 4 | AI Agents | Completed |
| Phase 5 | Workflow Templates | Completed |
| Phase 6 | Operating Commands | Completed |
| Phase 7 | Runtime Docs and Examples | Completed |
| Phase 8 | Index and Navigation Layer | Completed |

---

# Current Architecture Status（当前架构状态）

```text
TSOS Architecture Status:
Readable
Navigable
Callable
Executable
Extensible
```

现在 TSOS 已经具备：

```text
1. Stable Knowledge Layer
2. Synced Production Database
3. AI Agent Execution Layer
4. Workflow Execution Layer
5. Operating Command Layer
6. Runtime Documentation Layer
7. Example Output Layer
8. Navigation Index Layer
```

---

# Next Architecture Goal（下一阶段架构目标）

Phase 8 完成后，下一阶段可以进入：

```text
Phase 9 — Validation and Test Runs
```

目标：

```text
Run COMMAND-001
Run COMMAND-002
Run COMMAND-003
Run COMMAND-004
Run COMMAND-005
Validate outputs against TSOS Source of Truth
```

---

## Database Layer

Character

Episode

Story

Environment

Motion

Camera

Lighting

Prompt

Asset

Project

---

## AI Layer

Director

Writer

Prompt Engineer

Cinematographer

Editor

Publisher

---

## Workflow

Idea

↓

Story

↓

Storyboard

↓

Prompt

↓

Image

↓

Animation

↓

Edit

↓

Publish

---

## Principle

GitHub is the source of truth.

Notion is the production dashboard.
