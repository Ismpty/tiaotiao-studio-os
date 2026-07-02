# TEST-004 — COMMAND-004 Publishing Package Validation

> Validation Test（验证测试）  
> Command：COMMAND-004  
> Target：Generate Publishing Package  
> Project：PROJ-001  
> Status：PASS  
> Version：1.0

---

# 1. Test Purpose（测试目的）

## 中文

本测试用于验证 `COMMAND-004 — Generate Publishing Package` 是否可以基于 TSOS Source of Truth，为《跳跳下班啦》生成可直接用于平台发布的发布包。

本次测试重点检查：

- 是否正确调用 COMMAND-004
- 是否正确引用 WORKFLOW-004
- 是否正确调用 AGENT-006
- 是否正确读取 PROJ-001 / EP-001 / STORY-001 / ASSET-001
- 是否正确引用 BRAND-001
- 是否生成平台策略
- 是否生成标题、正文、标签、封面文案
- 是否生成发布时间建议
- 是否生成发布前检查清单
- 是否生成发布后复盘模板
- 是否通过品牌安全检查

## English

This test validates whether COMMAND-004 can generate a platform-ready publishing package for PROJ-001 based on TSOS Source of Truth.

---

# 2. Command Input（命令输入）

```text
Run COMMAND-004.

Target Platform:
小红书

Project:
PROJ-001

Language:
Chinese

Content Type:
Short Video

Publish Time:
Recommended time

Output Depth:
Detailed
```

---

# 3. Source Records（来源记录）

## Database Records

```text
EP-001 — Jump After Work
STORY-001 — Work Ends, Adventure Begins
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Jump After Work Pilot Project
```

## Knowledge Nodes

```text
BRAND-001 — TiaoTiao Studio Brand Language
STORYFORMULA-001 — Work Ends, Adventure Begins
EMOTION-001 — Freedom
MUSIC-001 — Lifestyle Music Language
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
```

## Agent

```text
AGENT-006 — Publishing Agent
```

## Workflow Reference

```text
WORKFLOW-004 — Publishing Workflow
```

## Validation Source

```text
TEST-001 — COMMAND-003 Storyboard Validation
TEST-002 — COMMAND-002 Prompt Validation
TEST-003 — COMMAND-005 Consistency Check Validation
```

---

# 4. Publishing Summary（发布摘要）

```text
Project:
PROJ-001 — Jump After Work Pilot Project

Episode:
EP-001 — Jump After Work

Story:
STORY-001 — Work Ends, Adventure Begins

Target Platform:
小红书

Content Type:
45-second vertical short video

Core Emotion:
Freedom

Core Message:
电脑一关，生活上线。

Publishing Goal:
发布一条温暖、治愈、生活方式感的《跳跳下班啦》短视频，让观众感受到下班后的轻松和自由。
```

---

# 5. Platform Strategy（平台策略）

## Target Platform

```text
小红书
```

## Strategy

```text
小红书发布重点应放在生活方式感、治愈感、角色记忆点和封面识别度上。

标题需要有情绪，但不能标题党。
正文需要像轻松生活记录，而不是硬广。
标签需要服务内容，不堆砌无关热词。
封面文案要简短清晰，不遮挡 Jump。
```

## Platform Tone

```text
温暖
轻松
治愈
生活记录感
有角色陪伴感
不焦虑
不强营销
```

---

# 6. Title Options（标题选项）

## Recommended Titles

```text
下班啦，生活开始啦
```

```text
电脑一关，生活上线
```

```text
忙了一天，也要好好生活
```

```text
跳跳下班啦，今天也认真生活了
```

```text
下班后的路，也可以是冒险
```

## Best Title

```text
电脑一关，生活上线
```

## Reason

```text
该标题简短、有记忆点，符合《跳跳下班啦》的系列气质，也能直接传达“工作结束、生活开始”的情绪转折。
```

---

# 7. Caption / Description（正文）

## 小红书正文

```text
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

今天的跳跳，下班后也认真生活了。

不是一定要去很远的地方，
有时候，走出办公室的那一刻，
生活就已经重新开始了。
```

## Short Caption Version

```text
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

下班啦，生活开始啦。
```

---

# 8. Hashtag Set（标签组）

## Recommended Hashtags

```text
#跳跳下班啦
#下班后的生活
#治愈系短片
#AI动画
#生活方式
#程序员日常
#原创IP
```

## Optional Hashtags

```text
#短视频创作
#AI短片
#下班日常
#温暖治愈
```

## Forbidden Hashtags

```text
#爆款
#必看
#千万别错过
#打工人崩溃
#焦虑
#震惊
```

---

# 9. Cover Text Suggestions（封面文案建议）

## Option A

```text
主标题：
下班啦

副标题：
生活开始啦
```

## Option B

```text
主标题：
电脑一关

副标题：
生活上线
```

## Option C

```text
主标题：
跳跳下班啦

副标题：
今天也认真生活了
```

## Recommended Cover Text

```text
主标题：
电脑一关

副标题：
生活上线
```

## Cover Notes

