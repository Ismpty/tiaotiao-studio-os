# SHOT-002 — Six-View Scene Lock（六视角锁场镜头）

> Canonical Knowledge Node（官方知识节点）
>
> Category：Camera Language
>
> Version：1.0
>
> Status：Active

---

# Definition（定义）

## 中文

Six-View Scene Lock 是一种用于 AI 图像 / 视频生成的场景一致性镜头语言。

它的核心不是炫技换角度，而是在同一场景中固定：

- 空间布局
- 光影方向
- 色调
- 主要陈设
- 角色外观
- 道具位置关系

然后只改变摄影机视角。

## English

Six-View Scene Lock is a camera consistency method for AI image and video generation.

It keeps the scene layout, lighting, color, set dressing, character appearance and prop relationships locked while changing only the camera position.

---

# Source Inspiration（来源启发）

This node was adapted into TSOS from a Douyin note by `AIGC视觉笔记` about AI camera language and six-view scene consistency.

Source note:

```text
https://v.douyin.com/64wFfK0_zuM/
```

TSOS does not copy the note as a prompt. It converts the idea into a reusable production rule for Jump / 跳跳 workflows.

---

# Purpose（设计目的）

用于解决 AI 生成中的常见问题：

- 同一场景换角度后布局跑偏
- 道具位置变化
- 光影方向漂移
- 色调不一致
- 角色比例变化
- 前后镜头空间关系断裂

目标是让模型理解：

```text
这是同一个场景，只是摄影机换了位置。
```

---

# Six View Order（六视角顺序）

默认六视角顺序：

```text
1. Front Eye-Level Wide View
2. 45-Degree Side Medium View
3. Low-Angle View
4. Oblique High-Angle View
5. Vertical Top-Down View
6. Reverse Eye-Level Lookback View
```

中文对应：

```text
1. 正面平视全景
2. 45 度斜侧中景
3. 低位仰拍
4. 斜向高俯
5. 垂直正俯视
6. 反向平视回望
```

---

# Scene Lock Rules（锁场规则）

切换视角时必须保持：

```text
[ ] 场景平面布局不变
[ ] 角色身份和外观不变
[ ] 角色相对位置不乱跳
[ ] 主要道具位置不漂移
[ ] 光源方向不反转
[ ] 色调和曝光不突然改变
[ ] 镜头高度变化合理
[ ] 透视变化符合真实摄影逻辑
```

---

# When to Use（适用场景）

推荐用于：

- Storyboard reference sheets
- Identity card + environment reference combinations
- 同一场景多镜头生成
- 场景一致性测试
- 室内空间
- 餐馆 / 超市 / 电影院 / 街边小摊
- 需要证明空间关系的镜头组

特别适合 PROJ-001：

```text
Shot 1 — Work Ending
Shot 3 — Dinner Time
Shot 4 — Supermarket Walk
Shot 5 — Movie Night
Shot 6 — Street Snack
```

---

# When NOT to Use（不适用场景）

避免用于：

- 快速追逐
- 强动作打斗
- 抽象情绪蒙太奇
- 完全梦境化画面
- 场景本身需要变化的转场
- 角色移动距离很长的连续跟拍

对于长距离移动镜头，优先使用：

```text
SHOT-001 — Hero Tracking Shot
```

---

# Prompt Translation Rule（提示词转写规则）

内部可以引用：

```text
SHOT-002
Six-View Scene Lock
```

但模型可见 Prompt 必须写成自然语言，例如：

```text
Keep the same scene layout, lighting direction, color palette, main props and character appearance locked. Only change the camera position.
```

不要只写：

```text
use SHOT-002
follow Six-View Scene Lock
```

---

# AI Prompt Building Block（AI 提示词模块）

可转写为：

```text
保持同一个场景不变，只改变机位。空间布局、主要道具、光源方向、色调、角色外观和角色相对位置必须保持一致。当前镜头使用 [填写视角名称]，视角变化必须符合真实摄影透视，不要改变场景结构，不要移动家具，不要让道具消失，不要让光线方向反转。
```

---

# View Usage Guide（视角使用指南）

| View | Best Use | Avoid |
|---|---|---|
| Front Eye-Level Wide View | 建立空间、角色和道具关系 | 不要过度空旷 |
| 45-Degree Side Medium View | 展示角色动作和环境层次 | 不要改变道具位置 |
| Low-Angle View | 增强角色存在感和空间高度 | 不要变成夸张英雄大片 |
| Oblique High-Angle View | 展示行动路线和场景结构 | 不要压扁角色 |
| Vertical Top-Down View | 锁定平面布局和道具位置 | 不要用于情绪表演主镜头 |
| Reverse Eye-Level Lookback View | 结尾回望、情绪落点、空间反打 | 不要改变前景/背景关系 |

---

# Jump Runtime Rule（跳跳运行规则）

用于 Jump / 跳跳时必须保持：

```text
Jump remains a real dog-form character wearing clothes.
```

六视角不能导致：

- 人形站立
- 人类手掌
- 人类手臂
- 人类双腿
- 身体比例漂移
- 服装丢失
- 小背包消失

---

# Relationship With SHOT-001（与 SHOT-001 的关系）

```text
SHOT-001 = movement companionship
SHOT-002 = scene consistency across camera angles
```

二者可以组合：

```text
先用 SHOT-002 锁定空间。
再用 SHOT-001 生成角色跟拍。
```

---

# Related Knowledge（关联知识）

STYLE-001

COLOR-001

MOTIONLANG-001

WORLD-001

---

# Changelog（更新记录）

| Version | Date | Changes |
|---------|------|----------|
| 1.0 | 2026 | Added six-view scene consistency camera language |
