# COMMAND-005 — Run Consistency Check（运行一致性检查）

> Canonical Operating Command（官方操作命令）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Run Consistency Check 是 TiaoTiao Studio OS 的一致性检查命令。

它用于检查任意 Project、Storyboard、Prompt、Script、Editing Plan、Publishing Package 或单个生成结果是否符合 TSOS 的 Source of Truth。

这个 Command 不负责创作新内容，也不负责修改角色、世界观或品牌方向。

它只负责检查：

当前输出是否仍然符合 Jump、TiaoTiao Universe、Knowledge Nodes、Database Records、Agents 和 Workflow 的统一规范。

## English

Run Consistency Check is the consistency verification command of TiaoTiao Studio OS.

It checks whether any project output, storyboard, prompt, script, editing plan, publishing package or generated result follows the TSOS source of truth.

---

# Command Goal（命令目标）

本命令用于：

- 检查 Jump 角色一致性
- 检查世界观一致性
- 检查视觉风格一致性
- 检查色彩一致性
- 检查情绪一致性
- 检查动作一致性
- 检查镜头一致性
- 检查灯光一致性
- 检查提示词一致性
- 检查品牌语言一致性
- 检查是否偏离 Frozen Roadmap
- 发现并标记需要修改的问题

---

# Command Syntax（命令格式）

标准调用方式：

```text
Run COMMAND-005.
```

完整调用方式：

```text
Run COMMAND-005 for PROJ-001.
Check storyboard, prompt, script, editing plan and publishing package.
```

中文调用方式：

```text
运行 COMMAND-005，检查当前内容是否符合 TSOS。
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
| Character DB | CHAR-001 | 检查 Jump 角色身份 |
| Episode DB | EP-001 | 检查剧集一致性 |
| Story DB | STORY-001 | 检查故事一致性 |
| Environment DB | ENV-001 | 检查环境一致性 |
| Motion DB | MOT-001 | 检查动作一致性 |
| Camera DB | CAM-001 | 检查镜头一致性 |
| Lighting DB | LGT-001 | 检查灯光一致性 |
| Prompt DB | PROMPT-001 | 检查提示词一致性 |
| Asset DB | ASSET-001 | 检查角色参考资产一致性 |
| Project DB | PROJ-001 | 检查项目目标一致性 |

---

# Required Knowledge Nodes（必需知识节点）

| Category | Knowledge Node |
|---|---|
| Style | STYLE-001 |
| Color | COLOR-001 |
| World | WORLD-001 |
| Emotion | EMOTION-001 |
| Camera Language | SHOT-001 |
| Motion Language | MOTIONLANG-001 |
| Outfit | OUTFIT-001 |
| Music | MUSIC-001 |
| Story Formula | STORYFORMULA-001 |
| Brand Language | BRAND-001 |

---

# Related Workflows（关联工作流）

本命令可检查以下 Workflow 输出：

| Workflow | Name |
|---|---|
| WORKFLOW-001 | Jump After Work Production Workflow |
| WORKFLOW-002 | Short Video Prompt Workflow |
| WORKFLOW-003 | Storyboard to Video Workflow |
| WORKFLOW-004 | Publishing Workflow |

---

# Related Agents（关联智能体）

本命令可检查以下 Agent 输出：

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-002 | Prompt Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |
| AGENT-006 | Publishing Output |

---

# Execution Order（执行顺序）

本命令必须按照以下顺序执行：

```text
1. Identify Target Output
↓
2. Load Required Database Records
↓
3. Load Required Knowledge Nodes
↓
4. Check Character Consistency
↓
5. Check World Consistency
↓
6. Check Visual Consistency
↓
7. Check Motion / Camera / Lighting Consistency
↓
8. Check Story / Emotion / Brand Consistency
↓
9. Check Workflow Compliance
↓
10. Identify Issues
↓
11. Output Consistency Report
```

---

# Input Requirements（输入要求）

用户可以提供以下输入：

```text
Check Target:
Storyboard / Prompt / Script / Editing Plan / Publishing Package / Generated Image / Generated Video / Project Package

Project:
PROJ-001 / Custom Project ID

Output Type:
Text / Image / Video / Mixed

Strictness:
Light / Standard / Strict

Language:
Chinese / English / Bilingual
```

如果用户没有指定，默认：

```text
Check Target:
Current Output

Project:
PROJ-001

