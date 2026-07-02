# COMMAND-002 — Generate Short Video Prompt（生成短视频提示词）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Generate Short Video Prompt 是 TiaoTiao Studio OS 的短视频提示词生成命令。

它用于快速调用 `WORKFLOW-002 — Short Video Prompt Workflow`，将 TSOS 中的角色、故事、环境、动作、镜头、灯光、资产和品牌规范转化为可直接用于 AI 图片 / 视频生成的 Prompt。

这个 Command 不负责重新设计角色，也不负责修改故事方向。

它只负责生成稳定、清晰、可复制、可执行的短视频 Prompt。

## English

Generate Short Video Prompt is the short-video prompt generation command of TiaoTiao Studio OS.

It calls WORKFLOW-002 to transform TSOS records into executable AI image and video prompts.

---

# Command Goal（命令目标）

本命令用于：

- 快速生成短视频镜头 Prompt
- 生成图片 Prompt
- 生成视频 Prompt
- 生成分镜 Prompt
- 生成封面 Prompt
- 生成角色一致性 Prompt
- 生成负面提示词
- 适配不同 AI 模型
- 保持 Jump 角色一致性
- 保持 TSOS 世界观、风格和品牌一致性

---

# Command Syntax（命令格式）

标准调用方式：

```text
Run COMMAND-002.
```

完整调用方式：

```text
Run COMMAND-002 for PROJ-001.
Use WORKFLOW-002.
Target Model: Kling.
Prompt Type: Video Prompt.
```

中文调用方式：

```text
运行 COMMAND-002，为《跳跳下班啦》生成短视频 Prompt。
```

---

# Default Workflow（默认工作流）

本命令默认调用：

```text
WORKFLOW-002 — Short Video Prompt Workflow
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
| Story DB | STORY-001 | 故事目标 |
| Environment DB | ENV-001 | 场景设定 |
| Motion DB | MOT-001 | 动作资产 |
| Camera DB | CAM-001 | 镜头资产 |
| Lighting DB | LGT-001 | 灯光资产 |
| Prompt DB | PROMPT-001 | 主提示词 |
| Asset DB | ASSET-001 | Jump 角色参考资产 |
| Project DB | PROJ-001 | 项目目标 |

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
| Brand Language | BRAND-001 |

---

# Required Agent（必需智能体）

| Agent | Role | Purpose |
|---|---|---|
| AGENT-002 | Prompt Agent | 生成可执行 AI Prompt |

---

# Optional Agent Outputs（可选智能体输出）

本命令可以读取：

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |

---

# Execution Order（执行顺序）

本命令必须按照以下顺序执行：

```text
1. Load Prompt Task
↓
2. Load Project Record
↓
3. Load Required Database Records
↓
4. Load Required Knowledge Nodes
↓
5. Run WORKFLOW-002
↓
6. Run AGENT-002 Prompt Agent
↓
7. Generate Base Prompt
↓
8. Generate Model-Specific Prompt
↓
9. Generate Negative Prompt
↓
10. Run Consistency Check
↓
11. Output Final Prompt Package
```

---

# Input Requirements（输入要求）

用户可以提供以下输入：

```text
Prompt Type:
Image Prompt / Video Prompt / Storyboard Prompt / Character Prompt / Environment Prompt / Motion Prompt / Camera Prompt / Lighting Prompt / Thumbnail Prompt

Target Model:
ChatGPT / Midjourney / Flux / ComfyUI / Kling / Veo / Runway

Aspect Ratio:
9:16 / 16:9 / 4:3 / 1:1

Language:
Chinese / English / Bilingual

Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels
```

如果用户没有指定，默认：

```text
Prompt Type:
Video Prompt

Target Model:
Kling / Veo / Runway

Aspect Ratio:
9:16

Language:
Bilingual
```

---

# Forbidden Inputs（禁止输入）

不得通过本命令临时修改：

- Jump 的物种
- Jump 的核心身份
- Jump 的默认服装系统
- Jump 的毛茸茸质感
- TiaoTiao Universe 世界观
- Brand Language
- Master Knowledge Nodes
- Database Record ID
- 文件命名规范

如果用户输入与 TSOS 核心设定冲突，Command 必须拒绝该修改，并回到 Source of Truth。

---

# Output Package（输出包）

本命令最终必须输出：

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

---

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-002 Output

## 1. Prompt Purpose

## 2. Target Model

## 3. Source Records

## 4. Base Prompt

## 5. Model-Specific Prompt

## 6. Negative Prompt

## 7. Consistency Checklist

## 8. Usage Notes
```

---

# Prompt Type Rules（提示词类型规则）

## Image Prompt

适用于：

- 静帧
- 封面
- 角色图
- 环境图
- 主视觉

必须强调：

```text
Subject
Scene
Composition
Lighting
Style
Brand Consistency
Asset Reference
Negative Prompt
```

---

## Video Prompt

适用于：

- AI 视频镜头
- 动作镜头
- 运镜镜头
- 分镜片段

必须强调：

```text
Duration
Subject
Start Frame
Action
End Frame
Camera Movement
Motion Continuity
Lighting
Environment
Negative Prompt
```

---

## Thumbnail Prompt

适用于：

- 小红书封面
- 抖音封面
- 视频号封面
- Shorts / Reels 封面

必须强调：

```text
Clear subject
Safe text area
High readability
Warm lifestyle emotion
Brand color consistency
No visual clutter
```

---

# Model Rules（模型规则）

## Kling / Veo / Runway

输出必须包含：

```text
Duration
Subject
Action
Camera
Motion
Lighting
Environment
Mood
Style
Negative Prompt
```

---

