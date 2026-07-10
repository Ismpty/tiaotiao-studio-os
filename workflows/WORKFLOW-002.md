# WORKFLOW-002 — Short Video Prompt Workflow（短视频提示词工作流）

> Canonical Workflow Template（官方工作流模板）
> Version：2.0
> Status：Active

---

# Definition（定义）

## 中文

Short Video Prompt Workflow 是 TiaoTiao Studio OS 的短视频提示词生成工作流。

它用于把 GitHub 中确认过的 Project、Story、Subject / Character、Storyboard、Environment、Camera、Lighting、Motion、Asset 和 Knowledge Nodes，转换成真实 AI 模型可执行的视频生成提示词包。

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
- 用身份卡锁定 Jump 或 Custom Subject 的主体外观
- 用故事板锁定镜头顺序、动作和构图
- 用通用视频 Prompt 执行逐镜头生成
- 保持 Jump 是真实小狗本体形态、穿衣服的角色
- 支持人物、动物、植物、物体、产品、场景和新 IP 的自定义主体身份卡
- 保持故事板为黑白粗略铅笔线稿
- 保留故事板彩色动态标注系统
- 避免模型可复制 Prompt 依赖裸露内部 ID
- 让 `COMMAND-005` 可以进行最终一致性检查

---

# Default Project（默认项目）

本 Workflow 默认服务：

```text
PROJ-001 — Little Security Guard and His Ancient Friends
《小保安和他的古人朋友们》
```

默认故事结构：

```text
Museum Closing / Jump Patrol: 10%–20%
Relic Friend Awakening and Misunderstanding: 50%–60%
Absurd Escalation and Warm Resolution: 20%–30%
```

AI 博物馆日常可以包括：

```text
闭馆巡逻
文物朋友苏醒
古画人物走出展柜
青铜器抢展位
瓷器投诉灯光
神兽误会扫地机器人
古籍找 Wi-Fi
跳跳认真处理展厅突发事件
```

非 Jump 项目或临时创作主体使用：

```text
Subject Mode:
Custom Subject Mode

Subject Type:
Human / Animal / Plant / Object / Scene Subject / Mascot / Other

Subject Identity:
用户已确认的主体描述、参考图、品牌资料或按 SUBJECT-001 生成的身份卡
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
| Subject Identity | SUBJECT-001 | 自定义主体身份卡语法 |
| Relic Friends | RELIC-001 | AI 博物馆文物朋友语法 |

---

# Required Knowledge Nodes（必需知识节点）

| Category | Knowledge Node |
|---|---|
| Subject Identity | SUBJECT-001 |
| Relic Friends | RELIC-001 |
| Style | STYLE-001 |
| Color | COLOR-001 |
| World | WORLD-001 |
| Emotion | EMOTION-001 |
| Visual Parameters | VISUALPARAM-001 |
| Scene Blocking | BLOCKING-001 |
| Camera Language | SHOT-001 |
| Camera Consistency | SHOT-002 |
| Transition Language | TRANSITION-001 |
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
跳跳是一只保持真实小狗本体形态的毛茸茸小狗角色，在 AI 博物馆里担任认真值班的小保安。她可以穿小狗尺寸的保安背心、小帽子、工牌或巡逻配件，也可以保留少量火龙果粉色点缀。她必须保持四足真实小狗身体结构、蓬松毛发和小狗比例。禁止半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例、变成人类、变成其他动物或变成没有服装的普通宠物狗。
```

Relic Friend 示例：

