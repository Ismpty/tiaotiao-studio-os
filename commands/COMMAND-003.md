# COMMAND-003 — Generate Storyboard（生成分镜）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Generate Storyboard 是 TiaoTiao Studio OS 的分镜生成命令。

它用于快速调用 `WORKFLOW-001` 中的 Storyboard Planning 阶段，或直接调用 `AGENT-001 — Storyboard Agent`，将 TSOS 中的 Project、Story、Character、Environment、Motion、Camera、Lighting、Asset 和 Knowledge Nodes 转化为可执行的分镜方案。

这个 Command 不负责重新创造故事设定，也不修改 Jump 角色。

它只负责把已经确认的 TSOS 内容拆解成清晰、稳定、可生产的镜头结构。

## English

Generate Storyboard is the storyboard generation command of TiaoTiao Studio OS.

It calls the Storyboard Planning stage of WORKFLOW-001 or directly runs AGENT-001 to transform TSOS records into production-ready storyboard plans.

---

# Command Goal（命令目标）

本命令用于：

- 快速生成短视频分镜
- 拆分故事节奏
- 生成镜头列表
- 生成逐镜头画面描述
- 匹配角色、环境、动作、镜头、灯光和资产引用
- 输出可进入 Prompt / Video / Editing 阶段的分镜方案
- 保持 Jump 角色一致性
- 保持 TSOS 世界观、品牌和视觉语言一致性

---

# Command Syntax（命令格式）

标准调用方式：

```text
Run COMMAND-003.
```

完整调用方式：

```text
Run COMMAND-003 for PROJ-001.
Use AGENT-001.
Output production-ready storyboard.
```

中文调用方式：

```text
运行 COMMAND-003，为《跳跳下班啦》生成分镜。
```

---

# Default Workflow（默认工作流）

本命令默认调用：

```text
WORKFLOW-001 — Jump After Work Production Workflow
```

只执行其中的：

```text
Stage 2 — Storyboard Planning
```

---

# Default Agent（默认智能体）

本命令默认调用：

```text
AGENT-001 — Storyboard Agent
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
| Project DB | PROJ-001 | 项目目标 |
| Character DB | CHAR-001 | Jump 角色身份 |
| Episode DB | EP-001 | 剧集设定 |
| Story DB | STORY-001 | 故事结构 |
| Environment DB | ENV-001 | 场景环境 |
| Motion DB | MOT-001 | 动作资产 |
| Camera DB | CAM-001 | 镜头资产 |
| Lighting DB | LGT-001 | 灯光资产 |
| Prompt DB | PROMPT-001 | 主提示词 |
| Asset DB | ASSET-001 | 角色参考资产 |

---

# Required Knowledge Nodes（必需知识节点）

| Category | Knowledge Node |
|---|---|
| Style | STYLE-001 |
| Color | COLOR-001 |
| World | WORLD-001 |
| Emotion | EMOTION-001 |
| Camera Language | SHOT-001 |
| Camera Consistency | SHOT-002 |
| Motion Language | MOTIONLANG-001 |
| Outfit | OUTFIT-001 |
| Music | MUSIC-001 |
| Story Formula | STORYFORMULA-001 |
| Brand Language | BRAND-001 |

---

# Execution Order（执行顺序）

本命令必须按照以下顺序执行：

```text
1. Load Project Record
↓
2. Load Story Record
↓
3. Load Character Record
↓
4. Load Environment / Motion / Camera / Lighting Records
↓
5. Load Asset Record
↓
6. Load Knowledge Nodes
↓
7. Run AGENT-001 Storyboard Agent
↓
8. Build Story Beat Breakdown
↓
9. Build Shot List
↓
10. Build Shot Details
↓
11. Run Continuity Check
↓
12. Output Production-Ready Storyboard
```

---

# Input Requirements（输入要求）

用户可以提供以下输入：

```text
Target Duration:
30s / 45s / 60s

Shot Count:
4 shots / 6 shots / 8 shots

Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels

Aspect Ratio:
9:16 / 16:9 / 4:3 / 1:1

Output Language:
Chinese / English / Bilingual

Detail Level:
Simple / Standard / Detailed
```

如果用户没有指定，默认：

```text
Target Duration:
45 seconds

Shot Count:
6 shots

Aspect Ratio:
9:16

Output Language:
Bilingual

