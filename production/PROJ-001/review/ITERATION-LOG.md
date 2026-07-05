# PROJ-001 — Iteration Log（生成迭代记录）

> Production Review Log（生产迭代记录）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Command：COMMAND-005  
> Workflow：WORKFLOW-003  
> Version：1.0  
> Status：Review Ready

---

# 1. Purpose（目的）

## 中文

本文件用于记录《跳跳下班啦》真实视频片段生成过程中的所有迭代。

每次生成、审片、发现问题、修改 Prompt、重新生成，都应该记录在这里。

它的作用是：

- 追踪每个镜头生成了几个版本
- 记录哪个版本通过审片
- 记录失败原因
- 记录 Prompt 如何修改
- 避免重复犯同样的问题
- 为后续 EP-002 / EP-003 提供经验

## English

This file tracks all generation and review iterations for PROJ-001.

It records shot versions, review results, issues, prompt fixes and approved outputs.

---

# 2. Source Files（来源文件）

本迭代记录应配合以下文件使用：

```text
production/PROJ-001/VIDEO-PROMPTS.md
production/PROJ-001/PRODUCTION-CHECKLIST.md
production/PROJ-001/review/CLIP-REVIEW-GUIDE.md
production/PROJ-001/review/SHOT-REVIEW-TEMPLATE.md
```

---

# 3. Iteration Status Overview（迭代状态总览）

| Shot | Generated Versions | Approved Version | Status | Notes |
|---|---:|---|---|---|
| Shot 1 — Work Ending | 0 | TBD | Not Started | TBD |
| Shot 2 — Clock Out | 0 | TBD | Not Started | High motion / backpack continuity risk |
| Shot 3 — Dinner Time | 0 | TBD | Not Started | Prop / food action risk |
| Shot 4 — Supermarket Walk | 0 | TBD | Not Started | Walking / shelf continuity risk |
| Shot 5 — Movie Night | 0 | TBD | Not Started | Screen light / prop risk |
| Shot 6 — Street Snack | 0 | TBD | Not Started | Night lighting / food prop risk |
| Shot 7 — Night Walk | 0 | TBD | Not Started | High motion / sliding feet risk |
| Shot 8 — Life Begins | 0 | TBD | Not Started | Lighting / emotion risk |

---

# 4. Version Status Rules（版本状态规则）

## Not Started

```text
尚未生成。
```

## Generated

```text
已经生成，但还没有审片。
```

## In Review

```text
正在审片。
```

## PASS

```text
通过审片，可以进入剪辑。
```

## PASS WITH MINOR FIXES

```text
轻微问题，可作为备用或轻修后使用。
```

## FAIL

```text
不能使用，需要重新生成。
```

## Approved

```text
最终选定版本。
```

---

# 5. Iteration Entry Template（迭代记录模板）

每次生成一个版本，复制以下模板填写：

```text
Iteration ID:
ITER-XXX

Shot:
Shot X — Name

Clip File:
production/PROJ-001/clips/SHOT-XXX-vXX.mp4

Model:
Jimeng / 即梦 / Veo / Runway / Other

Prompt Source:
production/PROJ-001/VIDEO-PROMPTS.md

Prompt Version:
v1 / v2 / v3 / custom

Generation Date:
TBD

Review File:
production/PROJ-001/review/SHOT-XXX-vXX-review.md

Review Result:
PASS / PASS WITH MINOR FIXES / FAIL

Issues Found:
1.
2.
3.

Prompt Changes:
1.
2.
3.

Decision:
Use / Backup / Regenerate

Next Action:
TBD
```

---

# 6. Shot 1 — Work Ending Iterations

## Target

```text
Jump sits at her desk, hands leaving the keyboard, warm screen glow, calm relief.
```

## Expected Result

```text
Character stable
Desk realistic
Laptop open
Hands natural
Warm lighting
Emotion calm
```

## Iterations

### ITER-001

```text
Shot:
Shot 1 — Work Ending

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 1 v01.
```

---

# 7. Shot 2 — Clock Out Iterations

## Target

```text
Jump looks toward window, gently smiles, closes laptop, shifts from work focus to after-work expectation.
```

## Expected Result

```text
Expression natural
Laptop closes correctly
Golden-hour light appears
Emotion shifts gently
No exaggerated acting
```

## Iterations

### ITER-002

```text
Shot:
Shot 2 — Clock Out

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 2 v01.
```

---

# 8. Shot 3 — Dinner Time Iterations

## Target

```text
Jump packs notebook and headphones into backpack, closes zipper, warm desk close-up.
```

## Expected Result

```text
Hands stable
Objects recognizable
Backpack visible
Desk not too messy
Object handling natural
```

## Iterations

### ITER-003

```text
Shot:
Shot 3 — Dinner Time

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 3 v01.
```

---

# 9. Shot 4 — Supermarket Walk Iterations

## Target

```text
Jump carries backpack and walks naturally through the studio toward the exit.
```

## Expected Result

```text
Natural walking
No sliding feet
Grounded foot contact
Backpack stable
Eye-level hero tracking camera
Warm studio continuity
```

## High-Risk Notes

Shot 4 是本项目动作风险最高的镜头之一。

重点检查：

