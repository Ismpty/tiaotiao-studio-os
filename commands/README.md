# Commands — Operating Commands Index（操作命令索引）

> Navigation Index（导航索引）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 `commands/` 目录的索引文件。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- 当前有哪些 Operating Commands
- 每个 Command 的用途是什么
- 用户提出什么需求时应该调用哪个 Command
- 每个 Command 对应哪些 Workflow / Agent
- 每个 Command 的标准输出是什么

## English

This file is the index for the `commands/` directory.

It helps AI tools understand available operating commands, command routing, related workflows, related agents and expected outputs.

---

# Command Layer Role（命令层作用）

Commands 是 TSOS 的操作入口。

```text
User Request
↓
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

Commands 不负责直接改写 Source of Truth。  
Commands 负责启动正确的执行流程。

---

# Current Commands（当前命令）

```text
COMMAND-001 — Run Little Security Guard Production
COMMAND-002 — Generate Video Prompt Package
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

---

# Command Index（命令索引）

| Command | Name | File | Primary Use |
|---|---|---|---|
| COMMAND-001 | Run Little Security Guard Production | COMMAND-001.md | 启动完整生产流程 |
| COMMAND-002 | Generate Video Prompt Package | COMMAND-002.md | 生成身份卡 / 故事板 / 通用视频 Prompt |
| COMMAND-003 | Generate Storyboard | COMMAND-003.md | 生成分镜 |
| COMMAND-004 | Generate Publishing Package | COMMAND-004.md | 生成发布包 |
| COMMAND-005 | Run Consistency Check | COMMAND-005.md | 检查一致性 |

---

# COMMAND-001 — Run Little Security Guard Production

## File

```text
commands/COMMAND-001.md
```

## Use When（使用场景）

当用户需要完整生产一条《小保安和他的古人朋友们》内容时使用。

示例：

```text
Run COMMAND-001.
```

```text
运行 COMMAND-001，启动《小保安和他的古人朋友们》完整生产流程。
```

```text
做一条完整的小保安和古人朋友视频，从分镜到发布包。
```

## Calls（调用）

```text
WORKFLOW-001
AGENT-001
AGENT-002
AGENT-003
AGENT-004
AGENT-005
AGENT-006
```

## Expected Output（预期输出）

```text
Project Brief
Storyboard Output
Prompt Output
Cinematography Output
Script Output
Editing Output
Publishing Output
Final Consistency Checklist
Next Production Actions
```

---

# COMMAND-002 — Generate Video Prompt Package

## File

```text
commands/COMMAND-002.md
```

## Use When（使用场景）

当用户需要生成视频生产提示词包时使用。

示例：

```text
Run COMMAND-002.
```

```text
运行 COMMAND-002，生成身份卡 + 故事板 + 通用视频 Prompt。
```

```text
运行 COMMAND-002 in Custom Subject Mode，为人物、动物、植物、产品或场景主体生成身份卡 + 故事板 + 通用视频 Prompt。
```

```text
给这个分镜生成可逐镜头执行的 Universal Video Prompt。
```

## Calls（调用）

```text
WORKFLOW-002
AGENT-002
```

## Expected Output（预期输出）

```text
Prompt Purpose
Source References
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Runtime Usage Example
Model-readable Check
COMMAND-005 Review
Usage Notes
```

## Required Rule（必要规则）

必须包含：

```text
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
```

---

# COMMAND-003 — Generate Storyboard

## File

```text
commands/COMMAND-003.md
```

## Use When（使用场景）

当用户需要分镜、镜头拆解或短视频镜头结构时使用。

示例：

```text
Run COMMAND-003.
```

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

```text
把这个故事拆成 6 个镜头。
```

## Calls（调用）

```text
WORKFLOW-001
AGENT-001
```

可选参考：

```text
WORKFLOW-003
```

## Expected Output（预期输出）

```text
Storyboard Summary
Story Beat Breakdown
Shot List
Shot Details
Camera / Motion / Lighting Mapping
Prompt Notes
Continuity Checklist
Next Production Actions
```

---

# COMMAND-004 — Generate Publishing Package

## File

```text
commands/COMMAND-004.md
```

## Use When（使用场景）

当用户需要发布标题、正文、标签、封面文案或发布检查清单时使用。

示例：

```text
Run COMMAND-004.
```

```text
运行 COMMAND-004，生成小红书发布包。
```

