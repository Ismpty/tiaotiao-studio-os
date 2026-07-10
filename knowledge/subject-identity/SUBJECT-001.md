# SUBJECT-001 — Generic Subject Identity Card Grammar（通用主体身份卡语法）

> Canonical Knowledge Node（官方知识节点）
>
> Category：Subject Identity
>
> Version：1.0
>
> Status：Active

---

# Definition（定义）

## 中文

Generic Subject Identity Card Grammar 是 TSOS 用于生成和锁定任意主体身份卡的通用语法。

它让系统不仅能服务 Jump / 跳跳，也能服务：

- 人物
- 动物
- 植物
- 物品 / 产品
- 场景主体
- 品牌吉祥物
- 非跳跳 IP 角色

身份卡的作用是让 AI 模型在后续故事板、视频生成和一致性检查中保持主体稳定。

## English

Generic Subject Identity Card Grammar is the TSOS grammar for creating and locking identity cards for any subject, including humans, animals, plants, objects, products, scene subjects, mascots and non-Jump IP characters.

---

# Source of Truth Rule（事实来源规则）

For Jump / 跳跳:

```text
CHAR-001
ASSET-001
OUTFIT-001
```

remain the source of truth.

For custom subjects:

```text
the user-provided subject brief
uploaded reference images
approved identity card
approved project notes
```

become the local source of truth for that custom subject.

GitHub remains the system source of truth.

Notion remains only the visual management layer.

---

# Subject Modes（主体模式）

TSOS supports two subject modes:

```text
1. Jump Mode
2. Custom Subject Mode
```

## Jump Mode

Use when the subject is Jump / 跳跳 or PROJ-001.

Non-negotiable rule:

```text
Jump remains a real dog-form character wearing clothes.
```

Jump Mode must not be weakened by this generic node.

## Custom Subject Mode

Use when the user explicitly requests a subject other than Jump.

Examples:

```text
一位女导演
一只狐狸
一株向日葵
一台复古相机
一个原创品牌吉祥物
一个非跳跳短剧角色
```

In Custom Subject Mode, do not apply Jump-only constraints unless the user explicitly says the subject is Jump or part of the Jump series.

---

# Identity Card Core Fields（身份卡核心字段）

Every subject identity card should define:

```text
Subject Name:
Subject Type:
Role / Function:
Core Visual Identity:
Shape / Structure:
Scale / Proportion:
Surface / Texture:
Color System:
Distinctive Features:
Accessories / Props:
Movement / Behavior:
Environment Relationship:
Personality / Mood:
Continuity Locks:
Negative Constraints:
Reference Inputs:
```

Not every field needs the same level of detail, but every identity card must define what cannot drift.

---

# Human Subject Identity（人物主体身份）

Use for real or fictional human subjects.

Required fields:

```text
age range
body type
face / hair / skin tone
clothing
accessories
posture
profession / role
personality mood
```

Continuity locks:

```text
same face
same hairstyle
same clothing
same body proportion
same accessories
same age range
same role identity
```

Negative constraints:

```text
do not change age
do not change face
do not change hairstyle
do not swap clothing
do not change gender presentation unless requested
do not add extra limbs or distorted anatomy
```

---

# Animal Subject Identity（动物主体身份）

Use for real animals, stylized animals or animal characters.

Required fields:

```text
species
body form
fur / feather / skin texture
size
color pattern
distinctive markings
accessories if any
movement style
temperament
```

Continuity locks:

```text
same species
same body anatomy
same size
same markings
same texture
same accessories
same movement style
```

Negative constraints:

```text
do not change species
do not turn into a human unless requested
do not add human hands or human legs unless the approved design requires them
do not lose markings
do not change body proportion between shots
```

Jump note:

```text
If the animal is Jump, use Jump Mode and keep the real dog-form character wearing clothes rule.
```

---

# Plant Subject Identity（植物主体身份）

Use for flowers, trees, crops, magical plants or plant characters.

Required fields:

```text
species / plant type
growth stage
stem / trunk structure
leaf shape
flower / fruit shape
color pattern
surface texture
root / pot / soil relationship
movement in wind
season / environment
```

Continuity locks:

```text
same species
same growth stage
same leaf shape
same flower / fruit color
same stem / trunk structure
same pot or ground relationship
same scale
```

Negative constraints:

```text
do not change species
do not change from flower to tree unless requested
do not change growth stage between shots without story reason
do not randomize leaf shape
do not change flower color
do not make roots, pot or ground relationship inconsistent
```

