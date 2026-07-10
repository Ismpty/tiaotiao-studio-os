# TiaoTiao Studio OS

> AI Native Content Studio Operating System

## Overview

TiaoTiao Studio OS is the single source of truth for all creative production within TiaoTiao Studio.

This repository manages:

- Creator Bible
- Knowledge Base
- Reference Library
- Production Database
- AI Agents
- Prompt System
- Workflow
- Assets
- Documentation

---

# Runtime Entry Points（运行入口）

TiaoTiao Studio OS is designed as an AI Native Studio Operating System.

It is not only a document collection. It contains:

```text
Knowledge Nodes
+
Reference Capture
+
Production Database Records
+
AI Agents
+
Workflow Templates
+
Operating Commands
+
Prompt Runtime Rules
+
Runtime Docs
+
Examples
```

Together, these files allow ChatGPT, Codex, Cursor, Claude or other AI tools to read, understand and execute TiaoTiao Studio production workflows.

---

## Source of Truth（唯一事实来源）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

All canonical rules, records, agents, workflows and commands must be maintained in GitHub first.

Notion is used for visual database management and synchronization, but GitHub remains the final source of truth.

---

## Runtime Docs（运行文档）

Runtime documentation lives in:

```text
docs/studio-os/
```

Current runtime docs:

```text
docs/studio-os/START-HERE.md
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
docs/studio-os/PROMPT-RUNTIME-RULES.md
```

Recommended reading order:

```text
1. docs/studio-os/START-HERE.md
2. docs/studio-os/RUNTIME.md
3. docs/studio-os/CODEX.md
4. docs/studio-os/COMMANDS.md
5. docs/studio-os/WORKFLOWS.md
6. docs/studio-os/AGENTS.md
7. docs/studio-os/PROMPT-RUNTIME-RULES.md
```

---

## Operating Commands（操作命令）

Commands are the main entry points for using TSOS.

Current commands:

