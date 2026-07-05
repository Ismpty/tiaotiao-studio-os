# PROJ-001 — Production Runbook（生产运行手册）

> Production Runtime Manual（生产运行手册）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Toolchain：Jimeng / 即梦 + CapCut / 剪映专业版  
> Version：1.0  
> Status：Runtime Ready

---

# 1. Purpose（目的）

## 中文

本文件是 PROJ-001 — Jump After Work Pilot Project 的实际生产运行手册。

它的目标是让你可以按照固定顺序完成第一条《跳跳下班啦》短视频：

```text
生成视频片段
↓
审片
↓
迭代 Prompt
↓
选片
↓
剪辑
↓
加字幕
↓
加音乐音效
↓
导出
↓
发布
↓
复盘
```

本文件不重新定义角色、故事或风格，只负责告诉你实际怎么操作。

---

# 2. Default Toolchain（默认工具链）

```text
Video Generation:
Jimeng / 即梦

Backup Video Generation:
Veo / Runway

Editing:
CapCut / 剪映专业版

Caption:
CapCut / 剪映手动添加

Cover:
ChatGPT Image / Midjourney / Flux

Review:
COMMAND-005 + review files

Publishing:
小红书 first
```

---

# 3. Source Files（生产来源文件）

开始生产前，先确认以下文件已经存在：

```text
production/PROJ-001/VIDEO-PROMPTS.md
production/PROJ-001/COVER-PACKAGE.md
production/PROJ-001/PUBLISHING-PACKAGE.md
production/PROJ-001/POST-PUBLISH-TRACKER.md
production/PROJ-001/PRODUCTION-CHECKLIST.md
production/PROJ-001/review/CLIP-REVIEW-GUIDE.md
production/PROJ-001/review/SHOT-REVIEW-TEMPLATE.md
production/PROJ-001/review/ITERATION-LOG.md
production/PROJ-001/review/FINAL-CLIP-SELECTION.md
production/PROJ-001/editing/EDITING-ASSEMBLY.md
production/PROJ-001/editing/CAPTION-TIMING.md
production/PROJ-001/editing/MUSIC-SOUND.md
production/PROJ-001/final/FINAL-EXPORT-CHECKLIST.md
```

---

# 4. Required Folders（必需文件夹）

正式生成真实资产前，建议创建以下文件夹：

```text
production/PROJ-001/clips/
production/PROJ-001/clips/approved/
production/PROJ-001/images/
production/PROJ-001/covers/
production/PROJ-001/final/
production/PROJ-001/review/
production/PROJ-001/editing/
```

命令：

```bash
mkdir -p production/PROJ-001/clips
mkdir -p production/PROJ-001/clips/approved
mkdir -p production/PROJ-001/images
mkdir -p production/PROJ-001/covers
mkdir -p production/PROJ-001/final
mkdir -p production/PROJ-001/review
mkdir -p production/PROJ-001/editing
```

---

# 5. Production Overview（生产总流程）

## Step 1 — Generate Shot 1–6 in Jimeng

```text
使用 production/PROJ-001/VIDEO-PROMPTS.md
复制每个 Shot 的 Jimeng Prompt
在即梦中逐镜头生成
每个镜头生成 2–3 个版本
```

---

## Step 2 — Save Generated Clips

推荐命名：

```text
production/PROJ-001/clips/SHOT-001-v01.mp4
production/PROJ-001/clips/SHOT-001-v02.mp4
production/PROJ-001/clips/SHOT-001-v03.mp4

production/PROJ-001/clips/SHOT-002-v01.mp4
production/PROJ-001/clips/SHOT-002-v02.mp4
production/PROJ-001/clips/SHOT-002-v03.mp4
```

---

## Step 3 — Review Each Clip

每个片段都用：

```text
production/PROJ-001/review/SHOT-REVIEW-TEMPLATE.md
```

复制一份生成审片文件。

示例：

```text
production/PROJ-001/review/SHOT-001-v01-review.md
```

---

## Step 4 — Update Iteration Log

每生成 / 审片 / 失败 / 迭代一次，都更新：

```text
production/PROJ-001/review/ITERATION-LOG.md
```

---

## Step 5 — Select Approved Clips

通过审片的片段复制到：

```text
production/PROJ-001/clips/approved/
```

推荐命名：

```text
SHOT-001-approved.mp4
SHOT-002-approved.mp4
SHOT-003-approved.mp4
SHOT-004-approved.mp4
SHOT-005-approved.mp4
SHOT-006-approved.mp4
```

---

## Step 6 — Fill Final Clip Selection

填写：

```text
production/PROJ-001/review/FINAL-CLIP-SELECTION.md
```

确认 6 个镜头都可以进入剪辑。

---

## Step 7 — Edit in CapCut

使用：

```text
production/PROJ-001/editing/EDITING-ASSEMBLY.md
```

在剪映专业版中按时间线组装。

