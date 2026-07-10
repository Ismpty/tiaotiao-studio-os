# BLOCKING-001 — Overhead Scene Blocking Map（俯视场景调度图）

> Canonical Knowledge Node（官方知识节点）
>
> Category：Scene Blocking
>
> Version：1.0
>
> Status：Active

---

# Definition（定义）

## 中文

Overhead Scene Blocking Map 是 TSOS 用于复杂视频生成前的空间调度工具。

它用一张俯视图提前锁定：

- 场景平面布局
- 角色初始站位
- 角色行动路线
- 角色之间的空间关系
- 摄影机位置
- 摄影机运动路径
- 镜头切换点
- 道具和障碍物位置
- 关键动作发生区域

它的目标是减少 AI 视频生成中的无效“抽卡”：

```text
人物站位乱
追逐方向乱
打斗空间乱
多人对话轴线乱
一镜到底路径乱
镜头切换后空间关系崩
```

## English

Overhead Scene Blocking Map is a top-down planning diagram used before AI video generation to lock spatial relationships, character positions, movement paths, camera paths and shot transition points.

---

# Source Inspiration（来源启发）

This node was adapted into TSOS from the user-provided Douyin video reference about `AI 俯视场景调度图`.

User-provided source:

```text
https://v.douyin.com/uE5U0gh3o8s/
```

Resolved video ID during capture:

```text
7658676046082909425
```

The user-provided source text attributes the method to `一帆老师`.

The Douyin share page returned an anti-crawler script during capture, so TSOS does not claim full video transcription.

This node converts the clearly described method into a reusable TSOS scene-blocking rule.

---

# Core Principle（核心原则）

For any scene with complex spatial relationships, create the overhead blocking map before writing final storyboard or video prompts.

Use the map to answer:

```text
Who is where?
Who moves where?
What blocks movement?
Where is the camera?
How does the camera move?
Where does the shot change?
What must stay spatially consistent?
```

If these questions are unclear, video generation should pause before prompt production.

---

# When to Use（适用场景）

Use BLOCKING-001 for:

- 多人对话
- 双人或多人走位
- 追逐
- 打斗调度
- 一镜到底
- 镜头切换较多的场景
- 房间内复杂移动
- 街道 / 商场 / 超市 / 餐厅的路线规划
- 角色、道具和摄影机都在移动的场景
- 需要保证左右关系、前后关系、距离关系的场景

For simple single-character static shots, BLOCKING-001 is optional.

---

# Overhead Map Elements（俯视图元素）

Every overhead scene blocking map should define:

```text
1. Scene Boundary
2. North / Screen Direction
3. Entrances and Exits
4. Key Props / Obstacles
5. Character Markers
6. Starting Positions
7. Movement Paths
8. Camera Positions
9. Camera Movement Path
10. Shot Change Points
11. Interaction Zones
12. Continuity Locks
```

---

# Standard Symbols（标准符号）

Use simple symbols that remain readable in a rough diagram:

```text
Rectangle = room / scene boundary
Thick line = wall / barrier
Gap = doorway / entrance / exit
Circle = character position
Triangle = camera position
Arrow = movement path
Dotted arrow = planned future movement
Star = key action beat
Square = important prop
Number = shot order or beat order
```

When used with TSOS storyboard annotation colors:

```text
Red = camera movement / camera path
Blue = character / dog movement path
Yellow = prop / obstacle / interaction point
Green = lighting / mood zone
Purple = continuity / transition / shot-change point
```

---

# Map Creation Order（创建顺序）

Create the blocking map in this order:

```text
1. Draw the scene boundary.
2. Mark doors, windows, furniture, obstacles and key props.
3. Mark each character's starting position.
4. Mark each character's destination or route.
5. Mark camera start position.
6. Mark camera movement path.
7. Mark shot-change points or transition points.
8. Mark action beats and interaction zones.
9. Add continuity locks.
10. Translate the map into storyboard shot details.
```

Do not start with camera tricks.

Start with spatial truth.

---

# Scene Blocking Grammar（调度语法）

Use this structure when writing a blocking note:

```text
Scene Layout:
[Describe the top-down space.]

Character Positions:
[Character A starts at... Character B starts at...]

Movement Paths:
[Character A moves from... to... Character B crosses behind...]

Camera Path:
[Camera starts at... tracks toward... pans to...]

Shot / Beat Points:
[Beat 1 happens at... Beat 2 happens when...]

Continuity Locks:
[Keep left-right relation, distance, direction, props and exits consistent.]
```