```text
COMMAND-001 — Run Little Security Guard Production
COMMAND-002 — Generate Video Prompt Package
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

Command files live in:

```text
commands/
```

Example usage:

```text
Run COMMAND-001.
```

```text
运行 COMMAND-002，生成身份卡 + 故事板 + 通用视频 Prompt。
```

```text
运行 COMMAND-003，生成 45 秒竖屏分镜。
```

```text
运行 COMMAND-004，生成小红书发布包。
```

```text
运行 COMMAND-005，检查这个 Prompt 是否符合跳跳设定。
```

---

## Runtime Layer Structure（运行层结构）

```text
knowledge/
↓
reference/
↓
database/
↓
agents/
↓
workflows/
↓
prompt runtime/
↓
commands/
↓
docs/studio-os/
↓
examples/
```

Meaning:

```text
Knowledge Nodes define rules.
Reference Capture stores external study material before it becomes a rule.
Database Records define production entities.
Agents define creative roles.
Workflows define execution order.
Prompt Runtime defines model-readable prompt execution.
Commands trigger operations.
Runtime Docs explain how to use the system.
Examples show expected outputs.
```

---

## Default Runtime Project（默认运行项目）

Unless otherwise specified, TSOS defaults to:

```text
PROJ-001 — Little Security Guard and His Ancient Friends
```

Default core records:

```text
CHAR-001 — Jump
EP-001 — Little Security Guard and His Ancient Friends
STORY-001 — Museum Night, Relic Friends Wake Up
ENV-001 — AI Museum Night Gallery
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Museum Night Lighting
PROMPT-001 — Little Security Guard Museum Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Little Security Guard and His Ancient Friends
```

---

## Examples（示例输出）

Example outputs live in:

```text
examples/
```

Current examples:

```text
examples/COMMAND-001-output.md
examples/COMMAND-002-prompt.md
examples/COMMAND-003-storyboard.md
```

These files show how command outputs should look in real usage.

---

## Runtime Safety Rule（运行安全规则）

Any AI tool using TSOS must not:

```text
change Jump's core identity
change TiaoTiao Universe worldbuilding
change Brand Language
change a confirmed Custom Subject identity card
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
invent unapproved canon
treat Notion as the source of truth
use raw internal IDs as model-facing prompt language
turn Jump into a humanoid, human or unclothed ordinary pet dog
apply Jump-only dog-form rules to Custom Subject Mode
ignore black-and-white rough pencil storyboard rules
```

Before formal production output, use:

```text
COMMAND-005 — Run Consistency Check
```

---

# Repository Structure（仓库结构）

TiaoTiao Studio OS 当前仓库结构：

```text
tiaotiao-studio-os/
├── README.md
├── ARCHITECTURE.md
├── CHANGELOG.md
│
├── knowledge/
│   ├── README.md
│   ├── style/
│   │   └── STYLE-001.md
│   ├── color/
│   │   └── COLOR-001.md
│   ├── world/
│   │   └── WORLD-001.md
│   ├── emotion/
│   │   └── EMOTION-001.md
│   ├── subject-identity/
│   │   └── SUBJECT-001.md
│   ├── museum-relic-friends/
│   │   └── RELIC-001.md
│   ├── visual-parameters/
│   │   └── VISUALPARAM-001.md
│   ├── scene-blocking/
│   │   └── BLOCKING-001.md
│   ├── camera-language/
│   │   ├── SHOT-001.md
│   │   └── SHOT-002.md
│   ├── transition-language/
│   │   └── TRANSITION-001.md
│   ├── motion-language/
│   │   └── MOTIONLANG-001.md
│   ├── outfit/
│   │   └── OUTFIT-001.md
│   ├── music/
│   │   └── MUSIC-001.md
│   ├── story-formula/
│   │   └── STORYFORMULA-001.md
│   └── brand-language/
│       └── BRAND-001.md
│
├── database/
│   ├── README.md
│   ├── characters/
│   │   └── CHAR-001.md
│   ├── episodes/
│   │   └── EP-001.md
│   ├── stories/
│   │   └── STORY-001.md
│   ├── environments/
│   │   └── ENV-001.md
│   ├── motions/
│   │   └── MOT-001.md
│   ├── cameras/
│   │   └── CAM-001.md
│   ├── lighting/
│   │   └── LGT-001.md
│   ├── prompts/
│   │   └── PROMPT-001.md
│   ├── assets/
│   │   └── ASSET-001.md
│   └── projects/
│       └── PROJ-001.md
│
├── agents/
│   ├── README.md
│   ├── director/
│   │   └── AGENT-001.md
│   ├── prompt-engineer/
│   │   └── AGENT-002.md
│   ├── cinematographer/
│   │   └── AGENT-003.md
│   ├── writer/
│   │   └── AGENT-004.md
│   ├── editor/
│   │   └── AGENT-005.md
│   └── publisher/
│       └── AGENT-006.md
│
├── workflows/
│   ├── README.md
│   ├── WORKFLOW-001.md
│   ├── WORKFLOW-002.md
│   ├── WORKFLOW-003.md
│   └── WORKFLOW-004.md
│
├── commands/
│   ├── README.md
│   ├── COMMAND-001.md
│   ├── COMMAND-002.md
│   ├── COMMAND-003.md
│   ├── COMMAND-004.md
│   └── COMMAND-005.md
│
├── docs/
│   ├── studio-os/
│   │   ├── INDEX.md
│   │   ├── RUNTIME.md
│   │   ├── CODEX.md
│   │   ├── COMMANDS.md
│   │   ├── WORKFLOWS.md
│   │   ├── AGENTS.md
│   │   └── PROMPT-RUNTIME-RULES.md
│   ├── creator-bible/
│   └── changelog/
│
└── examples/
    ├── README.md
    ├── COMMAND-001-output.md
    ├── COMMAND-002-prompt.md
    └── COMMAND-003-storyboard.md
```

---

# System Layer Overview（系统层总览）

TSOS 当前由 8 个核心层组成：

```text
Knowledge Layer
↓
Production Database
↓
AI Agents
↓
Workflow Templates
↓
Prompt Runtime Layer
↓
Operating Commands
↓
Runtime Docs
↓
Examples
```

---

## 1. Knowledge Layer（知识层）

Path：

```text
knowledge/
```

Purpose：

定义长期稳定规则。

包括：

```text
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
VISUALPARAM-001
BLOCKING-001
SHOT-001
SHOT-002
TRANSITION-001
MOTIONLANG-001
OUTFIT-001
MUSIC-001
STORYFORMULA-001
BRAND-001
```

---

## 2. Production Database（生产数据库）

Path：

```text
database/
```

Purpose：

定义具体生产记录。

包括：

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

---

## 3. AI Agents（AI 智能体）

Path：

```text
agents/
```

Purpose：

定义 AI 执行角色。

包括：

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Engineer Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

---

## 4. Workflow Templates（工作流模板）

Path：

```text
workflows/
```

Purpose：

定义任务执行顺序。

包括：

```text
WORKFLOW-001 — Little Security Guard Production Workflow
WORKFLOW-002 — Short Video Prompt Workflow
WORKFLOW-003 — Storyboard to Video Workflow
WORKFLOW-004 — Publishing Workflow
```

---

## 5. Prompt Runtime Layer（提示词运行层）

Path：

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
commands/COMMAND-002.md
commands/COMMAND-005.md
workflows/WORKFLOW-002.md
workflows/WORKFLOW-003.md
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
production/PROJ-001/VIDEO-PROMPTS.md
```

