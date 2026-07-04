# Prompt Runtime Rules（提示词运行规则）

> System Rule（系统规则）  
> Project：TiaoTiao Studio OS  
> Scope：Prompt Generation / Model Execution / Asset Consistency  
> Version：1.0  
> Status：Active

---

# 1. Purpose（目的）

本文档定义 TiaoTiao Studio OS 中所有提示词在真实模型中运行时必须遵守的规则。

TSOS 内部可以使用数据库编号、知识节点和系统索引，但任何真正复制进 AI 模型的 Prompt，必须转换成模型可理解的自然语言描述。

核心原则：

```text
Internal system language is not model language.
内部系统语言 ≠ 模型可读语言。
```

---

# 2. Source of Truth Rule（事实来源规则）

TiaoTiao Studio OS 的事实来源规则：

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

GitHub 存放正式规则、数据库、工作流、命令、智能体、生产记录和运行文档。

Notion 只作为可视化管理层，不作为最终事实来源。

---

# 3. Internal Reference Rule（内部索引规则）

以下内容属于 TSOS 内部索引：

```text
CHAR-001
ASSET-001
STYLE-001
BRAND-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
PROJ-001
```

这些编号可以用于：

```text
GitHub 文档
Notion 数据库
Production Records
Changelog
Review Logs
Consistency Check
Workflow Tracking
```

但不能直接作为模型提示词使用。

---

# 4. Forbidden Model Prompt Pattern（禁止的模型提示词写法）

禁止在可复制进模型的 Prompt 中只写：

```text
consistent with ASSET-001
follow CHAR-001
use STYLE-001
match BRAND-001
based on ENV-001
```

原因：

```text
模型不知道 ASSET-001 / CHAR-001 / STYLE-001 代表什么。
```

如果这些内部编号没有展开成自然语言，模型无法理解角色、风格、场景和品牌规则。

---

# 5. Required Model-Readable Pattern（必须使用的模型可读写法）

所有模型 Prompt 必须展开成自然语言描述。

## Example

内部引用：

```text
CHAR-001 — Jump
ASSET-001 — Jump Character Reference Pack
```

模型可读描述：

```text
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，穿程序员风格小狗衣服，可以背小包、戴工牌或项圈挂饰，有少量火龙果粉色点缀。她必须保持真实小狗身体结构，禁止半人身体、人类手掌、人类手臂、人类双腿站立。
```

---

# 6. Prompt Output Structure（提示词输出结构）

以后所有生产级 Prompt 必须分为两层：

## 1. Source References（内部来源）

用于 Git / Notion / Review / Consistency Check。

```text
CHAR-001
ASSET-001
STYLE-001
BRAND-001
ENV-001
```

## 2. Model-Readable Prompt（模型可读提示词）

用于复制进模型。

必须完整描述：

```text
角色
场景
动作
镜头
灯光
情绪
风格
负面要求
连续性规则
```

不得只出现内部编号。

---

# 7. Video Generation Prompt Architecture（视频生成提示词结构）

TSOS 以后默认采用三层视频生成结构：

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
```

这三层分别承担不同职责：

```text
Identity Card = 角色外观
Storyboard = 镜头细节
Universal Video Prompt = 模型执行规则
```

---

# 8. Identity Card Prompt Rule（身份卡提示词规则）

身份卡用于锁定角色外观。

身份卡 Prompt 必须说明：

```text
角色名称
物种
身体形态
体貌特征
毛发特征
脸部特征
体型
服装
配件
颜色点缀
禁止漂移规则
```

对于 Jump 当前设定，必须强调：

```text
真实小狗本体形态
穿衣服
可以背小包
可以戴工牌 / 项圈挂饰
少量火龙果粉色点缀
禁止半人拟人化
禁止人类手掌
禁止人类手臂
禁止人类双腿站立
禁止人类比例四肢
```

---

# 9. Storyboard Prompt Rule（故事板提示词规则）

故事板用于锁定：

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

故事板负责 Shot 细节。

当故事板已经存在时，不应该在每个视频 Prompt 里重复写大量 Shot 内容。

---

# 10. Fixed Storyboard Visual Style（固定故事板视觉风格）

所有 TSOS 故事板默认采用：

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

# 11. Storyboard Color Annotation System（故事板彩色标注系统）

虽然故事板主体必须是黑白铅笔草图，但必须保留彩色动态标注系统。

固定颜色规则：

```text
红色：镜头运动（camera movement）
蓝色：角色动作 / 小狗动作（character motion / dog movement）
黄色：道具 / 交互（prop interaction）
绿色：灯光 / 情绪（lighting / mood）
紫色：镜头衔接 / 转场（continuity / transition）
```

要求：

```text
彩色箭头必须清楚
动态变化必须明显
道具变化必须圈注
情绪和灯光必须标注
镜头连续性必须标出
黑白主体和彩色标注必须形成清晰对比
```

---

# 12. Universal Video Prompt Rule（通用视频提示词规则）

当身份卡和故事板已经存在时，视频 Prompt 不需要重复所有 Shot 细节。

正确结构：

```text
请严格参考上传的角色身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

