# PROJ-001 — Shot-by-Shot Video Prompts（逐镜头视频提示词）

> Production Output（生产输出）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Command：COMMAND-002  
> Workflow：WORKFLOW-003  
> Target Models：Kling / Veo / Runway  
> Version：1.0  
> Status：Production Ready

---

# 1. Production Purpose（生产目的）

## 中文

本文件用于正式生成《跳跳下班啦》试播项目的逐镜头 AI 视频片段。

每个镜头都可以单独复制到 Kling / Veo / Runway 中生成视频片段，再进入剪辑阶段。

本文件必须遵守 TSOS Source of Truth：

```text
CHAR-001
ASSET-001
ENV-001
MOT-001
CAM-001
LGT-001
STYLE-001
COLOR-001
BRAND-001
```

## English

This file provides production-ready shot-by-shot AI video prompts for PROJ-001 — Jump After Work Pilot Project.

Each shot can be generated separately in Kling, Veo or Runway, then assembled in editing.

---

# 2. Global Production Settings（全局生产设置）

```text
Project:
PROJ-001 — Jump After Work Pilot Project

Episode:
EP-001 — Jump After Work

Story:
STORY-001 — Work Ends, Adventure Begins

Character:
CHAR-001 — Jump

Asset Reference:
ASSET-001 — Jump Character Reference Pack

Aspect Ratio:
9:16 vertical video

Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels

Visual Style:
Cinematic documentary realism

Core Emotion:
Freedom

Brand Tone:
Warm, optimistic, honest, lifestyle-focused
```

---

# 3. Global Character Lock（全局角色锁定）

所有镜头必须保持：

```text
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit, Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.
```

禁止：

```text
Do not change Jump's species.
Do not turn Jump into a human.
Do not remove fluffy fur.
Do not make Jump muscular.
Do not change outfit.
Do not remove Fire Dragon Fruit Pink accents.
Do not make Jump aggressive.
Do not make Jump horror, cyberpunk or game-render style.
```

---

# 4. Global Negative Prompt（全局负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, do not remove fluffy fur, do not make Jump muscular, do not change outfit, do not remove Fire Dragon Fruit Pink accents, do not use horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, floating body, mechanical tail movement, impossible motion, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, inconsistent environment, aggressive expression, cheap CGI look, hard-selling commercial mood, clickbait visual style.
```

---

# 5. Shot Prompt Package（逐镜头提示词包）

---

## Shot 1 — Work Ending

### Shot Info

```text
Duration:
6 seconds

Aspect Ratio:
9:16

Story Function:
Establish that Jump has finished a long day of coding work.

Emotion:
Calm relief
```

### Kling Prompt

```text
Duration:
6 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit with subtle Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Start Frame:
Jump sits at her desk inside TiaoTiao Studio Office at the end of the workday. The laptop screen casts a soft warm glow on her fluffy face. A keyboard, monitor, desk lamp, notebook, coffee cup, backpack, headphones and small plant are visible in the warm creator studio.

Action:
Jump’s hands pause above the keyboard, then slowly relax and leave the keyboard. Her shoulders soften slightly as she realizes the workday is finished.

End Frame:
Jump looks calm and quietly relieved. The laptop remains open. The backpack is visible near the desk, suggesting she will leave soon.

Camera:
Medium desk shot, 35mm lens, eye-level framing, natural documentary stillness, realistic depth, no dramatic camera movement.

Motion:
Small relaxed hand movement, subtle breathing, soft body mechanics, no exaggerated acting.

Lighting:
Warm Studio Lighting, soft laptop screen glow, practical desk lamp, gentle warm shadows, cozy creator studio mood.

Mood:
Calm relief, end of workday, warm and quiet.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, high-quality film still.
```

### Chinese Notes

```text
这一镜头重点是“工作结束”的状态，不要太夸张。
跳跳还坐在桌前，电脑还开着，动作很小，只是手离开键盘、肩膀放松。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

## Shot 2 — Decision Moment

### Shot Info

```text
Duration:
6 seconds

Aspect Ratio:
9:16

Story Function:
Show Jump deciding to leave work and begin after-work life.

Emotion:
Expectation and freedom
```

### Kling Prompt

```text
Duration:
6 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit with Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Start Frame:
Jump sits near her desk inside TiaoTiao Studio Office. She turns her head slightly toward the window. Golden-hour light spills softly into the warm studio.

Action:
Jump gives a small, gentle smile. She closes the laptop calmly. As the laptop closes, her expression changes from tired focus to quiet expectation.

End Frame:
The laptop is closed. Jump looks ready to leave work and begin her after-work life.

Camera:
Medium close-up, 50mm lens, soft push-in, eye-level framing, natural camera motion, intimate but not dramatic.

Motion:
Subtle head turn, gentle smile, natural laptop closing motion, relaxed shoulders, soft breathing.

Lighting:
Warm screen glow fades as the laptop closes. Golden-hour window spill becomes more present. Practical desk lamp remains warm and soft.

Mood:
Hopeful, quiet, warm, life beginning after work.

Style:
Cinematic documentary realism, soft emotional close-up, warm lifestyle storytelling.
```

