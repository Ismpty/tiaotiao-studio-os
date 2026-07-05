# PROMPT-001 — Jump After Work Master Prompt（跳跳下班啦主提示词）

> Canonical Prompt Record（官方提示词记录）  
> Version：1.0  
> Status：Active

---

# Overview（提示词概述）

## 中文

Jump After Work Master Prompt 是《跳跳下班啦》系列的默认主提示词模块。

它不是单次生成用的临时 Prompt，而是一个可重复调用的生产提示词模板。

它的作用是把当前 TSOS 中已经建立的角色、剧集、故事、环境、动作、镜头、灯光和 Knowledge Layer 组合成一个统一的生成指令。

## English

Jump After Work Master Prompt is the default reusable master prompt module for the Jump After Work series.

It combines production database records and Knowledge Layer references into one consistent generation framework.

---

# Database References（数据库引用）

| Database | Record |
|---|---|
| Character DB | CHAR-001 |
| Episode DB | EP-001 |
| Story DB | STORY-001 |
| Environment DB | ENV-001 |
| Motion DB | MOT-001 |
| Camera DB | CAM-001 |
| Lighting DB | LGT-001 |

---

# Knowledge References（知识引用）

| Category 分类 | Knowledge Node 知识节点 |
|---|---|
| Style 视觉风格 | STYLE-001 — Cinematic Documentary |
| Color 配色 | COLOR-001 — Fire Dragon Fruit Palette |
| World 世界观 | WORLD-001 — TiaoTiao Universe |
| Emotion 情绪 | EMOTION-001 — Freedom |
| Camera Language 镜头语言 | SHOT-001 — Hero Tracking Shot |
| Motion Language 动作语言 | MOTIONLANG-001 — Natural Walking Language |
| Outfit 服装 | OUTFIT-001 — Programmer Outfit System |
| Music 音乐语言 | MUSIC-001 — Lifestyle Music Language |
| Story Formula 故事公式 | STORYFORMULA-001 — Work Ends, Adventure Begins |
| Brand Language 品牌语言 | BRAND-001 — TiaoTiao Studio Brand Language |

---

# Prompt Role（提示词作用）

这个 Prompt 主要用于：

- 生成《跳跳下班啦》的分镜
- 生成单张画面 Prompt
- 生成视频镜头 Prompt
- 生成动画动作 Prompt
- 生成封面主视觉 Prompt
- 保持 Jump 角色一致性
- 保持世界观、情绪、镜头和灯光一致性

---

# Master Prompt Structure（主提示词结构）

标准结构：

```text
[Character]
CHAR-001 — Jump

[Episode]
EP-001 — Jump After Work

[Story]
STORY-001 — Work Ends, Adventure Begins

[Environment]
ENV-001 — TiaoTiao Studio Office

[Motion]
MOT-001 — Natural Walking

[Camera]
CAM-001 — Hero Tracking Camera

[Lighting]
LGT-001 — Warm Studio Lighting

[Knowledge Layer]
STYLE-001 + COLOR-001 + WORLD-001 + EMOTION-001 + STORYFORMULA-001 + BRAND-001
```

---

# Prompt Body（提示词正文）

```text
Create a warm cinematic scene for the Jump After Work series.

Main character: Jump, a fluffy real dog-form character wearing programmer-style dog clothes. Jump must keep four-legged dog anatomy, dog proportions, fluffy fur, friendly expression, warm optimistic personality, optional small backpack / badge / collar charm, and subtle Fire Dragon Fruit Pink brand accents.

Scene context: Jump has just finished work inside TiaoTiao Studio Office. The environment is a warm modern creator studio with a realistic programmer desk, laptop, keyboard, monitor, desk lamp, notebook, coffee cup, backpack, headphones and small plant.

Story feeling: Work ends, adventure begins. The mood should express freedom, relaxation, everyday joy and the feeling that life begins again after work.

Camera: Hero tracking camera, 35mm lens, eye-level framing, natural camera motion, cinematic documentary style, subtle handheld energy, environmental storytelling.

Motion: Natural dog-form walking, relaxed pace, realistic weight transfer, grounded paw contact, soft body mechanics, subtle tail movement, friendly expression. Do not use human walking or humanoid posing.

Lighting: Warm studio lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows, cozy creator studio mood.

Visual style: Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth, soft warm atmosphere, high-quality film still.

Brand consistency: Follow TiaoTiao Studio brand language. Keep the image warm, optimistic, honest, creative and lifestyle-focused.
```

---

# Negative Prompt（负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, humanoid character, other animal or unclothed ordinary pet dog. Do not use human hands, human arms, human legs, bipedal human standing pose, human body proportions, horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, or inconsistent outfit.
```

---

# Usage Rule（使用规则）

使用这个 Prompt 时必须：

- 默认保持 Jump 身份一致
- 默认引用 TSOS Database Record
- 默认引用 Knowledge Layer
- 不重复改写角色设定
- 不临时改变世界观
- 不使用与品牌语言冲突的风格

---

# Model Use（模型使用）

推荐用于：

- ChatGPT：拆分分镜、生成完整 Prompt
- Kling：生成视频镜头
- Veo：生成视频镜头
- Runway：生成视频镜头
- Midjourney：生成静帧或封面视觉
- Flux / ComfyUI：生成角色或环境静帧

---

# Related Database Records（关联数据库记录）

| Database | Record |
|---|---|
| Character DB | CHAR-001 |
| Episode DB | EP-001 |
| Story DB | STORY-001 |
| Environment DB | ENV-001 |
| Motion DB | MOT-001 |
| Camera DB | CAM-001 |
| Lighting DB | LGT-001 |

---

# Usage Scope（应用范围）

适用于：

- Prompt
- Episode
- Story
- Project
- Storyboard
- Animation
- Short Video
- Cover Design
- AI Video Generation

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical prompt record |
