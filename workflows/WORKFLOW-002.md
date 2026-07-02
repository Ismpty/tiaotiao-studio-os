# WORKFLOW-002 — Short Video Prompt Workflow（短视频提示词工作流）

> Canonical Workflow Template（官方工作流模板）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Short Video Prompt Workflow 是 TiaoTiao Studio OS 的短视频提示词生成工作流。

它用于把 Project、Storyboard、Character、Environment、Camera、Lighting、Motion、Asset 和 Knowledge Nodes 转化为可直接用于 AI 图片 / 视频生成的 Prompt。

这个 Workflow 不负责重新设计角色，也不负责改写故事。

它只负责把已经确认的 TSOS 内容组织成稳定、清晰、可复制、可执行的提示词。

## English

Short Video Prompt Workflow is the short-video prompt generation workflow of TiaoTiao Studio OS.

It transforms project records, storyboard outputs, character records, environment records, camera records, lighting records, motion records, asset references and knowledge nodes into executable AI image and video prompts.

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 快速生成可用的短视频镜头 Prompt
- 保持 Jump 角色一致性
- 保持 TSOS 世界观一致性
- 保持镜头、灯光、动作、风格统一
- 避免每次从零写 Prompt
- 支持不同 AI 模型适配
- 让提示词可以进入实际生产

---

# Default Project（默认项目）

本 Workflow 默认服务：

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
| Asset DB | ASSET-001 | 角色参考资产 |
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

| Agent | Role |
|---|---|
| AGENT-002 | Prompt Agent |

---

# Optional Agent Inputs（可选智能体输入）

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Prompt Task Setup
↓
2. Source Record Collection
↓
3. Shot Context Extraction
↓
4. Prompt Variable Mapping
↓
5. Base Prompt Generation
↓
6. Model Adaptation
↓
7. Negative Prompt Generation
↓
8. Consistency Check
↓
9. Final Prompt Package
```

---

# Stage 1 — Prompt Task Setup（提示词任务初始化）

## Input（输入）

确认本次 Prompt 用途：

```text
Image Prompt
Video Prompt
Storyboard Prompt
Character Prompt
Environment Prompt
Motion Prompt
Camera Prompt
Lighting Prompt
Thumbnail Prompt
```

## Task（任务）

确定：

- 目标平台
- 目标模型
- 输出比例
- 是否为单张图
- 是否为视频镜头
- 是否需要中英文 Prompt
- 是否需要负面词

## Output（输出）

```text
Prompt Task Brief
```

## Required Check（必须检查）

```text
[ ] 是否明确 Prompt 类型
[ ] 是否明确目标模型
[ ] 是否明确输出用途
[ ] 是否明确画幅比例
[ ] 是否需要视频动作描述
```

---

# Stage 2 — Source Record Collection（来源记录收集）

## Input（输入）

读取：

```text
PROJ-001
PROMPT-001
CHAR-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
ASSET-001
```

## Task（任务）

提取：

- 主角身份
- 场景设定
- 故事情绪
- 动作要求
- 镜头要求
- 灯光要求
- 资产参考
- 项目目标

## Output（输出）

```text
Source Record Summary
```

## Required Check（必须检查）

```text
[ ] 是否读取 CHAR-001
[ ] 是否读取 ASSET-001
[ ] 是否读取 PROMPT-001
[ ] 是否读取 PROJ-001
[ ] 是否没有临时新增未确认设定
```

---

# Stage 3 — Shot Context Extraction（镜头上下文提取）

## Input（输入）

可读取：

```text
Storyboard Output
Cinematography Output
Script Output
```

## Task（任务）

提取当前镜头的：

- Shot Number
- Shot Name
- Story Function
- Character Action
- Environment
- Camera
- Motion
- Lighting
- Emotion
- Continuity Notes

## Output（输出）

```text
Shot Context
```

## Required Check（必须检查）

```text
[ ] 当前镜头是否有明确叙事功能
[ ] 当前镜头是否能追溯到 Storyboard Output
[ ] 当前镜头是否符合 PROJ-001
[ ] 当前镜头是否没有脱离故事目标
```

---

# Stage 4 — Prompt Variable Mapping（提示词变量映射）

## Task（任务）

将 TSOS 记录映射为 Prompt 变量：

```text
Subject = CHAR-001 + ASSET-001
Scene = ENV-001
Action = MOT-001 / Storyboard Output
Camera = CAM-001 / SHOT-001
Lighting = LGT-001
Style = STYLE-001
Color = COLOR-001
Emotion = EMOTION-001
Brand = BRAND-001
Negative = PROMPT-001 Negative Rules
```

## Output（输出）

```text
Prompt Variables
```

## Required Check（必须检查）

```text
[ ] Subject 是否来自 CHAR-001 + ASSET-001
[ ] Scene 是否来自 ENV-001
[ ] Camera 是否来自 CAM-001
[ ] Lighting 是否来自 LGT-001
[ ] Style 是否来自 STYLE-001
[ ] Brand 是否来自 BRAND-001
```

---

# Stage 5 — Base Prompt Generation（基础提示词生成）

## Task（任务）

生成基础 Prompt。

标准结构：

```text
Subject:
Scene:
Action:
Camera:
Lighting:
Mood:
Style:
Brand Consistency:
Asset Reference:
```

## Output（输出）

```text
Base Prompt
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