Strictness:
Strict

Language:
Chinese
```

---

# Forbidden Behavior（禁止行为）

本命令不得：

- 自动修改 Source of Truth
- 自动改写 Database Records
- 自动改写 Knowledge Nodes
- 自动更改 Frozen Roadmap
- 自动新增世界观
- 自动接受与 Jump 设定冲突的内容
- 自动把错误内容合理化

如果发现冲突，必须明确标记：

```text
Issue Found
```

并说明冲突对象。

---

# Output Package（输出包）

本命令最终必须输出：

```text
1. Consistency Summary
2. Character Consistency Check
3. World Consistency Check
4. Visual Style Check
5. Color Check
6. Emotion Check
7. Motion Check
8. Camera Check
9. Lighting Check
10. Story / Brand Check
11. Workflow Compliance Check
12. Issue List
13. Fix Suggestions
14. Final Pass / Fail Result
```

---

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-005 Output

## 1. Consistency Summary

## 2. Character Consistency Check

## 3. World Consistency Check

## 4. Visual Style Check

## 5. Color Check

## 6. Emotion Check

## 7. Motion Check

## 8. Camera Check

## 9. Lighting Check

## 10. Story / Brand Check

## 11. Workflow Compliance Check

## 12. Issue List

## 13. Fix Suggestions

## 14. Final Result
```

---

# Check Level（检查等级）

## Light

适用于快速检查。

检查：

```text
Character
Brand
Major visual consistency
Major story consistency
```

---

## Standard

适用于普通生产检查。

检查：

```text
Character
World
Style
Color
Emotion
Story
Prompt
Brand
Workflow
```

---

## Strict

适用于正式发布前检查。

检查：

```text
Character
World
Style
Color
Emotion
Outfit
Motion
Camera
Lighting
Music
Story Formula
Prompt
Asset
Brand
Workflow
Publishing Safety
```

默认使用：

```text
Strict
```

---

# Character Consistency Check（角色一致性检查）

默认对照：

```text
CHAR-001
ASSET-001
OUTFIT-001
COLOR-001
```

必须检查：

```text
[ ] Jump 是否仍然是拟人化小狗
[ ] Jump 是否保持女性角色设定
[ ] Jump 是否保持程序员身份
[ ] Jump 是否保持毛茸茸质感
[ ] Jump 是否保持苗条体型
[ ] Jump 表情是否友好温暖
[ ] Jump 是否没有变成人类
[ ] Jump 是否没有变成其他动物
[ ] Jump 是否没有变成肌肉型角色
[ ] Jump 是否没有失去品牌色识别
[ ] Jump 是否参考 ASSET-001
[ ] Jump 服装是否符合 OUTFIT-001
```

---

# World Consistency Check（世界观一致性检查）

默认对照：

```text
WORLD-001
EP-001
STORY-001
PROJ-001
```

必须检查：

```text
[ ] 是否仍然属于 TiaoTiao Universe
[ ] 是否仍然服务《跳跳下班啦》系列
[ ] 是否没有新增未确认世界观
[ ] 是否没有加入黑暗、恐怖、暴力或极端设定
[ ] 是否保持日常生活和创作者世界的基调
[ ] 是否符合 PROJ-001 的试播项目目标
```

---

# Visual Style Check（视觉风格检查）

默认对照：

```text
STYLE-001
BRAND-001
```

必须检查：

```text
[ ] 是否保持电影纪录片质感
[ ] 是否保持真实生活方式视觉
[ ] 是否没有变成游戏渲染感
[ ] 是否没有变成廉价 CGI
[ ] 是否没有过度卡通化
[ ] 是否没有恐怖片风格
[ ] 是否没有赛博朋克风格
[ ] 是否符合 TiaoTiao Studio 温暖、真实、乐观的品牌气质
```

---

# Color Check（色彩检查）

默认对照：

```text
COLOR-001
```

必须检查：

```text
[ ] 是否保持自然暖色基调
[ ] 是否正确使用 Fire Dragon Fruit Pink 作为品牌点缀
[ ] 是否没有让品牌色过度泛滥
[ ] 是否没有使用冷蓝赛博朋克主色
[ ] 是否没有高饱和 RGB 灯效
[ ] 是否没有破坏 Jump 的主体识别
```

---

# Emotion Check（情绪检查）

默认对照：

```text
EMOTION-001
STORYFORMULA-001
BRAND-001
```