---

# Object / Product Subject Identity（物品 / 产品主体身份）

Use for props, products, tools, devices, vehicles and hero objects.

Required fields:

```text
object category
shape
material
color
scale
surface finish
brand marks if any
functional details
wear / age / condition
how it is handled
```

Continuity locks:

```text
same shape
same material
same color
same scale
same surface details
same logo / mark placement
same functional parts
```

Negative constraints:

```text
do not change product design
do not move logo position
do not change material
do not add unsupported buttons, screens or parts
do not change scale between shots
```

---

# Scene Subject Identity（场景主体身份）

Use when the subject is a place or environment.

Required fields:

```text
location type
spatial layout
main structures
entrances / exits
key props
lighting source
color tone
texture
time of day
atmosphere
```

Continuity locks:

```text
same layout
same entrance / exit positions
same major props
same lighting direction
same color tone
same scale
```

Use with:

```text
SHOT-002
BLOCKING-001
VISUALPARAM-001
```

---

# Identity Card Prompt Template（身份卡提示词模板）

Model-facing prompt:

```text
Create an identity card for [subject name], a [subject type].

The subject's core identity is:
[natural language description of role, appearance and function].

Visual identity:
[shape, structure, scale, texture, color, distinctive features].

Movement / behavior:
[how the subject moves, behaves or changes].

Environment relationship:
[where the subject belongs and how it relates to space, props or other characters].

Continuity locks:
Keep [specific features] consistent across all future images, storyboards and videos.

Negative constraints:
Do not [specific drift risks].
```

中文模板：

```text
为 [主体名称] 创建一张身份卡。主体类型是 [人物 / 动物 / 植物 / 物品 / 场景 / 其他]。

主体核心身份：
[用自然语言描述角色、外观、功能和气质]。

视觉身份：
[形状、结构、比例、材质、颜色、识别特征]。

运动 / 行为：
[主体如何移动、变化或表现]。

环境关系：
[主体属于什么环境，如何与空间、道具或其他角色发生关系]。

连续性锁定：
后续所有图像、故事板和视频中必须保持 [具体特征] 不变。

负面约束：
禁止 [具体漂移风险]。
```

---

# Storyboard Use Rule（故事板使用规则）

Storyboard generation must load the approved identity card.

For any subject:

```text
Identity Card = subject appearance and continuity
Storyboard = shot structure and action
Universal Video Prompt = execution rules
```

Do not use storyboard prompts to redesign the subject unless the user explicitly asks to revise the identity card.

---

# Prompt Runtime Rule（提示词运行规则）

Internal TSOS references may use:

```text
SUBJECT-001
Generic Subject Identity Card Grammar
```

Model-facing prompts must translate this into natural language.

Do not write only:

```text
use SUBJECT-001
follow the generic identity card rule
```

Write:

```text
Create a stable identity card for this subject. Clearly define the subject type, core appearance, shape, scale, texture, color pattern, distinctive features, movement behavior, environment relationship, continuity locks and negative constraints so future images, storyboards and videos keep the same subject.
```

---

# COMMAND-005 Review Requirements（COMMAND-005 审查要求）

COMMAND-005 must check subject identity for:

```text
[ ] Whether the output is in Jump Mode or Custom Subject Mode.
[ ] Whether the subject type is clearly defined.
[ ] Whether the identity card defines shape, structure, scale, texture and color.
[ ] Whether distinctive features are locked.
[ ] Whether movement or behavior is appropriate to the subject type.
[ ] Whether environment relationship is clear.
[ ] Whether continuity locks are specific.
[ ] Whether negative constraints prevent subject drift.
[ ] Whether model-facing prompts avoid raw internal IDs.
[ ] If Jump Mode, whether Jump remains a real dog-form character wearing clothes.
[ ] If Custom Subject Mode, whether Jump-only constraints were not accidentally applied.
```

---

# Relationship With Other Knowledge（与其他知识节点关系）

```text
SUBJECT-001 = subject identity and continuity
VISUALPARAM-001 = visual parameter clarity
BLOCKING-001 = spatial planning
SHOT-001 / SHOT-002 = camera language and scene consistency
TRANSITION-001 = transitions between shots
```

SUBJECT-001 should be loaded before storyboard and prompt generation for any non-default subject.

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial generic subject identity card grammar for humans, animals, plants, objects and scene subjects |
