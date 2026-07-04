# WORKFLOW-002 — Short Video Prompt Workflow（短视频提示词工作流）

> Canonical Workflow Template（官方工作流模板）
> Version：2.0
> Status：Active

---

# Definition（定义）

## 中文

Short Video Prompt Workflow 是 TiaoTiao Studio OS 的短视频提示词生成工作流。

它用于把 GitHub 中确认过的 Project、Story、Character、Storyboard、Environment、Camera、Lighting、Motion、Asset 和 Knowledge Nodes，转换成真实 AI 模型可执行的视频生成提示词包。

从 v2.0 开始，本 Workflow 不再为每个 Shot 生成大量重复的长视频 Prompt。

标准结构改为：

```text
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

## English

Short Video Prompt Workflow is the short-video prompt generation workflow of TiaoTiao Studio OS.

It converts confirmed GitHub source records and knowledge nodes into a model-readable video prompt package for real AI video production.

Starting from v2.0, this workflow no longer creates duplicated long per-shot prompts. Shot details belong to the storyboard. The video prompt remains compact and refers to the uploaded identity card, uploaded storyboard and current shot name.

---

# Source of Truth Rule（事实来源规则）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

本 Workflow 必须以 GitHub 文件为正式依据。

Notion 可以用于可视化管理、进度看板和任务追踪，但不得作为最终事实来源。

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 生成可直接用于 AI 视频生产的提示词包
- 用身份卡锁定 Jump 角色外观
- 用故事板锁定镜头顺序、动作和构图
- 用通用视频 Prompt 执行逐镜头生成
- 保持 Jump 是真实小狗本体形态、穿衣服的角色
- 保持故事板为黑白粗略铅笔线稿
- 保留故事板彩色动态标注系统
- 避免模型可复制 Prompt 依赖裸露内部 ID
- 让 `COMMAND-005` 可以进行最终一致性检查

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

下班后生活可以包括：

```text
晚饭
逛超市
看电影
买街边小吃
夜间散步
回家
洗澡
睡前放松
周末户外生活
```

---

# Required Source References（必需内部来源）

以下内部编号可以用于 GitHub 文档、Notion 管理、Review、Changelog 和一致性检查。

但它们不得裸露在模型可复制 Prompt 中。

| Source | Record | Purpose |
|---|---|---|
| Project DB | PROJ-001 | 项目目标 |
| Character DB | CHAR-001 | Jump 角色身份 |
| Asset DB | ASSET-001 | Jump 角色参考资产 |
| Story DB | STORY-001 | 故事目标 |
| Environment DB | ENV-001 | 场景设定 |
| Motion DB | MOT-001 | 动作资产 |
| Camera DB | CAM-001 | 镜头资产 |
| Lighting DB | LGT-001 | 灯光资产 |
| Prompt DB | PROMPT-001 | 提示词规则 |

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
| Brand Language | BRAND-001 |

---

# Required Agent（必需智能体）

| Agent | Role |
|---|---|
| AGENT-002 | Prompt Engineer Agent |

---

# Optional Agent Inputs（可选智能体输入）

| Agent | Output |
|---|---|
| AGENT-001 | Storyboard Output |
| AGENT-003 | Cinematography Output |
| AGENT-004 | Script Output |
| AGENT-005 | Editing Output |

---

# Model-Readable Rule（模型可读规则）

内部来源可以在 `Source References` 中列出。

模型可复制 Prompt 必须写成自然语言。

## Forbidden in Model-Facing Prompts（模型提示词禁止写法）

```text
consistent with ASSET-001
follow CHAR-001
use STYLE-001
match BRAND-001
based on ENV-001
```

## Required Model-Facing Pattern（模型提示词必须写法）

```text
跳跳是一只保持真实小狗本体形态的毛茸茸小狗角色，穿程序员风格小狗衣服，可以背小包、戴工牌或项圈挂饰，身上可以有少量火龙果粉色点缀。她必须保持四足真实小狗身体结构、蓬松毛发和小狗比例。禁止半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例、变成人类、变成其他动物或变成没有服装的普通宠物狗。
```

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Prompt Task Setup
↓
2. Source Reference Collection
↓
3. Identity Card Prompt
↓
4. Storyboard Prompt
↓
5. Universal Video Prompt
↓
6. Model-readable check
↓
7. COMMAND-005 review
↓
8. Final Prompt Package
```

---

# Stage 1 — Prompt Task Setup（提示词任务初始化）

## Input（输入）

确认本次视频提示词任务：

```text
Project
Episode / Story
Target platform
Target model
Video length
Aspect ratio
Language
Required outputs
```

## Task（任务）

确定：

- 目标平台，例如 Jimeng / 即梦、Kling、Veo、Runway
- 输出比例
- 是否需要中英文 Prompt
- 是否需要身份卡图
- 是否需要故事板图
- 是否逐镜头生成视频
- 是否已有可上传的身份卡和故事板

## Output（输出）

```text
Prompt Task Brief
```