必须检查：

```text
[ ] 是否表达 Freedom
[ ] 是否表达下班后的轻松感
[ ] 是否有温暖、治愈、生活感
[ ] 是否没有制造焦虑
[ ] 是否没有职场抱怨主导
[ ] 是否没有强行煽情
[ ] 是否没有负面压迫感
```

---

# Motion Check（动作检查）

默认对照：

```text
MOT-001
MOTIONLANG-001
```

必须检查：

```text
[ ] 动作是否自然可信
[ ] 行走是否符合 MOT-001
[ ] 是否有真实重心转移
[ ] 脚步是否没有滑动
[ ] 身体是否没有漂浮
[ ] 尾巴动作是否自然
[ ] 动作是否没有机器人感
[ ] 动作是否没有游戏动画感
```

---

# Camera Check（镜头检查）

默认对照：

```text
CAM-001
SHOT-001
```

必须检查：

```text
[ ] 镜头是否服务故事
[ ] 是否保持 35mm / 自然视角为主
[ ] 是否使用合理机位
[ ] 是否保持 eye-level 亲近感
[ ] 是否没有极端广角变形
[ ] 是否没有 FPS 游戏视角
[ ] 是否没有无人机环绕炫技
[ ] 是否没有不符合物理逻辑的镜头运动
```

---

# Lighting Check（灯光检查）

默认对照：

```text
LGT-001
STYLE-001
COLOR-001
```

必须检查：

```text
[ ] 是否保持 Warm Studio Lighting
[ ] 是否有实用台灯 / 屏幕柔光 / 傍晚窗光
[ ] 是否保留柔和阴影
[ ] 是否没有恐怖片高反差
[ ] 是否没有冷蓝赛博朋克灯光
[ ] 是否没有舞台聚光灯
[ ] 是否没有过曝或死黑
```

---

# Story / Brand Check（故事与品牌检查）

默认对照：

```text
STORYFORMULA-001
BRAND-001
EP-001
PROJ-001
```

必须检查：

```text
[ ] 是否符合 Work Ends, Adventure Begins
[ ] 是否有 Work / Decision / Exploration / Discovery / Emotion / Reflection 结构
[ ] 是否体现“下班后生活重新开始”
[ ] 是否符合 TiaoTiao Studio 品牌使命
[ ] 是否温暖、乐观、真诚
[ ] 是否没有强营销腔
[ ] 是否没有标题党
[ ] 是否没有虚假承诺
```

---

# Prompt Consistency Check（提示词一致性检查）

默认对照：

```text
PROMPT-001
COMMAND-002
WORKFLOW-002
```

必须检查：

```text
[ ] Prompt 是否引用 Source Records
[ ] Prompt 是否引用 ASSET-001
[ ] Prompt 是否包含 Negative Prompt
[ ] Prompt 是否适配目标模型
[ ] Prompt 是否没有临时修改 Jump
[ ] Prompt 是否没有省略关键视觉约束
[ ] Prompt 是否可直接执行
```

---

# Workflow Compliance Check（工作流合规检查）

默认对照：

```text
WORKFLOW-001
WORKFLOW-002
WORKFLOW-003
WORKFLOW-004
```

必须检查：

```text
[ ] 是否使用正确 Workflow
[ ] 是否使用正确 Agent
[ ] 是否按阶段执行
[ ] 是否没有跳过一致性检查
[ ] 是否输出了规定结构
[ ] 是否没有绕过 TSOS Source of Truth
```

---

# Publishing Safety Check（发布安全检查）

默认对照：

```text
COMMAND-004
WORKFLOW-004
AGENT-006
BRAND-001
```

必须检查：

```text
[ ] 标题是否不标题党
[ ] 正文是否不焦虑
[ ] 标签是否相关
[ ] 封面文案是否简洁
[ ] 是否没有夸张营销
[ ] 是否没有虚假承诺
[ ] 是否符合平台表达习惯
[ ] 是否支持发布后复盘
```

---

# Issue Severity（问题严重级别）

发现问题时必须标记严重级别。

## Critical

必须修改，不能进入下一步。

示例：

```text
Jump 被改成人类
世界观被改成恐怖片
品牌语言变成强营销
核心角色身份错误
```

---

## Major

建议修改，否则影响生产质量。

示例：

```text
灯光偏冷
镜头过度游戏感
字幕遮挡角色
Prompt 负面词不足
```

