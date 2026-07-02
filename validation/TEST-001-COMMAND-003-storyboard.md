# TEST-001 — COMMAND-003 Storyboard Validation

> Validation Test（验证测试）  
> Command：COMMAND-003  
> Target：Generate Storyboard  
> Project：PROJ-001  
> Status：PASS  
> Version：1.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-003 — Generate Storyboard` 是否可以基于 TSOS Source of Truth 稳定生成《跳跳下班啦》的标准分镜输出。

本次测试重点检查：

- 是否正确调用 COMMAND-003
- 是否正确引用 AGENT-001
- 是否正确读取 PROJ-001
- 是否正确引用 CHAR-001 / ASSET-001
- 是否正确使用 STORYFORMULA-001
- 是否输出完整 Shot List
- 是否输出逐镜头说明
- 是否通过一致性检查

## English

This test validates whether COMMAND-003 can generate a production-ready storyboard for PROJ-001 using TSOS source records and knowledge constraints.

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

Detail Level:
Detailed
```

---

# 3. Source Records（来源记录）

## Database Records

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
```

## Knowledge Nodes

```text
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
```

## Agent

```text
AGENT-001 — Storyboard Agent
```

## Workflow Reference

```text
WORKFLOW-001 — Jump After Work Production Workflow
```

---

# 4. Storyboard Summary（分镜摘要）

## Project

```text
PROJ-001 — Jump After Work Pilot Project
```

## Story

```text
STORY-001 — Work Ends, Adventure Begins
```

## Main Character

```text
CHAR-001 — Jump
```

## Asset Reference

```text
ASSET-001 — Jump Character Reference Pack
```

## Format

```text
45-second vertical short video
9:16 aspect ratio
6-shot structure
```

## Core Emotion

```text
Freedom
```

## Core Message

```text
电脑一关，生活上线。
```

---

# 5. Story Beat Breakdown（故事节奏拆解）

```text
Work
↓
Decision
↓
Packing Up
↓
Walking Out
↓
Door Exit
↓
Warm Reflection
```

| Beat | 中文含义 | English Meaning |
|---|---|---|
| Work | 跳跳结束一天的代码工作 | Jump finishes her coding work |
| Decision | 她决定离开办公室 | She decides to leave work |
| Packing Up | 从工作状态切换到生活状态 | She shifts from work mode to life mode |
| Walking Out | 她走出工作室 | She walks out of the studio |
| Door Exit | 从工作空间进入下班后的世界 | She transitions into after-work life |
| Warm Reflection | 用温暖结尾完成情绪落点 | The story ends with a warm emotional landing |

---

# 6. Shot List（镜头列表）

| Shot | Name | Duration | Story Function |
|---|---|---:|---|
| Shot 1 | Work Ending | 6s | Establish Jump finishing work |
| Shot 2 | Decision Moment | 6s | Show Jump deciding to leave |
| Shot 3 | Packing Up | 7s | Transition from work mode to life mode |
| Shot 4 | Walking Out | 10s | Show physical movement and emotional release |
| Shot 5 | Door Exit | 8s | Transition from office to after-work world |
| Shot 6 | Warm Ending | 8s | End with a warm series memory point |

Total Duration：

```text
45 seconds
```

---

# 7. Shot Details（逐镜头说明）

## Shot 1 — Work Ending

```text
Shot Number:
Shot 1

Shot Name:
Work Ending

Duration:
6 seconds

Story Function:
Establish that Jump has finished a long day of coding work.

Visual Description:
Jump sits at her desk inside TiaoTiao Studio Office. The laptop screen casts a soft warm glow on her fluffy face. Her hands pause above the keyboard, then slowly relax. The space feels warm, focused and lived-in.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — TiaoTiao Studio Office

Camera:
Medium desk shot, 35mm lens, eye-level framing, natural documentary stillness.

Motion:
Small relaxed hand movement, shoulders softening, hands leaving the keyboard.

