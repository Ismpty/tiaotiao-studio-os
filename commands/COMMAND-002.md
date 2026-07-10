# COMMAND-002 — Generate Video Prompt Package

> Operating Command（操作命令）  
> Category：Prompt Generation  
> Version：2.0  
> Status：Active

---

# 1. Purpose（目的）

`COMMAND-002` 用于生成视频生产所需的完整提示词包。

从 v2.0 开始，`COMMAND-002` 不再只输出单段视频 Prompt，而是输出三层结构：

```text
Identity Card Prompt
+
Storyboard Prompt
+
Universal Video Prompt
```

该结构用于提高主体一致性、镜头准确性、动作连续性和模型可执行性。

---

# 2. When to Use（什么时候使用）

当用户需要生成以下内容时，使用本命令：

```text
AI video prompt
即梦视频提示词
视频生成提示词
角色视频生成包
分镜视频生成包
故事板 + 视频 Prompt
短视频生成 Prompt
```

---

# 3. Required Inputs（必需输入）

执行本命令前，至少需要明确：

```text
Project ID
Subject Mode
Subject Type
Main Character
Story / Episode
Target Platform
Video Length
Visual Style
Character Form Rule
```

对于《小保安和他的古人朋友们》当前默认项目：

```text
Project:
PROJ-001 — Little Security Guard and His Ancient Friends

Character:
Jump / 跳跳 / AI 博物馆小保安

Character Form:
Real dog-form character wearing clothes

Toolchain:
Jimeng / 即梦
```

对于非 Jump 项目或临时创作主体：

```text
Subject Mode:
Custom Subject Mode

Subject Type:
Human / Animal / Plant / Object / Scene Subject / Mascot / Other

Subject Brief:
用户提供的主体描述、参考图、品牌资料或故事设定
```

---

# 4. Source References（内部来源）

输出时可以引用内部来源，但这些来源只用于 Git / Notion / Review / Consistency Check。

```text
CHAR-001
ASSET-001
EP-001
STORY-001
ENV-001
STYLE-001
COLOR-001
EMOTION-001
SUBJECT-001
RELIC-001
VISUALPARAM-001
BLOCKING-001
BRAND-001
```

---

# 5. Model-Readable Rule（模型可读规则）

任何复制进模型的 Prompt，必须是模型可读自然语言。

禁止只写：

```text
consistent with ASSET-001
follow CHAR-001
use STYLE-001
match BRAND-001
```

必须展开成：

```text
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，在 AI 博物馆里担任认真值班的小保安。她可以穿小狗尺寸的保安背心、小帽子、工牌或巡逻配件，也可以保留少量火龙果粉色点缀。禁止半人身体、人类手掌、人类手臂、人类双腿站立。
```

---

# 6. Output Structure（输出结构）

`COMMAND-002` 必须输出以下结构：

```text
1. Source References
2. Identity Card Prompt
3. Storyboard Prompt
4. Universal Video Prompt
5. Runtime Usage Example
6. Review Checklist
```

---

# 7. Identity Card Prompt Requirements（身份卡提示词要求）

身份卡 Prompt 必须用于锁定主体外观、结构和连续性。

默认引用：

```text
SUBJECT-001 — Generic Subject Identity Card Grammar
```

必须包含：

```text
主体名称
主体类型
核心视觉身份
形状 / 身体结构
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

对于 Jump Mode，必须明确：

```text
真实小狗本体形态
穿小狗尺寸的 AI 博物馆小保安服装或已确认小狗服装
可以背小包
可以有工牌 / 项圈挂饰
有少量火龙果粉色点缀
禁止半人拟人化
禁止人类手掌
禁止人类手臂
禁止人类双腿站立
```

对于 Custom Subject Mode，身份卡必须按主体类型展开：

```text
人物：年龄段、体型、脸部特征、发型、服装、姿态、职业或角色功能。
动物：物种、体型、毛发或皮肤、耳朵尾巴四肢、自然动作、是否穿戴配件。
植物：品种、株型、叶片、花果、枝干、盆器或生长环境、季节状态。
物体 / 产品：形状、材质、尺寸、功能部件、品牌或标识、使用场景。
场景主体：空间结构、入口出口、关键道具、光源、动线和视觉焦点。
```

Custom Subject Mode 不得自动套用 Jump 的小狗形态、小保安服装、火龙果粉色点缀或 AI 博物馆故事结构，除非用户明确要求。

---

# 8. Storyboard Prompt Requirements（故事板提示词要求）

故事板 Prompt 必须用于锁定：

```text
镜头结构
镜头顺序
角色位置
动作方向
道具位置
灯光变化
情绪变化
镜头衔接
基础画面参数
复杂空间调度图
```

## Fixed Storyboard Style

故事板主体必须采用：

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

---

# 9. Storyboard Color Annotation System（故事板彩色标注系统）

虽然故事板主体必须是黑白铅笔草图，但动态标注必须使用彩色系统：

```text
红色：镜头运动（camera movement）
蓝色：角色动作 / 小狗动作（character motion / dog movement）
黄色：道具 / 交互（prop interaction）
绿色：灯光 / 情绪（lighting / mood）
紫色：镜头衔接 / 转场（continuity / transition）
```

要求：

```text
彩色箭头清楚
动作方向明显
道具变化有圈注
灯光和情绪有标注
镜头衔接有提示
```

---

# 10. Universal Video Prompt Requirements（通用视频提示词要求）

当身份卡和故事板已经存在时，视频 Prompt 不应重复大量 Shot 细节。

通用结构必须为：

```text
请严格参考上传的主体身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