Purpose：

定义模型可执行 Prompt 的结构、可读性和审查方式。

当前标准结构：

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Model-readable check
↓
COMMAND-005 review
```

核心规则：

```text
Internal system language is not model language.
```

内部编号可以用于 GitHub、Notion、Review 和 Changelog。

模型可复制 Prompt 必须写成自然语言，不能依赖裸露内部 ID。

---

## 6. Operating Commands（操作命令）

Path：

```text
commands/
```

Purpose：

定义用户可直接调用的操作入口。

包括：

```text
COMMAND-001 — Run Little Security Guard Production
COMMAND-002 — Generate Video Prompt Package
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

---

## 7. Runtime Docs（运行文档）

Path：

```text
docs/studio-os/
```

Purpose：

定义 TSOS 如何被 ChatGPT / Codex / Cursor / Claude 等 AI 工具读取和运行。

包括：

```text
INDEX.md
RUNTIME.md
CODEX.md
COMMANDS.md
WORKFLOWS.md
AGENTS.md
PROMPT-RUNTIME-RULES.md
```

---

## 8. Examples（示例层）

Path：

```text
examples/
```

Purpose：

展示标准输出格式。

包括：

```text
COMMAND-001-output.md
COMMAND-002-prompt.md
COMMAND-003-storyboard.md
```

---

# Quick Start（快速开始）

Fastest entry point:

```text
docs/studio-os/START-HERE.md
```

## For AI Tools（给 AI 工具）

推荐读取顺序：

```text
1. AGENTS.md
2. CODEX-HANDOFF.md
3. docs/studio-os/START-HERE.md
4. README.md
5. docs/studio-os/RUNTIME.md
6. docs/studio-os/COMMANDS.md
7. docs/studio-os/WORKFLOWS.md
8. docs/studio-os/AGENTS.md
9. docs/studio-os/PROMPT-RUNTIME-RULES.md
```

---

## For Production（用于生产）

完整生产一条《小保安和他的古人朋友们》内容：

```text
Run COMMAND-001.
```

生成短视频 Prompt：

```text
Run COMMAND-002.
```

生成非 Jump 主体的身份卡、故事板和视频 Prompt：

```text
Run COMMAND-002 in Custom Subject Mode.

Subject Type:
Human / Animal / Plant / Object / Scene Subject / Mascot / Other
```

生成分镜：

```text
Run COMMAND-003.
```

生成发布包：

```text
Run COMMAND-004.
```

运行一致性检查：

```text
Run COMMAND-005.
```

当前视频 Prompt 生产结构：

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Model-readable check
↓
COMMAND-005 review
```

---

# Current Default Project（当前默认项目）

```text
PROJ-001 — Little Security Guard and His Ancient Friends
```

默认核心链路：

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

---

# Navigation Entry Points（导航入口）

| Need | File |
|---|---|
| Understand full system | docs/studio-os/INDEX.md |
| Understand runtime behavior | docs/studio-os/RUNTIME.md |
| Guide Codex usage | docs/studio-os/CODEX.md |
| Find command usage | commands/README.md |
| Find workflow usage | workflows/README.md |
| Find agent usage | agents/README.md |
| Understand prompt runtime | docs/studio-os/PROMPT-RUNTIME-RULES.md |
| Generate custom subject identity | knowledge/subject-identity/SUBJECT-001.md |
| Understand AI Museum relic friends | knowledge/museum-relic-friends/RELIC-001.md |
| Find database records | database/README.md |
| Find example outputs | examples/README.md |

---

# Source of Truth（唯一事实来源）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Notion 用于可视化管理 Production Database Records。  
GitHub 负责保存所有正式规则、记录、命令、工作流、智能体、运行文档和示例。

---

# Runtime Safety（运行安全）

任何 AI 工具运行 TSOS 时，不得：

```text
change Jump's core identity
change TiaoTiao Universe worldbuilding
change Brand Language
change a confirmed Custom Subject identity card
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
ignore transition continuity
ignore base visual parameters
ignore scene blocking for complex spatial scenes
invent unapproved canon
treat Notion as the source of truth
use raw internal IDs as model-facing prompt language
turn Jump into a humanoid, human or unclothed ordinary pet dog
apply Jump-only dog-form rules to Custom Subject Mode
ignore black-and-white rough pencil storyboard rules
```

正式输出前，建议运行：

```text
COMMAND-005 — Run Consistency Check
```
## Core Databases

- Character DB
- Episode DB
- Story DB
- Environment DB
- Motion DB
- Camera DB
- Lighting DB
- Prompt DB
- Asset DB
- Project DB

---

## Development Rules

Architecture Freeze

Single Source of Truth

Documentation First

Version Control

Permanent IDs

---

## Current Version

TSOS v1.0