Lighting:
LGT-001 — Warm Studio Lighting
Soft screen glow, practical desk lamp, gentle warm shadows.

Emotion:
Calm relief

Prompt Notes:
Warm cinematic documentary realism, realistic programmer desk, soft screen glow, cozy creator studio.

Negative Notes:
No cold corporate office, no cyberpunk blue lighting, no horror contrast, no game-render look.

Continuity Notes:
Laptop is still open. Backpack is visible near the desk. Coffee cup and desk lamp remain in place.
```

---

## Shot 2 — Decision Moment

```text
Shot Number:
Shot 2

Shot Name:
Decision Moment

Duration:
6 seconds

Story Function:
Show Jump deciding to leave work and begin her after-work life.

Visual Description:
Jump looks toward the window. Golden-hour light spills into the studio. She smiles slightly, closes the laptop, and her expression changes from tired focus to gentle expectation.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — TiaoTiao Studio Office

Camera:
Medium close-up, 50mm lens, soft push-in, eye-level.

Motion:
Subtle head turn, soft smile, laptop closing.

Lighting:
Warm screen glow fading as the laptop closes, golden-hour window spill becoming more present.

Emotion:
Expectation and freedom

Prompt Notes:
Emotional close-up, subtle smile, warm window light, cinematic after-work feeling.

Negative Notes:
No exaggerated smile, no dramatic acting, no hard commercial expression, no cold blue lighting.

Continuity Notes:
Laptop closes at the end of this shot. Jump’s decision is clear but quiet.
```

---

## Shot 3 — Packing Up

```text
Shot Number:
Shot 3

Shot Name:
Packing Up

Duration:
7 seconds

Story Function:
Create a tactile transition from work mode to life mode.

Visual Description:
Close-up details of Jump packing her backpack. Notebook, headphones, laptop, coffee cup and small desk objects appear in warm light. The movement is gentle and natural, like the end of a real workday.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — TiaoTiao Studio Office

Camera:
Detail close-ups, 50mm lens, soft depth of field.

Motion:
Hands packing notebook and headphones, backpack zipper closing, small object movement.

Lighting:
Warm practical desk lamp, soft ambient fill, gentle shadows.

Emotion:
Gentle transition

Prompt Notes:
Tactile realism, close-up object details, warm after-work routine, clean but lived-in desk.

Negative Notes:
No messy chaotic office, no over-staged commercial props, no cold corporate desk.

Continuity Notes:
Backpack becomes part of Jump’s state for the following shots. Laptop is now closed.
```

---

## Shot 4 — Walking Out

```text
Shot Number:
Shot 4

Shot Name:
Walking Out

Duration:
10 seconds

Story Function:
Show Jump physically leaving the work environment and entering a freer emotional state.

Visual Description:
Jump walks naturally through the studio with her backpack. The camera follows her at eye level. Her tail moves subtly. The studio remains warm, realistic and calm behind her.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 — TiaoTiao Studio Office

Camera:
CAM-001 — Hero Tracking Camera
35mm lens, eye-level tracking, subtle handheld documentary energy.

Motion:
MOT-001 — Natural Walking
Relaxed pace, grounded foot contact, realistic weight transfer, subtle tail motion.

Lighting:
LGT-001 — Warm Studio Lighting
Warm interior light with gentle depth.

Emotion:
Freedom begins

Prompt Notes:
Hero tracking shot, natural walking, cinematic documentary realism, warm creator studio.

Negative Notes:
No sliding feet, no robotic walking, no floating body, no impossible camera movement, no game camera.

Continuity Notes:
Jump carries backpack. Walking direction should remain consistent toward the exit.
```

---

## Shot 5 — Door Exit

```text
Shot Number:
Shot 5

Shot Name:
Door Exit

Duration:
8 seconds

Story Function:
Create the transition from work to after-work life.

Visual Description:
From behind, the camera follows Jump as she reaches the office door. She opens the door. Warm indoor light transitions toward brighter outside golden light. The frame feels open and hopeful.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
ENV-001 transitioning toward exterior after-work space

