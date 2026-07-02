# PROJ-001 — Clip Review Guide（视频片段审片指南）

> Production Review（生产审片）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Command：COMMAND-005  
> Workflow：WORKFLOW-003  
> Version：1.0  
> Status：Review Ready

---

# 1. Purpose（目的）

## 中文

本文件用于检查《跳跳下班啦》试播项目真实生成的视频片段。

每个 Shot 生成后，都必须先经过本审片规则检查，再决定是否进入剪辑阶段。

本文件重点检查：

- Jump 角色是否漂移
- 毛茸茸质感是否稳定
- 动作是否自然
- 脚步是否滑动
- 镜头是否符合设定
- 灯光是否正确
- 场景是否连续
- 情绪是否符合《跳跳下班啦》
- 是否可以进入最终剪辑

## English

This file defines the clip review rules for real generated video clips of PROJ-001.

Each generated shot must be reviewed before entering the editing stage.

---

# 2. Source of Truth（唯一事实来源）

所有视频片段必须遵守：

```text
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
EMOTION-001 — Freedom
BRAND-001 — TiaoTiao Studio Brand Language
```

---

# 3. Review Workflow（审片流程）

每个镜头生成后，按照以下顺序检查：

```text
1. Character Check
2. Motion Check
3. Camera Check
4. Lighting Check
5. Environment Check
6. Continuity Check
7. Emotion Check
8. Technical Quality Check
9. Final Decision
```

---

# 4. File Naming Rule（文件命名规则）

生成视频片段建议命名：

```text
production/PROJ-001/clips/SHOT-001-v01.mp4
production/PROJ-001/clips/SHOT-001-v02.mp4
production/PROJ-001/clips/SHOT-001-v03.mp4

production/PROJ-001/clips/SHOT-002-v01.mp4
production/PROJ-001/clips/SHOT-002-v02.mp4
production/PROJ-001/clips/SHOT-002-v03.mp4
```

通过审片的版本建议复制到：

```text
production/PROJ-001/clips/approved/
```

命名：

```text
SHOT-001-approved.mp4
SHOT-002-approved.mp4
SHOT-003-approved.mp4
SHOT-004-approved.mp4
SHOT-005-approved.mp4
SHOT-006-approved.mp4
```

---

# 5. Character Check（角色检查）

## Must Pass

```text
[ ] Jump 仍然是拟人化毛茸茸小狗
[ ] Jump 没有变成人类
[ ] Jump 没有变成其他动物
[ ] Jump 保持女性角色设定
[ ] Jump 保持程序员身份
[ ] Jump 保持苗条体型
[ ] Jump 毛发清晰且稳定
[ ] Jump 表情温暖友好
[ ] Jump 服装没有明显漂移
[ ] Fire Dragon Fruit Pink 仍然作为点缀存在
[ ] Jump 没有变成肌肉型角色
[ ] Jump 没有恐怖、攻击性或诡异表情
```

## Critical Fail

以下任意一项出现，片段不能使用：

```text
Jump 变成人类
Jump 变成其他动物
Jump 毛发消失
Jump 脸部严重变形
Jump 身体比例严重错误
Jump 变成恐怖 / 赛博朋克 / 游戏角色
```

---

# 6. Motion Check（动作检查）

## Must Pass

```text
[ ] 动作自然可信
[ ] 身体有真实重心
[ ] 脚步没有明显滑动
[ ] 身体没有漂浮
[ ] 手部动作没有严重变形
[ ] 尾巴动作自然
[ ] 行走节奏轻松
[ ] 动作符合下班后的放松感
```

## Shot 4 / Shot 5 Special Check

Shot 4 和 Shot 5 是动作风险最高的镜头，必须重点检查：

```text
[ ] 脚是否贴地
[ ] 步伐是否稳定
[ ] 身体是否没有穿模
[ ] 背包是否稳定
[ ] 门的开合是否自然
[ ] 镜头跟拍是否不晃乱
```

## Critical Fail

```text
严重滑步
身体漂浮
四肢扭曲
手部融化
尾巴机械乱动
角色瞬移
门或道具穿模严重
```

