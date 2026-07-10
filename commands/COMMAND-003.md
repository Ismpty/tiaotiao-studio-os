# COMMAND-003 — Generate Storyboard（生成分镜）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Generate Storyboard 是 TiaoTiao Studio OS 的分镜生成命令。

它用于快速调用 `WORKFLOW-001` 中的 Storyboard Planning 阶段，或直接调用 `AGENT-001 — Storyboard Agent`，将 TSOS 中的 Project、Story、Subject / Character、Environment、Motion、Camera、Transition、Lighting、Asset 和 Knowledge Nodes 转化为可执行的分镜方案。

这个 Command 不负责重新创造故事设定，也不修改已确认的主体身份。Jump Mode 下不得修改 Jump 角色；Custom Subject Mode 下不得修改用户已确认的主体身份卡。

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
- 支持人物、动物、植物、物体、产品、场景或新 IP 的自定义主体分镜
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
运行 COMMAND-003，为《小保安和他的古人朋友们》生成分镜。
```

---

# Default Workflow（默认工作流）

本命令默认调用：

```text
WORKFLOW-001 — Little Security Guard Production Workflow
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
PROJ-001 — Little Security Guard and His Ancient Friends
```

非 Jump 项目或临时主体使用：

```text
Subject Mode:
Custom Subject Mode

Subject Identity:
用户已确认的主体身份卡，按 SUBJECT-001 展开
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
| Subject Identity | SUBJECT-001 |
| Relic Friends | RELIC-001 |
| Style | STYLE-001 |
| Color | COLOR-001 |
| World | WORLD-001 |
| Emotion | EMOTION-001 |
| Visual Parameters | VISUALPARAM-001 |
| Scene Blocking | BLOCKING-001 |
| Camera Language | SHOT-001 |
| Camera Consistency | SHOT-002 |
| Transition Language | TRANSITION-001 |
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
3. Load Subject Identity / Character Record
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

Subject Mode:
Jump Mode / Custom Subject Mode

Subject Type:
Jump / Human / Animal / Plant / Object / Scene Subject / Mascot / Other

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
- 文物朋友的来源文物、材质、纹样、色彩和文化身份
- Custom Subject 的已确认主体类型
- Custom Subject 的核心视觉身份
- Custom Subject 的连续性锁定
- TiaoTiao Universe 世界观
- Brand Language
- Master Knowledge Nodes
- Database Record ID
- Frozen Roadmap

如果用户输入与 TSOS Source of Truth 或已确认的主体身份卡冲突，Command 必须拒绝该修改，并回到现有记录。

---

# Output Package（输出包）

本命令最终必须输出：

```text
1. Storyboard Summary
2. Story Beat Breakdown
3. Shot List
4. Shot Details
5. Camera / Motion / Transition / Lighting Mapping
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

## 5. Camera / Motion / Transition / Lighting Mapping

## 6. Prompt Notes

## 7. Continuity Checklist

## 8. Next Production Actions
```

---

# Story Beat Breakdown Rules（故事节奏拆解规则）

默认故事节奏：

```text
Museum Closing
↓
Jump Patrol
↓
Relic Friend Awakening
↓
Ancient-Modern Misunderstanding
↓
Absurd Escalation
↓
Warm Resolution
```

对于 `PROJ-001`，默认映射为：

```text
Museum Closing:
The AI museum closes and the night gallery becomes quiet.

Jump Patrol:
Jump, a real dog-form little security guard, patrols the gallery in dog-size museum security clothing.

Relic Friend Awakening:
A Chinese relic, ancient painting figure, artifact, beast motif or mythic object wakes up while retaining its source material and patterns.

Ancient-Modern Misunderstanding:
The relic friend misunderstands a modern museum rule, device, visitor habit or AI system.

Absurd Escalation:
The misunderstanding becomes a strange, funny, harmless museum incident.

Warm Resolution:
Jump gently solves the incident, and the relic friend becomes a friend instead of a problem.
```

---

# Default Shot Structure（默认镜头结构）

本命令默认生成 6 个镜头：

