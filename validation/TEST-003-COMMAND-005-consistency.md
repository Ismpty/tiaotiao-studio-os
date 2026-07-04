# TEST-003 — COMMAND-005 Consistency Check Validation

> Validation Test（验证测试）  
> Command：COMMAND-005  
> Target：Run Consistency Check  
> Project：PROJ-001  
> Status：PASS  
> Version：2.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-005 — Run Consistency Check` 是否可以正确检查 TEST-001 分镜输出和 TEST-002 提示词包输出是否符合 TSOS Source of Truth 与 Prompt Runtime Rules。

本次测试重点检查：

- 是否正确调用 COMMAND-005
- 是否正确读取 Production Database Records
- 是否正确读取 Knowledge Nodes
- 是否检查 GitHub 是 Source of Truth
- 是否检查 Notion 只作为 Visual Management Layer
- 是否检查 Jump 真实小狗本体形态和穿衣服规则
- 是否检查故事板黑白粗略铅笔线稿风格
- 是否检查故事板彩色动态标注系统
- 是否检查 Identity Card Prompt / Storyboard Prompt / Universal Video Prompt 结构
- 是否检查模型可复制 Prompt 不依赖裸露内部 ID
- 是否输出 PASS / FAIL / PASS WITH MINOR FIXES

## English

This test validates whether COMMAND-005 can check the updated storyboard and prompt package against TSOS Source of Truth and Prompt Runtime Rules.

---

# 2. Command Input（命令输入）

```text
Run COMMAND-005.

Check Target:
TEST-001 COMMAND-003 Storyboard Output
TEST-002 COMMAND-002 Prompt Package Output

Project:
PROJ-001

Strictness:
Strict

Language:
Chinese

Output:
Consistency report with PASS / FAIL result.
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
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
WORLD-001 — TiaoTiao Universe
EMOTION-001 — Freedom
SHOT-001 — Hero Tracking Shot
MOTIONLANG-001 — Natural Walking Language
OUTFIT-001 — Programmer Outfit System
MUSIC-001 — Lifestyle Music Language
STORYFORMULA-001 — Work Ends, Adventure Begins
BRAND-001 — TiaoTiao Studio Brand Language
docs/studio-os/PROMPT-RUNTIME-RULES.md
COMMAND-002
WORKFLOW-002
WORKFLOW-003
AGENT-001
AGENT-002
```

---

# 4. Checked Outputs（被检查输出）

```text
validation/TEST-001-COMMAND-003-storyboard.md
validation/TEST-002-COMMAND-002-prompt.md
```

---

# 5. Consistency Summary（一致性总结）

```text
Result:
PASS

Summary:
TEST-001 and TEST-002 follow TSOS Source of Truth and current Prompt Runtime Rules.

TEST-001 confirms the storyboard uses black-and-white rough pencil line art, preserves colored annotations and keeps Jump as a real dog-form character wearing clothes.

