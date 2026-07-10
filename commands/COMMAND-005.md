# COMMAND-005 — Run Consistency Check（运行一致性检查）

> Canonical Operating Command（官方操作命令）  
> Version：2.0
> Status：Active

---

# Definition（定义）

## 中文

Run Consistency Check 是 TiaoTiao Studio OS 的一致性检查命令。

它用于检查任意 Project、Storyboard、Prompt、Script、Editing Plan、Publishing Package、主体身份卡或单个生成结果是否符合 TSOS 的 Source of Truth。

这个 Command 不负责创作新内容，也不负责修改角色、世界观或品牌方向。

它只负责检查：

当前输出是否仍然符合 Jump Mode 或 Custom Subject Mode、TiaoTiao Universe、Knowledge Nodes、Database Records、Agents 和 Workflow 的统一规范。

## English

Run Consistency Check is the consistency verification command of TiaoTiao Studio OS.

It checks whether any project output, storyboard, prompt, script, editing plan, publishing package or generated result follows the TSOS source of truth.

From v2.0, this command also checks the Prompt Runtime Architecture:

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Model-readable check
```

---

# Source of Truth Rule（事实来源规则）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

本命令必须以 GitHub 文件为正式依据。

Notion 只能作为可视化管理层、任务看板和同步界面，不能作为最终事实来源。

---

# Command Goal（命令目标）

本命令用于：

- 检查 Jump 角色一致性
- 检查 Custom Subject 主体身份一致性
- 检查世界观一致性
- 检查视觉风格一致性
- 检查色彩一致性
- 检查情绪一致性
- 检查动作一致性
- 检查镜头一致性
- 检查灯光一致性
- 检查提示词一致性
- 检查 Prompt Runtime 架构一致性
- 检查模型可复制 Prompt 是否模型可读
- 检查故事板黑白铅笔线稿和彩色标注系统
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
PROJ-001 — Little Security Guard and His Ancient Friends
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
| Music | MUSIC-001 |
| Story Formula | STORYFORMULA-001 |
| Brand Language | BRAND-001 |

---

# Related Workflows（关联工作流）

本命令可检查以下 Workflow 输出：

| Workflow | Name |
|---|---|
| WORKFLOW-001 | Little Security Guard Production Workflow |
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
4. Identify Subject Mode
↓
5. Check Subject / Character Consistency
↓
6. Check World Consistency
↓
7. Check Visual Consistency
↓
8. Check Motion / Camera / Transition / Lighting Consistency
↓
9. Check Story / Emotion / Brand Consistency
↓
10. Check Prompt Runtime Compliance
↓
11. Check Workflow Compliance
↓
12. Identify Issues
↓
13. Output Consistency Report
```

---

# Input Requirements（输入要求）

用户可以提供以下输入：

```text
Check Target:
Storyboard / Prompt / Prompt Package / Script / Editing Plan / Publishing Package / Generated Image / Generated Video / Project Package

Project:
PROJ-001 / Custom Project ID

Subject Mode:
Jump Mode / Custom Subject Mode

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
- 自动接受与 Custom Subject 已确认身份卡冲突的内容
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
2. Subject Mode Check
3. Subject / Character Consistency Check
4. World Consistency Check
5. Visual Style Check
6. Visual Parameter Check
7. Color Check
8. Emotion Check
9. Motion Check
10. Scene Blocking Check
11. Camera Check
12. Transition Check
13. Lighting Check
14. Story / Brand Check
15. Workflow Compliance Check
16. Prompt Runtime Compliance Check
17. Issue List
18. Fix Suggestions
19. Final Pass / Fail Result
```

---

# Output Format（输出格式）

输出必须使用以下结构：

```text
# COMMAND-005 Output

## 1. Consistency Summary

## 2. Subject Mode Check

## 3. Subject / Character Consistency Check

## 4. World Consistency Check

## 5. Visual Style Check

## 6. Visual Parameter Check

## 7. Color Check

## 8. Emotion Check

## 9. Motion Check

## 10. Scene Blocking Check

## 11. Camera Check

## 12. Transition Check

## 13. Lighting Check

## 14. Story / Brand Check

## 15. Workflow Compliance Check

## 16. Prompt Runtime Compliance Check

## 17. Issue List

## 18. Fix Suggestions

## 19. Final Result
```

---

# Check Level（检查等级）

## Light

适用于快速检查。

检查：

```text
Subject / Character
Brand
Major visual consistency
Major story consistency
```

---

## Standard

适用于普通生产检查。

检查：

