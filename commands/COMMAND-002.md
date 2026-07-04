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

该结构用于提高角色一致性、镜头准确性、动作连续性和模型可执行性。

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
Main Character
Story / Episode
Target Platform
Video Length
Visual Style
Character Form Rule
```

对于《跳跳下班啦》当前默认项目：

```text
Project:
PROJ-001 — Jump After Work Pilot Project

Character:
Jump / 跳跳

Character Form:
Real dog-form character wearing clothes

Toolchain:
Jimeng / 即梦
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
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，穿程序员风格小狗衣服，可以有小背包、工牌、项圈挂饰和少量火龙果粉色点缀。禁止半人身体、人类手掌、人类手臂、人类双腿站立。
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

身份卡 Prompt 必须用于锁定角色外观。

必须包含：

```text
角色名称
物种
身体形态
体貌特征
毛发特征
服装
配件
颜色点缀
禁止漂移规则
```

对于 Jump，必须明确：

```text
真实小狗本体形态
穿程序员风格小狗衣服
可以背小包
可以有工牌 / 项圈挂饰
有少量火龙果粉色点缀
禁止半人拟人化
禁止人类手掌
禁止人类手臂
禁止人类双腿站立
```

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
请严格参考上传的角色身份卡和故事板生成视频。

本次只生成故事板中的：
[SHOT NUMBER AND NAME]

角色外观以身份卡为准。
镜头内容以故事板对应 Shot 为准。
视频规格、动作要求、场景要求、镜头要求、灯光情绪和负面要求如下……
```

---

# 11. Shot Detail Ownership（镜头细节归属）

`COMMAND-002` 必须遵守以下职责划分：

```text
Identity Card = 角色外观
Storyboard = 镜头细节
Universal Video Prompt = 模型执行规则
```

不得把所有细节重复塞进每个 Shot Prompt。

---

# 12. Default Jump Character Form Rule（跳跳角色形态规则）

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

# 13. Default Story Structure Rule（默认故事结构规则）

《跳跳下班啦》系列不应只展示离开办公室。

默认结构：

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

生活片段可以包括：

```text
吃饭
逛超市
看电影
买小吃
散步
回家
洗澡
睡前放松
周末户外
```

---

# 14. COMMAND-002 Output Example（输出示例）

执行本命令时，应输出类似结构：

```text
Source References:
CHAR-001
ASSET-001
STORY-001
STYLE-001
BRAND-001

Identity Card Prompt:
用于生成角色身份卡。

Storyboard Prompt:
用于生成黑白铅笔线条故事板，并保留彩色动态标注系统。

Universal Video Prompt:
用于拿身份卡 + 故事板逐镜头生成视频。
```

---

# 15. Runtime Usage（运行方式）

真实生产时执行顺序：

```text
1. Generate Identity Card
2. Generate Storyboard
3. Upload Identity Card + Storyboard to video model
4. Use Universal Video Prompt
5. Replace [SHOT NUMBER AND NAME]
6. Generate clip
7. Review clip
8. Iterate if needed
```

---

# 16. Review Checklist（检查清单）

生成 Prompt 后，必须检查：

```text
[ ] 是否包含身份卡 Prompt
[ ] 是否包含故事板 Prompt
[ ] 是否包含通用视频 Prompt
[ ] 模型可复制区域是否没有裸露内部编号
[ ] 内部编号是否已翻译成自然语言
[ ] 故事板是否使用黑白铅笔线条风格
[ ] 故事板是否保留彩色动态标注系统
[ ] 视频 Prompt 是否避免重复 Shot 细节
[ ] 角色形态规则是否清楚
[ ] 负面要求是否清楚
```

---

# 17. Related Files（相关文件）

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
production/PROJ-001/VIDEO-PROMPTS.md
commands/COMMAND-005.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
```

---

# 18. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 2.0 | 2026 | Updated COMMAND-002 to generate identity card prompt, storyboard prompt and universal video prompt |
| 1.0 | 2026 | Initial short video prompt command |
