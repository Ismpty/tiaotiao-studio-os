# WORKFLOW-003 — Storyboard to Video Workflow（分镜到视频工作流）

> Canonical Workflow Template（官方工作流模板）  
> Version：2.0
> Status：Active

---

# Definition（定义）

## 中文

Storyboard to Video Workflow 是 TiaoTiao Studio OS 的分镜到视频生成工作流。

它用于把已经确认的身份卡、故事板和通用视频 Prompt，转化为可生成、可审查、可剪辑的视频片段。

从 v2.0 开始，本 Workflow 不再为每个 Shot 复制一份长视频 Prompt。

镜头细节归属故事板。

视频生成时使用：

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Current Shot Name
↓
COMMAND-005 review
```

## English

Storyboard to Video Workflow transforms an approved identity card, approved storyboard and universal video prompt into executable video clips.

Starting from v2.0, shot details belong to the storyboard, and video generation uses a compact universal prompt with the uploaded identity card, uploaded storyboard and current shot name.

---

# Source of Truth Rule（事实来源规则）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

本 Workflow 必须以 GitHub 文件为正式依据。

Notion 只能用于可视化管理和进度追踪，不能作为最终事实来源。

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 用身份卡锁定 Jump 角色外观
- 用故事板锁定镜头细节
- 用通用视频 Prompt 执行逐镜头生成
- 避免每个 Shot 产生重复长 Prompt
- 保持 Jump 是真实小狗本体形态、穿衣服的角色
- 保持故事板黑白粗略铅笔线稿风格
- 保持故事板彩色动态标注系统
- 保持镜头之间动作、道具、灯光和情绪连续
- 让每个视频片段可以进入 `COMMAND-005` 审查和剪辑阶段

---

# Default Project（默认项目）

本 Workflow 默认服务：

```text
PROJ-001 — Jump After Work Pilot Project
《跳跳下班啦》
```

默认故事比例：

```text
Office / clock-out part: 10%–20%
After-work life montage: 80%–90%
```

---

# Required Source References（必需内部来源）

以下内部编号用于 GitHub 文档、Notion 管理、Review、Changelog 和一致性检查。

它们不得裸露在模型可复制 Prompt 中。

| Source | Record | Purpose |
|---|---|---|
| Project DB | PROJ-001 | 项目目标 |
| Character DB | CHAR-001 | Jump 角色身份 |
| Episode DB | EP-001 | 剧集设定 |
| Story DB | STORY-001 | 故事目标 |
| Environment DB | ENV-001 | 场景环境 |
| Motion DB | MOT-001 | 动作连续性 |
| Camera DB | CAM-001 | 镜头语言 |
| Lighting DB | LGT-001 | 灯光一致性 |
| Prompt DB | PROMPT-001 | 提示词规则 |
| Asset DB | ASSET-001 | 角色参考资产 |

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

# Required Agents（必需智能体）

| Agent | Role |
|---|---|
| AGENT-001 | Storyboard Agent |
| AGENT-002 | Prompt Engineer Agent |
| AGENT-003 | Cinematography Agent |
| AGENT-005 | Editing Agent |

---

# Runtime Ownership（运行职责归属）

```text
Identity Card = character appearance
Storyboard = shot details
Universal Video Prompt = model execution rules
COMMAND-005 = consistency review
```

不得把身份卡、故事板和视频 Prompt 混成一段长 Prompt。

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Runtime Input Review
↓
2. Identity Card Verification
↓
3. Storyboard Verification
↓
4. Universal Video Prompt Setup
↓
5. Shot Execution Plan
↓
6. Clip Generation Package
↓
7. Clip Review with COMMAND-005
↓
8. Iteration Notes
↓
9. Assembly Notes
```

---

# Stage 1 — Runtime Input Review（运行输入检查）

## Input（输入）

读取：

```text
Identity Card Prompt
Storyboard Prompt / Storyboard Output
Universal Video Prompt
PROJ-001
CHAR-001
ASSET-001
STORY-001
```

## Task（任务）

确认是否具备：

- 可上传的 Jump 身份卡
- 可上传的故事板
- 通用视频 Prompt
- 目标模型
- 画幅比例
- Shot List
- 每个 Shot 的名称、时长和叙事功能

## Output（输出）

```text
Runtime Input Review Result
```

## Required Check（必须检查）

```text
[ ] 是否存在 Identity Card Prompt
[ ] 是否存在 Storyboard Prompt / Storyboard Output
[ ] 是否存在 Universal Video Prompt
[ ] 是否明确目标模型
[ ] 是否明确逐镜头生成方式
[ ] 是否没有把 Notion 当作 Source of Truth
```

