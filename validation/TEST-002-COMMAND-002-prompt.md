# TEST-002 — COMMAND-002 Prompt Validation

> Validation Test（验证测试）  
> Command：COMMAND-002  
> Target：Generate Short Video Prompt  
> Project：PROJ-001  
> Status：PASS  
> Version：1.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-002 — Generate Short Video Prompt` 是否可以基于 TEST-001 的分镜结果，稳定生成适用于 AI 视频模型的短视频 Prompt。

本次测试重点检查：

- 是否正确调用 COMMAND-002
- 是否正确引用 WORKFLOW-002
- 是否正确调用 AGENT-002
- 是否正确读取 PROMPT-001
- 是否正确引用 CHAR-001 / ASSET-001
- 是否包含模型专用 Prompt
- 是否包含 Negative Prompt
- 是否通过一致性检查

## English

This test validates whether COMMAND-002 can generate model-ready short video prompts from the validated storyboard output of TEST-001.

---

# 2. Command Input（命令输入）

```text
Run COMMAND-002.

Prompt Type:
Video Prompt

Target Model:
Kling / Veo / Runway

Target Platform:
小红书

Aspect Ratio:
9:16

Duration:
6–8 seconds per shot

Source:
TEST-001 COMMAND-003 Storyboard Output

Language:
English prompt with Chinese production notes
```

---

# 3. Source Records（来源记录）

## Database Records

```text
CHAR-001 — Jump
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Jump After Work Pilot Project
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
BRAND-001 — TiaoTiao Studio Brand Language
```

## Agent

```text
AGENT-002 — Prompt Agent
```

## Workflow Reference

```text
WORKFLOW-002 — Short Video Prompt Workflow
```

## Storyboard Source

```text
TEST-001 — COMMAND-003 Storyboard Validation
```

---

# 4. Prompt Purpose（提示词用途）

```text
Generate model-ready 9:16 AI video prompts for the Jump After Work storyboard.

The prompts should help generate warm cinematic short video clips where Jump finishes work, packs her backpack and leaves TiaoTiao Studio Office.
```

---

# 5. Prompt Task Brief（提示词任务简报）

```text
Prompt Type:
Video Prompt

Target Models:
Kling / Veo / Runway

Aspect Ratio:
9:16 vertical video

Clip Duration:
6–8 seconds per shot

Main Character:
Jump

Main Scene:
TiaoTiao Studio Office

Core Action:
Jump finishes work and walks toward after-work freedom.

Core Emotion:
Freedom

Style:
Cinematic documentary realism

Brand:
Warm, optimistic, honest, lifestyle-focused TiaoTiao Studio brand language.
```

---

# 6. Base Prompt（基础提示词）

```text
Create a warm cinematic vertical short video for the Jump After Work series.

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, wearing her default programmer outfit with Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Scene:
TiaoTiao Studio Office, a warm modern creator studio with a realistic programmer desk, laptop, keyboard, monitor, desk lamp, notebook, coffee cup, backpack, headphones and small plant. The office feels clean but lived-in, warm, creative and not corporate.

Action:
Jump has just finished work. She closes the laptop, gently packs her backpack, then walks naturally toward the office exit. Her body language is relaxed and light, expressing the feeling that life begins again after work.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, natural camera motion, subtle handheld documentary energy, environmental storytelling.

Motion:
Natural walking, relaxed pace, realistic weight transfer, grounded foot contact, soft body mechanics, subtle tail movement, no robotic motion.

Lighting:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows, cozy creator studio mood.

Mood:
Freedom, relaxation, warmth, everyday joy, gentle after-work relief.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth, high-quality film still, soft warm atmosphere.

Brand Consistency:
Warm, optimistic, honest, creative and lifestyle-focused TiaoTiao Studio brand language.
```

---

# 7. Shot-by-Shot Prompt Test（逐镜头 Prompt 测试）

## Shot 1 — Work Ending

```text
Duration:
6 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, warm friendly expression, soft realistic fur texture, consistent with ASSET-001.

