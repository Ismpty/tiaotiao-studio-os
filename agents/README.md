# Agents — AI Agents Index（AI 智能体索引）

> Navigation Index（导航索引）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 `agents/` 目录的索引文件。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- 当前有哪些 AI Agents
- 每个 Agent 的职责是什么
- 每个 Agent 放在哪个目录
- 每个 Agent 应该什么时候使用
- 每个 Agent 会读取哪些 Database Records
- 每个 Agent 会参考哪些 Knowledge Nodes
- 每个 Agent 与 Commands / Workflows 的关系
- 每个 Agent 的输出边界是什么

## English

This file is the index for the `agents/` directory.

It helps AI tools understand available AI agents, their responsibilities, file locations, related commands, related workflows and expected outputs.

---

# Agent Layer Role（智能体层作用）

Agents 是 TSOS 的执行角色层。

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

Commands 决定用户要做什么。  
Workflows 决定任务按什么顺序执行。  
Agents 决定每一步由哪个专业角色完成。

---

# Current Agents（当前智能体）

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Engineer Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

---

# Agent Index（智能体索引）

| Agent | Name | Role Group | File | Primary Use |
|---|---|---|---|---|
| AGENT-001 | Storyboard Agent | Director | director/AGENT-001.md | 分镜规划 |
| AGENT-002 | Prompt Engineer Agent | Prompt Engineer | prompt-engineer/AGENT-002.md | 模型可读提示词包生成 |
| AGENT-003 | Cinematography Agent | Cinematographer | cinematographer/AGENT-003.md | 摄影方案 |
| AGENT-004 | Script Agent | Writer | writer/AGENT-004.md | 脚本文案 |
| AGENT-005 | Editing Agent | Editor | editor/AGENT-005.md | 剪辑方案 |
| AGENT-006 | Publishing Agent | Publisher | publisher/AGENT-006.md | 发布方案 |

---

# Directory Structure（目录结构）

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

---

# AGENT-001 — Storyboard Agent

## File

```text
agents/director/AGENT-001.md
```

## Role Group

```text
Director
```

## 中文说明

AGENT-001 是分镜智能体。

它负责把 Project、Story、Character、Environment、Motion、Camera、Lighting、Asset 和 Knowledge Nodes 转化为可生产的分镜方案。

## Use When（使用场景）

当用户需要：

```text
生成分镜
拆分镜头
设计镜头顺序
生成 6 镜头结构
把故事拆成短视频镜头
做 Storyboard
```

## Related Commands

```text
COMMAND-001
COMMAND-003
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
WORKFLOW-003
```

## Expected Output

```text
Project Summary
Story Beat Breakdown
Shot List
Storyboard Prompt
Camera / Motion / Lighting Mapping
Storyboard Color Annotation Plan
Continuity Checklist
Production Notes
```

---

# AGENT-002 — Prompt Engineer Agent

## File

```text
agents/prompt-engineer/AGENT-002.md
```

## Role Group

```text
Prompt Engineer
```

## 中文说明

AGENT-002 是提示词工程智能体。

它负责把 Database Records、Knowledge Nodes 和其他 Agent 输出转化为模型可读的视频提示词包。

## Use When（使用场景）

当用户需要：

```text
生成视频 Prompt
生成 Identity Card Prompt
生成 Storyboard Prompt
生成 Universal Video Prompt
生成 Jimeng / Veo / Runway 视频执行 Prompt
检查模型可读性
```

## Related Commands

```text
COMMAND-001
COMMAND-002
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
WORKFLOW-002
WORKFLOW-003
```

## Expected Output

```text
Prompt Purpose
Source Records
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
Usage Notes
```

---

# AGENT-003 — Cinematography Agent

## File

```text
agents/cinematographer/AGENT-003.md
```

## Role Group

```text
Cinematographer
```

## 中文说明

AGENT-003 是摄影指导智能体。

它负责把 Camera、Lighting、Style、Environment、Story 和 Project 记录转化为可执行的摄影方案。

## Use When（使用场景）

当用户需要：

```text
设计镜头语言
设计摄影构图
设计机位
设计焦段
设计运镜
设计景深
设计灯光关系
增强视频 Prompt 的电影感
```

## Related Commands

```text
COMMAND-001
COMMAND-002
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
WORKFLOW-003
```

## Expected Output

```text
Cinematography Summary
Visual Strategy
Lens Plan
Camera Movement Plan
Composition Plan
Lighting Plan
Shot-by-Shot Cinematography Notes
Cinematic Consistency Checklist
AI Visual Prompt Add-ons
```

---

# AGENT-004 — Script Agent

## File

```text
agents/writer/AGENT-004.md
```

## Role Group

```text
Writer
```

## 中文说明

AGENT-004 是脚本智能体。

它负责把 Project、Story、Episode、Character、Knowledge Nodes 和其他 Agent 输出转化为视频脚本、旁白、字幕、对白和节奏结构。

## Use When（使用场景）

当用户需要：

```text
生成短视频脚本
生成旁白
生成字幕
生成开场 Hook
生成结尾金句
生成对白
生成内心独白
把故事变成文案
```

## Related Commands

```text
COMMAND-001
COMMAND-004
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
```

## Expected Output