# Stage 6 — Model Adaptation（模型适配）

## Task（任务）

根据目标模型生成对应版本。

---

## ChatGPT Prompt

用于：

- 分镜
- 脚本
- 提示词优化
- 一致性检查

结构要求：

```text
Clear sections
Reference IDs
Bilingual output if needed
Consistency checklist
```

---

## Midjourney Prompt

用于：

- 静帧
- 封面
- 主视觉
- 角色图

结构要求：

```text
Visual-first
Cinematic detail
Composition
Lighting
Style keywords
No long procedural explanation
```

---

## Flux / ComfyUI Prompt

用于：

- 可控图像生成
- 角色一致性
- 环境图
- 参考图

结构要求：

```text
Subject clarity
Material detail
Composition detail
Negative prompt
Asset reference
```

---

## Kling / Veo / Runway Prompt

用于：

- AI 视频镜头生成
- 动作镜头
- 运镜镜头

结构要求：

```text
Duration
Subject
Action
Camera movement
Motion continuity
Lighting change
Environment continuity
Negative motion rules
```

---

# Stage 7 — Negative Prompt Generation（负面提示词生成）

## Task（任务）

生成覆盖以下维度的 Negative Prompt：

```text
Character
Style
Motion
Camera
Lighting
Environment
Brand
```

## Output（输出）

```text
Negative Prompt
```

---

# Standard Negative Prompt（标准负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, do not remove fluffy fur, do not make Jump muscular, do not use horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, floating body, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, inconsistent outfit, aggressive expression, hard-selling commercial mood, clickbait visual style.
```

---

# Stage 8 — Consistency Check（一致性检查）

## Task（任务）

检查最终 Prompt 是否符合 TSOS。

## Checklist（检查表）

```text
[ ] Jump 是否仍然是拟人化毛茸茸小狗
[ ] 是否保持程序员身份
[ ] 是否保持苗条体型
[ ] 是否引用 ASSET-001
[ ] 是否符合 OUTFIT-001
[ ] 是否符合 COLOR-001
[ ] 是否符合 STYLE-001
[ ] 是否符合 ENV-001
[ ] 是否符合 CAM-001
[ ] 是否符合 LGT-001
[ ] 是否符合 BRAND-001
[ ] 是否没有新增未确认设定
[ ] 是否包含 Negative Prompt
```

---

# Stage 9 — Final Prompt Package（最终提示词包）

最终输出必须包含：

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

# Image Prompt Output Template（图片 Prompt 输出模板）

```text
# Image Prompt Output

## Prompt Purpose

## Target Model

## Source Records

## Base Prompt

## Model-Specific Prompt

## Negative Prompt

## Consistency Checklist

## Usage Notes
```

---

# Video Prompt Output Template（视频 Prompt 输出模板）

```text
# Video Prompt Output

## Prompt Purpose

## Target Model

## Duration

## Subject

## Action

## Camera

## Motion

## Lighting

## Environment

## Mood

## Style

## Negative Prompt

## Consistency Checklist

## Usage Notes
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-002 for PROJ-001.

Prompt Type:
Video Prompt

Target Model:
Kling / Veo / Runway

Use:
CHAR-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
PROJ-001

Use Knowledge:
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
MOTIONLANG-001
OUTFIT-001
BRAND-001

Output:
Production-ready short video prompt.
```

---

# Workflow Rules（工作流规则）

## Must Do（必须）

- 必须读取现有 TSOS 记录
- 必须引用 ASSET-001
- 必须包含负面提示词
- 必须适配目标模型
- 必须保持角色一致
- 必须保持品牌一致
- 必须输出可复制执行的 Prompt

---

## Never Do（禁止）

- 不得重新设计 Jump
- 不得临时改变世界观
- 不得省略负面提示词
- 不得生成空泛描述
- 不得忽略目标模型差异
- 不得使用与 BRAND-001 冲突的视觉语言
- 不得输出不可执行 Prompt

---

# Related Files（关联文件）

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
- Character Prompt
- Environment Prompt
- Motion Prompt
- Camera Prompt
- Lighting Prompt
- Cover Prompt
- Prompt QA

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical workflow template |