## Required Check（必须检查）

```text
[ ] 是否明确目标项目
[ ] 是否明确目标模型 / 平台
[ ] 是否明确视频长度
[ ] 是否明确画幅比例
[ ] 是否明确需要 Identity Card Prompt
[ ] 是否明确需要 Storyboard Prompt
[ ] 是否明确需要 Universal Video Prompt
```

---

# Stage 2 — Source Reference Collection（来源记录收集）

## Input（输入）

读取 GitHub 中的正式来源：

```text
PROJ-001
CHAR-001
ASSET-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
MOTIONLANG-001
OUTFIT-001
BRAND-001
```

## Task（任务）

提取：

- Jump 的真实小狗本体形态规则
- Jump 的服装、配件、毛发和颜色点缀
- 故事目标和情绪
- 场景和道具
- 动作、镜头、灯光和转场要求
- 品牌语言和负面规则
- 默认故事比例

## Output（输出）

```text
Source References
Source Summary
```

## Required Check（必须检查）

```text
[ ] 是否只把内部编号用于 Source References / Review
[ ] 是否以 GitHub 文件为事实来源
[ ] 是否没有把 Notion 当作 canonical source
[ ] 是否没有临时新增未确认设定
[ ] 是否记录 Jump 必须是真实小狗本体形态并穿衣服
```

---

# Stage 3 — Identity Card Prompt（身份卡提示词）

## Purpose（目的）

身份卡 Prompt 用于生成或锁定 Jump 的角色外观参考。

身份卡只负责角色外观，不负责镜头叙事。

## Task（任务）

生成模型可读的身份卡 Prompt，必须包含：

```text
角色名称
物种
身体形态
四足小狗解剖结构
毛发特征
脸部特征
体型
服装
配件
颜色点缀
禁止漂移规则
```

## Required Jump Rule（Jump 必须规则）

```text
跳跳必须保持真实小狗本体形态。
跳跳必须穿程序员风格小狗衣服。
跳跳可以背小包、戴工牌或项圈挂饰。
跳跳可以有少量火龙果粉色点缀。
跳跳必须保持蓬松毛发和四足小狗身体结构。
禁止半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例。
禁止变成人类、其他动物或没有服装的普通宠物狗。
```

## Output（输出）

```text
Identity Card Prompt
```

## Required Check（必须检查）

```text
[ ] 是否完整描述 Jump 外观
[ ] 是否明确 Jump 是真实小狗本体形态
[ ] 是否明确 Jump 穿衣服
[ ] 是否明确禁止人形化身体结构
[ ] 是否没有裸露内部 ID
[ ] 是否可以直接复制进模型
```

---

# Stage 4 — Storyboard Prompt（故事板提示词）

## Purpose（目的）

故事板 Prompt 用于生成或锁定镜头细节。

故事板负责：