---

# 7. Camera Check（镜头检查）

## Must Pass

```text
[ ] 镜头为自然平视视角
[ ] 镜头服务故事
[ ] 35mm / 50mm 视角感合理
[ ] 主体没有被严重裁切
[ ] 运镜自然可信
[ ] 没有 FPS 游戏感
[ ] 没有无人机环绕炫技
[ ] 没有极端广角变形
[ ] 没有强烈人工抖动
```

## Preferred Camera Feel

```text
Cinematic documentary realism
Natural eye-level framing
Warm lifestyle storytelling
Gentle hero tracking
Realistic depth
```

---

# 8. Lighting Check（灯光检查）

## Must Pass

```text
[ ] 灯光温暖
[ ] 有工作室室内暖光
[ ] 有台灯 / 屏幕柔光 / 傍晚窗光
[ ] 阴影柔和
[ ] 没有冷蓝赛博朋克主光
[ ] 没有恐怖片高反差
[ ] 没有过度 RGB 灯效
[ ] 没有严重过曝
[ ] 没有死黑
```

## Shot 5 / Shot 6 Special Check

```text
[ ] 室内到门外光线过渡自然
[ ] 门外光不刺眼
[ ] 金色暖光有下班后的自由感
[ ] 结尾画面不空、不假、不商业摆拍
```

---

# 9. Environment Check（环境检查）

## Must Pass

```text
[ ] 场景符合 TiaoTiao Studio Office
[ ] 桌面道具符合程序员工作室
[ ] 办公室温暖、有生活感
[ ] 背景不杂乱
[ ] 没有冷冰冰企业办公室感
[ ] 没有赛博朋克城市空间
[ ] 没有恐怖走廊
[ ] 没有不相关场景突然出现
```

## Required Objects

根据镜头不同，可出现：

```text
laptop
keyboard
monitor
desk lamp
notebook
coffee cup
backpack
headphones
small plant
office door
```

---

# 10. Continuity Check（连续性检查）

## Shot Continuity

```text
Shot 1:
Laptop open. Jump is still working.

Shot 2:
Laptop closes. Jump decides to leave.

Shot 3:
Backpack is packed. Laptop is closed.

Shot 4:
Jump carries backpack and walks toward exit.

Shot 5:
Jump opens door and transitions toward outside light.

Shot 6:
Jump pauses in warm after-work light.
```

## Must Check

```text
[ ] 电脑状态是否连续
[ ] 背包状态是否连续
[ ] Jump 方向是否连续
[ ] 光线变化是否合理
[ ] 场景空间是否可连接
[ ] Shot 4 是否能接 Shot 5
[ ] Shot 5 是否能接 Shot 6
```

---

# 11. Emotion Check（情绪检查）

## Must Pass

```text
[ ] 情绪是温暖的
[ ] 情绪是轻松的
[ ] 情绪有下班后的自由感
[ ] 没有焦虑
[ ] 没有职场抱怨
[ ] 没有逃离公司的恐慌感
[ ] 没有硬广感
[ ] 没有过度煽情
```

## Correct Emotional Direction

```text
Work ends.
Life begins again.
A small ordinary moment becomes meaningful.
```

---

# 12. Technical Quality Check（技术质量检查）

## Must Pass

```text
[ ] 视频清晰
[ ] 主体不糊
[ ] 脸部不崩
[ ] 手部不崩
[ ] 物体不严重变形
[ ] 没有明显闪烁
[ ] 没有严重画面撕裂
[ ] 没有跳帧影响观看
[ ] 没有字幕乱码
[ ] 没有错误文字
```

---

# 13. Review Result Levels（审片结果等级）

## PASS

可以进入剪辑阶段。

条件：

```text
角色稳定
动作自然
画面清晰
情绪正确
与上下镜头可衔接
```

---

## PASS WITH MINOR FIXES

可作为备用，或轻修后使用。

适用：

```text
轻微动作不稳
轻微光线不一致
轻微背景漂移
不影响 Jump 识别
不影响故事理解
```