## Midjourney

输出必须包含：

```text
Subject
Composition
Lighting
Style
Color
Mood
Visual Quality
Negative Direction
```

---

## Flux / ComfyUI

输出必须包含：

```text
Subject clarity
Material detail
Fur texture
Outfit consistency
Lighting
Composition
Negative Prompt
```

---

## ChatGPT

输出必须包含：

```text
Clear sections
Reference IDs
Prompt reasoning summary
Consistency checklist
```

---

# Base Prompt Template（基础提示词模板）

```text
Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit, Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Scene:
TiaoTiao Studio Office, warm modern creator studio, realistic programmer workspace, laptop, keyboard, monitor, desk lamp, notebook, coffee cup, backpack, headphones and small plant.

Action:
Jump finishes work and begins a small after-work moment, relaxed and natural, expressing freedom and everyday joy.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, natural camera motion, cinematic documentary style, environmental storytelling.

Lighting:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows, cozy creator studio mood.

Mood:
Freedom, relaxation, warmth, ordinary life becoming meaningful after work.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth, high-quality film still.

Brand Consistency:
Warm, optimistic, honest, creative, lifestyle-focused TiaoTiao Studio brand language.

Asset Reference:
Use ASSET-001 for Jump character consistency.
```

---

# Standard Video Prompt Template（标准视频提示词模板）

```text
Duration:
6–8 seconds

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit, Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Start Frame:
Jump is inside TiaoTiao Studio Office at the end of the workday.

Action:
Jump finishes work, closes the laptop, packs her backpack and begins to leave the warm studio with a relaxed and natural movement.

End Frame:
Jump moves toward the office exit, carrying the feeling that life begins again after work.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, natural camera movement, subtle handheld documentary energy, environmental storytelling.

Motion:
Natural walking, relaxed pace, realistic weight transfer, grounded foot contact, soft body mechanics, subtle tail movement.

Lighting:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows.

Environment:
TiaoTiao Studio Office, warm modern creator studio, realistic programmer workspace.

Mood:
Freedom, warmth, relaxation, everyday joy.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth.

Negative Prompt:
Do not change Jump's species, no human version, no sliding feet, no robotic motion, no game animation, no cyberpunk lighting, no horror mood, no extreme wide-angle distortion.
```

---

# Standard Negative Prompt（标准负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, do not remove fluffy fur, do not make Jump muscular, do not change outfit, do not remove Fire Dragon Fruit Pink accents, do not use horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, floating body, mechanical tail movement, impossible motion, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, inconsistent environment, aggressive expression, cheap CGI look, hard-selling commercial mood, clickbait visual style.
```

---

# Consistency Checklist（一致性检查）

本命令结束前必须检查：

```text
[ ] Jump 是否仍然是拟人化毛茸茸小狗
[ ] Jump 是否保持程序员身份
[ ] Jump 是否保持苗条体型
[ ] Jump 外观是否参考 ASSET-001
[ ] 是否符合 OUTFIT-001
[ ] 是否符合 COLOR-001
[ ] 是否符合 STYLE-001
[ ] 是否符合 ENV-001
[ ] 是否符合 CAM-001
[ ] 是否符合 LGT-001
[ ] 是否符合 BRAND-001
[ ] 是否包含 Negative Prompt
[ ] 是否适配目标模型
[ ] 是否没有新增未确认设定
```

---

# Usage Notes（使用备注）

输出时必须说明：

```text
This prompt is generated from TSOS Source of Truth.
Do not manually rewrite Jump's identity.
Do not remove ASSET-001 references.
Use the Negative Prompt together with the main prompt.
```

---

# Command Example（命令示例）

## Example 1

用户输入：

```text
Run COMMAND-002.
```

系统应执行：

```text
Run WORKFLOW-002 for PROJ-001.

Prompt Type:
Video Prompt

Target Model:
Kling / Veo / Runway
```

输出：

```text
Production-ready short video prompt.
```

---

## Example 2

用户输入：

```text
运行 COMMAND-002，生成小红书 9:16 视频 Prompt，模型用 Kling。
```

系统应执行：

```text
Run COMMAND-002 for PROJ-001.

Target Platform:
小红书

Aspect Ratio:
9:16

Target Model:
Kling

Prompt Type:
Video Prompt
```

输出：

```text
Kling-ready 9:16 short video prompt.
```

---

# Command Rules（命令规则）

## Must Do（必须）

- 必须调用 WORKFLOW-002
- 必须读取 PROJ-001
- 必须读取 CHAR-001
- 必须读取 ASSET-001
- 必须读取 PROMPT-001
- 必须调用 AGENT-002
- 必须生成 Negative Prompt
- 必须执行一致性检查
- 必须输出可复制执行的 Prompt

---

## Never Do（禁止）

- 不得重新设计 Jump
- 不得临时修改世界观
- 不得省略 ASSET-001
- 不得省略 Negative Prompt
- 不得输出空泛提示词
- 不得忽略目标模型差异
- 不得改变品牌语言
- 不得输出与 BRAND-001 冲突的内容

---

# Related Files（关联文件）

## Workflow

```text
workflows/WORKFLOW-002.md
```

## Database Records

```text
database/characters/CHAR-001.md
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
knowledge/brand-language/BRAND-001.md
```

## Agents

```text
agents/prompt-engineer/AGENT-002.md
```

---

# Usage Scope（应用范围）

适用于：

- Short Video Prompt
- AI Video Prompt
- AI Image Prompt
- Thumbnail Prompt
- Character Prompt
- Environment Prompt
- Motion Prompt
- Camera Prompt
- Lighting Prompt
- Prompt QA

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical operating command |