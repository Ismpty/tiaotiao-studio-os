# COMMAND-002 Prompt Example — Video Prompt Package

> Example Output（示例输出）  
> Command：COMMAND-002  
> Workflow：WORKFLOW-002  
> Agent：AGENT-002  
> Project：PROJ-001  
> Version：2.0
> Status：Example

---

# 1. Source References（内部来源）

以下来源只用于 GitHub / Notion / Review / Consistency Check，不应裸露在模型可复制 Prompt 中。

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

---

# 2. Prompt Task Brief（提示词任务简报）

```text
Project:
PROJ-001 — Jump After Work Pilot Project

Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels

Target Model:
Jimeng / 即梦

Backup Models:
Veo / Runway

Aspect Ratio:
9:16 vertical video

Runtime Structure:
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Model-readable check
↓
COMMAND-005 review
```

---

# 3. Identity Card Prompt（身份卡提示词）

```text
请生成一张角色身份卡，用于锁定跳跳在后续视频生成中的外观一致性。

跳跳是一只保持真实小狗本体形态的毛茸茸小狗角色，穿程序员风格小狗衣服。她必须保持四足小狗身体结构、小狗比例、蓬松毛发和温暖友好的表情。她可以背小包、戴工牌或项圈挂饰，身上可以有少量火龙果粉色点缀。

身份卡应清楚展示跳跳的正面、侧面和简单动作姿态。服装应像小狗可以穿的程序员风格服装，而不是人类身体上的衣服。整体感觉温暖、真实、生活化，有创作者气质。

禁止把跳跳画成半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例、直立人形角色、其他动物、无衣服普通宠物狗、肌肉角色或恐怖 / 赛博朋克风格角色。
```

---

# 4. Storyboard Prompt（故事板提示词）

```text
请为《跳跳下班啦》生成 9:16 竖屏短视频故事板。

故事板主体必须是黑白粗略铅笔线稿，保持极简细节、快速动态描绘、简单解剖结构、清晰轮廓和导演前期预演分镜草图感。不要做成彩色成片插画、真实渲染成片、精修概念图、儿童绘本风或漫画上色成稿。

跳跳必须保持真实小狗本体形态，穿程序员风格小狗衣服，可以背小包、戴工牌或项圈挂饰，有少量火龙果粉色点缀。故事板中的跳跳动作必须符合小狗身体结构，不要出现人类手掌、人类手臂、人类双腿站立或人类身体比例。

请输出 6 个镜头：

Shot 1 — Work Ending，6 秒：跳跳在温暖的创作者工作室桌前结束代码工作，电脑屏幕和台灯发出柔和暖光。
Shot 2 — Decision Moment，6 秒：跳跳看向窗外的傍晚光，轻轻合上电脑，表情从专注变成期待。
Shot 3 — Packing Up，7 秒：跳跳把笔记本、耳机和小物件放进小背包，道具动作温柔清楚。
Shot 4 — Walking Out，10 秒：跳跳背着小包，用自然小狗动作穿过工作室，镜头平视跟拍。
Shot 5 — Door Exit，8 秒：跳跳到达门口，门打开，室内暖光过渡到下班后的金色光。
Shot 6 — Warm Ending，8 秒：跳跳进入下班后的光线中，画面停留在温暖、自由、生活重新开始的情绪上。

请保留彩色动态标注系统：
红色箭头表示镜头运动。
蓝色箭头表示跳跳 / 小狗动作方向。
黄色圈注表示道具互动。
绿色标注表示灯光和情绪变化。
紫色标注表示连续性和转场。
```

---

# 5. Universal Video Prompt（通用视频提示词）

```text
请严格参考上传的角色身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

角色外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。

视频规格：
9:16 竖屏，单镜头 6–10 秒，温暖真实的生活方式短视频质感。

动作要求：
跳跳必须保持真实小狗本体形态和四足小狗身体结构。动作要自然、有真实重心、脚步不滑、身体不漂浮。不要出现人类式走路、人类手掌、人类手臂、人类双腿站立或人类身体比例。

镜头要求：
使用自然平视镜头，35mm 生活化纪录片视角，镜头运动必须服务故事，不要炫技，不要无人机环绕，不要第一人称游戏视角。

灯光和情绪：
保持温暖工作室灯光、柔和屏幕光、台灯光和傍晚金色光。情绪是下班后的自由、轻松、温暖和生活重新开始。

连续性要求：
严格匹配故事板中的前后镜头关系，保持跳跳服装、毛发、小包、工牌 / 项圈挂饰、火龙果粉色点缀、道具状态和光线方向连续。

负面要求：
不要改变跳跳的物种。不要把跳跳变成人类、半人角色、其他动物或无衣服普通宠物狗。不要出现人类手掌、人类手臂、人类双腿站立、人类身体比例、恐怖、暴力、黑暗反乌托邦、赛博朋克蓝光、霓虹科幻光、游戏动画感、机器人动作、滑步、漂浮身体、极端广角畸变、无人机环绕、第一人称镜头、杂乱办公室、冷冰冰公司办公室、强销售广告感或标题党风格。
```

---

# 6. Runtime Usage Example（运行方式示例）

```text
1. Use the Identity Card Prompt to generate or confirm Jump's identity card.
2. Use the Storyboard Prompt to generate the black-and-white rough pencil storyboard with colored annotations.
3. Upload the identity card and storyboard to Jimeng / 即梦.
4. Use the Universal Video Prompt.
5. Replace [SHOT NUMBER AND NAME] with the target storyboard shot.
6. Generate one shot at a time.
7. Run COMMAND-005 review for every generated clip.
```

---

# 7. Model-readable Check Report（模型可读检查报告）

```text
[PASS] Identity Card Prompt is model-readable natural language.
[PASS] Storyboard Prompt is model-readable natural language.
[PASS] Universal Video Prompt is model-readable natural language.
[PASS] Model-copyable prompt sections do not rely on raw internal IDs.
[PASS] Jump is described as a real dog-form character wearing clothes.
[PASS] Humanoid body, human hands, human arms, human legs and human proportions are forbidden.
[PASS] Storyboard style is black-and-white rough pencil line art.
[PASS] Storyboard color annotation system is preserved.
[PASS] Shot details belong to the storyboard.
[PASS] Universal Video Prompt is compact and shot-placeholder based.
```

---

# 8. COMMAND-005 Review Result（COMMAND-005 审查结果）

```text
Result:
PASS

Reason:
The prompt package follows the current Prompt Runtime Architecture, preserves Jump as a real dog-form character wearing clothes, keeps storyboard body style black-and-white rough pencil line art, retains colored annotations, and avoids raw internal IDs in model-copyable prompt sections.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated example to Identity Card Prompt, Storyboard Prompt and Universal Video Prompt structure |
| 1.0 | 2026 | Initial COMMAND-002 prompt example |