Detail Level:
Detailed
```

---

# Forbidden Inputs（禁止输入）

不得通过本命令临时修改：

- Jump 的物种
- Jump 的核心身份
- Jump 的角色外观
- Jump 的默认服装系统
- TiaoTiao Universe 世界观
- Brand Language
- Master Knowledge Nodes
- Database Record ID
- Frozen Roadmap

如果用户输入与 TSOS Source of Truth 冲突，Command 必须拒绝该修改，并回到现有记录。

---

# Output Package（输出包）

本命令最终必须输出：

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

---

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-003 Output

## 1. Storyboard Summary

## 2. Story Beat Breakdown

## 3. Shot List

## 4. Shot Details

## 5. Camera / Motion / Lighting Mapping

## 6. Prompt Notes

## 7. Continuity Checklist

## 8. Next Production Actions
```

---

# Story Beat Breakdown Rules（故事节奏拆解规则）

默认引用：

```text
STORYFORMULA-001 — Work Ends, Adventure Begins
```

标准故事节奏：

```text
Work
↓
Decision
↓
Exploration
↓
Discovery
↓
Emotion
↓
Reflection
```

对于 `PROJ-001`，默认映射为：

```text
Work:
Jump finishes coding.

Decision:
Jump closes the laptop and decides to leave.

Exploration:
Jump packs her backpack and walks through the studio.

Discovery:
A warm after-work moment begins.

Emotion:
Jump feels free and relaxed.

Reflection:
Life begins again after work.
```

---

# Default Shot Structure（默认镜头结构）

本命令默认生成 6 个镜头：

```text
Shot 1 — Work Ending
Shot 2 — Decision Moment
Shot 3 — Packing Up
Shot 4 — Walking Out
Shot 5 — Door Exit
Shot 6 — Warm Ending
```

---

# Standard Shot Format（标准镜头格式）

每个镜头必须使用以下格式：

```text
Shot Number:
Shot Name:
Duration:
Story Function:
Visual Description:
Character:
Environment:
Camera:
Motion:
Lighting:
Asset Reference:
Emotion:
Prompt Notes:
Negative Notes:
Continuity Notes:
```

---

# Shot Detail Requirements（逐镜头要求）

## Shot Number

必须使用：

```text
Shot 1
Shot 2
Shot 3
...
```

---

## Shot Name

必须简短清晰。

示例：

```text
Work Ending
Decision Moment
Packing Up
Walking Out
Door Exit
Warm Ending
```

---

## Duration

必须给出建议时长。

示例：

```text
6 seconds
8 seconds
5 seconds
```

---

## Story Function

必须说明该镜头在故事中的作用。

示例：

```text
Establish Jump's workday ending.
Show Jump making the decision to leave.
Create emotional transition from work to life.
```

---

## Visual Description

必须描述画面。

要求：

- 清晰
- 可拍摄
- 可生成
- 不空泛
- 有角色、环境、动作、情绪

---

## Character

必须引用：

```text
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack
```

---

## Environment

默认引用：

```text
ENV-001 — TiaoTiao Studio Office
```

---

## Camera

默认引用：

```text
CAM-001 — Hero Tracking Camera
SHOT-001 — Hero Tracking Shot
SHOT-002 — Six-View Scene Lock
```

---

## Motion

默认引用：

```text
MOT-001 — Natural Walking
MOTIONLANG-001 — Natural Walking Language
```

---

## Lighting

默认引用：

```text
LGT-001 — Warm Studio Lighting
```

---

## Emotion

默认引用：

```text
EMOTION-001 — Freedom
```

---

# Default Storyboard Example（默认分镜示例）

```text
Shot 1
Shot Name:
Work Ending

Duration:
6 seconds

Story Function:
Establish that Jump has finished a day of work.

Visual Description:
Jump sits at her desk inside TiaoTiao Studio Office. The computer screen casts a soft warm glow on her fluffy face. Her posture relaxes as the workday comes to an end.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — TiaoTiao Studio Office

Camera:
Medium desk shot, 35mm lens, eye-level camera.

Motion:
Small relaxed body movement, hands leaving the keyboard.

Lighting:
LGT-001 — Warm Studio Lighting

Emotion:
Calm, slight relief.

Prompt Notes:
Warm cinematic documentary realism, realistic programmer workspace, soft screen glow.

Negative Notes:
No cold corporate office, no cyberpunk lighting, no game render.

Continuity Notes:
Laptop is still open. Backpack is visible nearby.
```

