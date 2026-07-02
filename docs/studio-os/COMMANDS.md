# COMMANDS — TiaoTiao Studio OS Commands Guide（命令使用指南）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件定义 TiaoTiao Studio OS 中所有 Operating Commands 的使用方式。

它的目标是让 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具能够快速理解：

- 当前有哪些命令
- 每个命令负责什么
- 用户说什么时应该调用哪个命令
- 每个命令会读取哪些文件
- 每个命令应该输出什么结果
- 命令之间如何协作
- 如何避免绕过 TSOS Source of Truth

## English

This file defines how Operating Commands should be used inside TiaoTiao Studio OS.

It helps AI tools understand available commands, command routing, required source files, expected outputs and execution rules.

---

# Core Principle（核心原则）

Commands 是 TSOS 的操作入口。

```text
User Request
↓
Operating Command
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
↓
Consistency Check
```

任何正式任务都应该优先通过 Command 路由，而不是临时自由发挥。

---

# Current Commands（当前命令）

当前 TSOS 已定义以下 5 个核心命令：

```text
COMMAND-001 — Run Jump After Work Production
COMMAND-002 — Generate Short Video Prompt
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

---

# Command Index（命令索引）

| Command | Name | Primary Use |
|---|---|---|
| COMMAND-001 | Run Jump After Work Production | 启动完整生产流程 |
| COMMAND-002 | Generate Short Video Prompt | 生成图片 / 视频 Prompt |
| COMMAND-003 | Generate Storyboard | 生成分镜 |
| COMMAND-004 | Generate Publishing Package | 生成发布包 |
| COMMAND-005 | Run Consistency Check | 运行一致性检查 |

---

# COMMAND-001 — Run Jump After Work Production

## File

```text
commands/COMMAND-001.md
```

## 中文说明

COMMAND-001 用于启动《跳跳下班啦》的完整生产流程。

它会串联：

```text
Project Brief
Storyboard
Prompt
Cinematography
Script
Editing
Publishing
Final Consistency Check
```

## When to Use（什么时候使用）

当用户说：

```text
运行完整生产流程
做一条《跳跳下班啦》视频
生成完整项目包
从分镜到发布都做一遍
Run Jump After Work production
```

应该调用：

```text
COMMAND-001
```

## Default Workflow

```text
WORKFLOW-001 — Jump After Work Production Workflow
```

## Default Agents

```text
AGENT-001
AGENT-002
AGENT-003
AGENT-004
AGENT-005
AGENT-006
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

## Standard User Input

```text
Run COMMAND-001.
```

```text
运行 COMMAND-001，启动《跳跳下班啦》完整生产流程。
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
9. Next Production Actions
```

---

# COMMAND-002 — Generate Short Video Prompt

## File

```text
commands/COMMAND-002.md
```

## 中文说明

COMMAND-002 用于生成 AI 图片、视频、封面、角色、环境或镜头 Prompt。

它的重点是：

```text
把 TSOS Source Records 转化为可执行 Prompt
```

而不是重新设计角色或重新写故事。

## When to Use（什么时候使用）

当用户说：

```text
生成视频 Prompt
生成 Kling Prompt
生成 Veo Prompt
生成小红书 9:16 视频提示词
生成封面图 Prompt
生成角色一致性 Prompt
生成短视频 Prompt
```

应该调用：

```text
COMMAND-002
```

## Default Workflow

```text
WORKFLOW-002 — Short Video Prompt Workflow
```

## Default Agent

```text
AGENT-002 — Prompt Agent
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

## Standard User Input

```text
Run COMMAND-002.
```

```text
运行 COMMAND-002，生成小红书 9:16 Kling 视频 Prompt。
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

任何 Prompt 必须包含：

```text
ASSET-001
Negative Prompt
Consistency Checklist
```

---

# COMMAND-003 — Generate Storyboard

## File

```text
commands/COMMAND-003.md
```

## 中文说明

COMMAND-003 用于生成分镜方案。

它会把：

```text
Project
Story
Character
Environment
Motion
Camera
Lighting
Asset
Knowledge Nodes
```

转化为可执行的镜头结构。

## When to Use（什么时候使用）

当用户说：

```text
生成分镜
拆分镜头
做 45 秒小红书分镜
做 6 镜头结构
生成短视频脚本分镜
把这个故事拆成镜头
```