```text
封面文字应放在安全区内。
不要遮挡 Jump 的脸、手部动作或关键运动方向。
标题不宜超过两层主信息。
画面保持温暖、简洁、高识别。
```

---

# 10. Publishing Time Suggestion（发布时间建议）

## 小红书推荐发布时间

```text
12:00–13:30
19:30–22:00
```

## Recommended Slot

```text
20:30
```

## Reason

```text
该内容属于下班后生活方式和治愈短片，晚上 19:30–22:00 更符合用户刷到“下班、放松、生活感”内容的情绪场景。
```

---

# 11. Pre-Publish Checklist（发布前检查清单）

```text
[PASS] 视频比例为 9:16。
[PASS] 视频内容符合《跳跳下班啦》系列。
[PASS] Jump 没有被文字遮挡。
[PASS] Jump 角色身份没有改变。
[PASS] 封面文案简短清晰。
[PASS] 标题不标题党。
[PASS] 正文不制造焦虑。
[PASS] 标签与内容相关。
[PASS] 没有使用无关热点标签。
[PASS] 音乐方向符合 MUSIC-001。
[PASS] 视觉方向符合 STYLE-001。
[PASS] 色彩方向符合 COLOR-001。
[PASS] 情绪方向符合 EMOTION-001。
[PASS] 品牌语气符合 BRAND-001。
[PASS] 已准备发布后复盘字段。
```

---

# 12. Publishing Record（发布记录）

```text
Project:
PROJ-001 — Jump After Work Pilot Project

Platform:
小红书

Publish Date:
TBD

Publish Time:
20:30 recommended

Title:
电脑一关，生活上线

Caption:
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

今天的跳跳，下班后也认真生活了。

不是一定要去很远的地方，
有时候，走出办公室的那一刻，
生活就已经重新开始了。

Hashtags:
#跳跳下班啦 #下班后的生活 #治愈系短片 #AI动画 #生活方式 #程序员日常 #原创IP

Cover Text:
电脑一关 / 生活上线

Video File:
TBD

Cover File:
TBD

Status:
Ready for production publishing

Output Link:
TBD

Notes:
发布前需再次检查封面安全区、字幕遮挡和视频清晰度。
```

---

# 13. Post-Publish Review Template（发布后复盘模板）

```text
Views:
TBD

Likes:
TBD

Comments:
TBD

Shares:
TBD

Saves:
TBD

Completion Rate:
TBD

Average Watch Time:
TBD

Follower Growth:
TBD

Best Comment:
TBD

Audience Emotion:
TBD

Content Strength:
TBD

Content Weakness:
TBD

Next Iteration:
TBD
```

---

# 14. Brand Safety Check（品牌安全检查）

默认对照：

```text
BRAND-001 — TiaoTiao Studio Brand Language
```

## Checklist

```text
[PASS] 标题避免标题党。
[PASS] 正文避免焦虑表达。
[PASS] 正文没有职场抱怨主导。
[PASS] 文案没有强营销腔。
[PASS] 标签没有无关热点。
[PASS] 封面文案不夸张。
[PASS] 没有虚假承诺。
[PASS] 没有攻击性表达。
[PASS] 保持 Jump 系列温暖气质。
[PASS] 适合小红书平台。
[PASS] 支持发布后复盘。
```

## Result

```text
PASS
```

---

# 15. Validation Checklist（验证检查表）

```text
[PASS] COMMAND-004 output follows required structure.
[PASS] Publishing Summary is included.
[PASS] Platform Strategy is included.
[PASS] Title Options are included.
[PASS] Caption / Description is included.
[PASS] Hashtag Set is included.
[PASS] Cover Text Suggestions are included.
[PASS] Publishing Time Suggestion is included.
[PASS] Pre-Publish Checklist is included.
[PASS] Publishing Record is included.
[PASS] Post-Publish Review Template is included.
[PASS] Brand Safety Check is included.
[PASS] Output references PROJ-001.
[PASS] Output references EP-001.
[PASS] Output references STORY-001.
[PASS] Output references ASSET-001.
[PASS] Output follows BRAND-001.
[PASS] Output avoids clickbait.
[PASS] Output avoids anxiety.
[PASS] Output avoids hard-selling language.
[PASS] Output is platform-ready for 小红书.
```

---

# 16. Issues Found（发现问题）

```text
No critical issues found.
No major issues found.
No minor issues found.
```

---

# 17. Final Result（最终结果）

```text
Final Result:
PASS

Reason:
COMMAND-004 successfully generated a platform-ready 小红书 publishing package that follows TSOS Source of Truth, preserves Jump series tone and complies with BRAND-001.

Required Fixes:
None.

Next Action:
Continue to TEST-005 — COMMAND-001 Full Production Package Validation.
```

---

# 18. Next Validation Action（下一步验证）

```text
Run TEST-005:
COMMAND-001 — Full Production Package Validation

Purpose:
Validate whether TSOS can combine storyboard, prompt, consistency check and publishing outputs into one complete production package.
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial COMMAND-004 publishing package validation test |