```text
Subject / Character
World
Style
Visual Parameters
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
Subject / Character
World
Style
Color
Emotion
Outfit
Motion
Scene Blocking
Camera
Transition
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

# Subject Mode Check（主体模式检查）

默认对照：

```text
SUBJECT-001
RELIC-001
CHAR-001
ASSET-001
```

必须先判断：

```text
[ ] 当前输出是否明确属于 Jump Mode 或 Custom Subject Mode
[ ] Jump Mode 是否继续使用 CHAR-001 / ASSET-001 / OUTFIT-001
[ ] Custom Subject Mode 是否使用用户已确认主体身份卡
[ ] Custom Subject Mode 是否明确主体类型：Human / Animal / Plant / Object / Scene Subject / Mascot / Other
[ ] Custom Subject Mode 是否按 SUBJECT-001 展开主体身份，而不是裸露内部编号
[ ] Custom Subject Mode 是否没有自动套用 Jump 的小狗身体、小保安服装、小包、工牌、项圈挂饰或火龙果粉色点缀
[ ] 文物朋友是否按 RELIC-001 检查来源、材质、纹样、文化身份和无厘头行为逻辑
```

---

# Subject / Character Consistency Check（主体 / 角色一致性检查）

默认对照：

```text
SUBJECT-001
RELIC-001
CHAR-001
ASSET-001
OUTFIT-001
COLOR-001
```

Jump Mode 必须检查：

```text
[ ] Jump 是否保持真实小狗本体形态
[ ] Jump 是否保持四足小狗解剖结构
[ ] Jump 是否保持 AI 博物馆小保安身份
[ ] Jump 是否保持毛茸茸质感
[ ] Jump 是否穿小狗尺寸的 AI 博物馆小保安服装或已确认小狗服装
[ ] Jump 是否可保留小包 / 工牌 / 项圈挂饰
[ ] Jump 表情是否友好温暖
[ ] Jump 是否没有变成人类
[ ] Jump 是否没有变成其他动物
[ ] Jump 是否没有出现人类手掌、人类手臂、人类双腿或人类身体比例
[ ] Jump 是否没有变成无衣服的普通宠物狗
[ ] Jump 是否没有失去品牌色识别
[ ] 内部检查是否参考 ASSET-001
[ ] 服装检查是否符合 OUTFIT-001
```

Custom Subject Mode 必须检查：

```text
[ ] 主体名称是否一致
[ ] 主体类型是否一致
[ ] 核心视觉身份是否一致
[ ] 形状、身体结构或空间结构是否一致
[ ] 比例、尺寸和尺度关系是否一致
[ ] 材质、表面质感或生长状态是否一致
[ ] 颜色系统是否一致
[ ] 识别特征是否没有丢失
[ ] 服装、配件、道具或产品部件是否按身份卡保留
[ ] 运动、行为或环境关系是否符合主体类型
[ ] 连续性锁定是否被执行
[ ] 负面约束是否覆盖主体漂移
[ ] 模型可复制 Prompt 是否把 SUBJECT-001 展开成自然语言
[ ] 若主体是文物朋友，是否把 RELIC-001 展开成自然语言
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
[ ] 是否仍然服务《小保安和他的古人朋友们》系列
[ ] 是否没有新增未确认世界观
[ ] 是否没有加入黑暗、恐怖、暴力或极端设定
[ ] 是否保持 AI 博物馆、文物朋友、温暖无厘头和文化错位喜剧基调
[ ] 是否符合 PROJ-001 的小保安系列目标
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
[ ] 是否保持真实电影感和 AI 博物馆夜间展厅视觉
[ ] 是否没有变成游戏渲染感
[ ] 是否没有变成廉价 CGI
[ ] 是否没有过度卡通化
[ ] 是否没有恐怖片风格
[ ] 是否没有赛博朋克风格
[ ] 文物朋友是否保留来源材质、纹样、色彩和文化身份
[ ] 是否符合 TiaoTiao Studio 温暖、真实、乐观的品牌气质
```

---

# Visual Parameter Check（画面参数检查）

默认对照：

```text
VISUALPARAM-001
STYLE-001
COLOR-001
SHOT-001
SHOT-002
TRANSITION-001
```

必须检查：

```text
[ ] 是否明确画幅 / 比例
[ ] 是否明确景别
[ ] 是否明确机位 / 摄影机高度
[ ] 是否明确焦段或镜头观感
[ ] 构图是否服务故事和角色连续性
[ ] 景深是否不会遮蔽角色、服装或场景错误
[ ] 灯光参数是否符合真实、温暖、自然的 TSOS 风格
[ ] 色彩参数是否符合 COLOR-001 且不过度泛滥品牌色
[ ] 材质参数是否避免塑料、玩具、游戏渲染感
[ ] 运动参数是否适合视频生成并符合物理惯性
[ ] 连续性参数是否锁定角色、服装、道具、场景和比例
[ ] 模型可复制区域是否没有只写 VISUALPARAM-001 这类裸露内部 ID
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
[ ] 是否表达闭馆后文物朋友醒来的好奇、温暖和无厘头反差
[ ] 是否有温暖、治愈、博物馆夜间日常感
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

