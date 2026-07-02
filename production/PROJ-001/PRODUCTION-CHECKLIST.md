# PROJ-001 — Production Checklist（生产检查清单）

> Production Output（生产输出）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Command：COMMAND-001 / COMMAND-005  
> Workflow：WORKFLOW-001 / WORKFLOW-003 / WORKFLOW-004  
> Version：1.0  
> Status：Production Ready

---

# 1. Purpose（目的）

## 中文

本文件用于检查《跳跳下班啦》试播项目从生成视频片段、剪辑、封面、发布到复盘的完整生产流程。

它的作用是确保每一步都符合 TSOS Source of Truth，并避免在真实生产中出现：

- Jump 角色漂移
- 视频镜头不连续
- 动作滑步或漂浮
- 封面文字遮挡主体
- 发布文案标题党
- 品牌语气偏离
- 复盘数据缺失

## English

This file provides the production checklist for PROJ-001 — Jump After Work Pilot Project.

It ensures that every production step follows TSOS Source of Truth and remains ready for publishing.

---

# 2. Source of Truth（唯一事实来源）

本项目必须遵守：

```text
CHAR-001 — Jump
EP-001 — Jump After Work
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Jump After Work Pilot Project
```

必须遵守以下 Knowledge Nodes：

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

---

# 3. Production File Checklist（生产文件检查）

## Required Files

```text
[ ] production/PROJ-001/VIDEO-PROMPTS.md
[ ] production/PROJ-001/COVER-PACKAGE.md
[ ] production/PROJ-001/PUBLISHING-PACKAGE.md
[ ] production/PROJ-001/POST-PUBLISH-TRACKER.md
[ ] production/PROJ-001/PRODUCTION-CHECKLIST.md
```

## Optional Future Folders

```text
[ ] production/PROJ-001/clips/
[ ] production/PROJ-001/images/
[ ] production/PROJ-001/covers/
[ ] production/PROJ-001/final/
[ ] production/PROJ-001/review/
```

---

# 4. Pre-Generation Checklist（生成前检查）

开始生成视频前，必须确认：

```text
[ ] 已读取 VIDEO-PROMPTS.md
[ ] 已确认目标模型：Kling / Veo / Runway
[ ] 已确认画幅为 9:16
[ ] 已确认每个镜头单独生成
[ ] 已确认使用 Global Character Lock
[ ] 已确认使用 Global Negative Prompt
[ ] 已确认 Jump 必须参考 ASSET-001
[ ] 已确认不得改变 Jump 物种
[ ] 已确认不得去掉毛茸茸质感
[ ] 已确认不得改变程序员身份
[ ] 已确认不得使用赛博朋克 / 恐怖 / 游戏感风格
```

---

# 5. Shot Generation Checklist（逐镜头生成检查）

## Shot 1 — Work Ending

```text
[ ] Jump 坐在办公室桌前
[ ] 电脑屏幕有柔和暖光
[ ] Jump 手离开键盘
[ ] 情绪是工作结束后的轻松
[ ] 背包在附近可见
[ ] 没有夸张表演
[ ] 没有角色变形
```

## Shot 2 — Decision Moment

```text
[ ] Jump 看向窗外
[ ] 有温暖傍晚光
[ ] Jump 轻微微笑
[ ] Jump 关闭电脑
[ ] 情绪从工作切换到期待
[ ] 表情自然，不夸张
[ ] 电脑关闭状态可接 Shot 3
```

## Shot 3 — Packing Up

```text
[ ] 出现背包
[ ] 出现笔记本 / 耳机 / 电脑等工作物件
[ ] 手部动作自然
[ ] 拉链动作不变形
[ ] 桌面温暖干净但有生活感
[ ] 不像商业硬广摆拍
[ ] 背包状态可接 Shot 4
```

## Shot 4 — Walking Out

```text
[ ] Jump 背着背包
[ ] 自然走向出口
[ ] 脚步没有滑动
[ ] 身体没有漂浮
[ ] 尾巴轻微自然摆动
[ ] 镜头为平视跟拍
[ ] 没有 FPS / 游戏镜头感
[ ] 办公室环境保持一致
```

## Shot 5 — Door Exit

```text
[ ] Jump 到达办公室门口
[ ] 自然开门
[ ] 室内暖光过渡到门外金色光
[ ] 动作不夸张
[ ] 没有“逃离公司”的戏剧感
[ ] 门外光不过曝
[ ] 可接 Shot 6
```

## Shot 6 — Warm Ending

```text
[ ] Jump 在下班后的暖光中停留
[ ] 情绪安静温暖
[ ] 尾巴自然轻微动作
[ ] 画面有结尾感
[ ] 没有商业摆拍
[ ] 没有过度口号感
[ ] 可添加最终字幕：下班啦，生活开始啦。
```

---

# 6. Clip Review Checklist（视频片段检查）

每个生成片段都必须检查：

```text
[ ] Jump 是否仍然是拟人化毛茸茸小狗
[ ] Jump 是否保持女性角色设定
[ ] Jump 是否保持程序员身份
[ ] Jump 是否保持苗条体型
[ ] Jump 毛发是否稳定
[ ] Jump 服装是否稳定
[ ] Fire Dragon Fruit Pink 是否作为点缀出现
[ ] Jump 是否没有变成人类
[ ] Jump 是否没有变成其他动物
[ ] Jump 是否没有肌肉化
[ ] 动作是否自然
[ ] 脚步是否没有滑动
[ ] 身体是否没有漂浮
[ ] 镜头是否自然可信
[ ] 灯光是否温暖
[ ] 场景是否符合 ENV-001
[ ] 风格是否符合 STYLE-001
[ ] 情绪是否符合 EMOTION-001
```

