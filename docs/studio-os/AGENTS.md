# AGENTS — TiaoTiao Studio OS Agents Guide（智能体使用指南）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件定义 TiaoTiao Studio OS 中所有 AI Agents 的使用方式。

它的目标是让 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具能够快速理解：

- 当前有哪些 Agents
- 每个 Agent 负责什么
- 每个 Agent 应该读取哪些文件
- 每个 Agent 应该输出什么内容
- Agent 之间如何协作
- Agent 与 Commands、Workflows、Database Records、Knowledge Nodes 的关系
- Agent 不能做什么
- 如何避免 Agent 随意改写角色、世界观和品牌方向

## English

This file defines how AI Agents should be used inside TiaoTiao Studio OS.

It helps AI tools understand agent roles, required source files, expected outputs, collaboration rules and boundaries.

---

# Core Principle（核心原则）

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

Command 决定要做什么。  
Workflow 决定按什么顺序做。  
Agent 决定由谁来做。  
Database Records 和 Knowledge Nodes 决定不能偏离什么。

---

# Current Agents（当前智能体）

当前 TSOS 已定义以下 6 个核心 Agents：

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

---

# Agent Index（智能体索引）

| Agent | Name | Role Group | Primary Use |
|---|---|---|---|
| AGENT-001 | Storyboard Agent | Director | 分镜规划 |
| AGENT-002 | Prompt Agent | Prompt Engineer | 提示词生成 |
| AGENT-003 | Cinematography Agent | Cinematographer | 摄影方案 |
| AGENT-004 | Script Agent | Writer | 脚本文案 |
| AGENT-005 | Editing Agent | Editor | 剪辑方案 |
| AGENT-006 | Publishing Agent | Publisher | 发布方案 |

---

# AGENT-001 — Storyboard Agent

## File

```text
agents/director/AGENT-001.md
```

## 中文说明

AGENT-001 是分镜智能体。

它负责把 TSOS 中的 Project、Story、Character、Environment、Motion、Camera、Lighting、Asset 和 Knowledge Nodes 转化为可生产的分镜方案。

它不负责重新创造世界观，不修改 Jump 角色设定，不改变品牌方向。

## When to Use（什么时候使用）

当用户需要：

```text
生成分镜
拆分镜头
设计镜头顺序
生成 6 镜头结构
把故事拆成短视频镜头
做 Storyboard
```

应该使用：

```text
AGENT-001
```

通常由以下命令调用：

```text
COMMAND-003
```

也会被以下工作流调用：

```text
WORKFLOW-001
WORKFLOW-003
```

## Required Records

```text
PROJ-001
PROMPT-001
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
ASSET-001
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

## Expected Output

```text
Project Summary
Story Beat Breakdown
Shot List
Shot-by-Shot Prompt
Camera / Motion / Lighting Mapping
Negative Prompt
Continuity Checklist
Production Notes
```

## Must Do

```text
[ ] 每个镜头必须有叙事功能
[ ] 每个镜头必须引用 TSOS 记录
[ ] 必须保持 Jump 角色一致
[ ] 必须引用 ASSET-001
[ ] 必须符合 STORYFORMULA-001
[ ] 必须符合 BRAND-001
```

## Never Do

```text
不得修改 Jump 的核心身份
不得新增未经确认的世界观
不得只输出漂亮画面而没有故事逻辑
不得跳过一致性检查
不得忽略角色参考资产
```

---

# AGENT-002 — Prompt Agent

## File

```text
agents/prompt-engineer/AGENT-002.md
```

## 中文说明

AGENT-002 是提示词工程智能体。

它负责把 TSOS 中的 Database Records、Knowledge Nodes 和其他 Agent 输出转化为可执行的 AI 图片、视频、封面、分镜和角色一致性 Prompt。

它不负责重新设计角色，也不负责修改故事方向。

## When to Use（什么时候使用）

当用户需要：

```text
生成视频 Prompt
生成图片 Prompt
生成 Kling Prompt
生成 Veo Prompt
生成 Runway Prompt
生成 Midjourney Prompt
生成 Flux / ComfyUI Prompt
生成封面 Prompt
生成角色一致性 Prompt
```

应该使用：

```text
AGENT-002
```

通常由以下命令调用：

```text
COMMAND-002
```

也会被以下工作流调用：

```text
WORKFLOW-001
WORKFLOW-002
WORKFLOW-003
```

## Required Records

```text
PROJ-001
PROMPT-001
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
ASSET-001
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-003 Cinematography Output
AGENT-004 Script Output
AGENT-005 Editing Output
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