# Scene Blocking Check（场景调度检查）

默认对照：

```text
BLOCKING-001
SHOT-002
VISUALPARAM-001
MOTIONLANG-001
TRANSITION-001
```

必须检查：

```text
[ ] 当前场景是否需要俯视场景调度图
[ ] 若需要，是否明确场景边界、门、出口、障碍物和关键道具
[ ] 是否明确每个角色的初始站位
[ ] 是否明确角色移动路线和行动方向
[ ] 是否明确摄影机起点和摄影机运动路径
[ ] 是否标出镜头切换点、转场点或关键动作点
[ ] 左右关系、前后关系、距离关系是否稳定
[ ] 分镜是否遵守俯视调度图
[ ] 视频 Prompt 是否用模型可读自然语言引用上传的调度图
[ ] Jump 是否仍以真实小狗本体形态和小狗高度运动逻辑呈现
```

---

# Camera Check（镜头检查）

默认对照：

```text
CAM-001
SHOT-001
SHOT-002
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

# Transition Check（转场检查）

默认对照：

```text
TRANSITION-001
SHOT-001
SHOT-002
MOTIONLANG-001
```

必须检查：

```text
[ ] 转场是否服务故事、动作、光影、时间、空间或剪辑节奏
[ ] 转场是否有可见载体或明确剪辑逻辑
[ ] 转场是否有清楚的触发锚点
[ ] 下一个镜头是否被清晰揭示
[ ] 角色身份、服装、道具和运动方向是否连续
[ ] Jump 是否保持真实小狗本体形态并穿衣服
[ ] 转场是否没有制造人类手掌、人类手臂、人类腿或人形站姿
[ ] 分镜中的紫色标注是否用于连续性 / 转场
[ ] 模型可复制转场描述是否使用自然语言而不是裸露内部 ID
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
[ ] 是否保持 Warm Museum Night Lighting
[ ] 是否有展柜柔光 / 展签低亮度光 / AI 扫描柔光 / 夜间安保通道暖光
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
[ ] 是否符合 Museum Closing / Jump Patrol / Relic Awakening / Ancient-Modern Misunderstanding / Absurd Escalation / Warm Resolution 结构
[ ] 是否体现“闭馆以后，朋友们才刚刚上班”
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
[ ] Prompt 是否列出 Source References 用于内部审查
[ ] Prompt 是否在内部审查区引用 ASSET-001
[ ] Prompt 是否包含 Negative Prompt
[ ] Prompt 是否适配目标模型
[ ] Prompt 是否没有临时修改 Jump
[ ] Prompt 是否没有省略关键视觉约束
[ ] Prompt 是否可直接执行
[ ] 模型可复制区域是否没有裸露内部 ID
[ ] 内部 ID 是否已经展开成自然语言描述
```

---

# Prompt Runtime Compliance Check（提示词运行架构合规检查）

默认对照：

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
COMMAND-002
WORKFLOW-002
AGENT-002
```

必须检查：

```text
[ ] 是否包含 Identity Card Prompt
[ ] 是否包含 Storyboard Prompt
[ ] 是否包含 Universal Video Prompt
[ ] 是否包含 Model-readable check
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] Identity Card Prompt 是否完整描述 Jump 的角色外观
[ ] Identity Card Prompt 是否明确 Jump 是真实小狗本体形态并穿衣服
[ ] Custom Subject 的 Identity Card Prompt 是否按 SUBJECT-001 完整描述主体类型、外观、结构、材质、颜色、识别特征、行为、连续性锁定和负面约束
[ ] Custom Subject 是否没有误套 Jump 的小狗形态、服装、配件或故事比例
[ ] Storyboard Prompt 是否使用黑白粗略铅笔线稿
[ ] Storyboard Prompt 是否保留彩色动态标注系统
[ ] Storyboard Prompt 是否没有变成彩色成片插画、真实渲染或儿童绘本风
[ ] Universal Video Prompt 是否引用上传身份卡
[ ] Universal Video Prompt 是否引用上传故事板
[ ] 如使用俯视场景调度图，Universal Video Prompt 是否引用上传调度图
[ ] Universal Video Prompt 是否使用当前 Shot 名称执行
[ ] Universal Video Prompt 是否避免重复大量 Shot 细节
[ ] Shot 细节是否归属 Storyboard
[ ] 转场细节是否归属 Storyboard 或当前 Shot 的 Transition To Next Shot
[ ] 基础画面参数是否已转写成模型可读自然语言
[ ] 模型可复制区域是否没有裸露 SUBJECT-001 / CHAR-001 / ASSET-001 / STYLE-001 / BRAND-001 等内部编号
[ ] 内部来源是否已翻译成模型可读自然语言
```

