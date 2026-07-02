# PROJ-001 — Shot Review Template（单镜头审片记录模板）

> Production Review Template（生产审片模板）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Command：COMMAND-005  
> Workflow：WORKFLOW-003  
> Version：1.0  
> Status：Review Ready

---

# 1. Purpose（目的）

## 中文

本文件用于记录《跳跳下班啦》每一个真实生成视频片段的审片结果。

每次生成一个视频片段，都应该复制本模板，填写对应镜头的检查结果。

它的作用是：

- 记录每个版本是否可用
- 记录角色、动作、镜头、灯光、场景问题
- 判断是否可以进入剪辑
- 记录 Prompt 需要如何迭代
- 保证最终入选片段符合 TSOS Source of Truth

## English

This file is the review template for each generated video clip of PROJ-001.

Each generated shot version should be reviewed using this template before entering the editing stage.

---

# 2. Review File Naming Rule（审片文件命名规则）

每个片段建议建立独立审片文件：

```text
production/PROJ-001/review/SHOT-001-v01-review.md
production/PROJ-001/review/SHOT-001-v02-review.md
production/PROJ-001/review/SHOT-001-v03-review.md

production/PROJ-001/review/SHOT-002-v01-review.md
production/PROJ-001/review/SHOT-002-v02-review.md
production/PROJ-001/review/SHOT-002-v03-review.md
```

通过审片的最终版本可以建立：

```text
production/PROJ-001/review/SHOT-001-approved-review.md
```

---

# 3. Clip Basic Info（片段基础信息）

```text
Clip File:
TBD

Shot:
TBD

Shot Name:
TBD

Model:
Jimeng / 即梦 / Veo / Runway / Other

Prompt Source:
production/PROJ-001/VIDEO-PROMPTS.md

Prompt Version:
v1 / v2 / v3 / custom

Generation Date:
TBD

Reviewer:
TBD

Review Date:
TBD
```

---

# 4. Source of Truth（唯一事实来源）

本片段必须符合：

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

# 5. Shot Intent（镜头意图）

填写本镜头原本应该完成的叙事功能。

```text
Expected Story Function:
TBD

Expected Action:
TBD

Expected Emotion:
TBD

Expected Continuity:
TBD
```

---

# 6. Character Check（角色检查）

## Checklist

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

## Character Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Character Issues

```text
1.
2.
3.
```

---

# 7. Motion Check（动作检查）

## Checklist

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

## Motion Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Motion Issues

```text
1.
2.
3.
```

---

# 8. Camera Check（镜头检查）

## Checklist

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

## Camera Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Camera Issues

```text
1.
2.
3.
```

---

# 9. Lighting Check（灯光检查）

## Checklist

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

## Lighting Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Lighting Issues

```text
1.
2.
3.
```

---

# 10. Environment Check（环境检查）

## Checklist

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

## Environment Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Environment Issues

```text
1.
2.
3.
```

---

# 11. Continuity Check（连续性检查）

## Checklist

```text
[ ] 与上一镜头状态可以衔接
[ ] 与下一镜头状态可以衔接
[ ] 电脑状态正确
[ ] 背包状态正确
[ ] Jump 移动方向正确
[ ] 光线变化合理
[ ] 空间关系合理
[ ] 角色位置没有瞬移感
```

## Continuity Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Continuity Issues

```text
1.
2.
3.
```

---

# 12. Emotion Check（情绪检查）

## Checklist

```text
[ ] 情绪温暖
[ ] 情绪轻松
[ ] 有下班后的自由感
[ ] 没有焦虑
[ ] 没有职场抱怨
[ ] 没有逃离公司的恐慌感
[ ] 没有硬广感
[ ] 没有过度煽情
```

## Emotion Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Emotion Issues

```text
1.
2.
3.
```

---

# 13. Technical Quality Check（技术质量检查）

## Checklist

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

## Technical Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Technical Issues

```text
1.
2.
3.
```

---

# 14. Shot-Specific Notes（镜头专项备注）

根据当前镜头填写专项检查。

## Shot 1 — Work Ending

```text
[ ] 电脑是否打开
[ ] 手是否离开键盘
[ ] 表情是否是轻松而不是夸张
[ ] 桌面是否温暖真实
```

## Shot 2 — Decision Moment

```text
[ ] 是否有看向窗外
[ ] 是否有轻微微笑
[ ] 是否自然关闭电脑
[ ] 情绪是否从工作切换到期待
```

## Shot 3 — Packing Up

```text
[ ] 背包是否出现
[ ] 手部动作是否自然
[ ] 物件是否没有严重变形
[ ] 背包状态是否可接 Shot 4
```

## Shot 4 — Walking Out

```text
[ ] 脚步是否贴地
[ ] 是否没有滑步
[ ] 背包是否稳定
[ ] 跟拍镜头是否自然
```

## Shot 5 — Door Exit

```text
[ ] 门是否自然打开
[ ] 光线过渡是否自然
[ ] 是否没有逃离公司的戏剧感
[ ] 是否可接 Shot 6
```

## Shot 6 — Warm Ending

```text
[ ] 情绪是否温暖安静
[ ] 光线是否不过曝
[ ] 画面是否有结尾感
[ ] 是否适合加最终字幕
```

---

# 15. Issue Severity（问题严重级别）

## Critical

```text
角色身份错误
Jump 变成人类
Jump 变成其他动物
严重变形
动作严重错误
风格严重偏离
无法进入剪辑
```

## Major

```text
动作不够自然
光线明显不一致
场景漂移明显
角色局部不稳定
影响镜头衔接
```

## Minor

```text
轻微背景变化
轻微动作不稳
轻微构图问题
轻微光线偏差
不影响核心理解
```

---

# 16. Issue List（问题列表）

| Severity | Area | Issue | Suggested Fix |
|---|---|---|---|
| Critical / Major / Minor | Character / Motion / Camera / Lighting / Environment / Continuity / Emotion / Technical | TBD | TBD |

---

# 17. Prompt Fix Suggestion（Prompt 修正建议）

## If Character Drift

```text
Add:
Keep Jump exactly consistent with ASSET-001. Do not change species, face shape, fur texture, body shape or outfit.
```

## If Sliding Feet

```text
Add:
Grounded foot contact, realistic weight transfer, no sliding feet, natural walking mechanics.
```

## If Camera Drift

```text
Add:
Stable eye-level 35mm camera, no FPS view, no drone orbit, no extreme wide-angle distortion.
```

## If Lighting Drift

```text
Add:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, no cyberpunk blue lighting.
```

## If Environment Drift

```text
Add:
Keep TiaoTiao Studio Office consistent, warm modern creator workspace, laptop, keyboard, desk lamp, backpack and small plant.
```

## Custom Fix

```text
TBD
```

---

# 18. Final Decision（最终决定）

## Result

```text
PASS / PASS WITH MINOR FIXES / FAIL
```

## Can Enter Edit

```text
YES / NO / BACKUP ONLY
```

## Reason

```text
TBD
```

## Next Action

```text
Use as approved clip / Keep as backup / Regenerate with revised prompt
```

---

# 19. Approved Clip Info（通过片段信息）

如果该片段通过，填写：

```text
Approved Clip File:
production/PROJ-001/clips/approved/SHOT-XXX-approved.mp4

Approved Reason:
TBD

Notes for Editor:
TBD
```

---

# 20. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial shot review template |