Start Frame:
Jump sits at her desk inside TiaoTiao Studio Office. The laptop screen gives a soft warm glow on her fluffy face.

Action:
Her hands pause above the keyboard, then slowly relax and leave the keyboard. Her shoulders soften as she finishes work.

End Frame:
Jump looks calm and relieved. The laptop remains open, and the backpack is visible nearby.

Camera:
Medium desk shot, 35mm lens, eye-level framing, natural documentary stillness.

Lighting:
Warm screen glow, practical desk lamp, gentle warm shadows.

Mood:
Calm relief, end of workday.

Style:
Warm cinematic documentary realism, realistic programmer workspace, cozy creator studio atmosphere.
```

---

## Shot 2 — Decision Moment

```text
Duration:
6 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, consistent with ASSET-001, fluffy female dog programmer with slim body and warm expression.

Start Frame:
Jump looks toward the window from her desk. Golden-hour light enters the studio.

Action:
She smiles slightly, closes the laptop, and shifts from tired focus to gentle expectation.

End Frame:
The laptop is closed. Jump’s expression shows that she has decided to leave work.

Camera:
Medium close-up, 50mm lens, soft push-in, eye-level framing.

Lighting:
Warm screen glow fading as the laptop closes, golden-hour window spill becoming more present.

Mood:
Expectation, freedom, quiet hope.

Style:
Cinematic documentary realism, warm lifestyle storytelling.
```

---

## Shot 3 — Packing Up

```text
Duration:
7 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, consistent with ASSET-001.

Start Frame:
Close-up of Jump’s hands near the desk objects.

Action:
Jump gently packs her notebook and headphones into her backpack. The backpack zipper closes naturally.

End Frame:
The backpack is packed and ready. The desk remains warm, clean and lived-in.

Camera:
Detail close-ups, 50mm lens, soft depth of field.

Lighting:
Warm practical desk lamp, soft ambient fill, gentle shadows.

Mood:
Gentle transition from work mode to life mode.

Style:
Tactile realism, warm after-work routine, cinematic lifestyle detail.
```

---

## Shot 4 — Walking Out

```text
Duration:
8–10 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, anthropomorphic fluffy female dog programmer, slim body, warm expression, backpack on, consistent with ASSET-001.

Start Frame:
Jump begins walking through TiaoTiao Studio Office.

Action:
She walks naturally toward the exit. Her steps are grounded, her body weight shifts realistically, and her tail moves subtly.

End Frame:
Jump continues toward the office door, carrying a light sense of freedom.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, subtle handheld documentary energy.

Motion:
Natural walking, relaxed pace, grounded foot contact, realistic weight transfer, soft body mechanics.

Lighting:
Warm studio lighting, gentle environmental depth.

Mood:
Freedom begins, relaxed after-work movement.

Style:
Cinematic documentary realism, environmental storytelling, warm creator-studio atmosphere.
```

---

## Shot 5 — Door Exit

```text
Duration:
8 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, consistent with ASSET-001, carrying her backpack.

Start Frame:
Jump reaches the office door from inside the warm studio.

Action:
She opens the door and steps toward the brighter outside golden light.

End Frame:
The door opens, and warm indoor light transitions into after-work light.

Camera:
Rear follow shot, 35mm lens, natural hero tracking movement.

Motion:
Natural walking, door opening, slight pause before stepping out.

Lighting:
Warm interior light transitioning into golden exterior light.

Mood:
Release, openness, life beginning after work.

Style:
Warm cinematic documentary realism, soft emotional transition.
```

---

## Shot 6 — Warm Ending

```text
Duration:
8 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, consistent with ASSET-001, seen in warm after-work light.

Start Frame:
Jump steps into the after-work light.

Action:
She pauses gently, breathing calmly. Her tail moves subtly. The final emotional moment holds.

End Frame:
A warm ending frame with the feeling that life begins again after work.

Camera:
Static hold or slow push-out, 35mm lens, gentle composition.

Lighting:
Golden-hour warmth, soft natural light.