```text
这位古人朋友来自一幅中国古代绢本女仙图。她被 AI 博物馆激活后成为真实国风仙子，仍保留原画的发冠珠饰、汉服纹样、瑞兽车驾、绢本旧色和东方神话气质，但她现在能在真实博物馆展厅里缓慢行动、认真误解现代安保规则，并和跳跳产生无厘头互动。
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
Subject Mode
Subject Type
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
- 主体模式：Jump Mode 或 Custom Subject Mode
- 主体类型：Jump / Human / Animal / Plant / Object / Scene Subject / Mascot / Other
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
[ ] 是否明确 Subject Mode
[ ] 是否明确 Subject Type
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
SUBJECT-001
RELIC-001
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
VISUALPARAM-001
BLOCKING-001
SHOT-001
SHOT-002
TRANSITION-001
MOTIONLANG-001
OUTFIT-001
BRAND-001
```

## Task（任务）

提取：

- Jump 的真实小狗本体形态规则
- Jump 的服装、配件、毛发和颜色点缀
- Custom Subject 的主体类型、核心视觉身份、连续性锁定和负面约束
- 文物朋友的来源、材质、纹样、时代气质和无厘头行为规则
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
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] 是否记录 Jump 必须是真实小狗本体形态并穿衣服
[ ] 若为 Custom Subject Mode，是否记录已确认主体身份卡或主体 brief
[ ] 若为文物朋友，是否记录 RELIC-001 来源、材质、纹样和文化身份
```

---

# Stage 3 — Identity Card Prompt（身份卡提示词）

## Purpose（目的）

身份卡 Prompt 用于生成或锁定 Jump 或 Custom Subject 的主体外观参考。

身份卡只负责主体外观、结构、比例、材质、识别特征和连续性锁定，不负责镜头叙事。

## Task（任务）

生成模型可读的身份卡 Prompt，必须包含：

```text
主体名称
主体类型
核心视觉身份
形状 / 身体结构 / 空间结构
比例 / 尺寸
材质 / 表面质感
颜色系统
识别特征
服装 / 配件 / 道具（如适用）
运动 / 行为方式
环境关系
连续性锁定
负面约束
```

## Required Jump Rule（Jump 必须规则）

```text
跳跳必须保持真实小狗本体形态。
跳跳必须穿小狗尺寸的 AI 博物馆小保安服装或其他已确认小狗服装。
跳跳可以背小包、戴工牌或项圈挂饰。
跳跳可以有少量火龙果粉色点缀。
跳跳必须保持蓬松毛发和四足小狗身体结构。
禁止半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例。
禁止变成人类、其他动物或没有服装的普通宠物狗。
```

## Custom Subject Identity Rule（自定义主体身份规则）

Custom Subject Mode 必须按 SUBJECT-001 展开主体身份：

```text
人物：年龄段、体型、脸部特征、发型、服装、姿态、职业或角色功能。
动物：物种、体型、毛发或皮肤、耳朵尾巴四肢、自然动作、是否穿戴配件。
植物：品种、株型、叶片、花果、枝干、盆器或生长环境、季节状态。
物体 / 产品：形状、材质、尺寸、功能部件、品牌或标识、使用场景。
场景主体：空间结构、入口出口、关键道具、光源、动线和视觉焦点。
```

Custom Subject Mode 不得自动套用 Jump 的小狗身体、小保安服装、小包、工牌、项圈挂饰、火龙果粉色点缀或 AI 博物馆故事结构，除非用户明确要求。

## Output（输出）

```text
Identity Card Prompt
```

## Required Check（必须检查）

```text
[ ] 是否完整描述主体外观
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] 是否明确 Jump 是真实小狗本体形态
[ ] 是否明确 Jump 穿衣服
[ ] 是否明确禁止人形化身体结构
[ ] Custom Subject 是否符合 SUBJECT-001 字段
[ ] Custom Subject 是否没有误套 Jump 专属规则
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
主体外观以身份卡为准
镜头内容以故事板对应 Shot 为准
视频规格
动作连续性
镜头连续性
灯光情绪
负面规则
```

## Required Structure（必须结构）

```text
请严格参考上传的主体身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

主体外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。

视频规格：
[duration / aspect ratio / frame style]

动作要求：
[subject-appropriate movement, no identity drift]

镜头要求：
[camera movement and framing rule]