TEST-002 confirms COMMAND-002 outputs Identity Card Prompt, Storyboard Prompt and Universal Video Prompt, with model-readable natural language and no reliance on raw internal IDs in model-copyable prompt sections.
```

---

# 6. Source of Truth Check（事实来源检查）

```text
[PASS] GitHub is treated as Source of Truth.
[PASS] Notion is treated only as Visual Management Layer.
[PASS] Internal source records are used for review and traceability.
[PASS] No Notion-only content overrides GitHub rules.
```

---

# 7. Character Consistency Check（角色一致性检查）

```text
[PASS] Jump remains a real dog-form character.
[PASS] Jump keeps four-legged dog anatomy.
[PASS] Jump keeps dog proportions.
[PASS] Jump keeps fluffy fur.
[PASS] Jump wears programmer-style dog clothes.
[PASS] Jump may keep small backpack, badge or collar charm.
[PASS] Jump may keep subtle dragon-fruit pink accents.
[PASS] Jump is not turned into a human.
[PASS] Jump is not turned into another animal.
[PASS] Jump is not turned into an unclothed ordinary pet dog.
[PASS] Human hands are forbidden.
[PASS] Human arms are forbidden.
[PASS] Human legs are forbidden.
[PASS] Bipedal human standing pose is forbidden.
[PASS] Human body proportions are forbidden.
```

---

# 8. Storyboard Runtime Check（故事板运行检查）

```text
[PASS] Storyboard body uses black-and-white line art.
[PASS] Storyboard body uses rough pencil lines.
[PASS] Storyboard uses minimal details.
[PASS] Storyboard uses fast dynamic sketching.
[PASS] Storyboard uses simple anatomy.
[PASS] Storyboard uses clear silhouettes.
[PASS] Storyboard has unfinished director previs sketch feeling.
[PASS] Storyboard avoids full-color concept art.
[PASS] Storyboard avoids polished illustration.
[PASS] Storyboard avoids realistic final render.
[PASS] Storyboard avoids children's picture book style.
[PASS] Storyboard avoids fully colored comic style.
```

---

# 9. Storyboard Color Annotation Check（故事板彩色标注检查）

```text
[PASS] Red is used for camera movement.
[PASS] Blue is used for character / dog movement.
[PASS] Yellow is used for prop interaction.
[PASS] Green is used for lighting / mood.
[PASS] Purple is used for continuity / transition.
[PASS] Colored annotations remain annotations only.
[PASS] Colored annotations do not turn storyboard body into full-color final art.
```

---

# 10. Prompt Runtime Compliance Check（提示词运行架构合规检查）

```text
[PASS] Identity Card Prompt exists.
[PASS] Storyboard Prompt exists.
[PASS] Universal Video Prompt exists.
[PASS] Model-readable check exists.
[PASS] COMMAND-005 review exists.
[PASS] Identity Card Prompt owns character appearance.
[PASS] Storyboard Prompt owns shot details.
[PASS] Universal Video Prompt owns model execution rules.
[PASS] Universal Video Prompt refers to uploaded identity card.
[PASS] Universal Video Prompt refers to uploaded storyboard.
[PASS] Universal Video Prompt uses [SHOT NUMBER AND NAME].
[PASS] Universal Video Prompt avoids duplicated long shot details.
```

---

# 11. Model-readable Prompt Check（模型可读提示词检查）

```text
[PASS] Model-copyable prompt sections use natural language.
[PASS] Source IDs are limited to Source References and review sections.
[PASS] Model-copyable prompt sections do not rely on "consistent with ASSET-001".
[PASS] Model-copyable prompt sections do not rely on "follow CHAR-001".
[PASS] Model-copyable prompt sections do not rely on "use STYLE-001".
[PASS] Model-copyable prompt sections do not rely on "match BRAND-001".
[PASS] Character, style, scene and brand requirements are expanded into natural language.
```

---

# 12. World / Style / Brand Check（世界观、风格、品牌检查）

```text
[PASS] Output remains within TiaoTiao Universe.
[PASS] Output serves Jump After Work.
[PASS] Output keeps warm, optimistic and honest brand tone.
[PASS] Output avoids horror, violence, dystopian and cyberpunk direction.
[PASS] Output avoids hard-selling tone.
[PASS] Output avoids clickbait.
[PASS] Output does not introduce unapproved canon.
```

---

# 13. Workflow Compliance Check（工作流合规检查）

```text
[PASS] TEST-001 follows COMMAND-003 storyboard validation structure.
[PASS] TEST-001 follows AGENT-001 storyboard responsibilities.
[PASS] TEST-002 follows COMMAND-002 prompt package structure.
[PASS] TEST-002 follows AGENT-002 prompt runtime responsibilities.
[PASS] TEST-002 follows WORKFLOW-002 output structure.
[PASS] Prompt package can feed WORKFLOW-003.
[PASS] Both tests preserve TSOS Source of Truth.
```

---

# 14. Issue List（问题列表）

| Severity | Area | Issue | Source of Truth | Suggested Fix |
|---|---|---|---|---|
| None | None | No issue found | N/A | N/A |

---

# 15. Fix Suggestions（修改建议）

```text
No required fixes.

Optional future improvement:
Update broader examples and end-to-end production validation files so every sample uses the new Prompt Runtime Architecture.
```

---

# 16. Final Result（最终结果）

```text
Final Result:
PASS

Reason:
TEST-001 and TEST-002 follow TSOS Source of Truth, preserve Jump as a real dog-form character wearing clothes, use black-and-white rough pencil storyboard style with colored annotations, and follow the Identity Card Prompt + Storyboard Prompt + Universal Video Prompt architecture.

Required Fixes:
None.

Next Action:
Continue to TEST-004 — COMMAND-004 Publishing Package Validation, or update broader examples before the next validation run.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated COMMAND-005 validation for Prompt Runtime Rules, model-readable prompts and storyboard runtime checks |
| 1.0 | 2026 | Initial COMMAND-005 consistency check validation test |