---

## FAIL

不能使用，必须重新生成。

适用：

```text
Jump 角色错误
动作严重错误
镜头严重错误
风格严重偏离
场景无法衔接
品牌调性错误
```

---

# 14. Review Form Template（审片记录模板）

每个片段填写：

```text
Clip File:
SHOT-XXX-vXX.mp4

Shot:
Shot X — Name

Model:
Kling / Veo / Runway

Prompt Version:
v1 / v2 / v3

Generation Date:
TBD

Reviewer:
TBD

Character Check:
PASS / PASS WITH MINOR FIXES / FAIL

Motion Check:
PASS / PASS WITH MINOR FIXES / FAIL

Camera Check:
PASS / PASS WITH MINOR FIXES / FAIL

Lighting Check:
PASS / PASS WITH MINOR FIXES / FAIL

Environment Check:
PASS / PASS WITH MINOR FIXES / FAIL

Continuity Check:
PASS / PASS WITH MINOR FIXES / FAIL

Emotion Check:
PASS / PASS WITH MINOR FIXES / FAIL

Technical Quality:
PASS / PASS WITH MINOR FIXES / FAIL

Issues Found:
1.
2.
3.

Suggested Fix:
1.
2.
3.

Final Decision:
PASS / PASS WITH MINOR FIXES / FAIL

Can Enter Edit:
YES / NO / BACKUP ONLY
```

---

# 15. Shot-Specific Risk Map（镜头风险地图）

| Shot | Main Risk | Review Priority |
|---|---|---|
| Shot 1 | Face / desk realism | Character + lighting |
| Shot 2 | Expression / laptop close | Character + emotion |
| Shot 3 | Hands / object handling | Motion + technical quality |
| Shot 4 | Walking / foot sliding | Motion + camera |
| Shot 5 | Door opening / light transition | Motion + continuity |
| Shot 6 | Emotional ending / overexposure | Emotion + lighting |

---

# 16. Prompt Iteration Rule（Prompt 迭代规则）

如果片段 FAIL，不要直接随意重写 Prompt。

必须按问题类型修正：

## Character Drift

追加：

```text
Keep Jump exactly consistent with ASSET-001.
Do not change species, face shape, fur texture, body shape or outfit.
```

## Sliding Feet

追加：

```text
Grounded foot contact, realistic weight transfer, no sliding feet, natural walking mechanics.
```

## Camera Drift

追加：

```text
Stable eye-level 35mm camera, no FPS view, no drone orbit, no extreme wide-angle distortion.
```

## Lighting Drift

追加：

```text
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, no cyberpunk blue lighting.
```

## Environment Drift

追加：

```text
Keep TiaoTiao Studio Office consistent, warm modern creator workspace, laptop, keyboard, desk lamp, backpack and small plant.
```

---

# 17. Approved Clip Rule（通过片段规则）

只有满足以下条件的片段才能进入最终剪辑：

```text
[ ] Final Decision = PASS
[ ] 或 Final Decision = PASS WITH MINOR FIXES 且不影响故事
[ ] Character Check 不能是 FAIL
[ ] Motion Check 不能是 FAIL
[ ] Continuity Check 不能是 FAIL
[ ] Brand / Emotion 不能是 FAIL
```

---

# 18. Final Clip Selection Rule（最终片段选择规则）

如果同一镜头有多个 PASS 版本，优先选择：

```text
1. Jump 最稳定的版本
2. 动作最自然的版本
3. 与上下镜头最容易衔接的版本
4. 光线最符合整体的版本
5. 情绪最温暖的版本
6. 画面最清晰的版本
```

---

# 19. Next Production Action（下一步生产动作）

```text
1. Generate Shot 1 using VIDEO-PROMPTS.md.
2. Save output as SHOT-001-v01.mp4.
3. Generate 2–3 variations.
4. Review each variation using this guide.
5. Select approved Shot 1.
6. Repeat for Shot 2–6.
7. Store approved clips in production/PROJ-001/clips/approved/.
8. Continue to editing assembly.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial clip review guide |