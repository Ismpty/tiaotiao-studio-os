# PROJ-001 — Little Security Guard and His Ancient Friends（小保安和他的古人朋友们）

> Canonical Project Record（官方项目记录）
>
> Version：2.0
>
> Status：Concept Pivot / System Upgrade

---

# Overview（项目概述）

## 中文

《小保安和他的古人朋友们》是 TiaoTiao Studio OS 的新主项目方向。

小保安是 Jump / 跳跳。跳跳仍然必须保持真实小狗本体形态并穿衣服，只是她在新系列中的日常身份从“下班后的程序员小狗”转为“AI 博物馆里的小保安”。

古人朋友是中国文物、古画人物、器物、神兽纹样和历史图像在 AI 博物馆中被激活后的朋友们。

系列核心是：

```text
一只认真值班的小狗保安
+
一群从中国文物里活过来的古人朋友
+
AI 博物馆里的奇葩无厘头日常
```

## English

Little Security Guard and His Ancient Friends is the new main project direction for TiaoTiao Studio OS.

Jump remains a real dog-form character wearing clothes, now working as a small security guard in an AI Museum. The ancient friends are Chinese relics, painting figures, artifacts, mythic motifs and historical images activated into living characters.

---

# Project Goal（项目目标）

本项目用于验证：

- Jump 作为“小保安”的角色一致性
- 中国文物朋友的身份卡、故事板和视频 Prompt 是否可复用
- AI 博物馆环境是否能支撑系列化无厘头短剧
- 文物激活、文化错位和现代安保规则之间的喜剧机制是否成立
- Jump 的真实小狗形态规则是否能在新职业身份下保持稳定
- `RELIC-001` 是否能作为文物朋友的长期规则节点
- Prompt Runtime 是否能支持多主体、多文物、多场景的短视频生产

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
| Prompt DB | PROMPT-001 |

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
| Outfit 服装 | OUTFIT-001 — Programmer Outfit System |
| Music 音乐语言 | MUSIC-001 — Lifestyle Music Language |
| Brand Language 品牌语言 | BRAND-001 — TiaoTiao Studio Brand Language |

---

# Project Format（项目形式）

## Type（类型）

Short Video / AI Museum Comedy Series

## Duration（时长）

推荐：

```text
20–60 seconds
```

## Platform（平台）

适用于：

- 抖音
- 小红书
- 视频号
- TikTok
- YouTube Shorts
- Instagram Reels

---

# Core Story Engine（核心故事引擎）

## 中文

AI 博物馆闭馆后，跳跳作为小保安认真巡逻。

某件中国文物、古画人物、器物或神兽纹样突然被 AI 展厅系统激活，变成跳跳的“古人朋友”。

古人朋友带着古代逻辑误解现代博物馆规则，引发奇葩无厘头事件。

跳跳用小狗式认真、善意和一点点笨拙解决问题，最后留下一个轻松、温暖、带一点文化趣味的结尾。

## Default Episode Flow（默认单集结构）

```text
1. Museum Night Trigger
   AI 博物馆闭馆，展厅系统启动。

2. Jump Patrol
   小保安跳跳开始巡逻。

3. Relic Awakening
   一位古人朋友从文物、古画或展柜中被激活。

4. Absurd Misunderstanding
   古人朋友误解现代规则，制造奇葩事件。

5. Security Guard Response
   跳跳认真处理，但因为她是小狗，处理方式可爱又无厘头。

6. Warm Resolution
   事件被温柔解决，文物朋友和跳跳建立关系。
```

---

# Standard Shot Plan（标准镜头规划）

## Shot 1 — Museum Closing

AI 博物馆闭馆，灯光从日间展览切换到夜间值班模式。

---

## Shot 2 — Little Security Guard Patrol

跳跳穿小保安制服，以真实小狗形态巡逻展厅。

---

## Shot 3 — Relic Activation

某件文物、古画人物、器物或神兽纹样被 AI 展厅系统激活。

---

## Shot 4 — Absurd Cultural Misunderstanding

古人朋友用古代逻辑误解现代展厅、游客规则、安保流程或 AI 设备。

---

## Shot 5 — Jump Handles the Incident

跳跳认真执行小保安职责，和古人朋友产生无厘头互动。

---

## Shot 6 — Warm Museum Ending

问题被解决，古人朋友回到展柜或继续和跳跳成为朋友。

---

# Production Requirements（制作要求）

必须保持：

- Jump 是真实小狗本体形态，穿衣服，不能变成人
- Jump 的新职业身份是 AI 博物馆小保安
- 古人朋友必须来自中国文物、古画、器物或神话纹样
- 喜剧来自文化错位和规则误解，不是贬低文物
- AI 博物馆要真实、温暖、带一点智能系统感，不能变成赛博朋克夜店
- 每集要有明确的文物朋友身份卡
- 模型可复制 Prompt 不能裸露内部 ID

---

# Prompt Workflow（提示词流程）

默认使用：

```text
PROMPT-001 — Little Security Guard Museum Master Prompt
```

工作流：

```text
PROJ-001
+
PROMPT-001
+
CHAR-001
+
EP-001
+
STORY-001
+
ENV-001
+
SUBJECT-001
+
RELIC-001
+
VISUALPARAM-001 / BLOCKING-001 / SHOT-002 / TRANSITION-001
```

---

# Success Criteria（成功标准）

本项目成功的标准：

- Jump 的小保安身份稳定
- Jump 仍是穿衣服的真实小狗，不变成人
- 古人朋友有清晰文物来源和视觉连续性
- AI 博物馆环境可复用
- 每集都有清楚的无厘头文化错位笑点
- 文物表达尊重、好玩、不低俗
- Prompt Runtime 能稳定生成身份卡、故事板和逐镜头视频 Prompt

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Pivoted PROJ-001 to Little Security Guard and His Ancient Friends |
| 1.0 | 2026 | Initial Jump After Work pilot project |