---

## Step 8 — Add Captions

使用：

```text
production/PROJ-001/editing/CAPTION-TIMING.md
```

添加字幕。

---

## Step 9 — Add Music and Sound

使用：

```text
production/PROJ-001/editing/MUSIC-SOUND.md
```

添加音乐和轻音效。

---

## Step 10 — Export Final Video

使用：

```text
production/PROJ-001/final/FINAL-EXPORT-CHECKLIST.md
```

导出最终视频和封面。

---

## Step 11 — Publish

使用：

```text
production/PROJ-001/PUBLISHING-PACKAGE.md
```

首发小红书。

---

## Step 12 — Track Performance

发布后填写：

```text
production/PROJ-001/POST-PUBLISH-TRACKER.md
```

---

# 6. Jimeng Generation Runtime（即梦生成流程）

## Open Jimeng

```text
1. 打开即梦。
2. 进入视频生成。
3. 选择图生视频或文生视频，按你当前素材情况决定。
4. 首版建议使用文生视频测试每个 Shot。
5. 每个 Shot 单独生成，不要一次生成完整 45 秒。
```

---

## Generate Shot 1

使用文件：

```text
production/PROJ-001/VIDEO-PROMPTS.md
```

复制：

```text
Shot 1 — Work Ending
Jimeng Prompt
```

生成：

```text
SHOT-001-v01
SHOT-001-v02
SHOT-001-v03
```

保存：

```text
production/PROJ-001/clips/SHOT-001-v01.mp4
production/PROJ-001/clips/SHOT-001-v02.mp4
production/PROJ-001/clips/SHOT-001-v03.mp4
```

---

## Review Shot 1

复制模板：

```text
production/PROJ-001/review/SHOT-REVIEW-TEMPLATE.md
```

生成审片文件：

```text
production/PROJ-001/review/SHOT-001-v01-review.md
```

检查重点：

```text
[ ] Jump 是否稳定
[ ] 毛茸茸质感是否稳定
[ ] 手是否自然离开键盘
[ ] 电脑是否打开
[ ] 工作结束情绪是否成立
[ ] 灯光是否温暖
```

---

## Repeat for Shot 2–6

按顺序生成：

```text
Shot 1 — Work Ending
Shot 2 — Decision Moment
Shot 3 — Packing Up
Shot 4 — Walking Out
Shot 5 — Door Exit
Shot 6 — Warm Ending
```

生成顺序不要跳过 Shot 4 和 Shot 5 的审片，因为这两个动作风险最高。

---

# 7. Shot Risk Priority（镜头风险优先级）

| Shot | Risk Level | Main Risk |
|---|---|---|
| Shot 1 | Medium | 脸部 / 桌面真实感 |
| Shot 2 | Medium | 表情 / 关电脑动作 |
| Shot 3 | High | 手部 / 物件变形 |
| Shot 4 | Very High | 行走 / 滑步 / 跟拍 |
| Shot 5 | Very High | 开门 / 光线转换 / 连续性 |
| Shot 6 | Medium | 情绪 / 过曝 / 结尾感 |

优先多生成版本：

```text
Shot 4
Shot 5
Shot 3
```

---

# 8. Prompt Iteration Rule（Prompt 迭代规则）

如果即梦生成失败，不要整段重写 Prompt。

按问题局部追加修正句。

## Character Drift

```text
Add:
Keep Jump as a fluffy real dog-form character wearing programmer-style dog clothes. Maintain four-legged dog anatomy, dog proportions, soft realistic fur texture, outfit continuity and Fire Dragon Fruit Pink accents throughout the entire clip.
```

## Sliding Feet

```text
Add:
Grounded foot contact, realistic weight transfer, natural walking mechanics, feet stay connected to the floor, no sliding feet, no floating body.
```

## Hand Distortion

```text
Add:
Simplify hand movement, natural object handling, clear hand position, no melting fingers, no extra fingers, no distorted paws or hands.
```

## Door Problem

```text
Add:
Simple natural door opening action, one clear hand reaches the door handle, door opens smoothly, no object morphing, no hand distortion.
```

## Lighting Drift

```text
Add:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows, no cyberpunk blue lighting, no horror contrast, no over-saturated RGB.
```

---

# 9. Approval Gate（通过门槛）

片段进入剪辑前必须满足：

```text
[ ] Character Check 不是 FAIL
[ ] Motion Check 不是 FAIL
[ ] Continuity Check 不是 FAIL
[ ] Emotion Check 不是 FAIL
[ ] Technical Quality 不是 FAIL
```

允许：

```text
PASS
PASS WITH MINOR FIXES
```

禁止：

```text
FAIL
```

---

# 10. CapCut Editing Runtime（剪映剪辑流程）

## Create Project

```text
1. 打开剪映专业版。
2. 新建项目。
3. 设置画幅：9:16。
4. 导入 approved clips。
5. 按 Shot 1–6 顺序放入时间线。
```

