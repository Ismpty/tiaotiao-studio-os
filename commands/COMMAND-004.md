# COMMAND-004 — Generate Publishing Package（生成发布包）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Generate Publishing Package 是 TiaoTiao Studio OS 的发布包生成命令。

它用于快速调用 `WORKFLOW-004 — Publishing Workflow` 和 `AGENT-006 — Publishing Agent`，将已经完成的视频、脚本、字幕、封面和项目记录转化为可直接发布到不同平台的发布包。

这个 Command 不负责重新创作视频内容，也不修改 Jump 角色设定。

它只负责生成：

标题、正文、标签、封面文案、发布时间建议、发布前检查清单和发布后复盘模板。

## English

Generate Publishing Package is the publishing package command of TiaoTiao Studio OS.

It calls WORKFLOW-004 and AGENT-006 to transform completed production materials into platform-ready publishing packages.

---

# Command Goal（命令目标）

本命令用于：

- 生成平台发布标题
- 生成发布正文 / 简介
- 生成标签组
- 生成封面文案
- 生成发布时间建议
- 生成发布前检查清单
- 生成发布后复盘模板
- 保持不同平台的品牌一致性
- 避免标题党、焦虑表达和强营销文案

---

# Command Syntax（命令格式）

标准调用方式：

```text
Run COMMAND-004.
```

完整调用方式：

```text
Run COMMAND-004 for PROJ-001.
Use WORKFLOW-004.
Target Platform: 小红书.
Output platform-ready publishing package.
```

中文调用方式：

```text
运行 COMMAND-004，为《跳跳下班啦》生成发布包。
```

---

# Default Workflow（默认工作流）

本命令默认调用：

```text
WORKFLOW-004 — Publishing Workflow
```

---

# Default Agent（默认智能体）

本命令默认调用：

```text
AGENT-006 — Publishing Agent
```

---

# Default Project（默认项目）

本命令默认服务：

```text
PROJ-001 — Jump After Work Pilot Project
```

---

# Required Database Records（必需数据库记录）

| Database | Record | Purpose |
|---|---|---|
| Episode DB | EP-001 | 剧集设定 |
| Story DB | STORY-001 | 故事目标 |
| Prompt DB | PROMPT-001 | 主提示词 |
| Asset DB | ASSET-001 | 角色参考资产 |
| Project DB | PROJ-001 | 项目目标 |

---

# Required Knowledge Nodes（必需知识节点）

| Category | Knowledge Node |
|---|---|
| Brand Language | BRAND-001 |
| Story Formula | STORYFORMULA-001 |
| Emotion | EMOTION-001 |
| Music | MUSIC-001 |
| Style | STYLE-001 |
| Color | COLOR-001 |

---

# Optional Agent Outputs（可选智能体输出）

本命令可以读取：

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-002 | Prompt Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |

---

# Execution Order（执行顺序）

本命令必须按照以下顺序执行：

```text
1. Load Project Record
↓
2. Load Publishing Target
↓
3. Load Required Database Records
↓
4. Load Required Knowledge Nodes
↓
5. Load Script / Editing Outputs if available
↓
6. Run WORKFLOW-004
↓
7. Run AGENT-006 Publishing Agent
↓
8. Generate Platform Strategy
↓
9. Generate Title / Caption / Hashtags / Cover Text
↓
10. Run Brand Safety Check
↓
11. Output Publishing Package
```

---

# Input Requirements（输入要求）

用户可以提供以下输入：

```text
Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels

Language:
Chinese / English / Bilingual

Content Type:
Short Video / Cover / Image Set / Prompt Test / Long Video

Publish Date:
YYYY-MM-DD / TBD

Publish Time:
Specific time / Recommended time

Output Depth:
Simple / Standard / Detailed
```

如果用户没有指定，默认：

```text
Target Platform:
小红书

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

# Forbidden Inputs（禁止输入）

不得通过本命令临时修改：

- Jump 的角色身份
- Jump 的角色外观
- TiaoTiao Universe 世界观
- Brand Language
- Master Knowledge Nodes
- Database Record ID
- Frozen Roadmap
- 已确认的视频内容核心

如果用户输入与 TSOS Source of Truth 冲突，Command 必须拒绝该修改，并回到现有记录。

---

# Output Package（输出包）

本命令最终必须输出：

```text
1. Publishing Summary
2. Platform Strategy
3. Title Options
4. Caption / Description
5. Hashtag Set
6. Cover Text Suggestions
7. Publishing Time Suggestion
8. Pre-Publish Checklist
9. Publishing Record
10. Post-Publish Review Template
11. Brand Safety Check
```

---

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-004 Output

## 1. Publishing Summary

## 2. Platform Strategy

## 3. Title Options

## 4. Caption / Description

## 5. Hashtag Set

## 6. Cover Text Suggestions

## 7. Publishing Time Suggestion

## 8. Pre-Publish Checklist

## 9. Publishing Record

## 10. Post-Publish Review Template

## 11. Brand Safety Check
```