## Expected Output

```text
Prompt Purpose
Source Records
Base Prompt
Model-Specific Prompt
Negative Prompt
Consistency Checklist
Usage Notes
```

## Must Do

```text
[ ] 必须生成可复制执行的 Prompt
[ ] 必须包含 Negative Prompt
[ ] 必须引用 ASSET-001
[ ] 必须保持 Jump 角色一致
[ ] 必须适配目标模型
[ ] 必须进行一致性检查
```

## Never Do

```text
不得重新设计 Jump
不得省略负面提示词
不得忽略目标模型差异
不得生成空泛提示词
不得改变品牌语言
```

---

# AGENT-003 — Cinematography Agent

## File

```text
agents/cinematographer/AGENT-003.md
```

## 中文说明

AGENT-003 是摄影指导智能体。

它负责把 TSOS 中的 Camera、Lighting、Style、Environment、Story 和 Project 记录转化为可执行的摄影方案。

它不负责重新编写故事，也不负责修改角色设定。

## When to Use（什么时候使用）

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

应该使用：

```text
AGENT-003
```

通常会被以下工作流调用：

```text
WORKFLOW-001
WORKFLOW-003
```

也可配合：

```text
COMMAND-002
COMMAND-003
```

## Required Records

```text
PROJ-001
PROMPT-001
CHAR-001
STORY-001
ENV-001
CAM-001
LGT-001
ASSET-001
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-002 Prompt Output
```

## Required Knowledge

```text
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
BRAND-001
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

## Must Do

```text
[ ] 镜头必须服务故事
[ ] Jump 必须是情绪中心
[ ] 环境必须参与叙事
[ ] 必须符合 CAM-001
[ ] 必须符合 LGT-001
[ ] 必须符合 STYLE-001
[ ] 必须保持真实电影感
```

## Never Do

```text
不得为了炫技使用复杂镜头
不得使用游戏感镜头
不得使用恐怖片构图
不得使用赛博朋克视觉
不得让角色严重变形
不得使用不符合物理逻辑的运镜
```

---

# AGENT-004 — Script Agent

## File

```text
agents/writer/AGENT-004.md
```

## 中文说明

AGENT-004 是脚本智能体。

它负责把 Project、Story、Episode、Character、Knowledge Nodes 和其他 Agent 输出转化为可执行的视频脚本、旁白、字幕、对白和节奏结构。

它不负责重新创造角色设定，也不修改世界观。

## When to Use（什么时候使用）

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

应该使用：

```text
AGENT-004
```

通常会被以下工作流调用：

```text
WORKFLOW-001
```

也可配合：

```text
COMMAND-001
COMMAND-003
COMMAND-004
```

## Required Records

```text
PROJ-001
EP-001
STORY-001
CHAR-001
PROMPT-001
ASSET-001
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-002 Prompt Output
AGENT-003 Cinematography Output
```

## Required Knowledge

```text
STORYFORMULA-001
BRAND-001
EMOTION-001
WORLD-001
STYLE-001
MUSIC-001
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

## Must Do

```text
[ ] 文案必须温暖真实
[ ] 必须符合 BRAND-001
[ ] 必须符合 STORYFORMULA-001
[ ] 必须保持 Jump 角色气质
[ ] 必须适合短视频节奏
[ ] 必须避免过度鸡汤
```

## Never Do

```text
不得制造职场焦虑
不得写成抱怨式文案
不得使用强营销腔
不得使用夸张标题党
不得写成说教内容
不得破坏 TiaoTiao Studio 温暖调性
```

---

# AGENT-005 — Editing Agent

## File

```text
agents/editor/AGENT-005.md
```

## 中文说明

AGENT-005 是剪辑智能体。

它负责把 Project、Storyboard、Script、Cinematography、Prompt 和 Music 相关记录转化为可执行的剪辑方案。

它不负责重新创作故事，也不修改角色设定。

## When to Use（什么时候使用）

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

应该使用：

```text
AGENT-005
```

通常会被以下工作流调用：

```text
WORKFLOW-001
WORKFLOW-003
```

也可配合：

```text
COMMAND-001
COMMAND-005
```

## Required Records

```text
PROJ-001
EP-001
STORY-001
PROMPT-001
ASSET-001
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-002 Prompt Output
AGENT-003 Cinematography Output
AGENT-004 Script Output
```

## Required Knowledge

