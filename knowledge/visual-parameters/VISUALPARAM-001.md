# VISUALPARAM-001 — AIGC Base Visual Parameter Grammar（AIGC 基础画面参数语法）

> Canonical Knowledge Node（官方知识节点）
>
> Category：Visual Parameters
>
> Version：1.0
>
> Status：Active

---

# Definition（定义）

## 中文

AIGC Base Visual Parameter Grammar 是 TSOS 用于描述 AI 图像 / 视频基础画面参数的通用语法。

它把“画面看起来怎么样”拆成模型更容易理解的参数层：

- 画幅
- 景别
- 构图
- 机位
- 焦段
- 景深
- 灯光
- 色彩
- 材质
- 运动
- 连续性
- 负面约束

它不是单独的风格，也不是镜头炫技词库。

它的作用是让每个 Prompt、Storyboard 和 Review 都能稳定回答：

```text
画面参数是否明确、可执行、可复现？
```

## English

AIGC Base Visual Parameter Grammar is the TSOS grammar for describing foundational AI image and video visual parameters.

It turns vague visual intent into structured, model-readable production parameters.

---

# Source Inspiration（来源启发）

This node was adapted into TSOS from the user-provided Douyin note reference by `赛博阿智pro` about AIGC basic visual parameters for AI short drama production.

User-provided source:

```text
https://v.douyin.com/L5OdepTLrX4/
```

Resolved note ID during capture:

```text
7657167225338987919
```

The Douyin share page returned an anti-crawler script during capture, so TSOS does not claim full slide-level extraction.

This node converts the visible source theme into a reusable TSOS visual parameter grammar.

---

# Core Principle（核心原则）

Every model-facing visual prompt should include enough parameters to define the image, but not so many that the model loses the story.

Use parameters to clarify:

```text
what the model must preserve
what the camera should see
what the image should feel like
what must not drift
```

Avoid using parameters as decoration.

---

# Base Grammar（基础语法）

Use this structure when writing model-facing prompts:

```text
Create a [format / aspect ratio] shot of [subject and action] in [environment].
Use [shot size], [camera angle], [lens / focal length], [camera distance] and [depth of field].
Compose the frame with [composition rule], [subject position] and [background relationship].
Light the scene with [lighting source], [lighting direction], [contrast level] and [mood].
Use [color palette], [texture detail] and [rendering realism].
Maintain [character identity / outfit / props / scene continuity].
Avoid [negative constraints].
```

中文结构：

```text
生成一个 [画幅 / 比例] 的画面，主体是 [角色和动作]，场景是 [环境]。
使用 [景别]、[机位]、[焦段]、[摄影机距离] 和 [景深]。
构图采用 [构图规则]，主体位于 [画面位置]，背景保持 [空间关系]。
灯光来自 [光源]，方向为 [光线方向]，对比度为 [对比强度]，情绪为 [情绪]。
色彩使用 [色彩系统]，材质细节为 [材质描述]，整体保持 [真实度]。
保持 [角色身份 / 服装 / 道具 / 场景连续性]。
避免 [负面约束]。
```

---

# Parameter Families（参数类型）

## 1. Format / Canvas（画幅）

Defines platform and frame shape.

Common values:

```text
vertical 9:16
horizontal 16:9
square 1:1
cinematic 2.39:1
portrait 4:5
```

TSOS defaults:

```text
Short video: vertical 9:16
Storyboard: match target platform, usually vertical 9:16
Reference sheet: neutral 1:1 or 4:5 when useful
```

Model-readable example:

```text
Use a vertical 9:16 short-video frame with enough headroom and floor space for a real dog-form character.
```

---

## 2. Shot Size（景别）

Defines how much of the subject appears in frame.

Common values:

```text
extreme wide shot
wide shot
full body shot
medium full shot
medium shot
medium close-up
close-up
extreme close-up
insert shot
```

Use guide:

| Shot Size | Best Use |
|---|---|
| Wide shot | Establish space and movement path |
| Full body shot | Show dog-form anatomy and outfit |
| Medium shot | Show action and emotion together |
| Close-up | Show expression, prop or detail |
| Insert shot | Show object interaction |