---

## Timeline

```text
0:00–0:06
Shot 1 — Work Ending

0:06–0:12
Shot 2 — Decision Moment

0:12–0:19
Shot 3 — Packing Up

0:19–0:29
Shot 4 — Walking Out

0:29–0:37
Shot 5 — Door Exit

0:37–0:45
Shot 6 — Warm Ending
```

---

## Transitions

推荐：

```text
直接剪切
动作点剪切
自然软切
光线转场
```

禁止：

```text
旋转转场
快闪转场
综艺转场
夸张缩放
模板化转场
```

---

# 11. Caption Runtime（字幕执行）

使用主字幕：

```text
今天的代码写完了

电脑一关，生活上线

想出去走走

不远，也可以是冒险

把时间还给自己一点点

下班啦，生活开始啦
```

字幕位置：

```text
下方偏中
3:4 安全区内
不遮挡 Jump 脸部
不遮挡手部动作
不遮挡脚步
```

---

# 12. Music Runtime（音乐执行）

第一版推荐：

```text
音乐 + 轻音效 + 字幕
```

旁白：

```text
Optional
```

首版建议：

```text
先不加旁白
```

原因：

```text
避免过度解释。
先验证 Jump 角色和画面情绪是否成立。
```

音乐方向：

```text
Warm lo-fi
Light acoustic
Soft indie pop instrumental
Gentle piano texture
Warm lifestyle beat
```

---

# 13. Sound Effects Runtime（音效执行）

可以轻微添加：

```text
keyboard typing
laptop closing
backpack zipper
soft footsteps
door opening
soft evening ambience
```

音效原则：

```text
轻
自然
不抢戏
不综艺
不广告
```

---

# 14. Cover Runtime（封面执行）

使用：

```text
production/PROJ-001/COVER-PACKAGE.md
```

推荐封面：

```text
Variation A — Warm Exit
```

推荐文字：

```text
主标题：
电脑一关

副标题：
生活上线
```

制作方式：

```text
1. 先生成无文字封面。
2. 选 Jump 最稳定的一张。
3. 在设计软件 / 剪映 / Canva 中手动加中文文字。
4. 确认文字在 3:4 安全区内。
5. 导出 1080 × 1920。
```

---

# 15. Final Export Runtime（最终导出流程）

使用：

```text
production/PROJ-001/final/FINAL-EXPORT-CHECKLIST.md
```

导出：

```text
production/PROJ-001/final/PROJ-001-final-video.mp4
production/PROJ-001/final/PROJ-001-cover.jpg
production/PROJ-001/final/PROJ-001-publishing-copy.txt
```

规格：

```text
9:16
1080 × 1920 or higher
MP4
H.264 / H.265
Around 45 seconds
Stereo audio
```

---

# 16. Final COMMAND-005 Gate（最终一致性关卡）

发布前必须检查：

```text
Final Video
Final Cover
Caption Text
Publishing Copy
Music / Sound Direction
```

允许发布：

```text
PASS
PASS WITH MINOR FIXES
```

禁止发布：

```text
FAIL
```

如果 FAIL：

```text
1. 不发布。
2. 找到失败项。
3. 回到对应文件修正。
4. 重新导出。
5. 再运行 COMMAND-005。
```

---

# 17. Publishing Runtime（发布流程）

首发平台：

```text
小红书
```

推荐发布时间：

```text
20:30
```

标题：

```text
电脑一关，生活上线
```

正文：

```text
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

今天的跳跳，下班后也认真生活了。

不是一定要去很远的地方，
有时候，走出办公室的那一刻，
生活就已经重新开始了。

下班啦，生活开始啦。
```

标签：

```text
#跳跳下班啦
#下班后的生活
#治愈系短片
#AI动画
#生活方式
#程序员日常
#原创IP
```

---

# 18. Post-Publish Runtime（发布后复盘）

发布后填写：

```text
production/PROJ-001/POST-PUBLISH-TRACKER.md
```

记录：

```text
24 小时数据
72 小时数据
一周数据
评论反馈
用户是否理解 Jump
用户是否理解《跳跳下班啦》
是否值得继续 EP-002
```

---

# 19. First Real Action（第一个真实动作）

现在真正开始生产时，第一个动作是：

```text
Generate Shot 1 — Work Ending in Jimeng / 即梦.
```

使用：

```text
production/PROJ-001/VIDEO-PROMPTS.md
```

复制：

```text
Shot 1 — Work Ending
Jimeng Prompt
```

生成：

```text
SHOT-001-v01
SHOT-001-v02
SHOT-001-v03
```

然后审片。

---

# 20. Runtime Summary（运行总结）

```text
Jimeng generates clips.
TSOS reviews clips.
CapCut assembles clips.
TSOS checks final video.
小红书 publishes first.
Tracker records results.
```

---

# 21. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial production runbook |