---

## Minor

可优化，不影响继续生产。

示例：

```text
标题可以更简洁
标签可以更精准
情绪表达可以更温暖
```

---

# Issue List Template（问题列表模板）

```text
| Severity | Area | Issue | Source of Truth | Suggested Fix |
|---|---|---|---|---|
| Critical / Major / Minor | Character / Camera / Brand | Issue description | CHAR-001 / BRAND-001 | Fix suggestion |
```

---

# Fix Suggestion Rules（修改建议规则）

修改建议必须：

- 指向具体问题
- 引用 Source of Truth
- 不新增未确认设定
- 不改变 Frozen Roadmap
- 不扩展无关内容
- 尽量给出可直接修改的文本

---

# Final Result Rules（最终结果规则）

最终结果必须明确给出：

```text
PASS
```

或：

```text
FAIL
```

或：

```text
PASS WITH MINOR FIXES
```

---

# Final Result Template（最终结果模板）

```text
Final Result:
PASS / FAIL / PASS WITH MINOR FIXES

Reason:
Brief explanation.

Required Fixes:
1.
2.
3.

Next Action:
Continue / Revise / Re-check
```

---

# Command Example（命令示例）

## Example 1

用户输入：

```text
Run COMMAND-005.
```

系统应执行：

```text
Run strict consistency check against PROJ-001 and TSOS Source of Truth.
```

输出：

```text
Consistency report with pass / fail result.
```

---

## Example 2

用户输入：

```text
运行 COMMAND-005，检查这份 Kling 视频 Prompt。
```

系统应执行：

```text
Run COMMAND-005.

Check Target:
Prompt

Target Model:
Kling

Strictness:
Strict
```

输出：

```text
Prompt consistency report.
```

---

## Example 3

用户输入：

```text
检查这个封面会不会偏离跳跳设定。
```

系统应执行：

```text
Run COMMAND-005.

Check Target:
Generated Image / Cover

Strictness:
Strict
```

输出：

```text
Character, visual, brand and cover safety consistency report.
```

---

# Command Rules（命令规则）

## Must Do（必须）

- 必须对照 Source of Truth
- 必须读取 10 个 Database Records
- 必须读取 10 个 Knowledge Nodes
- 必须检查 ASSET-001
- 必须标记问题严重级别
- 必须给出修改建议
- 必须给出最终 PASS / FAIL
- 必须拒绝核心设定冲突

---

## Never Do（禁止）

- 不得合理化错误设定
- 不得忽略 Jump 身份错误
- 不得忽略品牌冲突
- 不得跳过 ASSET-001
- 不得用主观审美替代 TSOS 规范
- 不得为了效率省略检查项
- 不得自动修改 Source of Truth
- 不得新增未确认设定

---

# Related Files（关联文件）

## Commands

```text
commands/COMMAND-001.md
commands/COMMAND-002.md
commands/COMMAND-003.md
commands/COMMAND-004.md
```

## Workflows

```text
workflows/WORKFLOW-001.md
workflows/WORKFLOW-002.md
workflows/WORKFLOW-003.md
workflows/WORKFLOW-004.md
```

## Database Records

```text
database/characters/CHAR-001.md
database/episodes/EP-001.md
database/stories/STORY-001.md
database/environments/ENV-001.md
database/motions/MOT-001.md
database/cameras/CAM-001.md
database/lighting/LGT-001.md
database/prompts/PROMPT-001.md
database/assets/ASSET-001.md
database/projects/PROJ-001.md
```

## Knowledge Nodes

```text
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/world/WORLD-001.md
knowledge/emotion/EMOTION-001.md
knowledge/camera-language/SHOT-001.md
knowledge/motion-language/MOTIONLANG-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/music/MUSIC-001.md
knowledge/story-formula/STORYFORMULA-001.md
knowledge/brand-language/BRAND-001.md
```

## Agents

```text
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
agents/cinematographer/AGENT-003.md
agents/writer/AGENT-004.md
agents/editor/AGENT-005.md
agents/publisher/AGENT-006.md
```

---

# Usage Scope（应用范围）

适用于：

- Consistency Check
- Prompt QA
- Storyboard QA
- Script QA
- Editing QA
- Publishing QA
- Image Review
- Video Review
- Project Review
- Brand Safety Review
- Final Production Check

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical operating command |