---

# Platform Rules（平台规则）

## 小红书

适合：

- 生活方式表达
- 治愈感标题
- 轻故事正文
- 高识别封面
- 温暖陪伴感

标题方向：

```text
下班啦，生活开始啦
电脑一关，生活上线
忙了一天，也要好好生活
跳跳下班啦，今天也认真生活了
```

正文风格：

```text
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

今天的跳跳，下班后也认真生活了。
```

---

## 抖音

适合：

- 简短标题
- 前 3 秒强识别
- 字幕清晰
- 节奏明确
- 结尾有记忆点

标题方向：

```text
电脑一关，生活上线
下班啦，生活开始啦
今天也认真生活了
```

---

## 视频号

适合：

- 温暖
- 稳定
- 有共鸣
- 不过度网感
- 适合朋友圈传播

标题方向：

```text
忙了一天，也要好好生活
下班后的时间，属于自己
今天也认真生活了
```

---

## YouTube Shorts

适合：

- 简洁英文标题
- 系列化命名
- 清晰角色识别
- 国际化标签

Title direction：

```text
Jump After Work
Life Begins After Work
A Little Adventure After Work
After Work, Life Begins
```

Description direction：

```text
Jump finishes work and starts a small everyday adventure.
```

---

## TikTok

适合：

- 快速进入情绪
- 简洁英文文案
- 角色标签化
- 轻故事感

Title direction：

```text
Life begins after work
After work, a little adventure
Jump clocks out
```

---

## Instagram Reels

适合：

- 视觉感
- 生活方式
- 情绪文案
- 简洁标签
- 品牌主页沉淀

Caption direction：

```text
A small reminder to give yourself a little life after work.
```

---

# Title Rules（标题规则）

标题必须：

- 简短
- 清晰
- 有情绪
- 有生活感
- 不夸张
- 不制造焦虑
- 不标题党
- 不强营销

推荐中文标题：

```text
下班啦，生活开始啦
电脑一关，生活上线
忙了一天，也要好好生活
下班后的路，也可以是冒险
今天也认真生活了
```

推荐英文标题：

```text
Jump After Work
Life Begins After Work
After Work, Life Begins
A Little Adventure After Work
```

禁止标题：

```text
打工人崩溃瞬间
成年人太惨了
老板看了都沉默
99% 的人都不知道
不看后悔
You Won't Believe This
This Will Shock You
```

---

# Caption Rules（正文规则）

正文必须：

- 温暖
- 真诚
- 生活化
- 不硬广
- 不焦虑
- 不夸张
- 不过度解释
- 保持 Jump 系列气质

---

# Caption Template — Chinese（中文正文模板）

```text
电脑一关，生活上线。

忙了一天，也要把时间还给自己一点点。

今天的跳跳，下班后也认真生活了。
```

---

# Caption Template — English（英文正文模板）

```text
Jump finishes work and starts a small everyday adventure.

A gentle reminder that life can begin again after work.
```

---

# Hashtag Rules（标签规则）

标签必须：

- 与内容相关
- 不堆砌
- 不蹭无关热点
- 不使用焦虑标签
- 不破坏品牌温暖感

---

# Chinese Hashtag Set（中文标签组）

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

# English Hashtag Set（英文标签组）

```text
#JumpAfterWork
#AfterWorkLife
#AIAnimation
#OriginalCharacter
#SliceOfLife
#LifestyleAnimation
#CreativeStudio
```

---

# Forbidden Hashtags（禁止标签）

```text
#爆款
#必看
#千万别错过
#打工人崩溃
#焦虑
#震惊
```

---

# Cover Text Rules（封面文案规则）

封面文案必须：

- 简短
- 清晰
- 高识别
- 不遮挡 Jump
- 不超过两层主信息
- 不标题党
- 有系列感
- 符合 STYLE-001 和 COLOR-001

---

# Cover Text Templates（封面文案模板）

## Template A

```text
主标题：
下班啦

副标题：
生活开始啦
```

---

## Template B

```text
主标题：
电脑一关

副标题：
生活上线
```