主体外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。
视频规格、动作要求、场景要求、镜头要求、灯光情绪和负面要求如下……
```

---

# 11. Visual Parameter Requirements（画面参数要求）

`COMMAND-002` 必须把基础画面参数转写成模型可读自然语言。

默认引用：

```text
VISUALPARAM-001 — AIGC Base Visual Parameter Grammar
```

视频 Prompt 至少应明确：

```text
format / aspect ratio
shot size
camera angle / height
lens
composition
depth of field
lighting
color / tone
texture detail
motion
continuity locks
negative constraints
```

模型可复制区域不能只写：

```text
use VISUALPARAM-001
```

必须写成自然语言，例如：

```text
使用竖屏 9:16 画幅，低位小狗视角平视机位，35mm 自然纪录片镜头，中等景深，暖色柔和实用光，真实毛发和布料质感，并保持跳跳的小狗身体结构、衣服、小包和场景比例连续。
```

---

# 12. Scene Blocking Map Requirements（场景调度图要求）

当视频涉及多人对话、追逐、打斗、复杂走位、一镜到底或多次镜头切换时，`COMMAND-002` 必须支持使用俯视场景调度图。

默认引用：

```text
BLOCKING-001 — Overhead Scene Blocking Map
```

模型可复制 Prompt 不能只写：

```text
use BLOCKING-001
```

必须写成自然语言，例如：

```text
请严格参考上传的俯视场景调度图。保持场景平面布局、角色初始站位、移动箭头、摄影机路径、门、道具、障碍物和左右关系一致。不要交换角色位置，不要反转移动方向，不要改变房间布局。
```

如果场景不复杂，可以写：

```text
No overhead blocking map required for this simple single-character shot.
```

---

# 13. Shot Detail Ownership（镜头细节归属）

`COMMAND-002` 必须遵守以下职责划分：

```text
Identity Card = 主体外观 / 结构 / 连续性
Storyboard = 镜头细节
Universal Video Prompt = 模型执行规则
```

不得把所有细节重复塞进每个 Shot Prompt。

---

# 14. Default Jump Character Form Rule（跳跳角色形态规则）

当前 Jump 系列默认规则：

```text
Jump must remain a real dog-form character wearing clothes.
No humanoid body.
No human hands.
No human arms.
No human legs.
No bipedal human standing pose.
```

中文规则：

```text
跳跳必须保持真实小狗本体形态。
可以穿衣服、背小包、戴配件。
禁止半人身体。
禁止人类手掌。
禁止人类手臂。
禁止人类双腿站立。
禁止人类比例四肢。
```

---

# 15. Custom Subject Mode Rule（自定义主体模式规则）

当本命令用于 Jump 之外的人物、动物、植物、物体、产品、场景或新 IP 时，必须进入 Custom Subject Mode。

Custom Subject Mode 必须遵守：

```text
以用户提供的主体描述、参考图或品牌资料为基础。
使用 SUBJECT-001 生成完整主体身份卡。
模型可复制 Prompt 必须用自然语言描述主体，不得只写 SUBJECT-001 或内部编号。
故事板继续使用黑白粗略铅笔线稿。
故事板继续保留红 / 蓝 / 黄 / 绿 / 紫彩色动态标注系统。
视频 Prompt 必须引用上传的主体身份卡和故事板。
COMMAND-005 必须检查主体类型、连续性锁定和负面约束。
```

Custom Subject Mode 禁止：

```text
自动把主体改成 Jump。
自动套用 Jump 的小狗身体、小保安服装、小包、工牌、项圈挂饰或火龙果粉色点缀。
自动套用《小保安和他的古人朋友们》的 AI 博物馆故事结构。
把人物、动物、植物、产品或场景主体混成另一个未确认主体。
```

---

# 16. Default AI Museum Story Structure Rule（默认 AI 博物馆故事结构规则）

《小保安和他的古人朋友们》系列不应只展示博物馆空镜或文物静态展示。

默认结构：

```text
闭馆 / 小保安巡逻
+
文物朋友苏醒与古今误会
+
无厘头升级与温暖解决
```

推荐比例：

```text
闭馆巡逻：10%–20%
文物朋友苏醒与误会：50%–60%
无厘头升级与温暖解决：20%–30%
```

博物馆片段可以包括：

```text
闭馆巡逻
展柜 AI 扫描
文物朋友从古画 / 器物 / 神兽纹样中苏醒
古人朋友误解现代展厅规则
文物抢展位
跳跳认真开小狗保安单
扫地机器人被误会成妖怪
古籍找 Wi-Fi
温暖和解
```

---

# 17. COMMAND-002 Output Example（输出示例）

执行本命令时，应输出类似结构：

```text
Source References:
CHAR-001
ASSET-001
STORY-001
STYLE-001
BRAND-001

