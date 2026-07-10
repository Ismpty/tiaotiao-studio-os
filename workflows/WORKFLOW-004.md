# WORKFLOW-004 — Publishing Workflow（发布工作流）

> Canonical Workflow Template（官方工作流模板）  
> Version：2.0
> Status：Active

---

# Definition（定义）

## 中文

Publishing Workflow 是 TiaoTiao Studio OS 的发布工作流模板。

它用于把已经完成的视频、脚本、字幕、封面、剪辑方案和品牌规范，转化为可直接发布到不同平台的发布包。

这个 Workflow 不负责重新创作视频内容，也不修改 Jump 角色设定。

它只负责规定：

内容完成后，如何生成标题、正文、标签、封面文案、发布时间建议、发布前检查和发布后复盘。

## English

Publishing Workflow transforms completed video assets, scripts, captions, cover concepts, editing notes and brand rules into platform-ready publishing packages.

It does not recreate content or modify character canon.

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 让每条内容都能稳定发布
- 保持不同平台的品牌一致性
- 避免标题党和强营销表达
- 让发布前检查标准化
- 让发布后复盘数据标准化
- 让内容发布不依赖临时判断
- 让 TiaoTiao Studio 的内容形成长期可复用的发布系统

---

# Default Project（默认项目）

本 Workflow 默认服务：

```text
PROJ-001 — Little Security Guard and His Ancient Friends
《小保安和他的古人朋友们》
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
| Relic Friends | RELIC-001 |

---

# Required Agent（必需智能体）

| Agent | Role |
|---|---|
| AGENT-006 | Publishing Agent |

---

# Optional Agent Inputs（可选智能体输入）

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-002 | Prompt Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Publish Asset Review
↓
2. Platform Selection
↓
3. Title Generation
↓
4. Caption / Description Generation
↓
5. Hashtag Generation
↓
6. Cover Text Planning
↓
7. Publishing Time Planning
↓
8. Pre-Publish Checklist
↓
9. Publish Record Setup
↓
10. Post-Publish Review
```

---

# Stage 1 — Publish Asset Review（发布资产检查）

## Input（输入）

读取：

```text
Final Video
Cover Image
Script Output
Editing Output
Publishing Target
PROJ-001
ASSET-001
BRAND-001
```

## Task（任务）

确认发布素材是否完整：

- 成片是否完成
- 封面是否完成
- 字幕是否完成
- 音乐是否确认
- 平台比例是否正确
- Jump 是否保持一致
- 封面是否不遮挡主体
- 文案是否符合品牌语言

## Output（输出）

```text
Publish Asset Review Result
```

## Required Check（必须检查）

```text
[ ] 是否有最终视频文件
[ ] 是否有封面图
[ ] 是否有标题方向
[ ] 是否有字幕版本
[ ] 是否有发布平台
[ ] Jump 是否符合 ASSET-001
[ ] 是否符合 BRAND-001
```

---

# Stage 2 — Platform Selection（平台选择）

## Input（输入）

确认目标平台：

```text
小红书
抖音
视频号
YouTube Shorts
TikTok
Instagram Reels
```

## Task（任务）

根据平台选择不同发布策略：

- 标题长度
- 正文长度
- 标签数量
- 封面文案
- 发布时间
- 语言版本
- 是否需要中英文版本

## Output（输出）

```text
Platform Strategy
```

---

# Platform Strategy Rules（平台策略规则）

## 小红书

适合：

- 生活方式
- 治愈感
- 轻故事
- 封面强识别
- 正文有陪伴感

重点：

```text
标题要有情绪
正文要像生活记录
封面要清晰高级
标签不要堆砌
```

---

## 抖音

适合：

- 快速进入情绪
- 标题简短
- 节奏明确
- 字幕清晰
- 结尾有记忆点

重点：

```text
前 3 秒要清楚
标题不要太长
字幕不能遮挡主体
```

---

## 视频号

适合：

- 温暖
- 稳定
- 有共鸣
- 适合朋友圈传播
- 不过度网感

重点：

```text
文案要自然
不要太标题党
适合熟人社交传播
```

---