应该调用：

```text
COMMAND-003
```

## Default Workflow

```text
WORKFLOW-001 — Jump After Work Production Workflow
```

只执行：

```text
Stage 2 — Storyboard Planning
```

也可以配合：

```text
WORKFLOW-003 — Storyboard to Video Workflow
```

## Default Agent

```text
AGENT-001 — Storyboard Agent
```

## Required Records

```text
PROJ-001
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
```

## Standard User Input

```text
Run COMMAND-003.
```

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

## Expected Output

```text
1. Storyboard Summary
2. Story Beat Breakdown
3. Shot List
4. Shot Details
5. Camera / Motion / Lighting Mapping
6. Prompt Notes
7. Continuity Checklist
8. Next Production Actions
```

## Default Shot Structure

```text
Shot 1 — Work Ending
Shot 2 — Decision Moment
Shot 3 — Packing Up
Shot 4 — Walking Out
Shot 5 — Door Exit
Shot 6 — Warm Ending
```

---

# COMMAND-004 — Generate Publishing Package

## File

```text
commands/COMMAND-004.md
```

## 中文说明

COMMAND-004 用于生成平台发布包。

它不重新创作视频内容，只负责生成：

```text
标题
正文
标签
封面文案
发布时间建议
发布前检查清单
发布后复盘模板
```

## When to Use（什么时候使用）

当用户说：

```text
生成发布包
生成小红书标题和正文
生成抖音发布文案
生成视频号发布方案
生成 YouTube Shorts 标题
生成标签
生成封面文案
```

应该调用：

```text
COMMAND-004
```

## Default Workflow

```text
WORKFLOW-004 — Publishing Workflow
```

## Default Agent

```text
AGENT-006 — Publishing Agent
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

## Standard User Input

```text
Run COMMAND-004.
```

```text
运行 COMMAND-004，为《跳跳下班啦》生成小红书发布包。
```

## Expected Output

```text
1. Publishing Summary
2. Platform Strategy
3. Title Options
4. Caption / Description
5. Hashtag Set
6. Cover Text Suggestions
7. Publishing Time Suggestion
8. Pre-Publish Checklist
9. Publishing Record
10. Post-Publish Review Template
11. Brand Safety Check
```

## Important Rule

COMMAND-004 必须避免：

```text
标题党
焦虑表达
强营销腔
虚假承诺
无关标签
```

---

# COMMAND-005 — Run Consistency Check

## File

```text
commands/COMMAND-005.md
```

## 中文说明

COMMAND-005 用于检查任何输出是否符合 TSOS Source of Truth。

它可以检查：

```text
Storyboard
Prompt
Script
Editing Plan
Publishing Package
Generated Image
Generated Video
Project Package
```

## When to Use（什么时候使用）

当用户说：

```text
检查是否符合设定
检查这个 Prompt
检查这个封面有没有偏离跳跳
检查一致性
检查视频是否符合 TSOS
运行一致性检查
```

应该调用：

```text
COMMAND-005
```

## Default Strictness

```text
Strict
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

## Required Knowledge

```text
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
MOTIONLANG-001
OUTFIT-001
MUSIC-001
STORYFORMULA-001
BRAND-001
```

## Standard User Input

```text
Run COMMAND-005.
```

```text
运行 COMMAND-005，检查这个 Kling Prompt 是否符合跳跳设定。
```

## Expected Output

```text
1. Consistency Summary
2. Character Consistency Check
3. World Consistency Check
4. Visual Style Check
5. Color Check
6. Emotion Check
7. Motion Check
8. Camera Check
9. Lighting Check
10. Story / Brand Check
11. Workflow Compliance Check
12. Issue List
13. Fix Suggestions
14. Final Result
```

## Final Result Must Be

```text
PASS
```

or

```text
FAIL
```

or

```text
PASS WITH MINOR FIXES
```

---

# Command Routing Table（命令路由表）