Identity Card Prompt:
用于生成主体身份卡。

Storyboard Prompt:
用于生成黑白铅笔线条故事板，并保留彩色动态标注系统。

Universal Video Prompt:
用于拿身份卡 + 故事板逐镜头生成视频。
```

---

# 18. Runtime Usage（运行方式）

真实生产时执行顺序：

```text
1. Generate Identity Card
2. Generate Overhead Scene Blocking Map when needed
3. Generate Storyboard
4. Upload Identity Card + Storyboard + Blocking Map to video model when applicable
5. Use Universal Video Prompt
6. Replace [SHOT NUMBER AND NAME]
7. Generate clip
8. Review clip
9. Iterate if needed
```

---

# 19. Review Checklist（检查清单）

生成 Prompt 后，必须检查：

```text
[ ] 是否包含身份卡 Prompt
[ ] 是否明确 Jump Mode / Custom Subject Mode
[ ] 是否包含故事板 Prompt
[ ] 是否包含通用视频 Prompt
[ ] 模型可复制区域是否没有裸露内部编号
[ ] 内部编号是否已翻译成自然语言
[ ] Custom Subject 是否符合 SUBJECT-001 的主体身份卡字段
[ ] Custom Subject 是否没有误套 Jump 专属规则
[ ] 文物朋友是否符合 RELIC-001 的来源、材质、纹样和文化身份
[ ] 是否没有把文物朋友做成现代网红、恐怖鬼魂或欧美怪物
[ ] 故事板是否使用黑白铅笔线条风格
[ ] 故事板是否保留彩色动态标注系统
[ ] 画面参数是否明确、模型可读且符合 VISUALPARAM-001
[ ] 复杂空间是否需要俯视场景调度图
[ ] 若使用调度图，Prompt 是否用自然语言引用其站位、动线和摄影机路径
[ ] 视频 Prompt 是否避免重复 Shot 细节
[ ] 角色形态规则是否清楚
[ ] 负面要求是否清楚
```

---

# 20. Related Files（相关文件）

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
production/PROJ-001/VIDEO-PROMPTS.md
commands/COMMAND-005.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
knowledge/subject-identity/SUBJECT-001.md
knowledge/museum-relic-friends/RELIC-001.md
knowledge/visual-parameters/VISUALPARAM-001.md
knowledge/scene-blocking/BLOCKING-001.md
```

---

# 21. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.4 | 2026 | Updated default prompt package command for AI Museum relic-friend series |
| 2.3 | 2026 | Added SUBJECT-001 generic subject identity support and Custom Subject Mode |
| 2.2 | 2026 | Added BLOCKING-001 overhead scene blocking map requirements |
| 2.1 | 2026 | Added VISUALPARAM-001 visual parameter requirements for model-readable prompt packages |
| 2.0 | 2026 | Updated COMMAND-002 to generate identity card prompt, storyboard prompt and universal video prompt |
| 1.0 | 2026 | Initial short video prompt command |
