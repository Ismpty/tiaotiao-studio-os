# PROMPT-001 — Little Security Guard Museum Master Prompt（小保安 AI 博物馆主提示词）

> Canonical Prompt Record（官方提示词记录）
>
> Version：2.0
>
> Status：Active

---

# Overview（提示词概述）

## 中文

Little Security Guard Museum Master Prompt 是《小保安和他的古人朋友们》的默认主提示词模块。

它不是单次生成用的临时 Prompt，而是一个可重复调用的生产提示词模板。

它的作用是把 Jump 的小保安身份、AI 博物馆环境、中国文物朋友、无厘头事件结构、镜头语言和 Knowledge Layer 组合成统一的生成指令。

## English

Little Security Guard Museum Master Prompt is the reusable master prompt module for Little Security Guard and His Ancient Friends.

It combines Jump's security-guard role, the AI Museum, living Chinese relic friends, absurd comedy structure and TSOS Knowledge Layer into one consistent generation framework.

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
| Subject Identity 主体身份 | SUBJECT-001 — Generic Subject Identity Card Grammar |
| Relic Friends 文物朋友 | RELIC-001 — AI Museum Relic Friends Grammar |
| Style 视觉风格 | STYLE-001 — Cinematic Documentary |
| Color 配色 | COLOR-001 — Fire Dragon Fruit Palette |
| World 世界观 | WORLD-001 — TiaoTiao Universe |
| Emotion 情绪 | EMOTION-001 — Freedom |
| Visual Parameters 画面参数 | VISUALPARAM-001 — AIGC Base Visual Parameter Grammar |
| Scene Blocking 场景调度 | BLOCKING-001 — Overhead Scene Blocking Map |
| Camera Language 镜头语言 | SHOT-001 / SHOT-002 |
| Transition Language 转场语言 | TRANSITION-001 — Universal AI Video Transition Grammar |
| Motion Language 动作语言 | MOTIONLANG-001 — Natural Walking Language |
| Outfit 服装 | OUTFIT-001 — Dog Outfit System / AI Museum Security Guard Variant |
| Music 音乐语言 | MUSIC-001 — Lifestyle Music Language |
| Story Formula 故事公式 | Museum Closing → Jump Patrol → Relic Awakening → Ancient-Modern Misunderstanding → Absurd Escalation → Warm Resolution |
| Brand Language 品牌语言 | BRAND-001 — TiaoTiao Studio Brand Language |

---

# Prompt Role（提示词作用）

这个 Prompt 主要用于：

- 生成《小保安和他的古人朋友们》的分镜
- 生成文物朋友身份卡 Prompt
- 生成 AI 博物馆单张画面 Prompt
- 生成视频镜头 Prompt
- 生成动画动作 Prompt
- 生成封面主视觉 Prompt
- 保持 Jump 小保安角色一致性
- 保持文物朋友来源、材质、纹样和时代气质一致性

---

# Master Prompt Structure（主提示词结构）

标准结构：

```text
[Security Guard]
CHAR-001 — Jump as Little Security Guard

[Relic Friend]
SUBJECT-001 + RELIC-001

[Episode]
EP-001 — Little Security Guard and His Ancient Friends

[Story]
STORY-001 — Museum Night, Relic Friends Wake Up

[Environment]
ENV-001 — AI Museum Night Gallery

[Motion]
MOT-001 — Natural Walking

[Camera]
CAM-001 + SHOT-001 + SHOT-002

[Lighting]
LGT-001 — Warm Museum Night Lighting

[Knowledge Layer]
STYLE-001 + COLOR-001 + WORLD-001 + EMOTION-001 + VISUALPARAM-001 + BLOCKING-001 + TRANSITION-001 + BRAND-001
```

---

# Model-Readable Prompt Body（模型可读提示词正文）

```text
Create a warm, absurd, cinematic AI Museum scene for the series Little Security Guard and His Ancient Friends.

Main character: Jump is a fluffy real dog-form character wearing clothes. In this series, Jump works as a small museum security guard. She must keep four-legged dog anatomy, dog proportions, fluffy fur, friendly but serious expression, small security-guard outfit or badge, optional tiny patrol accessories, and subtle TiaoTiao Studio color accents. Do not turn Jump into a human security guard.

Relic friend: introduce one Chinese relic friend awakened by the AI Museum system. The relic friend must come from a clear Chinese cultural source such as an ancient painting figure, porcelain object, bronze ritual vessel, jade ornament, tomb figurine, calligraphy object, mythic dragon, phoenix, qilin, crane, tiger, deer or other auspicious motif. Preserve the relic friend's original artifact identity, dynasty feeling, material, texture, color, pattern, costume or motif. The relic friend can talk, move and misunderstand modern rules, but must not become a modern influencer, cartoon mascot or Western fantasy creature.

Scene context: after the AI Museum closes, warm night security lights turn on. Jump patrols through a realistic Chinese relic gallery with transparent display cases, exhibit labels, soft AI scanning light, security route signs, guide screens, museum floor reflections, and quiet mist-like activation effects.

Story feeling: a cultural relic wakes up and creates an absurd misunderstanding in the museum. Jump takes the situation very seriously, but her dog-form security-guard behavior makes the incident funny, strange and warm.

Camera: cinematic documentary realism, 35mm natural lens, low dog-height patrol shots, exhibit close-ups, reaction shots between Jump and the relic friend, stable spatial continuity, and museum layout consistency.

Motion: Jump moves with natural dog-form walking and grounded paw contact. Relic friends move according to their source identity: ancient painting figures move slowly and elegantly, ceramic or bronze objects move with careful weight, mythic beasts move with believable body mass. Do not use robotic movement or floating without narrative reason.

Lighting: warm night museum lighting, soft display-case glow, gentle AI activation light, subtle reflections on glass, readable faces and fur, no horror lighting.

Visual style: real-world cinematic Chinese mythological museum comedy, warm, odd, clever, respectful toward relics, with slight magical activation. Keep the image grounded and physical.

Brand consistency: keep the tone warm, optimistic, honest, creative and playful. The humor should be absurd but not disrespectful.
```

---

# Negative Prompt（负面提示词）

```text
Do not change Jump's species. Do not turn Jump into a human, humanoid character, other animal or unclothed ordinary pet dog. Do not use human hands, human arms, human legs, bipedal human standing pose or human body proportions for Jump. Do not make the relic friend a modern influencer, generic anime character, cheap mascot, horror ghost, Western fantasy monster or unrelated object. Do not mock real cultural heritage. Do not use cyberpunk nightclub lighting, neon sci-fi glow, horror museum atmosphere, tomb-raiding mood, game CG, robotic motion, sliding feet, extreme wide-angle distortion, drone orbit, FPS camera, over-saturated RGB lights, or inconsistent outfits. Do not let model-facing prompts rely on raw internal IDs.
```

---

# Usage Rule（使用规则）

使用这个 Prompt 时必须：

- 默认保持 Jump 是真实小狗本体形态
- 默认将 Jump 设定为 AI 博物馆小保安
- 默认为每集文物朋友生成或引用主体身份卡
- 默认引用 `RELIC-001` 的文物朋友规则
- 默认引用 TSOS Database Records
- 默认引用 Knowledge Layer
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
| 2.0 | 2026 | Pivoted master prompt to AI Museum little security guard series |
| 1.0 | 2026 | Initial Jump After Work master prompt |