Jump rule:

```text
Use full body or medium full shots whenever anatomy continuity must be verified.
```

---

## 3. Camera Angle / Height（机位与高度）

Defines where the camera looks from.

Common values:

```text
eye-level
low angle
high angle
top-down
45-degree side view
over-the-shoulder
reverse angle
profile view
front view
three-quarter view
```

TSOS default:

```text
eye-level or slightly low dog-height camera
```

Avoid:

- extreme drone angle without story purpose
- FPS game perspective
- camera height that turns Jump into a human-like standing figure

Model-readable example:

```text
Place the camera at a low dog-height eye level, close enough to feel companion-like but wide enough to preserve the full dog-form body and clothing.
```

---

## 4. Lens / Focal Length（镜头焦段）

Defines perspective, compression and intimacy.

Common values:

```text
24mm wide
28mm wide-natural
35mm natural documentary
50mm normal portrait
70mm compressed portrait
85mm close portrait
macro lens
```

TSOS default:

```text
35mm natural documentary lens
```

Use guide:

| Lens | Best Use | Avoid |
|---|---|---|
| 24mm | small rooms, environmental energy | face/body distortion |
| 35mm | default lifestyle realism | overusing for close-up faces |
| 50mm | calm portrait and detail | losing environment context |
| 70mm / 85mm | compressed emotional moment | flattening movement |
| Macro | object detail | using for main action |

---

## 5. Composition（构图）

Defines subject placement and visual hierarchy.

Common values:

```text
rule of thirds
center composition
leading lines
foreground / midground / background layering
negative space
symmetrical composition
frame within frame
diagonal movement line
look room
walking room
```

TSOS default:

```text
rule of thirds with environmental storytelling and clear movement direction
```

Model-readable example:

```text
Compose with Jump on the lower third, leaving walking room in the direction of movement and visible background context.
```

---

## 6. Depth of Field（景深）

Defines focus separation.

Common values:

```text
deep focus
moderate depth of field
shallow depth of field
soft background bokeh
selective focus
rack focus
```

TSOS default:

```text
moderate depth of field
```

Avoid:

- background blur so strong that scene continuity cannot be reviewed
- shallow focus that hides wrong anatomy or outfit drift
- fake mobile portrait blur around fur edges

---

## 7. Lighting（光线）

Defines source, direction, contrast and mood.

Core fields:

```text
source
direction
quality
contrast
color temperature
mood
```

Common values:

```text
soft window light
warm practical lamp
golden hour
overcast soft light
screen glow
street light
cinema lobby light
restaurant warm light
```

TSOS default:

```text
warm natural light, soft shadows, realistic exposure
```

Avoid:

- cold cyberpunk lighting unless approved
- high-saturation RGB
- horror contrast
- dead black shadows
- overexposed white highlights

---

## 8. Color / Tone（色彩与色调）

Defines palette and color logic.

Common fields:

```text
base palette
accent color
white balance
saturation
contrast
skin / fur tone realism
brand accent control
```

TSOS default:

```text
warm low-saturation cinematic documentary color with small Fire Dragon Fruit Pink accents
```

Model-readable example:

```text
Use warm low-saturation documentary color, realistic white balance and only small dragon-fruit pink accent details on accessories or brand elements.
```

---

## 9. Texture / Detail（材质与细节）

Defines surface realism.

Common fields:

```text
fur texture
fabric texture
desk material
food steam
street texture
screen reflection
soft shadow detail
natural imperfections
```

TSOS default:

```text
realistic tactile texture, not plastic, not toy-like, not over-sharpened
```

Jump rule:

```text
Jump's fur must remain fluffy and tactile. Clothing should look like small real dog clothing, not a human outfit pasted onto a human body.
```

---

## 10. Motion / Temporal Parameters（运动与时间参数）

Defines movement quality for video prompts.

Common fields:

```text
camera movement
subject movement
motion speed
motion blur
frame rate feeling
transition beat
continuity direction
```

TSOS default:

```text
24fps cinematic motion, natural camera movement, subtle motion blur, believable physical inertia
```

Avoid:

