# TiaoTiao Studio OS

> AI Native Content Studio Operating System

## Overview

TiaoTiao Studio OS is the single source of truth for all creative production within TiaoTiao Studio.

This repository manages:

- Creator Bible
- Knowledge Base
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
Production Database Records
+
AI Agents
+
Workflow Templates
+
Operating Commands
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
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
```

Recommended reading order:

```text
1. docs/studio-os/RUNTIME.md
2. docs/studio-os/CODEX.md
3. docs/studio-os/COMMANDS.md
4. docs/studio-os/WORKFLOWS.md
5. docs/studio-os/AGENTS.md
```

---

## Operating Commands（操作命令）

Commands are the main entry points for using TSOS.

Current commands:

```text
COMMAND-001 — Run Jump After Work Production
COMMAND-002 — Generate Short Video Prompt
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
运行 COMMAND-002，生成小红书 9:16 Kling 视频 Prompt。
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

Meaning:

```text
Knowledge Nodes define rules.
Database Records define production entities.
Agents define creative roles.
Workflows define execution order.
Commands trigger operations.
Runtime Docs explain how to use the system.
Examples show expected outputs.
```

---

## Default Runtime Project（默认运行项目）

Unless otherwise specified, TSOS defaults to:

```text
PROJ-001 — Jump After Work Pilot Project
```

Default core records:

```text
CHAR-001 — Jump
EP-001 — Jump After Work
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Jump After Work Pilot Project
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
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
invent unapproved canon
treat Notion as the source of truth
```

Before formal production output, use:

```text
COMMAND-005 — Run Consistency Check
```

---

## Repository Structure

```
docs/
database/
agents/
skills/
templates/
workflows/
archive/
```

---

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
