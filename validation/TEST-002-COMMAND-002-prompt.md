# TEST-002 — COMMAND-002 Prompt Package Validation

> Validation Test（验证测试）  
> Command：COMMAND-002  
> Target：Generate Video Prompt Package
> Project：PROJ-001  
> Status：PASS  
> Version：2.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-002 — Generate Video Prompt Package` 是否能按照新的 Prompt Runtime Architecture，生成模型可读的视频提示词包。

本次测试重点检查：

- 是否正确调用 COMMAND-002
- 是否正确引用 WORKFLOW-002
- 是否正确调用 AGENT-002
- 是否输出 Identity Card Prompt
- 是否输出 Storyboard Prompt
- 是否输出 Universal Video Prompt
- 是否包含 Model-readable check
- 是否能交给 COMMAND-005 review
- 模型可复制 Prompt 是否不依赖裸露内部 ID
- Jump 是否保持真实小狗本体形态并穿衣服
- 故事板是否为黑白粗略铅笔线稿并保留彩色动态标注系统

## English

This test validates whether COMMAND-002 can generate a model-readable prompt package using the current Identity Card Prompt, Storyboard Prompt and Universal Video Prompt structure.

---

# 2. Command Input（命令输入）

```text
Run COMMAND-002.

Project:
PROJ-001 — Jump After Work Pilot Project

Target Model:
Jimeng / 即梦

Backup Models:
Veo / Runway

Target Platform:
小红书

Aspect Ratio:
9:16

Source:
TEST-001 COMMAND-003 Storyboard Output

Required Output:
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
```

---

# 3. Source References（内部来源）

```text
PROJ-001 — Jump After Work Pilot Project
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
PROMPT-001 — Jump After Work Master Prompt
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
EMOTION-001 — Freedom
BRAND-001 — TiaoTiao Studio Brand Language
```

Source References are allowed in this validation file, but model-copyable prompt sections must use natural language.

---

# 4. Required Output Structure（必需输出结构）

```text
1. Source References
2. Prompt Task Brief
3. Identity Card Prompt
4. Storyboard Prompt
5. Universal Video Prompt
6. Runtime Usage Example
7. Model-readable Check Report
8. COMMAND-005 Review Result
9. Usage Notes
```

## Result

```text
PASS
```

---

# 5. Identity Card Prompt Validation（身份卡提示词验证）

```text
[PASS] Prompt clearly names Jump / 跳跳.
[PASS] Prompt describes Jump as a real dog-form character.
[PASS] Prompt requires four-legged dog anatomy and dog proportions.
[PASS] Prompt requires fluffy fur.
[PASS] Prompt requires programmer-style dog clothes.
[PASS] Prompt allows small backpack, badge or collar charm.
[PASS] Prompt allows subtle dragon-fruit pink accents.
[PASS] Prompt forbids humanoid body.
[PASS] Prompt forbids human hands, human arms and human legs.
[PASS] Prompt forbids bipedal human standing pose.
[PASS] Prompt forbids turning into a human, another animal or an unclothed ordinary pet dog.
[PASS] Prompt is model-readable natural language.
[PASS] Prompt does not rely on raw internal IDs.
```

---

# 6. Storyboard Prompt Validation（故事板提示词验证）

```text
[PASS] Prompt requests black-and-white line art.
[PASS] Prompt requests rough pencil lines.
[PASS] Prompt requests minimal details.
[PASS] Prompt requests fast dynamic sketching.
[PASS] Prompt requests simple anatomy and clear silhouettes.
[PASS] Prompt requests unfinished director storyboard / previs sketch feeling.
[PASS] Prompt forbids full-color concept art.
[PASS] Prompt forbids polished illustration.
[PASS] Prompt forbids realistic final render.
[PASS] Prompt forbids children's picture book style.
[PASS] Prompt forbids fully colored comic style.
[PASS] Prompt keeps colored annotation system.
[PASS] Red is used for camera movement.
[PASS] Blue is used for character / dog movement.
[PASS] Yellow is used for prop interaction.
[PASS] Green is used for lighting / mood.
[PASS] Purple is used for continuity / transition.
[PASS] Prompt is model-readable natural language.
[PASS] Prompt does not rely on raw internal IDs.
```

---

# 7. Universal Video Prompt Validation（通用视频提示词验证）

```text
[PASS] Prompt refers to the uploaded identity card.
[PASS] Prompt refers to the uploaded storyboard.
[PASS] Prompt uses [SHOT NUMBER AND NAME] as the current-shot placeholder.
[PASS] Prompt says character appearance follows the identity card.
[PASS] Prompt says shot content follows the storyboard shot.
[PASS] Prompt includes video specification.
[PASS] Prompt includes natural dog-form movement requirements.
[PASS] Prompt includes camera requirements.
[PASS] Prompt includes lighting and mood requirements.
[PASS] Prompt includes continuity requirements.
[PASS] Prompt includes negative rules.
[PASS] Prompt avoids duplicated long shot details.
[PASS] Prompt is model-readable natural language.
[PASS] Prompt does not rely on raw internal IDs.
```

---

# 8. Model-readable Check（模型可读检查）

```text
[PASS] Model-copyable sections contain natural language descriptions.
[PASS] Source IDs are limited to Source References and review areas.
[PASS] No model-copyable section relies on "consistent with ASSET-001".
[PASS] No model-copyable section relies on "follow CHAR-001".
[PASS] No model-copyable section relies on "use STYLE-001".
[PASS] No model-copyable section relies on "match BRAND-001".
[PASS] Internal source references are translated into character, style, scene and brand descriptions.
```

---

# 9. COMMAND-005 Review Simulation（COMMAND-005 审查模拟）

```text
[PASS] GitHub remains the Source of Truth.
[PASS] Notion is only the Visual Management Layer.
[PASS] Identity Card Prompt exists.
[PASS] Storyboard Prompt exists.
[PASS] Universal Video Prompt exists.
[PASS] Model-readable check exists.
[PASS] Jump remains a real dog-form character wearing clothes.
[PASS] Storyboard body style is black-and-white rough pencil line art.
[PASS] Colored annotation system is retained.
[PASS] Universal Video Prompt follows uploaded identity card + uploaded storyboard + current shot.
[PASS] Default project goal is preserved.
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
Run TEST-003:
COMMAND-005 — Consistency Check Validation

Purpose:
Validate whether COMMAND-005 can check the updated storyboard and prompt package against TSOS Source of Truth and Prompt Runtime Rules.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated validation for identity card prompt, storyboard prompt, universal video prompt and model-readable checks |
| 1.0 | 2026 | Initial COMMAND-002 prompt validation test |