Mood:
Freedom, quiet joy, warm reflection.

Caption:
下班啦，生活开始啦。

Style:
Cinematic lifestyle storytelling, emotional stillness, warm optimistic ending.
```

---

# 8. Model-Specific Prompt Validation（模型适配验证）

## Kling Prompt Test

```text
Kling prompt contains:
[PASS] Duration
[PASS] Subject
[PASS] Start Frame
[PASS] Action
[PASS] End Frame
[PASS] Camera
[PASS] Motion
[PASS] Lighting
[PASS] Environment
[PASS] Continuity
[PASS] Negative Prompt
```

## Veo Prompt Test

```text
Veo prompt contains:
[PASS] Cinematic scene description
[PASS] Character identity
[PASS] Environment
[PASS] Natural motion
[PASS] Camera language
[PASS] Lighting mood
[PASS] Emotional tone
[PASS] Character consistency rule
```

## Runway Prompt Test

```text
Runway prompt contains:
[PASS] Short executable description
[PASS] Clear subject
[PASS] Clear action
[PASS] Camera instruction
[PASS] Motion restriction
[PASS] Lighting direction
[PASS] Consistency constraints
```

---

# 9. Standard Negative Prompt（标准负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, do not remove fluffy fur, do not make Jump muscular, do not change outfit, do not remove Fire Dragon Fruit Pink accents, do not use horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, floating body, mechanical tail movement, impossible motion, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, inconsistent environment, aggressive expression, cheap CGI look, hard-selling commercial mood, clickbait visual style.
```

---

# 10. Chinese Production Notes（中文制作备注）

```text
画幅：
9:16 竖屏

视频时长：
每个镜头 6–8 秒左右

核心内容：
跳跳下班，关电脑，收拾背包，走出办公室。

角色要求：
跳跳必须保持拟人化毛茸茸小狗程序员身份，身体苗条，表情温暖，不能变成人，不能变成其他动物。

动作要求：
自然行走，脚步不能滑，身体不能漂浮，不能机器人动作，尾巴轻微自然摆动。

镜头要求：
35mm 平视跟拍，电影纪录片质感，不要 FPS 游戏感，不要无人机环绕，不要极端广角。

灯光要求：
温暖工作室灯光、台灯、屏幕柔光、傍晚窗光，不要赛博朋克蓝光，不要恐怖片高反差。

情绪要求：
下班后的自由、轻松、温暖、生活重新开始。
```

---

# 11. Validation Checklist（验证检查表）

```text
[PASS] COMMAND-002 output follows required structure.
[PASS] Prompt Purpose is included.
[PASS] Target Model is included.
[PASS] Source Records are included.
[PASS] Base Prompt is included.
[PASS] Shot-by-shot prompts are included.
[PASS] Model-specific prompt validation is included.
[PASS] Negative Prompt is included.
[PASS] Chinese Production Notes are included.
[PASS] Consistency Checklist is included.
[PASS] Prompt references CHAR-001.
[PASS] Prompt references ASSET-001.
[PASS] Prompt references PROMPT-001.
[PASS] Prompt references ENV-001.
[PASS] Prompt references MOT-001.
[PASS] Prompt references CAM-001.
[PASS] Prompt references LGT-001.
[PASS] Prompt follows STYLE-001.
[PASS] Prompt follows BRAND-001.
[PASS] Prompt avoids cyberpunk, horror, game-render and dark dystopian directions.
[PASS] Prompt does not change Jump's identity.
```

---

# 12. Issues Found（发现问题）

```text
No critical issues found.
No major issues found.
No minor issues found.
```

---

# 13. Final Result（最终结果）

```text
PASS
```

---

# 14. Next Validation Action（下一步验证）

```text
Run TEST-003:
COMMAND-005 — Consistency Check Validation

Purpose:
Validate whether TSOS can detect consistency risks and confirm that TEST-001 and TEST-002 outputs follow the Source of Truth.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial COMMAND-002 prompt validation test |