```text
给这条视频生成 YouTube Shorts 标题和描述。
```

## Calls（调用）

```text
WORKFLOW-004
AGENT-006
```

## Expected Output（预期输出）

```text
Publishing Summary
Platform Strategy
Title Options
Caption / Description
Hashtag Set
Cover Text Suggestions
Publishing Time Suggestion
Pre-Publish Checklist
Publishing Record
Post-Publish Review Template
Brand Safety Check
```

---

# COMMAND-005 — Run Consistency Check

## File

```text
commands/COMMAND-005.md
```

## Use When（使用场景）

当用户需要检查输出是否符合 TSOS、Jump 设定、品牌语言或项目规范时使用。

示例：

```text
Run COMMAND-005.
```

```text
运行 COMMAND-005，检查这个 Prompt 是否符合跳跳设定。
```

```text
检查这个封面有没有偏离 Jump 的角色一致性。
```

## Calls（调用）

```text
Checks all relevant Database Records
Checks all relevant Knowledge Nodes
Checks Subject Mode and Custom Subject identity cards when applicable
Checks Agent / Workflow / Command compliance
```

## Expected Output（预期输出）

```text
Consistency Summary
Subject Mode Check
Subject / Character Consistency Check
World Consistency Check
Visual Style Check
Color Check
Emotion Check
Motion Check
Camera Check
Lighting Check
Story / Brand Check
Workflow Compliance Check
Issue List
Fix Suggestions
Final Result
```

## Final Result（最终结果）

必须输出：

```text
PASS
```

或：

```text
FAIL
```

或：

```text
PASS WITH MINOR FIXES
```

---

# Command Routing Table（命令路由表）

| User Request | Command |
|---|---|
| 完整做一条视频 | COMMAND-001 |
| 从分镜到发布都生成 | COMMAND-001 |
| 生成视频 Prompt Package | COMMAND-002 |
| 生成身份卡 + 故事板 + 通用视频 Prompt | COMMAND-002 |
| 生成 Jimeng / Veo / Runway 视频执行 Prompt | COMMAND-002 |
| 生成分镜 | COMMAND-003 |
| 拆镜头 | COMMAND-003 |
| 做 Storyboard | COMMAND-003 |
| 生成标题正文标签 | COMMAND-004 |
| 生成小红书发布包 | COMMAND-004 |
| 生成 YouTube Shorts 发布包 | COMMAND-004 |
| 检查一致性 | COMMAND-005 |
| 检查是否偏离跳跳设定 | COMMAND-005 |
| 检查 Prompt / 图片 / 视频 | COMMAND-005 |

---

# Command and Workflow Mapping（命令与工作流映射）

| Command | Workflow |
|---|---|
| COMMAND-001 | WORKFLOW-001 |
| COMMAND-002 | WORKFLOW-002 |
| COMMAND-003 | WORKFLOW-001 / WORKFLOW-003 |
| COMMAND-004 | WORKFLOW-004 |
| COMMAND-005 | Checks WORKFLOW-001 / WORKFLOW-002 / WORKFLOW-003 / WORKFLOW-004 outputs |

---

# Command and Agent Mapping（命令与智能体映射）

| Command | Agent |
|---|---|
| COMMAND-001 | AGENT-001 / AGENT-002 / AGENT-003 / AGENT-004 / AGENT-005 / AGENT-006 |
| COMMAND-002 | AGENT-002 |
| COMMAND-003 | AGENT-001 |
| COMMAND-004 | AGENT-006 |
| COMMAND-005 | Checks outputs from all Agents |

---

# Source of Truth Rule（事实来源规则）

所有 Commands 必须遵守：

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Commands 不得以 Notion 内容覆盖 GitHub 内容。

---

# Command Safety Rules（命令安全规则）

所有 Commands 都不得：

```text
修改 Jump 核心身份
修改 TiaoTiao Universe 世界观
修改 Brand Language
绕过 ASSET-001
绕过 Knowledge Nodes
绕过 Database Records
跳过一致性检查
临时发明未确认设定
改变命名规则
改变目录结构
```

---

# Required Runtime Docs（相关运行文档）

执行 Commands 时应参考：

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/COMMANDS.md
```

---

# Related Directories（相关目录）

```text
commands/
workflows/
agents/
database/
knowledge/
examples/
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial commands index |
