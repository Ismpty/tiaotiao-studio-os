# COMMAND-001 — Run Jump After Work Production（运行跳跳下班啦完整生产流程）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Run Jump After Work Production 是 TiaoTiao Studio OS 的第一个完整生产启动命令。

它用于一键启动《跳跳下班啦》从项目设定、分镜、提示词、摄影、脚本、剪辑到发布规划的完整生产流程。

这个 Command 不新增世界观，不修改角色设定，不改变品牌方向。

它只负责调用已经建立好的 Workflow、Agents、Database Records 和 Knowledge Nodes。

## English

Run Jump After Work Production is the first full production operating command in TiaoTiao Studio OS.

It starts the complete Jump After Work production process from project setup to storyboard, prompt, cinematography, script, editing and publishing planning.

---

# Command Goal（命令目标）

本命令用于：

- 快速启动《跳跳下班啦》完整生产流程
- 调用 WORKFLOW-001
- 自动串联 6 个 AI Agents
- 默认读取 PROJ-001
- 默认引用所有核心 Database Records
- 默认遵守所有 Master Knowledge Nodes
- 输出完整生产包

---

# Command Syntax（命令格式）

标准调用方式：

```text
Run COMMAND-001.
```

完整调用方式：

```text
Run COMMAND-001 for PROJ-001.
Use WORKFLOW-001.
Output complete production package.
```

中文调用方式：

```text
运行 COMMAND-001，启动《跳跳下班啦》完整生产流程。
```

---

# Default Workflow（默认工作流）

本命令默认调用：

```text
WORKFLOW-001 — Jump After Work Production Workflow
```

---

# Default Project（默认项目）

本命令默认服务：

```text
PROJ-001 — Jump After Work Pilot Project
```

---

# Required Database Records（必需数据库记录）

| Database | Record | Purpose |
|---|---|---|
| Character DB | CHAR-001 | Jump 角色身份 |
| Episode DB | EP-001 | 跳跳下班啦剧集设定 |
| Story DB | STORY-001 | 下班冒险故事 |
| Environment DB | ENV-001 | 跳跳工作室办公室 |
| Motion DB | MOT-001 | 自然行走动作 |
| Camera DB | CAM-001 | 主角跟拍镜头 |
| Lighting DB | LGT-001 | 温暖工作室灯光 |
| Prompt DB | PROMPT-001 | 主提示词模块 |
| Asset DB | ASSET-001 | Jump 角色参考资产 |
| Project DB | PROJ-001 | 试播项目记录 |

---

# Required Knowledge Nodes（必需知识节点）

| Category | Knowledge Node |
|---|---|
| Style | STYLE-001 |
| Color | COLOR-001 |
| World | WORLD-001 |
| Emotion | EMOTION-001 |
| Camera Language | SHOT-001 |
| Motion Language | MOTIONLANG-001 |
| Outfit | OUTFIT-001 |
| Music | MUSIC-001 |
| Story Formula | STORYFORMULA-001 |
| Brand Language | BRAND-001 |

---

# Required Agents（必需智能体）

| Agent | Role | Purpose |
|---|---|---|
| AGENT-001 | Storyboard Agent | 生成分镜方案 |
| AGENT-002 | Prompt Agent | 生成 AI Prompt |
| AGENT-003 | Cinematography Agent | 生成摄影方案 |
| AGENT-004 | Script Agent | 生成脚本文案 |
| AGENT-005 | Editing Agent | 生成剪辑方案 |
| AGENT-006 | Publishing Agent | 生成发布方案 |

---

# Execution Order（执行顺序）

本命令必须按照以下顺序执行：

```text
1. Load Project
↓
2. Load Database Records
↓
3. Load Knowledge Nodes
↓
4. Run WORKFLOW-001
↓
5. Run AGENT-001 Storyboard Agent
↓
6. Run AGENT-002 Prompt Agent
↓
7. Run AGENT-003 Cinematography Agent
↓
8. Run AGENT-004 Script Agent
↓
9. Run AGENT-005 Editing Agent
↓
10. Run AGENT-006 Publishing Agent
↓
11. Run Final Consistency Check
↓
12. Output Final Production Package
```