---

# Camera / Motion / Lighting Mapping（镜头动作灯光映射）

输出必须包含一张映射表：

```text
| Shot | Camera | Motion | Lighting | Asset |
|---|---|---|---|---|
| Shot 1 | CAM-001 | Desk movement | LGT-001 | ASSET-001 |
| Shot 2 | CAM-001 | Subtle smile | LGT-001 | ASSET-001 |
| Shot 3 | Close-up | Object handling | LGT-001 | ASSET-001 |
| Shot 4 | CAM-001 | MOT-001 | LGT-001 | ASSET-001 |
| Shot 5 | CAM-001 | MOT-001 | LGT-001 | ASSET-001 |
| Shot 6 | Static / Slow push | Emotional hold | LGT-001 / Golden hour | ASSET-001 |
```

---

# Continuity Checklist（一致性检查）

本命令结束前必须检查：

```text
[ ] 每个镜头是否有明确叙事功能
[ ] 每个镜头是否可以连接到下一镜头
[ ] Jump 是否保持真实小狗本体形态
[ ] Jump 是否保持四足小狗身体结构
[ ] Jump 是否保持毛茸茸质感
[ ] Jump 是否穿程序员风格小狗衣服
[ ] 内部审查是否参考 ASSET-001
[ ] 服装是否符合 OUTFIT-001
[ ] 场景是否符合 ENV-001
[ ] 镜头是否符合 CAM-001 / SHOT-001 / SHOT-002
[ ] 动作是否符合 MOT-001 / MOTIONLANG-001
[ ] 灯光是否符合 LGT-001
[ ] 情绪是否符合 EMOTION-001
[ ] 风格是否符合 STYLE-001
[ ] 品牌语气是否符合 BRAND-001
[ ] 是否没有新增未确认设定
```

---

# Next Production Actions（下一步生产动作）

Command 输出结尾必须给出下一步动作：

```text
Next Actions:

1. Review storyboard.
2. Select target video model.
3. Run COMMAND-002 to generate shot prompts.
4. Run WORKFLOW-003 to convert storyboard into video clips.
5. Review continuity before editing.
```

---

# Command Example（命令示例）

## Example 1

用户输入：

```text
Run COMMAND-003.
```

系统应执行：

```text
Run AGENT-001 Storyboard Agent for PROJ-001 using default TSOS records.
```

输出：

```text
Production-ready 6-shot storyboard.
```

---

## Example 2

用户输入：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

系统应执行：

```text
Run COMMAND-003 for PROJ-001.

Target Platform:
小红书

Target Duration:
45 seconds

Aspect Ratio:
9:16

Shot Count:
6 shots
```

输出：

```text
45-second 9:16 storyboard for 小红书.
```

---

# Command Rules（命令规则）

## Must Do（必须）

- 必须调用 AGENT-001
- 必须读取 PROJ-001
- 必须读取 CHAR-001
- 必须读取 STORY-001
- 必须读取 ENV-001
- 必须读取 ASSET-001
- 必须生成 Shot List
- 必须生成 Shot Details
- 必须执行 Continuity Checklist
- 必须输出下一步动作

---

## Never Do（禁止）

- 不得重新设计 Jump
- 不得修改故事核心
- 不得临时改变世界观
- 不得省略 ASSET-001
- 不得输出空泛镜头
- 不得只输出画面灵感
- 不得跳过一致性检查
- 不得使用与 BRAND-001 冲突的故事方向

---

# Related Files（关联文件）

## Workflow

```text
workflows/WORKFLOW-001.md
workflows/WORKFLOW-003.md
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
knowledge/camera-language/SHOT-002.md
knowledge/motion-language/MOTIONLANG-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/music/MUSIC-001.md
knowledge/story-formula/STORYFORMULA-001.md
knowledge/brand-language/BRAND-001.md
```

## Agents

```text
agents/director/AGENT-001.md
```

---

# Usage Scope（应用范围）

适用于：

- Storyboard Generation
- Shot Planning
- Short Video Planning
- AI Video Planning
- Production Breakdown
- Prompt Preparation
- Editing Preparation
- Series Development

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical operating command |