- robotic movement
- game-camera motion
- impossible camera paths
- over-cranked slow motion without story purpose

---

## 11. Continuity Parameters（连续性参数）

Defines what must stay stable across shots.

Core fields:

```text
character identity
body anatomy
outfit
accessories
prop position
scene layout
light direction
color palette
movement direction
scale
```

Model-readable example:

```text
Maintain the same real dog-form character, same small programmer-style dog outfit, same backpack, same fur texture, same warm lighting direction and consistent scale across the shot.
```

---

# Standard Visual Parameter Block（标准画面参数块）

Use this block in storyboard, prompt package or review output:

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
Motion:
Continuity Locks:
Negative Constraints:
```

---

# TSOS Default Visual Parameter Preset（TSOS 默认参数预设）

For Jump / 跳跳 short videos:

```text
Format:
Vertical 9:16 short-video frame.

Shot Size:
Medium full shot or full body shot when anatomy must be visible.

Camera Angle / Height:
Low dog-height eye-level camera.

Lens:
35mm natural documentary lens.

Composition:
Rule of thirds, clear walking room, foreground / midground / background layering.

Depth of Field:
Moderate depth of field, background readable.

Lighting:
Warm natural light or practical lamp light, soft shadows.

Color / Tone:
Warm low-saturation cinematic documentary palette with small dragon-fruit pink accents.

Texture Detail:
Fluffy real fur, tactile dog clothing, realistic environment materials.

Motion:
24fps cinematic motion, natural camera movement, believable physical inertia.

Continuity Locks:
Same real dog-form body, same clothing, same accessories, same scale, same scene logic.

Negative Constraints:
No humanoid body, no human hands, no human arms, no human legs, no bipedal human standing pose, no plastic toy texture, no game render, no cyberpunk RGB lighting.
```

---

# Prompt Runtime Rule（提示词运行规则）

Internal TSOS references may use:

```text
VISUALPARAM-001
AIGC Base Visual Parameter Grammar
```

Model-facing prompts must translate this into natural language.

Do not write only:

```text
use VISUALPARAM-001
apply basic visual parameters
```

Write:

```text
Use a vertical 9:16 short-video frame, a low dog-height eye-level camera, a 35mm natural documentary lens, moderate depth of field, warm soft practical light, realistic fur and fabric texture, and clear continuity of the character's dog-form anatomy, clothing and backpack.
```

---

# Storyboard Runtime Rule（故事板运行规则）

Storyboards must remain:

```text
black-and-white rough pencil line art
```

Visual parameters may be added as small annotation text beside each shot.

Colored annotations remain:

```text
Red = camera movement
Blue = character / dog movement
Yellow = prop / interaction
Green = lighting / mood
Purple = continuity / transition
```

Do not turn the storyboard into polished color concept art just because visual parameters are detailed.

---

# COMMAND-005 Review Requirements（COMMAND-005 审查要求）

COMMAND-005 must check visual parameters for:

```text
[ ] Format / aspect ratio is specified when needed.
[ ] Shot size supports story and character continuity.
[ ] Camera angle and height are physically plausible.
[ ] Lens choice does not distort Jump or the scene.
[ ] Composition gives the subject clear space and readable context.
[ ] Depth of field does not hide continuity problems.
[ ] Lighting is consistent with STYLE-001 and COLOR-001.
[ ] Color palette respects the TSOS warm documentary look.
[ ] Texture detail avoids plastic, toy-like or game-render results.
[ ] Motion parameters are believable for video.
[ ] Continuity locks preserve character, outfit, props, scene and scale.
[ ] Model-facing prompts do not rely on raw internal IDs.
```

---

# Relationship With Other Knowledge（与其他知识节点关系）

```text
STYLE-001 = overall visual style
COLOR-001 = brand color system
SHOT-001 / SHOT-002 = camera language
TRANSITION-001 = shot-to-shot bridge
VISUALPARAM-001 = base image/video parameter grammar
```

VISUALPARAM-001 should be used to make prompts more precise, not to override story, character, style or brand rules.

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial AIGC base visual parameter grammar adapted from user-provided Douyin source theme |