### Chinese Notes

```text
这一镜头是情绪转折点。
不要大笑，不要夸张表演，只需要一个很轻的微笑和关电脑动作。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

## Shot 3 — Packing Up

### Shot Info

```text
Duration:
7 seconds

Aspect Ratio:
9:16

Story Function:
Show transition from work mode to life mode.

Emotion:
Gentle transition
```

### Kling Prompt

```text
Duration:
7 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, anthropomorphic fluffy female dog programmer, consistent with ASSET-001. Focus on her hands, backpack and desk objects while keeping character identity consistent.

Start Frame:
Close-up of Jump’s hands near the warm desk. Notebook, headphones, laptop, coffee cup and backpack are visible in soft warm light.

Action:
Jump gently packs her notebook and headphones into the backpack. She closes the backpack zipper naturally. Small desk objects move slightly as she prepares to leave.

End Frame:
The backpack is packed and ready beside Jump. The desk remains clean but lived-in, warm and realistic.

Camera:
Detail close-ups, 50mm lens, soft depth of field, tactile realism, no fast camera movement.

Motion:
Natural hand movement, realistic object handling, gentle zipper closing, no robotic movement.

Lighting:
Warm practical desk lamp, soft ambient fill, gentle shadows, cozy end-of-work atmosphere.

Mood:
Quiet transition, warm routine, life mode starting.

Style:
Cinematic documentary realism, tactile lifestyle detail, natural warm color.
```

### Chinese Notes

```text
这一镜头可以多生成几个备用版本。
重点是手部、背包、耳机、笔记本、拉链这些细节。
不要让桌面过乱，也不要像商业广告摆拍。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

## Shot 4 — Walking Out

### Shot Info

```text
Duration:
8–10 seconds

Aspect Ratio:
9:16

Story Function:
Show Jump physically leaving the work environment.

Emotion:
Freedom begins
```

### Kling Prompt

```text
Duration:
8–10 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit with Fire Dragon Fruit Pink brand accents, backpack on, consistent with ASSET-001.

Start Frame:
Jump stands inside TiaoTiao Studio Office with her backpack. The warm creator studio is visible behind her.

Action:
Jump walks naturally through the studio toward the office exit. Her steps are grounded and relaxed. Her body weight shifts realistically. Her tail moves subtly with her walking rhythm.

End Frame:
Jump continues toward the office door, carrying a light sense of freedom and after-work relief.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, natural camera movement, subtle handheld documentary energy, environmental storytelling.

Motion:
Natural walking, relaxed pace, grounded foot contact, realistic weight transfer, soft body mechanics, subtle tail movement.

Lighting:
Warm Studio Lighting, practical ambient light, soft golden-hour window spill, gentle shadows, realistic depth.

Mood:
Freedom begins, relaxed movement, warm after-work feeling.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth.
```

### Chinese Notes

```text
这一镜头最容易出问题，重点检查脚步。
必须避免滑步、漂浮、机器人动作。
镜头是平视跟拍，不要游戏视角，不要无人机环绕。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

## Shot 5 — Door Exit

### Shot Info

```text
Duration:
8 seconds

Aspect Ratio:
9:16

Story Function:
Transition from office to after-work world.

Emotion:
Release and openness
```

### Kling Prompt

```text
Duration:
8 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, anthropomorphic fluffy female dog programmer, slim body, soft realistic fur, default programmer outfit, Fire Dragon Fruit Pink accents, carrying backpack, consistent with ASSET-001.

Start Frame:
Jump reaches the office door from inside TiaoTiao Studio Office. Warm indoor light surrounds her.

Action:
Jump opens the door naturally and steps toward the brighter golden outside light. Her movement is calm, grounded and relaxed.

End Frame:
The door opens. Warm indoor light transitions into brighter after-work golden light. Jump is about to step into the outside world.

Camera:
Rear follow shot, 35mm lens, eye-level hero tracking movement, natural documentary camera, gentle depth.

Motion:
Natural walking, realistic door opening, slight pause before stepping out, subtle tail motion.

Lighting:
Warm interior light transitioning into golden exterior light, soft shadows, no harsh contrast.

Mood:
Release, openness, life beginning after work.

Style:
Warm cinematic documentary realism, soft emotional transition, lifestyle storytelling.
```

### Chinese Notes

```text
这一镜头是空间转换。
不要做成“逃离公司”的戏剧感，而是温暖、轻松、自然地离开。
门外光线要温暖，不要过曝。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

## Shot 6 — Warm Ending

### Shot Info