---

# Stage 2 — Identity Card Verification（身份卡验证）

## Task（任务）

验证身份卡是否足以锁定 Jump 外观。

必须检查：

```text
[ ] Jump 是否是真实小狗本体形态
[ ] Jump 是否保持四足小狗身体结构
[ ] Jump 是否有蓬松毛发
[ ] Jump 是否穿程序员风格小狗衣服
[ ] Jump 是否可保留小包 / 工牌 / 项圈挂饰
[ ] Jump 是否可保留少量火龙果粉色点缀
[ ] 是否明确禁止半人身体、人类手掌、人类手臂、人类双腿站立和人类身体比例
[ ] 是否明确禁止变成人类、其他动物或无衣服普通宠物狗
[ ] 模型可复制区是否没有裸露内部 ID
```

## Output（输出）

```text
Identity Card Verification Result
```

---

# Stage 3 — Storyboard Verification（故事板验证）

## Task（任务）

验证故事板是否足以锁定镜头细节。

故事板必须说明：

```text
Shot Number
Shot Name
Duration
Story Function
Character Position
Dog Movement Direction
Prop Interaction
Camera Movement
Lighting / Mood
Continuity / Transition
```

## Fixed Storyboard Style（固定故事板风格）

故事板主体必须是：

```text
黑白线条
粗略铅笔线条
极简细节
快速动态描绘
简单解剖结构
清晰轮廓
轻盈、动态、未完成感
导演前期预演分镜草图风格
```

## Color Annotation System（彩色标注系统）

```text
Red / 红色：camera movement / 镜头运动
Blue / 蓝色：character or dog movement / 角色动作、小狗动作
Yellow / 黄色：prop interaction / 道具、交互
Green / 绿色：lighting or mood / 灯光、情绪
Purple / 紫色：continuity or transition / 连续性、转场
```

## Required Check（必须检查）

```text
[ ] 故事板主体是否是黑白粗略铅笔线稿
[ ] 故事板是否保留彩色动态标注系统
[ ] 每个 Shot 是否有明确镜头内容
[ ] 每个 Shot 是否有明确动作方向
[ ] 每个 Shot 是否有明确道具和灯光变化
[ ] 每个 Shot 是否有明确连续性提示
[ ] 故事板是否没有变成彩色成片插画、真实渲染或儿童绘本风
```

## Output（输出）

```text
Storyboard Verification Result
```

---

# Stage 4 — Universal Video Prompt Setup（通用视频提示词设置）

## Task（任务）

确认通用视频 Prompt 可用于逐镜头生成。

通用视频 Prompt 必须保持紧凑，并使用以下结构：

```text
请严格参考上传的角色身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

角色外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。

视频规格：
[duration / aspect ratio / frame style]

动作要求：
[natural dog-form movement, no humanoid movement]

镜头要求：
[camera movement and framing rule]

灯光和情绪：
[lighting and mood rule]

连续性要求：
[match previous and next storyboard shots]

负面要求：
[forbidden character, style, motion, camera, lighting and continuity drift]
```

## Required Check（必须检查）

```text
[ ] 是否引用上传身份卡
[ ] 是否引用上传故事板
[ ] 是否要求替换 [SHOT NUMBER AND NAME]
[ ] 是否避免重复大量 Shot 细节
[ ] 是否包含角色、动作、镜头、灯光、风格和连续性负面规则
[ ] 模型可复制区是否没有裸露内部 ID
```

## Output（输出）

```text
Universal Video Prompt Verification Result
```

---

# Stage 5 — Shot Execution Plan（逐镜头执行计划）

## Task（任务）

把故事板中的每个 Shot 转化为视频生成任务。

每个视频任务只需要指向：

```text
Uploaded Identity Card
Uploaded Storyboard
Universal Video Prompt
Current Shot Number and Name
Target Model
Duration
Aspect Ratio
Continuity Notes
Review Status
```

## Output（输出）

```text
Shot Execution Plan
```

---

# Shot Execution Unit Template（逐镜头执行单元模板）

```text
Shot Number:
Shot Name:
Duration:
Target Model:
Aspect Ratio:
Uploaded Identity Card:
Uploaded Storyboard:
Universal Video Prompt:
Current Shot Placeholder:
Continuity Notes:
COMMAND-005 Review Status:
```

---

# Stage 6 — Clip Generation Package（片段生成包）

## Task（任务）

为每个 Shot 输出生成包。

## Output（输出）

```text
Clip Generation Package
```