Model-readable prompt block:

```text
Use the uploaded overhead scene blocking map as the spatial reference. Keep all character positions, movement paths, camera path, doors, props and left-right relationships consistent with the map. Do not swap character positions, reverse movement direction, remove obstacles or change the room layout.
```

---

# Use Cases（使用案例）

## 1. Multi-Character Dialogue（多人对话）

Blocking map must define:

```text
who sits / stands where
who faces whom
conversation axis
camera side of the axis
shot-reverse-shot direction
empty space between characters
```

Avoid:

- crossing the 180-degree axis without intent
- swapping left / right character positions
- changing table or chair positions between shots

---

## 2. Chase（追逐）

Blocking map must define:

```text
chaser starting point
target starting point
movement direction
obstacles
distance gap
camera tracking side
turning points
exit point
```

Avoid:

- characters teleporting
- distance gap randomly changing
- chase direction reversing between shots

---

## 3. Fight / Action Blocking（打斗调度）

Blocking map must define:

```text
fighter positions
attack direction
defense direction
safe distance
impact zone
fall / dodge path
camera safety side
```

Avoid:

- impossible body contact
- characters changing sides without a visible cross
- camera crossing into action without spatial reason

TSOS safety:

```text
Violent or harmful content must stay within project and platform safety rules.
```

---

## 4. One-Take Camera Movement（一镜到底运镜）

Blocking map must define:

```text
camera start point
camera end point
character route
turning points
foreground wipes
focus handoffs
timing beats
exit / entrance moments
```

Avoid:

- impossible camera path through walls
- camera moving faster than the subject without explanation
- unplanned foreground occlusion

---

# Jump Runtime Rule（跳跳运行规则）

When used for Jump / 跳跳:

```text
Jump remains a real dog-form character wearing clothes.
```

The overhead map should mark Jump with a dog-form marker, not a humanoid marker.

Use labels such as:

```text
Jump / real dog-form character
dog-height camera
four-legged movement path
small backpack position
```

Do not use a human stick figure if it causes the model to turn Jump into a human body.

---

# Relationship With Storyboard（与分镜关系）

The overhead blocking map is not the final storyboard.

It comes before or alongside storyboard generation:

```text
Overhead Blocking Map
↓
Storyboard
↓
Universal Video Prompt
↓
Model-readable check
↓
COMMAND-005 review
```

Storyboard still must use:

```text
black-and-white rough pencil line art
colored annotation system
```

The blocking map may be more schematic than the storyboard, but it should use the same annotation color meanings.

---

# Relationship With Other Knowledge（与其他知识节点关系）

```text
BLOCKING-001 = spatial plan
SHOT-002 = same-scene camera consistency
VISUALPARAM-001 = image/video parameter clarity
TRANSITION-001 = bridge between shots
MOTIONLANG-001 = believable character motion
```

Use BLOCKING-001 before SHOT-002 when the scene has multiple characters or complex movement.

Use BLOCKING-001 before TRANSITION-001 when the transition depends on spatial direction or camera path.

---

# Prompt Runtime Rule（提示词运行规则）

Internal TSOS references may use:

```text
BLOCKING-001
Overhead Scene Blocking Map
```

Model-facing prompts must translate this into natural language.

Do not write only:

```text
use BLOCKING-001
follow the blocking map
```

Write:

```text
Use the uploaded top-down scene blocking map as the spatial reference. Keep the room layout, character starting positions, movement arrows, camera path, doors, props and left-right relationships consistent throughout the shot.
```

---

# COMMAND-005 Review Requirements（COMMAND-005 审查要求）

COMMAND-005 must check blocking for:

```text
[ ] Whether the scene needs an overhead blocking map.
[ ] Whether scene boundary, doors, props and obstacles are clear.
[ ] Whether character starting positions are clear.
[ ] Whether movement paths are clear.
[ ] Whether camera position and movement path are clear.
[ ] Whether shot-change or transition points are marked.
[ ] Whether left-right, front-back and distance relationships remain stable.
[ ] Whether the storyboard follows the blocking map.
[ ] Whether video prompts reference the uploaded map in model-readable language.
[ ] For Jump, whether the map preserves real dog-form anatomy and dog-height camera logic.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial overhead scene blocking map grammar adapted from user-provided Douyin source theme |