## YouTube Shorts

适合：

- 英文标题
- 系列化命名
- 清晰角色识别
- 简短描述
- 国际化标签

重点：

```text
Title should be simple
Character identity should be clear
Series name should stay consistent
```

---

## TikTok

适合：

- 快速情绪进入
- 简洁英文文案
- 角色标签化
- 轻故事感

重点：

```text
Keep it short
Emotion first
Use consistent character tags
```

---

## Instagram Reels

适合：

- 视觉感
- 生活方式
- 情绪文案
- 简洁标签
- 适合品牌主页沉淀

重点：

```text
Caption should be warm, absurd and museum-specific
Hashtags should support AI museum, relic friend and original IP identity
```

---

# Stage 3 — Title Generation（标题生成）

## Agent（执行智能体）

```text
AGENT-006 — Publishing Agent
```

## Input（输入）

读取：

```text
PROJ-001
Script Output
Editing Output
BRAND-001
Target Platform
```

## Task（任务）

生成平台适配标题。

标题必须：

- 简短
- 清晰
- 有情绪
- 不标题党
- 不制造焦虑
- 不使用强营销腔
- 保持 Jump 系列感
- 保持“小保安和他的古人朋友们”的 AI 博物馆系列识别

## Output（输出）

```text
Title Options
```

---

# Title Style Rules（标题风格规则）

## 中文标题方向

推荐：

```text
闭馆以后，古人朋友醒了
小保安今天又遇到大事了
AI 博物馆夜班也太离谱了
这件文物说它要当销冠
闭馆以后，朋友们才刚刚上班
```

避免：

```text
打工人崩溃瞬间
成年人太惨了
老板看了都沉默
99% 的人都不知道
不看后悔
```

---

## English Title Direction

Recommended：

```text
The Little Security Guard and His Ancient Friends
After Closing, the Relics Wake Up
AI Museum Night Shift
Jump's Weird Museum Patrol
The Museum Is Not Quiet Tonight
```

Avoid：

```text
You Won't Believe This
This Will Shock You
The Sad Truth About Work
Most People Don't Know This
```

---

# Stage 4 — Caption / Description Generation（正文 / 简介生成）

## Input（输入）

读取：

```text
Script Output
Story Output
Brand Language
Platform Strategy
```

## Task（任务）

生成平台正文或简介。

正文必须：

- 温暖
- 真诚
- 生活化
- 不过度解释
- 不硬广
- 不焦虑
- 不夸张
- 尊重中国文物和神话意象，不恐怖化、不廉价吉祥物化

## Output（输出）

```text
Caption / Description
```

---

# Caption Templates（正文模板）

## 小红书 / 视频号 / 抖音

```text
AI 博物馆闭馆以后，真正的热闹才开始。

小保安跳跳认真巡逻，古人朋友认真添乱。

今晚的展厅，又被它们过成了大型无厘头现场。
```

---

## YouTube Shorts / TikTok / Instagram Reels

```text
Jump is on night patrol at the AI museum.

After closing, the ancient relic friends wake up and turn the gallery into a warm, absurd little adventure.
```

---

# Stage 5 — Hashtag Generation（标签生成）

## Task（任务）

生成平台标签组。

标签必须：

- 与内容相关
- 不堆砌
- 不蹭无关热点
- 不使用焦虑标签
- 不破坏品牌温暖感

## Output（输出）

```text
Hashtag Set
```

---

# Hashtag Rules（标签规则）

## 中文平台推荐标签

```text
#小保安和他的古人朋友们
#AI博物馆
#文物朋友
#国风AI
#AI动画
#原创IP
```

## 中文平台避免标签

```text
#爆款
#必看
#千万别错过
#打工人崩溃
#焦虑
```

---

## English Platform Recommended Tags

```text
#LittleSecurityGuard
#AIMuseum
#RelicFriends
#AIAnimation
#OriginalCharacter
#ChineseRelics
#AbsurdComedy
```

---

# Stage 6 — Cover Text Planning（封面文案规划）

## Input（输入）

读取：

```text
Cover Image
Script Output
Brand Language
Platform Strategy
```