---

# 7. Clip Approval Rule（片段通过规则）

## PASS

可以进入剪辑阶段：

```text
Jump 角色稳定
动作自然
画面清晰
情绪正确
可接上下镜头
```

## PASS WITH MINOR FIXES

可作为备用片段：

```text
轻微动作问题
轻微光线问题
轻微环境不稳定
不影响核心角色识别
```

## FAIL

不能进入剪辑阶段：

```text
Jump 变成人类
Jump 变成其他动物
脚步严重滑动
身体漂浮
脸部严重变形
风格变成赛博朋克 / 恐怖 / 游戏感
品牌语气明显偏离
```

---

# 8. Editing Checklist（剪辑检查）

进入剪辑阶段前，必须确认：

```text
[ ] 已选择每个 Shot 的最佳版本
[ ] Shot 1–6 顺序正确
[ ] 镜头之间动作连续
[ ] 背包状态连续
[ ] 电脑状态连续
[ ] 门口状态连续
[ ] 光线过渡自然
[ ] 视频总时长约 45 秒
[ ] 开头 3 秒能看懂工作结束
[ ] 结尾有情绪停留
```

---

# 9. Caption Checklist（字幕检查）

```text
[ ] 字幕不遮挡 Jump 的脸
[ ] 字幕不遮挡关键手部动作
[ ] 字幕放在安全区
[ ] 字幕简洁，不超过画面承载
[ ] 字幕节奏和镜头节奏一致
[ ] 字幕语气符合 BRAND-001
[ ] 字幕不制造焦虑
[ ] 字幕不标题党
```

## Recommended Caption Sequence

```text
今天的代码写完了

电脑一关，生活上线

想出去走走

不远，也可以是冒险

把时间还给自己一点点

下班啦，生活开始啦
```

---

# 10. Music / Sound Checklist（音乐音效检查）

```text
[ ] 音乐符合 MUSIC-001
[ ] 音乐温暖、轻松、生活方式感
[ ] 音乐不压过画面情绪
[ ] 环境音不过度嘈杂
[ ] 键盘声自然
[ ] 电脑关闭声自然
[ ] 背包拉链声自然
[ ] 脚步声自然
[ ] 开门声自然
[ ] 结尾音乐有轻微情绪落点
```

---

# 11. Cover Checklist（封面检查）

```text
[ ] 封面比例为 9:16
[ ] 封面至少 1080 × 1920 px
[ ] Jump 清晰
[ ] Jump 没有变形
[ ] Jump 没有被文字遮挡脸部
[ ] 文字在 3:4 安全区内
[ ] 主标题清晰
[ ] 副标题简短
[ ] 背景不杂乱
[ ] 色彩符合 COLOR-001
[ ] 风格符合 STYLE-001
[ ] 情绪符合 EMOTION-001
[ ] 品牌语气符合 BRAND-001
```

## Recommended Cover Text

```text
主标题：
电脑一关

副标题：
生活上线
```

---

# 12. Publishing Checklist（发布检查）

```text
[ ] 标题已确认
[ ] 正文已确认
[ ] 标签已确认
[ ] 封面已确认
[ ] 视频文件已导出
[ ] 封面文件已导出
[ ] 发布时间已确认
[ ] 发布平台已确认
[ ] 发布记录已填写
[ ] 发布后复盘表已准备
```

## Recommended First Publish

```text
Platform:
小红书

Title:
电脑一关，生活上线

Cover Text:
电脑一关 / 生活上线

Publish Time:
20:30
```

---

# 13. Final Export Checklist（最终导出检查）

```text
[ ] Final video aspect ratio：9:16
[ ] Final video resolution：1080 × 1920 or higher
[ ] Final video duration：約 45s
[ ] Final video format：MP4
[ ] Final cover format：JPG / PNG
[ ] Final cover resolution：1080 × 1920 or higher
[ ] File name is clear
[ ] Files are stored in production/PROJ-001/final/
```

## Recommended File Names

```text
production/PROJ-001/final/PROJ-001-final-video.mp4
production/PROJ-001/final/PROJ-001-cover.jpg
```

---

# 14. COMMAND-005 Final Check（最终一致性检查）

发布前必须运行：

```text
COMMAND-005 — Run Consistency Check
```

检查对象：

```text
Final Video
Final Cover
Publishing Package
```

## Final Check Items

```text
[ ] Character Consistency
[ ] World Consistency
[ ] Visual Style Consistency
[ ] Color Consistency
[ ] Emotion Consistency
[ ] Motion Consistency
[ ] Camera Consistency
[ ] Lighting Consistency
[ ] Story / Brand Consistency
[ ] Publishing Safety
```

## Required Result

```text
PASS
```

或：

```text
PASS WITH MINOR FIXES
```

如果结果是：

```text
FAIL
```

则不能发布。

---

# 15. Post-Publish Checklist（发布后检查）

发布后必须记录：

```text
[ ] 发布时间
[ ] 发布链接
[ ] 首小时数据
[ ] 24 小时数据
[ ] 72 小时数据
[ ] 一周数据
[ ] 评论区代表反馈
[ ] 用户是否理解 Jump
[ ] 用户是否理解系列方向
[ ] 是否值得继续做 EP-002
```

---

# 16. Production Decision（生产决策）

## Ready to Generate Clips

```text
YES
```

## Ready to Edit

```text
Only after approved clips are selected.
```

## Ready to Publish

```text
Only after final COMMAND-005 check passes.
```

---

# 17. Final Production Status（最终生产状态）

```text
Production Status:
Ready for real video generation

Next Required Action:
Generate Shot 1–6 clips using VIDEO-PROMPTS.md
```

---

# 18. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial production checklist |