```text
STORYFORMULA-001
MUSIC-001
EMOTION-001
BRAND-001
STYLE-001
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

## Must Do

```text
[ ] 剪辑必须服务故事
[ ] 开头 3 秒必须清晰
[ ] 字幕不能遮挡 Jump
[ ] 音乐不能压过情绪
[ ] 必须保留情绪停顿
[ ] 必须符合 BRAND-001
```

## Never Do

```text
不得过度快切
不得使用无意义转场
不得让字幕占满画面
不得制造焦虑感
不得把生活感剪成广告感
不得让音乐喧宾夺主
```

---

# AGENT-006 — Publishing Agent

## File

```text
agents/publisher/AGENT-006.md
```

## 中文说明

AGENT-006 是发布智能体。

它负责把 Project、Script、Editing、Prompt、Brand Language 和平台规则转化为可执行的发布方案。

它不负责重新创作视频内容，也不修改角色设定。

## When to Use（什么时候使用）

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

应该使用：

```text
AGENT-006
```

通常由以下命令调用：

```text
COMMAND-004
```

也会被以下工作流调用：

```text
WORKFLOW-001
WORKFLOW-004
```

## Required Records

```text
PROJ-001
EP-001
STORY-001
PROMPT-001
ASSET-001
```

## Optional Agent Inputs

```text
AGENT-001 Storyboard Output
AGENT-002 Prompt Output
AGENT-003 Cinematography Output
AGENT-004 Script Output
AGENT-005 Editing Output
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

## Must Do

```text
[ ] 标题必须清晰但不标题党
[ ] 文案必须温暖真实
[ ] 标签必须相关
[ ] 封面文案必须简洁
[ ] 必须符合 BRAND-001
[ ] 必须输出复盘指标
```

## Never Do

```text
不得使用夸张标题党
不得制造职场焦虑
不得使用强营销腔
不得虚假宣传
不得使用无关标签
不得为了流量破坏品牌一致性
```

---

# Agent Collaboration Chain（智能体协作链路）

完整生产链路为：

```text
AGENT-001 Storyboard Agent
↓
AGENT-002 Prompt Agent
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

# Agent Output Standard（智能体输出标准）

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

# Agent Safety Rules（智能体安全规则）

所有 Agent 都不得：

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

# Jump Agent Rules（Jump 智能体规则）

任何 Agent 只要涉及 Jump，都必须保持：

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

禁止：

```text
把 Jump 改成人类
把 Jump 改成其他动物
去掉毛茸茸质感
改成肌肉体型
改变程序员身份
改变品牌色
改成恐怖 / 黑暗 / 赛博朋克角色
```

---

# Agent Failure Handling（智能体失败处理）

如果 Agent 缺少必要输入，必须输出：

```text
Missing Input:
[缺少内容]

Required Source:
[需要读取的文件]

Action:
Cannot complete agent task until required source is loaded.
```

如果用户要求 Agent 违反 TSOS：

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

# Agent Review Requirement（智能体检查要求）

正式输出后，必要时应调用：

```text
COMMAND-005 — Run Consistency Check
```

特别是以下内容：

```text
Storyboard Output
Prompt Output
Cinematography Output
Script Output
Editing Output
Publishing Output
```

---

# Agent Runtime Example（智能体运行示例）

## Example 1 — Storyboard

User：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

Runtime：

```text
COMMAND-003
↓
AGENT-001
↓
Read PROJ-001, CHAR-001, STORY-001, ENV-001, ASSET-001
↓
Output Storyboard
↓
Continuity Checklist
```

---

## Example 2 — Prompt

User：

```text
运行 COMMAND-002，生成 Kling 视频 Prompt。
```

Runtime：

```text
COMMAND-002
↓
AGENT-002
↓
Read PROMPT-001, CHAR-001, ASSET-001, ENV-001, CAM-001, LGT-001
↓
Output Prompt + Negative Prompt
↓
Consistency Checklist
```

---

## Example 3 — Publishing

User：

```text
运行 COMMAND-004，生成小红书发布包。
```

Runtime：

```text
COMMAND-004
↓
AGENT-006
↓
Read PROJ-001, BRAND-001, SCRIPT OUTPUT if available
↓
Output Title, Caption, Hashtags, Cover Text
↓
Brand Safety Check
```

---

# Relationship to Docs（与文档关系）

Agent 使用时应该参考：

```text
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
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

```text
AGENTS.md
```

定义智能体职责。

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial agents guide |