```text
Shot 1 — Museum Closing
Shot 2 — Little Security Guard Patrol
Shot 3 — Relic Friend Awakens
Shot 4 — Ancient-Modern Misunderstanding
Shot 5 — Absurd Museum Incident
Shot 6 — Warm Gallery Ending
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
Subject Identity:
Character:
Environment:
Camera:
Visual Parameters:
Blocking Map:
Motion:
Lighting:
Transition To Next Shot:
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
Museum Closing
Little Security Guard Patrol
Relic Friend Awakens
Ancient-Modern Misunderstanding
Absurd Museum Incident
Warm Gallery Ending
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
Establish the AI museum after closing.
Show Jump beginning a serious little security guard patrol.
Reveal the relic friend awakening and misunderstanding the modern museum world.
Resolve the absurd incident with warmth.
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

Jump Mode 必须引用：

```text
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack
```

Custom Subject Mode 必须引用用户已确认的主体身份卡，并按 SUBJECT-001 用自然语言写出主体外观、结构、比例、材质、颜色、识别特征、行为方式、连续性锁定和负面约束。

模型可复制区域不能只写：

```text
use SUBJECT-001
```

必须写成自然语言，例如：

```text
主体是一株放在陶土盆里的小型柠檬树，矮壮主干、椭圆深绿叶片、几颗未成熟青绿色小柠檬和一颗黄色成熟柠檬，叶片有轻微蜡质反光，整体比例必须保持盆栽小树而不是森林大树。
```

---

## Environment

默认引用：

```text
ENV-001 — AI Museum Night Gallery
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

## Visual Parameters

默认引用：

```text
VISUALPARAM-001 — AIGC Base Visual Parameter Grammar
```

每个镜头必须说明基础画面参数：

```text
Format:
Shot Size:
Camera Angle / Height:
Lens:
Composition:
Depth of Field:
Lighting:
Color / Tone:
Texture Detail:
Continuity Locks:
```

这些参数必须服务分镜，而不是把黑白铅笔故事板变成彩色成片插画。

---

## Blocking Map

默认引用：

```text
BLOCKING-001 — Overhead Scene Blocking Map
```

当场景包含多人、复杂走位、追逐、打斗、一镜到底或空间关系容易崩坏时，必须先输出俯视场景调度图。

Blocking Map 必须说明：

```text
Scene Boundary:
Entrances / Exits:
Props / Obstacles:
Character Starting Positions:
Movement Paths:
Camera Start Position:
Camera Path:
Shot / Beat Points:
Continuity Locks:
```

简单单角色镜头可写：

```text
No overhead blocking map required.
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
LGT-001 — Warm Museum Night Lighting
```

---

## Transition To Next Shot

默认引用：

```text
TRANSITION-001 — Universal AI Video Transition Grammar
```

每个镜头必须说明它如何连接到下一个镜头。

若该镜头为最后一个镜头，写：

```text
End hold / no next transition.
```

转场描述必须使用模型可读自然语言，不能只写：

```text
use TRANSITION-001
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
Museum Closing

Duration:
6 seconds

Story Function:
Establish the AI museum after closing and the start of Jump's night patrol.

Visual Description:
The AI museum gallery is closed and quiet. Display cases glow softly. Jump, a fluffy real dog-form little security guard wearing a dog-size museum security vest, badge and collar charm, trots into frame with a tiny patrol light.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — AI Museum Night Gallery

Camera:
Medium dog-height tracking shot, 35mm lens, calm museum perspective.

Visual Parameters:
Vertical 9:16 frame, medium shot, low dog-height eye-level camera, 35mm natural documentary lens, moderate depth of field, warm museum display light, realistic fur, cloth and artifact texture.

Blocking Map:
No overhead blocking map required for this simple desk shot.

Motion:
Natural four-legged dog walking, tiny patrol light swaying gently.

Lighting:
LGT-001 — Warm Museum Night Lighting

Transition To Next Shot:
Soft display-case glow blooms across the frame and reveals the next artifact.

Emotion:
Calm, curious, slightly serious.

Prompt Notes:
Warm cinematic documentary realism, AI museum night gallery, soft display-case glow, respectful Chinese relic atmosphere.

Negative Notes:
No human security guard, no humanoid dog body, no horror museum, no cyberpunk neon, no game render.

Continuity Notes:
Jump's dog-size security outfit, badge and patrol light remain visible. The museum gallery layout stays consistent.
```