```text
Duration:
8 seconds

Aspect Ratio:
9:16

Story Function:
End with emotional memory point.

Emotion:
Freedom, quiet joy, reflection
```

### Kling Prompt

```text
Duration:
8 seconds

Aspect Ratio:
9:16 vertical video

Subject:
Jump, anthropomorphic fluffy female dog programmer, slim body, warm friendly expression, soft realistic fur texture, default programmer outfit with Fire Dragon Fruit Pink brand accents, backpack on, consistent with ASSET-001.

Start Frame:
Jump steps into warm after-work golden light outside the studio. The atmosphere feels open, calm and gentle.

Action:
Jump pauses for a quiet moment. She breathes calmly. Her tail moves subtly. She looks relaxed, like she has given time back to herself.

End Frame:
A warm emotional ending frame. Jump stands in the after-work light. The final feeling is that life begins again after work.

Camera:
Static hold or slow push-out, 35mm lens, gentle composition, eye-level, natural depth.

Motion:
Small relaxed breathing, subtle tail movement, soft emotional hold, no exaggerated posing.

Lighting:
Golden-hour warmth, soft natural light, gentle shadows, warm optimistic atmosphere.

Mood:
Freedom, quiet joy, warmth, everyday life becoming meaningful.

Style:
Cinematic lifestyle storytelling, soft warm film still, natural color balance, emotional stillness.
```

### Final Caption

```text
下班啦，生活开始啦。
```

### Chinese Notes

```text
结尾不要喊口号，不要商业摆拍。
保持安静、温暖、有一点回味。
这一帧可以作为系列固定结尾风格参考。
```

### Negative Prompt

```text
Use Global Negative Prompt.
```

---

# 6. Recommended Generation Order（推荐生成顺序）

建议按以下顺序生成：

```text
1. Shot 1 — Work Ending
2. Shot 2 — Decision Moment
3. Shot 3 — Packing Up
4. Shot 4 — Walking Out
5. Shot 5 — Door Exit
6. Shot 6 — Warm Ending
```

原因：

```text
先生成室内稳定镜头，再生成动作复杂的行走镜头。
Shot 4 和 Shot 5 最容易出现动作漂移，需要多生成几个版本。
```

---

# 7. Clip Review Checklist（视频片段检查表）

每个视频片段生成后必须检查：

```text
[ ] Jump 是否仍然是拟人化毛茸茸小狗
[ ] Jump 是否没有变成人类
[ ] Jump 是否保持苗条体型
[ ] Jump 是否保持程序员身份
[ ] Jump 是否参考 ASSET-001
[ ] 毛发是否稳定
[ ] 服装是否稳定
[ ] 品牌色点缀是否稳定
[ ] 动作是否自然
[ ] 脚步是否没有滑动
[ ] 身体是否没有漂浮
[ ] 尾巴动作是否自然
[ ] 镜头是否平视自然
[ ] 灯光是否温暖
[ ] 场景是否符合 ENV-001
[ ] 是否没有赛博朋克 / 恐怖 / 游戏感
```

---

# 8. Continuity Notes（连续性备注）

```text
Shot 1:
Laptop is open. Jump is still working.

Shot 2:
Laptop closes. Jump decides to leave.

Shot 3:
Backpack is packed. Laptop is closed.

Shot 4:
Jump carries backpack and walks toward the exit.

Shot 5:
Jump opens the door and transitions toward outside light.

Shot 6:
Jump is outside or near the exit in warm after-work light.
```

---

# 9. Production Notes（制作备注）

```text
Shot 1–3:
Can be generated with stable character and environment priority.

Shot 4–5:
Need stronger motion checking. Generate multiple takes if necessary.

Shot 6:
Focus on emotional ending and warm lighting. Avoid overexposure.

Recommended workflow:
Generate each shot separately.
Review each shot using COMMAND-005.
Only approved clips should enter editing.
```

---

# 10. Final Consistency Checklist（最终一致性检查）

```text
[PASS] Uses PROJ-001.
[PASS] Uses CHAR-001.
[PASS] Uses ASSET-001.
[PASS] Uses ENV-001.
[PASS] Uses MOT-001.
[PASS] Uses CAM-001.
[PASS] Uses LGT-001.
[PASS] Uses STYLE-001.
[PASS] Uses BRAND-001.
[PASS] Includes Negative Prompt.
[PASS] Supports shot-by-shot production.
[PASS] Ready for AI video generation.
```

---

# 11. Next Production Action（下一步生产动作）

```text
1. Copy Shot 1 prompt into Kling / Veo / Runway.
2. Generate 2–3 versions.
3. Select the most stable version.
4. Run COMMAND-005 visual consistency check.
5. Repeat for Shot 2–6.
6. Save selected clips into production/PROJ-001/clips/.
7. Continue to cover package generation.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial shot-by-shot video prompt production file |