---

# Input Requirements（输入要求）

默认情况下，本命令不需要额外输入。

如果用户提供额外需求，只允许作为以下内容的补充：

- Target Platform
- Target Duration
- Target Aspect Ratio
- Target Model
- Language Version
- Output Depth
- Publishing Platform

允许示例：

```text
Target Platform:
小红书

Target Duration:
45 seconds

Target Model:
Kling

Language:
Chinese
```

---

# Forbidden Inputs（禁止输入）

不得通过本命令临时修改：

- Jump 的物种
- Jump 的核心身份
- Jump 的默认角色设定
- TiaoTiao Universe 世界观
- Brand Language
- Master Knowledge Nodes
- Frozen Roadmap
- Database Record ID
- 文件命名规范

如果用户输入与 TSOS 核心设定冲突，Command 必须拒绝该修改，并回到 Source of Truth。

---

# Output Package（输出包）

本命令最终必须输出：

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

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-001 Output

## 1. Project Brief

## 2. Storyboard Output

## 3. Prompt Output

## 4. Cinematography Output

## 5. Script Output

## 6. Editing Output

## 7. Publishing Output

## 8. Final Consistency Checklist

## 9. Next Production Actions
```

---

# Stage 1 — Project Brief（项目简报）

## Output Should Include

```text
Project:
PROJ-001

Episode:
EP-001

Story:
STORY-001

Character:
CHAR-001

Core Emotion:
EMOTION-001

Target Output:
Short Video Production Package
```

## Required Check

```text
[ ] 是否读取 PROJ-001
[ ] 是否读取 CHAR-001
[ ] 是否读取 EP-001
[ ] 是否读取 STORY-001
[ ] 是否读取 ASSET-001
```

---

# Stage 2 — Storyboard Output（分镜输出）

## Agent

```text
AGENT-001 — Storyboard Agent
```

## Output Should Include

```text
Project Summary
Story Beat Breakdown
Shot List
Shot-by-Shot Description
Camera / Motion / Lighting Mapping
Continuity Checklist
Production Notes
```

## Required Check

```text
[ ] 每个镜头是否有叙事功能
[ ] 每个镜头是否引用 TSOS 记录
[ ] Jump 是否保持一致
[ ] 是否引用 ASSET-001
[ ] 是否符合 STORYFORMULA-001
```

---

# Stage 3 — Prompt Output（提示词输出）

## Agent

```text
AGENT-002 — Prompt Agent
```

## Output Should Include

```text
Prompt Purpose
Source Records
Target Model
Base Prompt
Model-Specific Prompt
Negative Prompt
Consistency Checklist
Usage Notes
```

## Required Check

```text
[ ] 是否可直接复制使用
[ ] 是否包含 Negative Prompt
[ ] 是否引用 ASSET-001
[ ] 是否适配目标模型
[ ] 是否没有改变 Jump 设定
```

---

# Stage 4 — Cinematography Output（摄影输出）

## Agent

```text
AGENT-003 — Cinematography Agent
```

## Output Should Include

```text
Cinematography Summary
Visual Strategy
Lens Plan
Camera Movement Plan
Composition Plan
Lighting Plan
Shot-by-Shot Cinematography Notes
AI Visual Prompt Add-ons
```

## Required Check

```text
[ ] 是否符合 CAM-001
[ ] 是否符合 LGT-001
[ ] 是否符合 STYLE-001
[ ] 是否避免极端广角
[ ] 是否避免游戏感镜头
```

---

# Stage 5 — Script Output（脚本输出）

## Agent

```text
AGENT-004 — Script Agent
```

## Output Should Include

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

## Required Check

```text
[ ] 是否温暖真实
[ ] 是否避免职场焦虑
[ ] 是否符合 BRAND-001
[ ] 是否符合 STORYFORMULA-001
[ ] 是否适合短视频节奏
```

---

# Stage 6 — Editing Output（剪辑输出）

## Agent

```text
AGENT-005 — Editing Agent
```

## Output Should Include

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

## Required Check

```text
[ ] 开头 3 秒是否清晰
[ ] 字幕是否不遮挡 Jump
[ ] 音乐是否不压过画面
[ ] 是否保留情绪停顿
[ ] 是否适合短视频平台
```

---

# Stage 7 — Publishing Output（发布输出）

## Agent

```text
AGENT-006 — Publishing Agent
```

## Output Should Include

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

## Required Check

```text
[ ] 标题是否不标题党
[ ] 正文是否不焦虑
[ ] 标签是否相关
[ ] 封面文案是否简洁
[ ] 是否符合 BRAND-001
```

---

# Final Consistency Checklist（最终一致性检查）

本命令结束前必须检查：

```text
[ ] Jump 是否仍然是拟人化小狗
[ ] Jump 是否保持程序员身份
[ ] Jump 外观是否参考 ASSET-001
[ ] 世界观是否符合 WORLD-001
[ ] 风格是否符合 STYLE-001
[ ] 色彩是否符合 COLOR-001
[ ] 情绪是否符合 EMOTION-001
[ ] 故事是否符合 STORYFORMULA-001
[ ] 镜头是否符合 SHOT-001 / CAM-001
[ ] 动作是否符合 MOTIONLANG-001 / MOT-001
[ ] 灯光是否符合 LGT-001
[ ] 音乐是否符合 MUSIC-001
[ ] 文案是否符合 BRAND-001
[ ] 是否没有新增未确认设定
[ ] 是否没有修改 Frozen Roadmap
```

---

# Next Production Actions（下一步生产动作）

Command 输出结尾必须给出下一步动作。

默认格式：

```text
Next Actions:

1. Review storyboard.
2. Select target model.
3. Generate shot prompts.
4. Produce video clips.
5. Review continuity.
6. Assemble edit.
7. Prepare publishing package.
```

---

# Command Example（命令示例）

## Example 1

用户输入：

```text
Run COMMAND-001.
```

系统应执行：

```text
Run WORKFLOW-001 for PROJ-001 using all default TSOS records and agents.
```

输出：

```text
Complete production package.
```

---

## Example 2

用户输入：

```text
运行 COMMAND-001，目标平台小红书，视频时长 45 秒。
```

系统应执行：

```text
Run COMMAND-001 for PROJ-001.

Target Platform:
小红书

Target Duration:
45 seconds
```

输出：

```text
Complete production package optimized for 小红书.
```

---

# Command Rules（命令规则）

## Must Do（必须）

- 必须调用 WORKFLOW-001
- 必须读取 PROJ-001
- 必须读取 10 个 Production Database Records
- 必须读取 10 个 Master Knowledge Nodes
- 必须调用 6 个 Agents
- 必须输出完整生产包
- 必须执行最终一致性检查

---

## Never Do（禁止）

- 不得跳过工作流
- 不得跳过 Agent
- 不得跳过 ASSET-001
- 不得临时修改 Jump 人设
- 不得临时改变世界观
- 不得改变品牌语言
- 不得输出空泛建议
- 不得省略最终一致性检查

---

# Related Files（关联文件）

## Workflow

```text
workflows/WORKFLOW-001.md
```

## Database Records

```text
database/characters/CHAR-001.md
database/episodes/EP-001.md
database/stories/STORY-001.md
database/environments/ENV-001.md
database/motions/MOT-001.md
database/cameras/CAM-001.md
database/lighting/LGT-001.md
database/prompts/PROMPT-001.md
database/assets/ASSET-001.md
database/projects/PROJ-001.md
```

## Knowledge Nodes

```text
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/world/WORLD-001.md
knowledge/emotion/EMOTION-001.md
knowledge/camera-language/SHOT-001.md
knowledge/motion-language/MOTIONLANG-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/music/MUSIC-001.md
knowledge/story-formula/STORYFORMULA-001.md
knowledge/brand-language/BRAND-001.md
```

## Agents

```text
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
agents/cinematographer/AGENT-003.md
agents/writer/AGENT-004.md
agents/editor/AGENT-005.md
agents/publisher/AGENT-006.md
```

---

# Usage Scope（应用范围）

适用于：

- Full short video production
- Jump After Work production
- AI native production workflow
- Storyboard generation
- Prompt generation
- Script generation
- Editing planning
- Publishing planning
- Production package generation

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical operating command |