---

## Template C

```text
主标题：
跳跳下班啦

副标题：
今天也认真生活了
```

---

# Publishing Time Suggestion（发布时间建议）

## 小红书

```text
12:00–13:30
19:30–22:00
```

## 抖音 / TikTok

```text
11:30–13:00
18:30–22:30
```

## 视频号

```text
07:30–09:00
12:00–13:30
19:30–22:00
```

## YouTube Shorts

```text
18:00–22:00 target audience local time
```

## Instagram Reels

```text
12:00–14:00
18:00–21:00
```

---

# Pre-Publish Checklist（发布前检查清单）

本命令必须输出：

```text
[ ] 视频比例是否正确
[ ] 视频清晰度是否达标
[ ] 封面是否清晰
[ ] Jump 是否没有被遮挡
[ ] 字幕是否没有遮挡 Jump 的脸
[ ] 音乐是否不压过画面
[ ] 标题是否符合品牌语气
[ ] 正文是否不焦虑、不标题党
[ ] 标签是否相关
[ ] 封面文案是否简短
[ ] 是否符合 BRAND-001
[ ] 是否符合平台发布规范
[ ] 是否准备好发布后复盘记录
```

---

# Publishing Record Template（发布记录模板）

本命令必须输出：

```text
Project:
Platform:
Publish Date:
Publish Time:
Title:
Caption:
Hashtags:
Cover Text:
Video File:
Cover File:
Status:
Output Link:
Notes:
```

---

# Post-Publish Review Template（发布后复盘模板）

本命令必须输出：

```text
Views:
Likes:
Comments:
Shares:
Saves:
Completion Rate:
Average Watch Time:
Follower Growth:
Best Comment:
Audience Emotion:
Content Strength:
Content Weakness:
Next Iteration:
```

---

# Brand Safety Check（品牌安全检查）

本命令结束前必须检查：

```text
[ ] 标题是否避免标题党
[ ] 正文是否避免焦虑表达
[ ] 标签是否没有蹭无关热点
[ ] 封面文案是否不夸张
[ ] 是否没有强营销腔
[ ] 是否没有虚假承诺
[ ] 是否符合 BRAND-001
[ ] 是否保持 Jump 系列温暖气质
[ ] 是否适合目标平台
[ ] 是否支持发布后复盘
```

---

# Command Example（命令示例）

## Example 1

用户输入：

```text
Run COMMAND-004.
```

系统应执行：

```text
Run WORKFLOW-004 for PROJ-001.

Target Platform:
小红书
```

输出：

```text
Platform-ready publishing package for 小红书.
```

---

## Example 2

用户输入：

```text
运行 COMMAND-004，给《跳跳下班啦》生成 YouTube Shorts 发布包。
```

系统应执行：

```text
Run COMMAND-004 for PROJ-001.

Target Platform:
YouTube Shorts

Language:
English
```

输出：

```text
YouTube Shorts publishing package.
```

---

# Command Rules（命令规则）

## Must Do（必须）

- 必须调用 WORKFLOW-004
- 必须调用 AGENT-006
- 必须读取 PROJ-001
- 必须读取 BRAND-001
- 必须生成标题
- 必须生成正文
- 必须生成标签
- 必须生成封面文案
- 必须生成发布前检查清单
- 必须生成发布后复盘模板
- 必须执行品牌安全检查

---

## Never Do（禁止）

- 不得使用标题党
- 不得制造焦虑
- 不得使用强营销腔
- 不得虚假宣传
- 不得使用攻击性文案
- 不得为了流量破坏品牌一致性
- 不得使用无关标签
- 不得忽略平台差异
- 不得省略复盘记录

---

# Related Files（关联文件）

## Workflow

```text
workflows/WORKFLOW-004.md
```

## Database Records

```text
database/episodes/EP-001.md
database/stories/STORY-001.md
database/prompts/PROMPT-001.md
database/assets/ASSET-001.md
database/projects/PROJ-001.md
```

## Knowledge Nodes

```text
knowledge/brand-language/BRAND-001.md
knowledge/story-formula/STORYFORMULA-001.md
knowledge/emotion/EMOTION-001.md
knowledge/music/MUSIC-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
```

## Agents

```text
agents/publisher/AGENT-006.md
```

---

# Usage Scope（应用范围）

适用于：

- Publishing Package
- Platform Publishing
- Title Writing
- Caption Writing
- Hashtag Planning
- Cover Text Planning
- Publishing Checklist
- Post-Publish Review
- Platform Strategy

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical operating command |