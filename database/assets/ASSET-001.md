# ASSET-001 — Jump Character Reference Pack（跳跳角色参考资产包）

> Canonical Asset Record（官方资产记录）  
> Version：2.0
> Status：Active

---

# Overview（资产概述）

## 中文

Jump Character Reference Pack 是 Jump 的默认角色参考资产包。

它用于保证 Jump 在图片、视频、封面、分镜和 AI 生成流程中的角色一致性。

这个记录不是角色设定本身，而是用于生产时调用的资产引用说明。

## English

Jump Character Reference Pack is the default character reference asset package for Jump.

It keeps Jump visually consistent across images, videos, covers, storyboards and AI generation workflows.

---

# Database References（数据库引用）

| Database | Record |
|---|---|
| Character DB | CHAR-001 |
| Episode DB | EP-001 |
| Story DB | STORY-001 |
| Prompt DB | PROMPT-001 |
| Project DB | PROJ-001 |

---

# Knowledge References（知识引用）

| Category 分类 | Knowledge Node 知识节点 |
|---|---|
| Style 视觉风格 | STYLE-001 — Cinematic Documentary |
| Color 配色 | COLOR-001 — Fire Dragon Fruit Palette |
| Emotion 情绪 | EMOTION-001 — Freedom |
| Outfit 服装 | OUTFIT-001 — Programmer Outfit System |
| Brand Language 品牌语言 | BRAND-001 — TiaoTiao Studio Brand Language |

---

# Asset Role（资产作用）

这个资产包主要用于：

- 保持 Jump 角色外观一致
- 作为 AI 图片生成参考
- 作为 AI 视频生成参考
- 作为封面和分镜参考
- 作为未来角色模型、LoRA、ComfyUI 工作流或参考图集合的索引

---

# Asset Content（资产内容）

当前资产包应包含或未来可包含：

- Front View（正面参考）
- Side View（侧面参考）
- Back View（背面参考）
- Facial Expression Reference（表情参考）
- Outfit Reference（服装参考）
- Color Reference（品牌色参考）
- Fur Texture Reference（毛发质感参考）
- Pose Reference（姿态参考）

---

# Character Consistency Rules（角色一致性规则）

必须保持：

- Jump 是真实小狗本体形态的角色
- Jump 保持四足小狗身体结构
- Jump 保持小狗比例
- 毛茸茸质感清晰
- 穿程序员风格小狗衣服
- 表情友好温暖
- 程序员身份明确
- 默认服装遵循 OUTFIT-001
- 火龙果粉作为品牌识别点缀

---

# Usage Rule（使用规则）

使用 ASSET-001 时，必须同时参考：

```text
CHAR-001
+
OUTFIT-001
+
COLOR-001
+
STYLE-001
+
BRAND-001
```

它不能单独替代角色设定，只能作为生产资产参考。

---

# AI Prompt Module（AI Prompt 模块）

推荐 Prompt：

```text
Use the Jump character reference: a fluffy real dog-form character wearing programmer-style dog clothes, four-legged dog anatomy, dog proportions, friendly warm expression, soft realistic fur texture, small backpack / badge / collar charm allowed, subtle Fire Dragon Fruit Pink accents, cinematic documentary realism, consistent character identity.
```

---

# Negative Rule（禁止项）

禁止：

```text
human character, humanoid body, human hands, human arms, human legs, bipedal human standing pose, human body proportions, non-dog character, unclothed ordinary pet dog, no fur, dark horror redesign, cyberpunk armor, inconsistent outfit, exaggerated jewelry, different species, aggressive expression, brand color missing
```

---

# Related Database Records（关联数据库记录）

| Database | Record |
|---|---|
| Character DB | CHAR-001 |
| Prompt DB | PROMPT-001 |
| Project DB | PROJ-001 |

---

# Storage Rule（存储规则）

实际文件未来应存放在：

```text
references/character/jump/
```

GitHub 记录路径：

```text
database/assets/ASSET-001.md
```

---

# Usage Scope（应用范围）

适用于：

- Character Reference
- Image Generation
- Video Generation
- Storyboard
- Cover Design
- Prompt Engineering
- Asset Management
- Project Production

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated asset consistency rules to real dog-form Jump wearing clothes |
| 1.0 | 2026 | Initial canonical asset record |

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical asset record |