## Task（任务）

生成封面文案。

封面文案必须：

- 简短
- 清晰
- 高识别
- 不遮挡 Jump
- 不超过两层主信息
- 不标题党
- 有系列感

## Output（输出）

```text
Cover Text Suggestions
```

---

# Cover Text Templates（封面文案模板）

## Template A

```text
主标题：
闭馆以后

副标题：
朋友们醒了
```

---

## Template B

```text
主标题：
小保安

副标题：
今天又遇到大事了
```

---

## Template C

```text
主标题：
AI 博物馆

副标题：
今晚不太安静
```

---

# Cover Safety Rules（封面安全规则）

```text
[ ] 主体是否清晰
[ ] Jump 是否没有被文字遮挡
[ ] 文字是否在安全区
[ ] 主标题是否易读
[ ] 副标题是否简短
[ ] 是否没有标题党
[ ] 是否符合 STYLE-001
[ ] 是否符合 COLOR-001
[ ] 是否符合 BRAND-001
[ ] 是否符合 AI 博物馆和文物朋友系列识别
```

---

# Stage 7 — Publishing Time Planning（发布时间规划）

## Task（任务）

根据平台生成发布时间建议。

## Output（输出）

```text
Publishing Time Suggestion
```

---

# Publishing Time Rules（发布时间规则）

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

# Stage 8 — Pre-Publish Checklist（发布前检查）

## Task（任务）

生成发布前检查清单。

## Output（输出）

```text
Pre-Publish Checklist
```

---

# Pre-Publish Checklist Template（发布前检查清单模板）

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

# Stage 9 — Publish Record Setup（发布记录建立）

## Task（任务）

发布前建立记录字段。

## Output（输出）

```text
Publishing Record
```

---

# Publishing Record Template（发布记录模板）

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

# Stage 10 — Post-Publish Review（发布后复盘）

## Task（任务）

发布后记录数据反馈。

## Output（输出）

```text
Post-Publish Review
```

---

# Post-Publish Review Metrics（发布后复盘指标）

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

# Review Rules（复盘规则）

复盘时必须关注：

- 观众是否理解 Jump
- 观众是否感受到温暖
- 哪个标题更有效
- 哪个封面更有效
- 哪个平台反馈最好
- 完播率是否健康
- 评论区情绪是否符合品牌目标
- 是否值得发展为下一条内容

---

# Final Output（最终输出）

完整工作流最终应输出：

```text
1. Publish Asset Review Result
2. Platform Strategy
3. Title Options
4. Caption / Description
5. Hashtag Set
6. Cover Text Suggestions
7. Publishing Time Suggestion
8. Pre-Publish Checklist
9. Publishing Record
10. Post-Publish Review Template
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-004 for PROJ-001.

Target Platform:
小红书 / 抖音 / 视频号 / YouTube Shorts / TikTok / Instagram Reels

Use:
PROJ-001
EP-001
STORY-001
PROMPT-001
ASSET-001

Use Agent:
AGENT-006

Use Knowledge:
BRAND-001
STORYFORMULA-001
EMOTION-001
MUSIC-001
STYLE-001
COLOR-001

Output:
Platform-ready publishing package.
```

---

# Workflow Rules（工作流规则）

## Must Do（必须）

- 必须符合 BRAND-001
- 必须根据平台适配标题和正文
- 必须检查封面安全区
- 必须避免标题党
- 必须避免焦虑表达
- 必须输出发布前检查清单
- 必须输出发布后复盘指标
- 必须保留 Jump 系列识别

---

## Never Do（禁止）

- 不得使用虚假宣传
- 不得使用强营销话术
- 不得制造职场焦虑
- 不得使用攻击性文案
- 不得为了流量破坏品牌一致性
- 不得使用无关标签
- 不得忽略平台差异
- 不得省略复盘记录

---

# Related Files（关联文件）

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

- Short Video Publishing
- Platform Publishing
- Cover Text Planning
- Title Writing
- Caption Writing
- Hashtag Planning
- Publishing Checklist
- Post-Publish Review
- Platform Strategy
- Series Distribution

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical workflow template |