| User Request | Command |
|---|---|
| 做完整一条《跳跳下班啦》 | COMMAND-001 |
| 从分镜到发布都生成 | COMMAND-001 |
| 生成 AI 视频 Prompt | COMMAND-002 |
| 生成 Kling / Veo / Runway Prompt | COMMAND-002 |
| 生成 Midjourney / Flux 图片 Prompt | COMMAND-002 |
| 生成封面 Prompt | COMMAND-002 |
| 生成分镜 | COMMAND-003 |
| 拆镜头 | COMMAND-003 |
| 做 Storyboard | COMMAND-003 |
| 生成发布文案 | COMMAND-004 |
| 生成标题、正文、标签 | COMMAND-004 |
| 生成小红书发布包 | COMMAND-004 |
| 检查是否偏离设定 | COMMAND-005 |
| 检查 Prompt / 视频 / 图片 | COMMAND-005 |
| 做一致性检查 | COMMAND-005 |

---

# Command Selection Rules（命令选择规则）

## If the user asks for complete production

Use：

```text
COMMAND-001
```

## If the user asks for prompt

Use：

```text
COMMAND-002
```

## If the user asks for storyboard or shots

Use：

```text
COMMAND-003
```

## If the user asks for publishing

Use：

```text
COMMAND-004
```

## If the user asks for review or check

Use：

```text
COMMAND-005
```

---

# Multi-Command Usage（多命令组合）

有些任务需要连续调用多个 Command。

## Full Video Production

```text
COMMAND-001
```

内部会串联所有流程。

---

## Storyboard to Video Prompt

```text
COMMAND-003
↓
COMMAND-002
↓
COMMAND-005
```

---

## Video Prompt to Publishing Package

```text
COMMAND-002
↓
COMMAND-005
↓
COMMAND-004
```

---

## Final Pre-Publish Check

```text
COMMAND-004
↓
COMMAND-005
```

---

# Standard Command Response Format（标准命令响应格式）

当执行任何 Command 时，输出应包含：

```text
# COMMAND-XXX Output

## Source Records

## Execution Summary

## Output

## Consistency Checklist

## Next Actions
```

对于复杂 Command，可以使用该 Command 自己定义的详细结构。

---

# Source of Truth Rules（事实来源规则）

所有 Command 必须遵守：

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Command 不得以 Notion 内容覆盖 GitHub 内容。

---

# Command Safety Rules（命令安全规则）

所有 Command 都不得：

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

# Jump Command Rules（Jump 命令规则）

任何涉及 Jump 的 Command，都必须保持：

```text
Jump = anthropomorphic fluffy female dog programmer
```

必须引用：

```text
CHAR-001
ASSET-001
OUTFIT-001
COLOR-001
BRAND-001
```

---

# Prompt Command Rules（Prompt 命令规则）

任何 Prompt Command 都必须包含：

```text
Source Records
Target Model
Base Prompt
Model-Specific Prompt
Negative Prompt
Consistency Checklist
Usage Notes
```

---

# Publishing Command Rules（发布命令规则）

任何 Publishing Command 都必须避免：

```text
标题党
焦虑表达
强营销
虚假承诺
无关标签
```

必须输出：

```text
Pre-Publish Checklist
Post-Publish Review Template
Brand Safety Check
```

---

# Consistency Command Rules（一致性命令规则）

COMMAND-005 是所有正式输出的最终检查入口。

任何正式产出前，都应该可以执行：

```text
Run COMMAND-005.
```

---

# Example Runtime Flows（运行示例）

## Example 1 — Generate Storyboard

User：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

System：

```text
Read COMMAND-003
Read AGENT-001
Read PROJ-001
Read required Database Records
Read required Knowledge Nodes
Output 6-shot storyboard
Run continuity checklist
```

---

## Example 2 — Generate Kling Prompt

User：

```text
运行 COMMAND-002，生成 Kling 视频 Prompt。
```

System：

```text
Read COMMAND-002
Read WORKFLOW-002
Read AGENT-002
Read PROMPT-001
Read CHAR-001
Read ASSET-001
Generate video prompt
Generate negative prompt
Run consistency checklist
```

---

## Example 3 — Generate Publishing Package

User：

```text
运行 COMMAND-004，生成小红书发布包。
```

System：

```text
Read COMMAND-004
Read WORKFLOW-004
Read AGENT-006
Read BRAND-001
Generate title, caption, hashtags, cover text
Run brand safety check
```

---

# Command Failure Handling（命令失败处理）

如果用户请求与 TSOS 冲突，Command 必须输出：

```text
Issue Found:
[问题描述]

Source of Truth:
[相关文件]

Result:
Cannot apply this change under current TSOS rules.

Suggested Alternative:
[符合 TSOS 的替代方案]
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial commands guide |