## Forbidden Model-Facing Prompt Patterns（模型提示词禁止写法）

模型可复制 Prompt 中禁止只写：

```text
consistent with ASSET-001
follow CHAR-001
use STYLE-001
match BRAND-001
based on ENV-001
use SUBJECT-001
```

必须改写成自然语言，例如：

```text
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，穿小狗尺寸的 AI 博物馆小保安服装，可以有小背包、工牌、项圈挂饰、小型巡逻配件和少量火龙果粉色点缀。禁止半人身体、人类手掌、人类手臂、人类双腿站立、人类身体比例和人类保安形象。文物朋友必须保留中国文物、古画、器物或神话纹样来源，不能变成现代网红、恐怖鬼魂、廉价吉祥物或欧美奇幻怪物。
```

---

# Storyboard Runtime Check（故事板运行检查）

默认对照：

```text
COMMAND-003
WORKFLOW-002
WORKFLOW-003
AGENT-001
```

必须检查：

```text
[ ] 故事板主体是否是黑白线条
[ ] 故事板主体是否是粗略铅笔线稿
[ ] 故事板是否保持极简细节、快速动态描绘、简单解剖结构和清晰轮廓
[ ] 故事板是否有导演前期预演分镜草图感
[ ] 红色标注是否用于镜头运动
[ ] 蓝色标注是否用于角色 / 小狗动作
[ ] 黄色标注是否用于道具 / 交互
[ ] 绿色标注是否用于灯光 / 情绪
[ ] 紫色标注是否用于连续性 / 转场
[ ] 彩色标注是否清楚但没有把故事板主体变成彩色成片
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
运行 COMMAND-005，检查这份视频 Prompt Package。
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
- 必须读取 14 个 Knowledge Nodes
- 必须检查 SUBJECT-001 或已确认主体身份卡
- 必须检查 ASSET-001
- 必须检查 GitHub 是否仍是 Source of Truth
- 必须检查 Notion 是否只作为 Visual Management Layer
- 必须检查模型可复制 Prompt 是否模型可读
- 必须检查模型可复制 Prompt 是否没有裸露内部 ID
- 必须检查 Identity Card Prompt / Storyboard Prompt / Universal Video Prompt 结构
- 必须检查故事板黑白铅笔线稿和彩色动态标注系统
- 必须检查转场是否符合 TRANSITION-001
- 必须检查基础画面参数是否符合 VISUALPARAM-001
- 必须检查复杂场景调度是否符合 BLOCKING-001
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
- 不得把 Notion 当作 Source of Truth
- 不得让模型可复制 Prompt 依赖 SUBJECT-001 / CHAR-001 / ASSET-001 / STYLE-001 / BRAND-001 等裸露内部编号
- 不得接受缺少身份卡的正式视频 Prompt 包
- 不得接受缺少故事板的正式视频 Prompt 包
- 不得接受彩色成片插画作为故事板主体
- 不得接受 Jump 被改成人形、半人身体或无衣服普通宠物狗
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
docs/studio-os/PROMPT-RUNTIME-RULES.md
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
knowledge/subject-identity/SUBJECT-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/world/WORLD-001.md
knowledge/emotion/EMOTION-001.md
knowledge/visual-parameters/VISUALPARAM-001.md
knowledge/scene-blocking/BLOCKING-001.md
knowledge/camera-language/SHOT-001.md
knowledge/camera-language/SHOT-002.md
knowledge/transition-language/TRANSITION-001.md
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
| 2.4 | 2026 | Added SUBJECT-001 subject mode and custom subject consistency checks |
| 2.3 | 2026 | Added BLOCKING-001 scene blocking consistency checks |
| 2.2 | 2026 | Added VISUALPARAM-001 visual parameter consistency checks |
| 2.1 | 2026 | Added TRANSITION-001 transition consistency checks |
| 2.0 | 2026 | Added Prompt Runtime checks for model-readable prompts, identity card, storyboard style, color annotation system and universal video prompt structure |
| 1.0 | 2026 | Initial canonical operating command |