---

# Clip Generation Package Template（片段生成包模板）

```text
# Clip Generation Package

## Source References

## Uploaded Identity Card

## Uploaded Storyboard

## Universal Video Prompt

## Current Shot

## Target Model

## Duration

## Aspect Ratio

## Continuity Notes

## Negative Rules

## COMMAND-005 Review Checklist
```

---

# Stage 7 — Clip Review with COMMAND-005（使用 COMMAND-005 审片）

## Task（任务）

每个生成片段必须使用 `COMMAND-005` 审查。

必须检查：

```text
[ ] Jump 是否保持真实小狗本体形态
[ ] Jump 是否穿程序员风格小狗衣服
[ ] 是否没有人类手掌、人类手臂、人类双腿站立或人类身体比例
[ ] 毛发、配件、品牌色点缀是否连续
[ ] 动作是否符合小狗身体结构
[ ] 脚步是否没有滑动
[ ] 身体是否没有漂浮
[ ] 镜头是否符合故事板对应 Shot
[ ] 灯光和情绪是否符合故事板对应 Shot
[ ] 是否能接入上一镜头和下一镜头
```

## Output（输出）

```text
COMMAND-005 Clip Review Result
Pass / Needs Revision
Revision Notes
```

---

# Stage 8 — Iteration Notes（迭代备注）

## Task（任务）

如果片段未通过审查，只能根据问题归因修改对应层：

```text
角色外观漂移 → 修改 Identity Card Prompt
镜头内容错误 → 修改 Storyboard Prompt / Storyboard Output
模型执行不清楚 → 修改 Universal Video Prompt
单个片段生成失败 → 重新生成该 Shot
剪辑衔接问题 → 记录到 Assembly Notes
```

不得为了修一个片段而临时改变 Jump 核心设定、故事目标或品牌语言。

## Output（输出）

```text
Iteration Notes
```

---

# Stage 9 — Assembly Notes（组装备注）

## Agent（执行智能体）

```text
AGENT-005 — Editing Agent
```

## Task（任务）

输出：

- 已通过审查的片段列表
- 镜头排列顺序
- 建议剪辑点
- 转场方式
- 字幕位置
- 音乐进入时间
- 环境音保留建议
- 片段备用方案

## Output（输出）

```text
Video Assembly Notes
```

---

# Final Output（最终输出）

完整工作流最终应输出：

```text
1. Runtime Input Review Result
2. Identity Card Verification Result
3. Storyboard Verification Result
4. Universal Video Prompt Verification Result
5. Shot Execution Plan
6. Clip Generation Package
7. COMMAND-005 Clip Review Result
8. Iteration Notes
9. Video Assembly Notes
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-003 for PROJ-001.

Input:
Identity Card Prompt
Storyboard Prompt / Storyboard Output
Universal Video Prompt

Target Model:
Jimeng / Kling / Veo / Runway

Output:
Shot execution plan and clip generation packages using uploaded identity card, uploaded storyboard and universal video prompt.
```

---

# Workflow Rules（工作流规则）

## Must Do（必须）

- 必须基于已确认身份卡
- 必须基于已确认故事板
- 必须使用通用视频 Prompt
- 必须逐镜头替换当前 Shot 名称
- 必须保持 Jump 是真实小狗本体形态并穿衣服
- 必须保持故事板黑白粗略铅笔线稿风格
- 必须保留故事板彩色动态标注系统
- 必须检查模型可复制 Prompt 是否没有裸露内部 ID
- 必须用 `COMMAND-005` 审查生成片段

---

## Never Do（禁止）

- 不得重新改写故事
- 不得重新设计 Jump
- 不得把 Jump 改成人形、半人身体或无衣服普通宠物狗
- 不得忽略分镜顺序
- 不得把所有 Shot 细节重复塞进每个视频 Prompt
- 不得让模型可复制 Prompt 依赖裸露内部 ID
- 不得省略连续性检查
- 不得省略负面规则
- 不得使用与品牌冲突的风格

---

# Related Files（关联文件）

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
commands/COMMAND-002.md
commands/COMMAND-005.md
workflows/WORKFLOW-002.md
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
agents/editor/AGENT-005.md
```

---

# Usage Scope（应用范围）

适用于：

- Storyboard to Video
- AI Video Generation
- Shot Execution Plan
- Clip Review
- Motion Continuity Check
- Video Assembly
- Series Production

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated workflow to use identity card, storyboard, universal video prompt and COMMAND-005 clip review |
| 1.0 | 2026 | Initial canonical workflow template |