---

# Camera / Motion / Transition / Lighting Mapping（镜头动作转场灯光映射）

输出必须包含一张映射表：

```text
| Shot | Camera | Motion | Transition To Next Shot | Lighting | Asset |
|---|---|---|---|---|---|
| Shot 1 | CAM-001 | Museum patrol walk | Display-case glow reveal | LGT-001 | ASSET-001 |
| Shot 2 | Dog-height tracking | MOT-001 | Patrol light sweep | LGT-001 | ASSET-001 |
| Shot 3 | Close-up / slow push | Relic activation | Artifact texture match cut | LGT-001 | ASSET-001 + RELIC-001 |
| Shot 4 | Medium two-subject shot | Misunderstanding action | Object/action bridge | LGT-001 | ASSET-001 + RELIC-001 |
| Shot 5 | CAM-001 / blocking-aware | Absurd escalation | Motion continuation | LGT-001 | ASSET-001 + RELIC-001 |
| Shot 6 | Static / Slow push | Warm resolution hold | End hold | LGT-001 | ASSET-001 + RELIC-001 |
```

---

# Continuity Checklist（一致性检查）

本命令结束前必须检查：

```text
[ ] 每个镜头是否有明确叙事功能
[ ] 每个镜头是否可以连接到下一镜头
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] Jump 是否保持真实小狗本体形态
[ ] Jump 是否保持四足小狗身体结构
[ ] Jump 是否保持毛茸茸质感
[ ] Jump 是否穿小狗尺寸的 AI 博物馆小保安服装或已确认小狗服装
[ ] 文物朋友是否保留来源文物、材质、纹样、色彩和文化身份
[ ] 文物朋友是否没有变成现代网红、恐怖鬼魂、廉价吉祥物或欧美奇幻怪物
[ ] Custom Subject 是否符合已确认主体身份卡
[ ] Custom Subject 是否没有误套 Jump 的小狗形态、服装、配件或故事比例
[ ] 内部审查是否参考 ASSET-001
[ ] 服装是否符合 OUTFIT-001
[ ] 场景是否符合 ENV-001
[ ] 基础画面参数是否符合 VISUALPARAM-001
[ ] 复杂空间是否符合 BLOCKING-001
[ ] 镜头是否符合 CAM-001 / SHOT-001 / SHOT-002
[ ] 转场是否符合 TRANSITION-001
[ ] 每个转场是否有可见载体、锚点和清晰揭示
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
- 必须在 Custom Subject Mode 下读取或生成已确认主体身份卡
- 必须读取 STORY-001
- 必须读取 ENV-001
- 必须读取 ASSET-001
- 必须生成 Shot List
- 必须生成 Shot Details
- 必须生成 Transition To Next Shot
- 必须执行 Continuity Checklist
- 必须输出下一步动作

---

## Never Do（禁止）

- 不得重新设计 Jump
- 不得重新设计已确认的 Custom Subject
- 不得修改故事核心
- 不得临时改变世界观
- 不得省略 ASSET-001
- 不得在 Custom Subject Mode 中只写 SUBJECT-001 而不展开主体自然语言
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
knowledge/subject-identity/SUBJECT-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/world/WORLD-001.md
knowledge/emotion/EMOTION-001.md
knowledge/visual-parameters/VISUALPARAM-001.md
knowledge/scene-blocking/BLOCKING-001.md
knowledge/camera-language/SHOT-001.md
knowledge/camera-language/SHOT-002.md
knowledge/transition-language/TRANSITION-001.md
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
| 1.4 | 2026 | Added SUBJECT-001 custom subject storyboard support |
| 1.3 | 2026 | Added BLOCKING-001 overhead scene blocking map requirements for complex spatial planning |
| 1.2 | 2026 | Added VISUALPARAM-001 visual parameter requirements for storyboard planning |
| 1.1 | 2026 | Added TRANSITION-001 requirements for shot-to-shot transition planning |
| 1.0 | 2026 | Initial canonical operating command |