角色外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。
视频规格、动作要求、场景要求、镜头要求、灯光情绪和负面要求如下……
```

避免为每个 Shot 重复大段角色设定、场景设定和负面要求。

---

# 13. Shot Detail Ownership（镜头细节归属）

TSOS 规定：

```text
身份卡负责角色外观。
故事板负责 Shot 细节。
通用视频 Prompt 负责模型执行规则。
```

也就是说：

```text
不要把所有细节都塞进视频 Prompt。
不要让视频 Prompt 替代故事板。
不要让故事板替代身份卡。
不要在模型可复制 Prompt 中裸露内部编号。
```

---

# 14. Real Dog Form Rule for Jump（跳跳小狗本体规则）

当前 Jump 系列使用以下角色规则：

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
禁止变成人类。
禁止变成其他动物。
```

---

# 15. Montage Story Rule（生活蒙太奇规则）

《跳跳下班啦》系列不应只展示离开办公室。

默认故事结构应为：

```text
少量下班动作
+
大量下班后的生活
```

推荐比例：

```text
办公室部分：10%–20%
下班后生活：80%–90%
```

适合内容：

```text
吃饭
逛超市
看电影
买小吃
夜晚散步
回家
洗澡
睡前放松
周末户外
```

---

# 16. Runtime Execution Order（运行顺序）

真实生产时，顺序固定为：

```text
1. Generate Identity Card
2. Generate Storyboard
3. Generate Shot Video
4. Review Clip
5. Iterate Prompt if needed
6. Approve Clip
7. Edit
8. Export
9. Publish
10. Review Performance
```

---

# 17. Review Gate（审片关卡）

任何生成结果必须检查：

```text
角色是否符合身份卡
镜头是否符合故事板
动作是否符合角色身体逻辑
画幅是否正确
风格是否偏移
是否出现禁止形态
是否可进入剪辑
```

如果角色形态错误，直接：

```text
FAIL
```

不能进入剪辑。

---

# 18. Prompt Compression Rule（提示词精简规则）

当已经有身份卡和故事板时，视频 Prompt 必须尽量精简。

应避免：

```text
每个 Shot 重复角色设定
每个 Shot 重复场景设定
每个 Shot 重复灯光规则
每个 Shot 重复负面词
```

应使用：

```text
一个 Universal Video Prompt
+
替换 [SHOT NUMBER AND NAME]
```

---

# 19. Failure Conditions（失败条件）

以下情况视为 Prompt Runtime 失败：

```text
模型可复制 Prompt 中只写 ASSET-001 / CHAR-001
没有身份卡 Prompt
没有故事板 Prompt
故事板变成彩色成片插画
故事板没有彩色动态标注系统
视频 Prompt 重复冗长
Jump 被描述成半人拟人角色
Jump 出现人类手掌 / 人类手臂 / 人类双腿站立
没有明确禁止角色形态漂移
```

---

# 20. Related Files（相关文件）

```text
commands/COMMAND-002.md
commands/COMMAND-005.md
agents/prompt-engineer/AGENT-002.md
agents/director/AGENT-001.md
workflows/WORKFLOW-002.md
workflows/WORKFLOW-003.md
production/PROJ-001/VIDEO-PROMPTS.md
ARCHITECTURE.md
README.md
CHANGELOG.md
```

---

# 21. Versioning Rule（版本规则）

当提示词结构发生重大变化时，需要升级版本。

示例：

```text
v1.0 — Direct shot prompts
v2.0 — Added identity card and storyboard
v3.0 — Revised Jump to real dog-form
v4.0 — Merged shot prompts into universal video prompt
```

---

# 22. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Added TSOS prompt runtime rules |