```text
脚步是否贴地
身体是否漂浮
尾巴是否自然
背包是否稳定
镜头是否游戏感
```

## Iterations

### ITER-004

```text
Shot:
Shot 4 — Supermarket Walk

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 4 v01.
```

---

# 10. Shot 5 — Movie Night Iterations

## Target

```text
Jump opens the office door and transitions from warm indoor light to golden after-work light.
```

## Expected Result

```text
Door opens naturally
Motion grounded
Light transition smooth
No overexposure
No escape drama
Continuity with Shot 4 and Shot 6
```

## High-Risk Notes

Shot 5 同时有屏幕光、道具和情绪稳定风险。

重点检查：

```text
屏幕光是否柔和
前爪和肢体是否变形
爆米花 / 小毯子等道具是否稳定
空间是否能接 Shot 6
```

## Iterations

### ITER-005

```text
Shot:
Shot 5 — Movie Night

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 5 v01.
```

---

# 11. Shot 6 — Street Snack Iterations

## Target

```text
Jump pauses in warm after-work golden light, quiet emotional ending, ready for final caption.
```

## Expected Result

```text
Warm ending frame
Jump stable
Light not overexposed
Emotion quiet and free
No commercial posing
Final caption can be added later
```

## Iterations

### ITER-006

```text
Shot:
Shot 6 — Street Snack

Clip File:
TBD

Model:
TBD

Prompt Version:
TBD

Generation Date:
TBD

Review Result:
TBD

Issues Found:
TBD

Prompt Changes:
TBD

Decision:
TBD

Next Action:
Generate Shot 6 v01.
```

---

# 12. Common Issue Log（常见问题记录）

用于记录重复出现的问题。

| Issue Type | Description | Shots Affected | Fix Strategy |
|---|---|---|---|
| Character Drift | TBD | TBD | Reference ASSET-001 more strongly |
| Sliding Feet | TBD | TBD | Add grounded foot contact |
| Floating Body | TBD | TBD | Add realistic weight transfer |
| Hand Distortion | TBD | TBD | Simplify hand action |
| Lighting Drift | TBD | TBD | Reinforce LGT-001 |
| Environment Drift | TBD | TBD | Reinforce ENV-001 |
| Camera Drift | TBD | TBD | Reinforce 35mm eye-level camera |
| Brand Tone Drift | TBD | TBD | Reinforce BRAND-001 |

---

# 13. Prompt Fix Library（Prompt 修正库）

## Character Drift Fix

```text
Keep Jump as a fluffy real dog-form character wearing programmer-style dog clothes. Maintain four-legged dog anatomy, dog proportions, soft realistic fur texture, outfit continuity and Fire Dragon Fruit Pink accents throughout the entire clip.
```

## Sliding Feet Fix

```text
Grounded foot contact, realistic weight transfer, natural walking mechanics, feet stay connected to the floor, no sliding feet, no floating body.
```

## Hand Distortion Fix

```text
Simplify hand movement, natural object handling, clear hand position, no melting fingers, no extra fingers, no distorted paws or hands.
```

## Backpack Stability Fix

```text
Keep the backpack stable on Jump's back. Do not morph, disappear or change shape during motion.
```

## Camera Drift Fix

```text
Stable eye-level 35mm camera, natural documentary camera movement, no FPS view, no drone orbit, no extreme wide-angle distortion, no artificial shake.
```

## Lighting Drift Fix

```text
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows, no cyberpunk blue lighting, no horror contrast, no over-saturated RGB.
```

## Environment Drift Fix

```text
Keep TiaoTiao Studio Office consistent, warm modern creator workspace, realistic programmer desk, laptop, keyboard, monitor, desk lamp, notebook, coffee cup, backpack, headphones and small plant.
```

## Emotion Drift Fix

```text
Keep the emotion warm, relaxed and quietly joyful. No anxiety, no panic, no workplace complaint, no dramatic escape feeling, no hard-selling commercial mood.
```

---

# 14. Approved Clip Register（通过片段登记）

| Shot | Approved Clip | Review File | Approval Reason |
|---|---|---|---|
| Shot 1 | TBD | TBD | TBD |
| Shot 2 | TBD | TBD | TBD |
| Shot 3 | TBD | TBD | TBD |
| Shot 4 | TBD | TBD | TBD |
| Shot 5 | TBD | TBD | TBD |
| Shot 6 | TBD | TBD | TBD |

---

# 15. Rejected Clip Register（未通过片段登记）

| Clip File | Shot | Reason | Fix Applied |
|---|---|---|---|
| TBD | TBD | TBD | TBD |

---

# 16. Final Selection Notes（最终选择备注）

```text
Selected Shot 1:
TBD

Selected Shot 2:
TBD

Selected Shot 3:
TBD

Selected Shot 4:
TBD

Selected Shot 5:
TBD

Selected Shot 6:
TBD
```

## Overall Continuity Notes

```text
TBD
```

## Ready for Editing

```text
YES / NO
```

---

# 17. Next Action（下一步动作）

```text
1. Generate Shot 1 v01.
2. Review using SHOT-REVIEW-TEMPLATE.md.
3. Record result in ITERATION-LOG.md.
4. Generate additional versions if needed.
5. Approve the best version.
6. Repeat for Shot 2–8.
```

---

# 18. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial iteration log |
