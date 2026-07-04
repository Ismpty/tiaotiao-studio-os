# TEST-001 — COMMAND-003 Storyboard Validation

> Validation Test（验证测试）  
> Command：COMMAND-003  
> Target：Generate Storyboard  
> Project：PROJ-001  
> Status：PASS  
> Version：2.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-003 — Generate Storyboard` 是否可以按照当前故事板运行规则，生成《跳跳下班啦》的可生产故事板。

本次测试重点检查：

- 是否正确调用 COMMAND-003
- 是否正确引用 AGENT-001
- 是否正确读取 PROJ-001
- 是否使用 GitHub 作为 Source of Truth
- 是否输出完整 Shot List
- 是否输出模型可读 Storyboard Prompt
- 故事板主体是否是黑白粗略铅笔线稿
- 是否保留红 / 蓝 / 黄 / 绿 / 紫彩色动态标注系统
- Jump 是否保持真实小狗本体形态并穿衣服
- 是否通过一致性检查

## English

This test validates whether COMMAND-003 can generate a production-ready storyboard using black-and-white rough pencil line art, colored annotations and the real dog-form Jump rule.

---

# 2. Command Input（命令输入）

```text
Run COMMAND-003.

Target Platform:
小红书

Target Duration:
45 seconds

Aspect Ratio:
9:16

Shot Count:
6 shots

Output Language:
Bilingual

Required Style:
Black-and-white rough pencil storyboard with colored annotations
```

---

# 3. Source References（内部来源）

```text
PROJ-001 — Jump After Work Pilot Project
CHAR-001 — Jump
EP-001 — Jump After Work
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
ASSET-001 — Jump Character Reference Pack
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
EMOTION-001 — Freedom
STORYFORMULA-001 — Work Ends, Adventure Begins
BRAND-001 — TiaoTiao Studio Brand Language
AGENT-001 — Storyboard Agent
```

Source References are allowed in validation and review sections. Model-facing storyboard prompts must use natural language.

---

# 4. Required Storyboard Output（必需故事板输出）

```text
1. Source References
2. Storyboard Summary
3. Fixed Storyboard Visual Style
4. Storyboard Color Annotation System
5. Story Beat Breakdown
6. Shot List
7. Shot Details
8. Storyboard Prompt
9. Continuity Checklist
10. Next Production Actions
```

## Result

```text
PASS
```

---

# 5. Storyboard Style Validation（故事板风格验证）

```text
[PASS] Storyboard body uses black-and-white line art.
[PASS] Storyboard body uses rough pencil lines.
[PASS] Storyboard uses minimal details.
[PASS] Storyboard uses fast dynamic sketching.
[PASS] Storyboard uses simple anatomy.
[PASS] Storyboard keeps clear silhouettes.
[PASS] Storyboard has unfinished director previs sketch feeling.
[PASS] Storyboard does not use full-color concept art.
[PASS] Storyboard does not use polished illustration.
[PASS] Storyboard does not use realistic final render.
[PASS] Storyboard does not use children's picture book style.
[PASS] Storyboard does not use fully colored comic style.
```

---

# 6. Color Annotation Validation（彩色标注验证）

```text
[PASS] Red annotation is used for camera movement.
[PASS] Blue annotation is used for character / dog movement.
[PASS] Yellow annotation is used for prop interaction.
[PASS] Green annotation is used for lighting / mood.
[PASS] Purple annotation is used for continuity / transition.
[PASS] Colored annotations are production notes only.
[PASS] Colored annotations do not turn storyboard body into full-color art.
```

---

# 7. Character Form Validation（角色形态验证）

```text
[PASS] Jump remains a real dog-form character.
[PASS] Jump keeps four-legged dog anatomy.
[PASS] Jump keeps dog proportions.
[PASS] Jump keeps fluffy fur.
[PASS] Jump wears programmer-style dog clothes.
[PASS] Jump may keep small backpack, badge or collar charm.
[PASS] Jump may keep subtle dragon-fruit pink accent details.
[PASS] Humanoid body is forbidden.
[PASS] Human hands are forbidden.
[PASS] Human arms are forbidden.
[PASS] Human legs are forbidden.
[PASS] Bipedal human standing pose is forbidden.
[PASS] Turning into a human is forbidden.
[PASS] Turning into another animal is forbidden.
[PASS] Turning into an unclothed ordinary pet dog is forbidden.
```

---

# 8. Shot Structure Validation（镜头结构验证）

| Shot | Name | Duration | Required Check |
|---|---|---:|---|
| Shot 1 | Work Ending | 6s | Establishes end of coding work |
| Shot 2 | Decision Moment | 6s | Shows quiet decision to leave |
| Shot 3 | Packing Up | 7s | Shows prop interaction and transition |
| Shot 4 | Walking Out | 10s | Shows natural dog-form movement |
| Shot 5 | Door Exit | 8s | Shows office-to-after-work transition |
| Shot 6 | Warm Ending | 8s | Holds warm emotional landing |

## Result

```text
PASS
```

---

# 9. Model-readable Storyboard Prompt Validation（模型可读故事板提示词验证）

```text
[PASS] Storyboard Prompt describes the visual style in natural language.
[PASS] Storyboard Prompt describes Jump in natural language.
[PASS] Storyboard Prompt describes colored annotations in natural language.
[PASS] Storyboard Prompt does not rely on raw internal IDs.
[PASS] Storyboard Prompt can be copied into a model directly.
```

---

# 10. Issues Found（发现问题）

```text
No critical issues found.
No major issues found.
No minor issues found.
```

---

# 11. Final Result（最终结果）

```text
PASS
```

---

# 12. Next Validation Action（下一步验证）

```text
Run TEST-002:
COMMAND-002 — Generate Video Prompt Package

Purpose:
Validate whether the storyboard can be converted into Identity Card Prompt, Storyboard Prompt and Universal Video Prompt.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated validation for black-and-white rough pencil storyboard, colored annotations and real dog-form Jump rule |
| 1.0 | 2026 | Initial COMMAND-003 storyboard validation test |