灯光和情绪：
[lighting and mood rule]

连续性要求：
[match previous and next storyboard shots]

负面要求：
[forbidden character, style, motion, camera, lighting and continuity drift]
```

## Jump Mode Negative Rules（Jump 模式负面规则）

```text
不要改变跳跳的物种。不要把跳跳变成人类、半人角色、其他动物或没有服装的普通宠物狗。不要出现人类手掌、人类手臂、人类双腿站立、人类身体比例、直立人形姿态或人类式走路。不要移除蓬松毛发、小狗尺寸的 AI 博物馆小保安服装、工牌、项圈挂饰或火龙果粉色点缀。不要把文物朋友做成现代网红、恐怖鬼魂、廉价吉祥物或欧美奇幻怪物。不要使用彩色成片插画作为故事板主体。不要使用恐怖、暴力、黑暗反乌托邦、赛博蓝光、霓虹科幻光、游戏动画感、机器人动作、滑步、漂浮身体、极端广角畸变、无人机环绕、第一人称镜头、冷冰冰公司办公室、强销售广告感或标题党风格。
```

## Custom Subject Negative Rules（自定义主体负面规则）

Custom Subject Mode 必须根据主体身份卡写出专属负面规则：

```text
不要改变主体类型、核心形状、比例、材质、颜色系统、识别特征、配件、道具、运动方式或环境关系。不要把人物、动物、植物、产品或场景主体混成另一个未确认主体。不要自动套用 Jump 的小狗形态、服装、配件或故事比例。不要使用彩色成片插画作为故事板主体。
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
[ ] 是否明确主体外观以身份卡为准
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
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] Jump 是否被描述为真实小狗本体形态
[ ] Jump 是否穿小狗尺寸的 AI 博物馆小保安服装或已确认小狗服装
[ ] Jump 是否保留蓬松毛发、小包 / 工牌 / 项圈挂饰和火龙果粉色点缀
[ ] 是否明确禁止半人身体、人类手掌、人类手臂、人类双腿站立
[ ] Custom Subject 是否按 SUBJECT-001 展开成自然语言
[ ] Custom Subject 是否没有误套 Jump 专属规则
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
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] Jump 是否保持真实小狗本体形态并穿衣服
[ ] Custom Subject 是否符合已确认主体身份卡和 SUBJECT-001
[ ] Custom Subject 是否没有误套 Jump 专属规则
[ ] 故事板是否为黑白粗略铅笔线稿
[ ] 故事板是否保留彩色动态标注系统
[ ] Universal Video Prompt 是否按身份卡 + 故事板 + 当前 Shot 执行
[ ] 是否符合默认故事结构：闭馆巡逻、文物苏醒、古今误会、无厘头升级、温暖解决
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
1. Confirm Subject Mode: Jump Mode or Custom Subject Mode.
2. Use the Identity Card Prompt to generate or confirm the subject identity card.
3. Use the Storyboard Prompt to generate the black-and-white rough pencil storyboard with colored annotations.
4. Upload the identity card and storyboard to the video model.
5. Use the Universal Video Prompt.
6. Replace [SHOT NUMBER AND NAME] with the target storyboard shot.
7. Generate only that shot.
8. Review the output with COMMAND-005.
9. Revise identity card, storyboard or universal prompt only where the review identifies drift.
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-002 for PROJ-001.

Target Platform:
Jimeng / Kling / Veo / Runway

Subject Mode:
Jump Mode / Custom Subject Mode

Subject Type:
Jump / Human / Animal / Plant / Object / Scene Subject / Mascot / Other

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
| 2.1 | 2026 | Added SUBJECT-001 generic subject identity and Custom Subject Mode |
| 2.0 | 2026 | Updated workflow to use Identity Card Prompt, Storyboard Prompt, Universal Video Prompt, model-readable check and COMMAND-005 review |
| 1.0 | 2026 | Initial short video prompt workflow |