```text
Script Summary
Story Beat Structure
Opening Hook
Voiceover Script
Caption Script
Dialogue / Inner Voice
Ending Line
Tone Check
Production Notes
```

---

# AGENT-005 — Editing Agent

## File

```text
agents/editor/AGENT-005.md
```

## Role Group

```text
Editor
```

## 中文说明

AGENT-005 是剪辑智能体。

它负责把 Project、Storyboard、Script、Cinematography、Prompt 和 Music 相关记录转化为可执行的剪辑方案。

## Use When（使用场景）

当用户需要：

```text
生成剪辑方案
设计剪辑节奏
设计镜头时长
设计转场
设计字幕时间点
设计旁白时间点
设计音乐进入和退出
生成时间线
```

## Related Commands

```text
COMMAND-001
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
WORKFLOW-003
```

## Expected Output

```text
Editing Summary
Timeline Structure
Shot Duration Plan
Transition Plan
Caption Timing
Voiceover Timing
Music / Sound Plan
Emotional Rhythm
Editing Checklist
Export Notes
```

---

# AGENT-006 — Publishing Agent

## File

```text
agents/publisher/AGENT-006.md
```

## Role Group

```text
Publisher
```

## 中文说明

AGENT-006 是发布智能体。

它负责把 Project、Script、Editing、Prompt、Brand Language 和平台规则转化为可执行的发布方案。

## Use When（使用场景）

当用户需要：

```text
生成发布标题
生成视频简介
生成平台标签
生成封面文案
生成小红书发布包
生成抖音发布包
生成 YouTube Shorts 发布包
生成发布时间建议
生成发布前检查清单
生成发布后复盘模板
```

## Related Commands

```text
COMMAND-001
COMMAND-004
COMMAND-005
```

## Related Workflows

```text
WORKFLOW-001
WORKFLOW-004
```

## Expected Output

```text
Publishing Summary
Platform Strategy
Title Options
Description / Caption
Hashtag Set
Cover Text Suggestions
Publishing Time Suggestion
Pre-Publish Checklist
Post-Publish Review Metrics
Brand Safety Check
```

---

# Agent Collaboration Chain（智能体协作链路）

完整生产链路：

```text
AGENT-001 Storyboard Agent
↓
AGENT-002 Prompt Engineer Agent
↓
AGENT-003 Cinematography Agent
↓
AGENT-004 Script Agent
↓
AGENT-005 Editing Agent
↓
AGENT-006 Publishing Agent
```

---

# Agent and Command Mapping（智能体与命令映射）

| Command | Agents |
|---|---|
| COMMAND-001 | AGENT-001, AGENT-002, AGENT-003, AGENT-004, AGENT-005, AGENT-006 |
| COMMAND-002 | AGENT-002 |
| COMMAND-003 | AGENT-001 |
| COMMAND-004 | AGENT-006 |
| COMMAND-005 | Checks outputs from all Agents |

---

# Agent and Workflow Mapping（智能体与工作流映射）

| Workflow | Agents |
|---|---|
| WORKFLOW-001 | AGENT-001, AGENT-002, AGENT-003, AGENT-004, AGENT-005, AGENT-006 |
| WORKFLOW-002 | AGENT-002 |
| WORKFLOW-003 | AGENT-001, AGENT-002, AGENT-003, AGENT-005 |
| WORKFLOW-004 | AGENT-006 |

---

# Required Default Database Records（默认数据库记录）

大多数 Agent 默认会引用以下 Production Records：

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

# Required Default Knowledge Nodes（默认知识节点）

大多数 Agent 默认会引用以下 Knowledge Nodes：

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

---

# Agent Source of Truth Rule（智能体事实来源规则）

Agents 只能执行任务，不能修改 Source of Truth。

Agents 不得覆盖：

```text
Knowledge Nodes
Database Records
Brand Language
Character Identity
Worldbuilding
Frozen Roadmap
```

如果 Agent 输出与 Source of Truth 冲突，必须以 Source of Truth 为准。

---

# Agent Safety Rules（智能体安全规则）

所有 Agents 都不得：

```text
修改 Jump 核心身份
修改 TiaoTiao Universe 世界观
修改 Brand Language
绕过 ASSET-001
绕过 Knowledge Nodes
绕过 Database Records
临时新增未确认设定
改变文件命名规则
改变目录结构
改变 Frozen Roadmap
```

---

# Jump Agent Rule（Jump 智能体规则）

任何 Agent 只要涉及 Jump，都必须保持：

```text
Jump = real dog-form character wearing programmer-style dog clothes
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

# Standard Agent Output Rule（标准输出规则）

所有 Agent 输出必须：

```text
[ ] 可执行
[ ] 可复制
[ ] 可追溯
[ ] 有明确来源
[ ] 不空泛
[ ] 不修改核心设定
[ ] 不绕过 ASSET-001
[ ] 不绕过 Knowledge Nodes
[ ] 不绕过 Database Records
[ ] 可以进入下一阶段
```

---

# Related Runtime Docs（相关运行文档）

执行 Agents 时应参考：

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/AGENTS.md
```

---

# Related Directories（相关目录）

```text
agents/
commands/
workflows/
database/
knowledge/
examples/
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial agents index |