```text
镜头结构
镜头顺序
角色位置
动作方向
道具位置
灯光变化
情绪变化
镜头衔接
连续性提示
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

禁止：

```text
彩色成片插画
真实渲染成片感
精修概念图
儿童绘本风
漫画上色成稿感
```

## Storyboard Color Annotation System（故事板彩色标注系统）

虽然故事板主体必须是黑白粗略铅笔线稿，但动态标注必须保留彩色系统：

```text
Red / 红色：camera movement / 镜头运动
Blue / 蓝色：character or dog movement / 角色动作、小狗动作
Yellow / 黄色：prop interaction / 道具、交互
Green / 绿色：lighting or mood / 灯光、情绪
Purple / 紫色：continuity or transition / 连续性、转场
```

## Output（输出）

```text
Storyboard Prompt
```

## Required Check（必须检查）

```text
[ ] 是否使用黑白粗略铅笔线稿
[ ] 是否保留彩色动态标注系统
[ ] 是否清楚说明每个 Shot 的镜头内容
[ ] 是否清楚说明 Jump 的动作方向
[ ] 是否清楚说明道具和场景变化
[ ] 是否清楚说明灯光和情绪变化
[ ] 是否清楚说明镜头衔接
[ ] 是否没有把故事板做成彩色成片插画
[ ] 是否没有裸露内部 ID
```

---

# Stage 5 — Universal Video Prompt（通用视频提示词）

## Purpose（目的）

Universal Video Prompt 用于在身份卡和故事板已经存在时，逐镜头生成视频。

它不重复所有 Shot 细节。

它只说明：

```text
上传身份卡
上传故事板
当前生成哪个 Shot
角色外观以身份卡为准
镜头内容以故事板对应 Shot 为准
视频规格
动作连续性
镜头连续性
灯光情绪
负面规则
```

## Required Structure（必须结构）

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

## Standard Negative Rules（标准负面规则）

```text
不要改变跳跳的物种。不要把跳跳变成人类、半人角色、其他动物或没有服装的普通宠物狗。不要出现人类手掌、人类手臂、人类双腿站立、人类身体比例、直立人形姿态或人类式走路。不要移除蓬松毛发、程序员风格小狗衣服、小包、工牌、项圈挂饰或火龙果粉色点缀。不要使用彩色成片插画作为故事板主体。不要使用恐怖、暴力、黑暗反乌托邦、赛博蓝光、霓虹科幻光、游戏动画感、机器人动作、滑步、漂浮身体、极端广角畸变、无人机环绕、第一人称镜头、杂乱办公室、冷冰冰公司办公室、强销售广告感或标题党风格。
```

## Output（输出）

```text
Universal Video Prompt
```

## Required Check（必须检查）

```text
[ ] 是否引用上传身份卡
[ ] 是否引用上传故事板
[ ] 是否要求替换 [SHOT NUMBER AND NAME]
[ ] 是否避免重复大量 Shot 细节
[ ] 是否明确角色外观以身份卡为准
[ ] 是否明确镜头内容以故事板对应 Shot 为准
[ ] 是否包含负面规则
[ ] 是否没有裸露内部 ID
```

---

# Stage 6 — Model-readable Check（模型可读检查）

## Purpose（目的）

模型可读检查用于确认所有可复制进模型的 Prompt 都能被模型直接理解。

## Task（任务）

检查以下区域：

```text
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Negative Rules
Runtime Usage Example
```

## Checklist（检查表）

```text
[ ] 模型可复制区域是否没有裸露内部 ID
[ ] 内部编号是否已经翻译成自然语言
[ ] Jump 是否被描述为真实小狗本体形态
[ ] Jump 是否穿程序员风格小狗衣服
[ ] Jump 是否保留蓬松毛发、小包 / 工牌 / 项圈挂饰和火龙果粉色点缀
[ ] 是否明确禁止半人身体、人类手掌、人类手臂、人类双腿站立
[ ] 故事板主体是否是黑白粗略铅笔线稿
[ ] 故事板是否保留红 / 蓝 / 黄 / 绿 / 紫彩色标注系统
[ ] Universal Video Prompt 是否紧凑并引用身份卡和故事板
[ ] Shot 细节是否归属 Storyboard，而不是重复塞进每个视频 Prompt
[ ] 负面规则是否覆盖角色、风格、动作、镜头、灯光和连续性漂移
```

## Output（输出）

```text
Model-readable Check Report
```

---

# Stage 7 — COMMAND-005 Review（COMMAND-005 一致性审查）

## Purpose（目的）

在提示词包交付前，必须运行或模拟 `COMMAND-005` 一致性检查。

## Task（任务）

使用 `COMMAND-005` 检查：

```text
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check Report
```

## Required Review Items（必须审查项）

```text
[ ] GitHub 是否仍是 Source of Truth
[ ] Notion 是否只作为 Visual Management Layer
[ ] 身份卡是否存在并可上传
[ ] 故事板是否存在并可上传
[ ] 模型可复制 Prompt 是否不依赖裸露内部 ID
[ ] Jump 是否保持真实小狗本体形态并穿衣服
[ ] 故事板是否为黑白粗略铅笔线稿
[ ] 故事板是否保留彩色动态标注系统
[ ] Universal Video Prompt 是否按身份卡 + 故事板 + 当前 Shot 执行
[ ] 是否符合默认故事比例：办公室 10%–20%，下班后生活 80%–90%
[ ] 是否没有新增未确认设定
```

## Output（输出）

```text
COMMAND-005 Review Result
Pass / Needs Revision
Revision Notes
```

---

# Stage 8 — Final Prompt Package（最终提示词包）

最终输出必须包含：

```text
1. Source References
2. Prompt Task Brief
3. Identity Card Prompt
4. Storyboard Prompt
5. Universal Video Prompt
6. Runtime Usage Example
7. Model-readable Check Report
8. COMMAND-005 Review Result
9. Usage Notes
```

---

# Final Output Template（最终输出模板）

```text
# Short Video Prompt Package

## Source References

## Prompt Task Brief

## Identity Card Prompt

## Storyboard Prompt

## Universal Video Prompt

## Runtime Usage Example

## Model-readable Check Report

## COMMAND-005 Review Result

## Usage Notes
```

---

# Runtime Usage Example（运行示例）

```text
1. Use the Identity Card Prompt to generate or confirm Jump's identity card.
2. Use the Storyboard Prompt to generate the black-and-white rough pencil storyboard with colored annotations.
3. Upload the identity card and storyboard to the video model.
4. Use the Universal Video Prompt.
5. Replace [SHOT NUMBER AND NAME] with the target storyboard shot.
6. Generate only that shot.
7. Review the output with COMMAND-005.
8. Revise identity card, storyboard or universal prompt only where the review identifies drift.
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-002 for PROJ-001.

Target Platform:
Jimeng / Kling / Veo / Runway

Required Output:
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check
COMMAND-005 Review
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated workflow to use Identity Card Prompt, Storyboard Prompt, Universal Video Prompt, model-readable check and COMMAND-005 review |
| 1.0 | 2026 | Initial short video prompt workflow |