Camera:
Rear follow shot, 35mm lens, natural hero tracking movement.

Motion:
Natural walking, door opening, slight pause before stepping out.

Lighting:
Warm interior light transitioning into golden outside light.

Emotion:
Release and openness

Prompt Notes:
Rear follow transition, warm-to-open light shift, everyday cinematic freedom.

Negative Notes:
No dramatic escape feeling, no dark hallway, no horror doorway, no cold corporate exit.

Continuity Notes:
Door opens at the end of the shot. Jump remains carrying backpack.
```

---

## Shot 6 — Warm Ending

```text
Shot Number:
Shot 6

Shot Name:
Warm Ending

Duration:
8 seconds

Story Function:
End with a warm reflection and series memory point.

Visual Description:
Jump steps into the after-work light. The camera holds for a quiet moment. Her silhouette and soft fur are visible in warm golden light. Final caption appears with a calm emotional landing.

Character:
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack

Environment:
Exterior transition / after-work light

Camera:
Static hold or slow push-out, 35mm lens, gentle composition.

Motion:
Small relaxed breathing, subtle tail movement, soft pause.

Lighting:
Golden-hour warmth, soft natural light.

Emotion:
Freedom, quiet joy, reflection

Caption:
下班啦，生活开始啦。

Prompt Notes:
Warm ending frame, cinematic lifestyle storytelling, emotional stillness, series memory point.

Negative Notes:
No forced dramatic ending, no hard slogan energy, no overexposed light, no commercial pose.

Continuity Notes:
End frame should feel open, warm and reusable as a series ending.
```

---

# 8. Camera / Motion / Lighting Mapping（镜头动作灯光映射）

| Shot | Camera | Motion | Lighting | Asset |
|---|---|---|---|---|
| Shot 1 | Medium desk shot / 35mm | Hands leaving keyboard | LGT-001 warm screen glow | ASSET-001 |
| Shot 2 | Medium close-up / 50mm / gentle push-in | Head turn + soft smile + laptop close | Warm screen glow + golden-hour window spill | ASSET-001 |
| Shot 3 | Detail close-ups / 50mm | Object handling + backpack packing | Practical desk lamp + soft ambient fill | ASSET-001 |
| Shot 4 | CAM-001 Hero Tracking Camera | MOT-001 Natural Walking | LGT-001 warm studio light | ASSET-001 |
| Shot 5 | Rear follow shot / 35mm | Natural walking + door opening | Warm interior to golden exterior transition | ASSET-001 |
| Shot 6 | Static hold / slow push-out | Emotional hold + subtle tail motion | Golden-hour warmth | ASSET-001 |

---

# 9. Validation Checklist（验证检查表）

```text
[PASS] COMMAND-003 output follows required structure.
[PASS] Storyboard Summary is included.
[PASS] Story Beat Breakdown is included.
[PASS] Shot List is included.
[PASS] Shot Details are included.
[PASS] Camera / Motion / Lighting Mapping is included.
[PASS] Prompt Notes are included.
[PASS] Continuity Notes are included.
[PASS] Each shot has a clear story function.
[PASS] Each shot references TSOS Source Records.
[PASS] Jump remains an anthropomorphic fluffy female dog programmer.
[PASS] ASSET-001 is referenced in every shot.
[PASS] ENV-001 is used for office environment.
[PASS] MOT-001 is used for walking movement.
[PASS] CAM-001 is used for hero tracking shots.
[PASS] LGT-001 is used for warm studio lighting.
[PASS] STORYFORMULA-001 is followed.
[PASS] BRAND-001 warm and optimistic tone is preserved.
[PASS] No unapproved canon is added.
[PASS] No horror, cyberpunk, dark dystopian or game-render style is introduced.
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
COMMAND-002 — Generate Short Video Prompt

Purpose:
Validate whether the storyboard can be converted into model-ready AI video prompts.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial COMMAND-003 storyboard validation test |