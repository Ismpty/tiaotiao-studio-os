# PROJ-001 — Video Generation Package（视频生成总包）

> Production Output（生产输出）  
> Project：PROJ-001 — Jump After Work Pilot Project  
> Toolchain：Jimeng / 即梦  
> Version：4.0
> Status：Production Ready  
> Core Character Rule：Jump must remain a real dog-form character wearing clothes. No humanoid body.

---

# 1. Purpose（目的）

本文件是 PROJ-001 的统一视频生成包。

它包含：

```text
1. Identity Card Prompt（身份卡提示词）
2. Storyboard Prompt（故事板提示词）
3. Universal Video Prompt（通用视频提示词）
4. Model-readable Check（模型可读检查）
5. COMMAND-005 Review（COMMAND-005 复核）
```

正式生产顺序：

```text
先生成身份卡
↓
再生成故事板
↓
再拿身份卡 + 故事板 + 通用视频 Prompt + 当前镜头名称去即梦生成视频
↓
每个镜头生成后运行 COMMAND-005 review
```

---

# 2. Core Character Rule（角色核心规则）

跳跳必须保持 **小狗本体形态**。

跳跳不是半人拟人角色，不是人形站立角色，不是人类比例身体。  
她是一只真实小狗形态的毛茸茸小狗，可以穿衣服、背小包、戴配件、坐在办公椅上、前爪搭在桌边、看电脑、自然走动。

## Required

```text
跳跳 = 小狗本体形态
真实小狗身体结构
四足动物体态
毛茸茸
穿程序员风格小狗衣服
可以有小背包 / 工牌 / 项圈 / 火龙果粉色点缀
聪明、温暖、轻松、治愈
```

## Forbidden

```text
禁止半人身体
禁止人类躯干
禁止人类手掌
禁止人类手臂
禁止人类双腿站立
禁止人类比例四肢
禁止拟人化半人角色
禁止变成人类
禁止变成其他动物
禁止肌肉体型
禁止普通裸体宠物狗
```

---

# 3. Model Usage Rule（模型使用规则）

## Internal References（内部索引）

以下内容只用于内部管理，不直接复制进模型：

```text
CHAR-001
ASSET-001
ENV-001
STYLE-001
COLOR-001
EMOTION-001
BRAND-001
```

## Model-Readable Rule（模型可读规则）

复制进即梦的 Prompt 必须是完整自然语言描述。

禁止只写：

```text
consistent with ASSET-001
use STYLE-001
follow CHAR-001
```

必须展开成模型可读描述，例如：

```text
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，穿浅色程序员风格小狗卫衣，带少量火龙果粉色点缀，身体轻盈，表情温暖聪明。
```

---

# 4. Generation Order（生成顺序）

## Step 1 — Generate Identity Card

先生成：

```text
Jump-Identity-Card-v02.jpg
```

## Step 2 — Generate Storyboard

再生成：

```text
PROJ-001-Storyboard-v02.jpg
```

## Step 3 — Generate Video Clips

最后拿着：

```text
Jump-Identity-Card-v02.jpg
PROJ-001-Storyboard-v02.jpg
Universal Video Prompt
Current Shot Name
```

去即梦生成：

```text
SHOT-001-v01
SHOT-001-v02
SHOT-001-v03

SHOT-002-v01
SHOT-002-v02
SHOT-002-v03

...
SHOT-006-v03
```

---

# 5. Identity Card Prompt（身份卡提示词）

## Use

用于先生成跳跳的小狗本体形态角色身份卡，锁定角色外观。

## Prompt

```text
请生成一张高质量角色身份卡（Character Identity Card / Character Sheet），用于后续 AI 视频生成参考。

角色名称：
Jump / 跳跳

角色核心设定：
跳跳是一只保持真实小狗本体形态的毛茸茸小狗，不是半人拟人角色。她可以穿衣服、背小包、戴配件，但身体结构必须始终是小狗本体形态。

物种：
小狗

体貌：
真实小狗身体结构，四足动物体态，身体轻盈，毛茸茸，柔软真实毛发，脸部圆润友好，眼神聪明、温暖、亲切。

性格气质：
温暖、轻松、聪明、治愈，有一点下班后的自由感。

角色身份：
程序员小狗，属于《跳跳下班啦》系列角色。

服装：
适合小狗穿的程序员风格衣服，例如浅色小狗连帽卫衣、小背心、小马甲、柔软舒适的宠物服装。可以有小工牌、小背包、项圈挂饰。服装上有少量火龙果粉色品牌点缀。服装必须适合小狗身体结构，不要变成人类衣服比例。

禁止：
不要半人身体，不要人类躯干，不要人类手掌，不要人类手臂，不要人类双腿站立，不要人类比例四肢，不要拟人化半人角色，不要变成人类，不要变成其他动物，不要变肌肉体型，不要去掉毛茸茸质感。

请把这张身份卡设计成专业角色设定卡版式，包含以下内容：

1. 角色主视图：
- 小狗自然站姿，四足站立
- 小狗自然坐姿
- 三分之二角度
- 侧面视图

2. 细节特征说明：
- Species: Dog
- Body Form: Real Dog Form
- Fur: Soft / Realistic / Fluffy
- Face: Rounded / Friendly / Smart
- Body Type: Light / Slim Dog Body
- Temperament: Warm / Relaxed / Smart / Healing
- Outfit: Programmer-style Dog Clothing
- Accent: Dragon-fruit Pink Details

3. 局部特写：
- 脸部特写
- 毛发质感特写
- 前爪特写
- 小狗服装细节特写
- 小背包 / 工牌 / 项圈挂饰细节

4. 角色标签区：
- Name: Jump / 跳跳
- Species: Fluffy Dog
- Role: Programmer Dog
- Mood: Warm / Relaxed / Friendly
- Body Form: Real Dog Form
- Style: Cinematic Lifestyle

5. 禁止漂移说明：
请在版面中清楚强调：
- Do not become human
- Do not become humanoid
- Do not have human hands
- Do not have human arms
- Do not stand like a human
- Do not lose dog body form
- Do not become another animal
- Do not lose fluffy fur
- Do not lose programmer-style outfit
- Do not lose dragon-fruit pink accents

整体版式要求：
专业角色设定卡风格，干净清晰，信息明确，高级质感，适合作为 AI 视频生成参考图。白底或浅灰底，带清晰标题与注释，视觉清楚易读。角色必须始终是小狗本体形态。
```

---

# 6. Storyboard Prompt（故事板提示词）

## Use（用途）

用于先生成故事板分镜图，锁定镜头、动作、道具和情绪变化。

这张故事板将作为后续即梦视频生成的镜头参考图。

---

## Core Rule（核心规则）

```text
跳跳必须保持真实小狗本体形态。
可以穿衣服、背小包、戴配件。
禁止半人拟人化身体。
禁止人类手掌。
禁止人类手臂。
禁止人类双腿站立。
禁止人类比例四肢。
```

---

## Storyboard Style Rule（故事板风格固定规则）

```text
故事板必须使用黑白线条分镜风格，不要彩色成片效果。

画面风格要求：
- 黑白线条
- 粗略的铅笔线条
- 极简的细节
- 快速的动态描绘
- 简单的解剖结构
- 清晰的轮廓
- 保持轻盈、动态、未完成感
- 像导演前期预演分镜 / 动作草图 / 电影分镜手稿
- 不要精修插画感
- 不要彩色厚涂
- 不要真实渲染成片感
- 不要儿童绘本风
- 不要漫画上色成稿感
```

---

## Color Annotation System（彩色标注系统）

注意：
虽然故事板主体必须是黑白铅笔线条草图，
但镜头动态变化必须保留清晰的彩色标注系统。

```text
红色：镜头运动（camera movement）
蓝色：小狗动作（dog movement）
黄色：道具 / 交互（prop interaction）
绿色：灯光 / 情绪（lighting / mood）
紫色：镜头衔接 / 转场（continuity / transition）
```

要求：
- 用彩色箭头明确标出镜头运动和动作方向
- 用彩色圈注或文字标出关键道具变化
- 用彩色注释标出情绪和灯光变化
- 保证黑白主体 + 彩色标注形成清晰对比
- 标注必须清楚、明显、易读

---

## Prompt

```text
请严格参考上传的角色身份卡生成一张专业电影分镜图 / 故事板（Storyboard），用于后续 AI 视频生成参考。

角色外观必须以身份卡中的 Jump / 跳跳为准：

跳跳是一只保持真实小狗本体形态的毛茸茸小狗，不是半人拟人角色。她穿适合小狗身体结构的程序员风格衣服，例如浅色小狗连帽卫衣、小背心、小马甲或柔软宠物服装，有少量火龙果粉色点缀，可以有小背包、工牌或项圈挂饰。

必须保持小狗四足体态。
不要人类身体。
不要人类手掌。
不要人类手臂。
不要人类站姿。
不要半人拟人化角色。

项目主题：
《跳跳下班啦》第一条视频

故事核心：
这条视频是“跳跳下班后的一晚”生活蒙太奇，不是单纯展示离开办公室。办公室部分只占前 3–6 秒，后面重点展示下班后的生活片段：吃饭、逛超市、看电影、买小吃、夜晚散步和暖光结尾。节奏要紧凑，每个生活片段清楚但不要拖沓。

请把整张故事板设计成 8 格分镜图，适合 9:16 竖屏短视频项目，专业导演分镜风格，信息清楚，适合后续 AI 视频生成参考。

重要风格要求：
整张故事板必须采用黑白线条粗略铅笔分镜风格：
- 只用黑白线条作为主体
- 粗略的铅笔线条
- 极简的细节
- 快速的动态描绘
- 简单的解剖结构
- 清晰的轮廓
- 保持前期预演分镜草图感
- 不要彩色成片插画
- 不要真实渲染

但必须同时保留彩色动态标注系统：
- 红色箭头：镜头运动
- 蓝色箭头：小狗动作
- 黄色圈注 / 箭头：道具变化
- 绿色注释：灯光 / 情绪变化
- 紫色注释：镜头衔接 / 连续性提示

8 个镜头如下：

Shot 1 — Work Ending
跳跳坐在办公椅或桌边小垫子上，电脑屏幕显示代码后慢慢变暗。她前爪离开键盘附近，身体轻轻放松，快速交代“工作结束”。

Shot 2 — Clock Out
跳跳穿着小狗衣服，背着小背包，从办公室门口自然四足走出。门外有温暖傍晚光线。这个镜头只用来完成下班转场，不要拖太久。

Shot 3 — Dinner Time
跳跳来到温暖的小餐馆或街边小饭店。画面里有小碗、餐盘、暖灯、餐桌，她坐在桌边或地面小垫子上，开心地看着晚饭。动作符合小狗本体形态，不要像人一样拿筷子。

Shot 4 — Supermarket Walk
跳跳在超市零食区或水果区逛逛，旁边有小购物篮、货架、饮料、零食、蔬果。她背着小包，四足自然走动，低头闻一闻或看向货架，表现下班后逛超市的小快乐。

Shot 5 — Movie Night
跳跳坐在电影院座位或家中投影前，旁边有爆米花、小毯子、柔和屏幕光。她安静看电影，表情放松，氛围温暖治愈。

Shot 6 — Street Snack
跳跳来到夜晚街边小摊或便利店门口，暖光下有热乎乎的小吃、纸袋或小零食。她低头闻一闻，表现下班后的小奖励。

Shot 7 — Night Walk
跳跳背着小包走在夜晚街道，路边有暖色橱窗、街灯、植物和生活化街景。她脚步轻松稳定，尾巴自然，表现“时间终于属于自己”。

Shot 8 — Life Begins
跳跳停在温暖夜色里，回头看一眼或抬头看向前方，表情放松、自由。画面有结尾感，可用于最后一句字幕“下班啦，生活开始啦”。

版式要求：
- 8 格清晰分镜图
- 每格标明 Shot 编号和镜头名称
- 每格都要有简短镜头说明
- 每格都要明确显示竖屏构图 9:16
- 每格都要清楚显示角色位置、道具位置和动作方向
- 每格主体必须是黑白粗略铅笔线条草图
- 每格必须保留彩色标注系统表示动态变化

视觉风格要求：
专业导演分镜图风格，黑白线条、粗略铅笔感、极简细节、快速动态描绘、简单解剖结构、清晰轮廓。整体像电影前期分镜手稿，不是成片概念图。

场景要求：
温暖的创作者工作室办公室、街边小餐馆、超市、电影院或投影空间、夜晚街边小摊、夜晚散步街道。整体是“下班后的一晚”的生活蒙太奇。

灯光要求：
虽然画面主体是黑白线条草图，但要通过绿色标注清楚说明灯光和情绪变化。Shot 2 开始要出现傍晚暖光，Shot 3–8 体现下班后生活的温暖、自由和松弛感。

重要限制：
跳跳必须保持真实小狗本体形态。
禁止半人身体。
禁止人类手掌。
禁止人类手臂。
禁止双腿直立人形站姿。
禁止拟人化半人角色。
禁止变成人类。
禁止变成其他动物。
禁止失去毛茸茸质感。
禁止失去小狗衣服和小背包设定。
```

---

# 7. Universal Video Prompt（通用视频提示词）

## Use（用途）

用于即梦 / Veo / Runway 等视频模型的通用视频生成 Prompt。

每次生成时上传：

```text
Jump-Identity-Card-v02.jpg
PROJ-001-Storyboard-v02.jpg
```

然后复制本节 Universal Video Prompt，并在最后填写当前镜头名称。

不要为每个 Shot 重新写一条长 Prompt。

Shot 细节已经由 Storyboard Prompt 锁定。

---

## Runtime Input（运行输入）

每次生成只替换这一行：

```text
Current Shot:
[填写故事板中的镜头名称，例如 Shot 3 — Dinner Time]
```

---

## Universal Video Prompt

```text
请严格参考上传的角色身份卡和故事板生成一段 9:16 竖屏短视频。

角色外观必须以身份卡中的 Jump / 跳跳为准。

跳跳是一只真实小狗本体形态的毛茸茸小狗，穿适合小狗身体结构的程序员风格小狗衣服，可以有小背包、工牌、项圈挂饰和少量火龙果粉色点缀。她必须始终保持小狗四足身体结构，不能变成人类，不能变成半人角色，不能出现人类手掌、人类手臂、人类双腿或人类比例身体。

镜头内容、构图、动作方向、道具关系、情绪变化、灯光变化和镜头衔接必须以上传故事板为准。

当前只生成指定的 Current Shot，不要一次生成完整视频，不要混合其他镜头内容。

视频规格：
9:16 竖屏，电影感生活纪录片风格，温暖真实，高级短视频质感，动作自然，节奏轻快但不夸张。

动作要求：
跳跳的动作必须符合真实小狗身体结构。四足行走要贴地稳定，身体不能漂浮，脚步不能滑动，背包和衣服不能消失或变形。不要让跳跳像人一样站立、伸手、拿东西或做复杂人类动作。

视觉要求：
保持温暖的 TiaoTiao Studio 生活感，画面干净但有真实生活痕迹。不要冷色企业办公室，不要赛博朋克，不要恐怖风，不要游戏感，不要宠物写真棚拍感，不要强广告感。

连续性要求：
角色脸型、体型、毛发、服装、小背包、火龙果粉色点缀、整体气质必须与身份卡一致。当前镜头必须与故事板中前后镜头的场景、动作和情绪关系保持连续。

负面要求：
不要横屏，不要 16:9，不要半人身体，不要人类躯干，不要人类手掌，不要人类手臂，不要人类双腿站立，不要人类比例四肢，不要拟人化半人角色，不要把跳跳变成人，不要变成其他动物，不要变肌肉，不要去掉毛茸茸质感，不要裸体宠物狗，不要丢失衣服，不要丢失小狗本体形态，不要恐怖风，不要赛博朋克，不要游戏感，不要廉价 CGI，不要宠物写真棚拍感，不要办公室杂乱，不要冷色企业办公室，不要强广告感，不要脸部崩坏，不要身体变形，不要四肢扭曲，不要滑步，不要身体漂浮。

Current Shot:
[填写故事板中的镜头名称]
```

---

# 8. Global Negative Prompt（全局负面提示词）

```text
不要横屏，不要 16:9，不要半人身体，不要人类躯干，不要人类手掌，不要人类手臂，不要人类双腿站立，不要人类比例四肢，不要拟人化半人角色，不要把跳跳变成人，不要变成其他动物，不要变肌肉，不要去掉毛茸茸质感，不要裸体宠物狗，不要丢失衣服，不要丢失小狗本体形态，不要恐怖风，不要赛博朋克，不要游戏感，不要廉价 CGI，不要宠物写真棚拍感，不要办公室杂乱，不要冷色企业办公室，不要强广告感，不要脸部崩坏，不要身体变形，不要四肢扭曲，不要滑步，不要身体漂浮。
```

---

# 9. Shot Runtime List（镜头运行列表）

生成视频时，每次使用同一个 Universal Video Prompt，只替换 `Current Shot`。

```text
Shot 1 — Work Ending
Shot 2 — Clock Out
Shot 3 — Dinner Time
Shot 4 — Supermarket Walk
Shot 5 — Movie Night
Shot 6 — Street Snack
Shot 7 — Night Walk
Shot 8 — Life Begins
```

每个 Shot 的具体画面、动作、道具、灯光、情绪和转场以第 6 节 Storyboard Prompt 为准。

---

# 10. Model-readable Check（模型可读检查）

复制到视频模型前，必须确认：

```text
[ ] 模型可见 Prompt 没有要求模型理解 CHAR-001 / ASSET-001 / STYLE-001 等内部编号
[ ] 身份卡 Prompt 已把 Jump 外观写成完整自然语言
[ ] Storyboard Prompt 已明确黑白粗略铅笔线条风格
[ ] Storyboard Prompt 已保留彩色标注系统
[ ] Universal Video Prompt 已说明上传身份卡和故事板
[ ] Universal Video Prompt 已说明当前只生成指定 Current Shot
[ ] Jump 仍是真实小狗本体形态
[ ] Jump 仍穿适合小狗身体结构的衣服
[ ] Negative Prompt 已禁止半人身体、人类手掌、人类手臂、人类双腿和物种漂移
```

---

# 11. COMMAND-005 Review（COMMAND-005 复核）

每个镜头生成前后都必须用 COMMAND-005 检查：

```text
[ ] 角色是否保持真实小狗本体形态
[ ] 是否没有半人身体
[ ] 是否没有人类手掌 / 人类手臂 / 人类双腿
[ ] 是否穿衣服且服装没有丢失
[ ] 是否保持身份卡外观一致
[ ] 是否符合故事板当前镜头
[ ] 是否符合 9:16 竖屏
[ ] 是否没有滑步、漂浮、身体变形或脸部崩坏
[ ] 是否没有把 Notion 当作 Source of Truth
```

Review result:

```text
PASS
FAIL
PASS WITH MINOR FIXES
```

---

# 12. Runtime Reminder（执行提醒）

实际执行时：

```text
1. 先用身份卡 Prompt 生成小狗本体形态的 Jump Identity Card v02
2. 再用故事板 Prompt 生成 8 格 Storyboard v02
3. 再拿身份卡 + 故事板 + Universal Video Prompt + Current Shot 去即梦生成
4. 每个 Shot 生成后运行 COMMAND-005 review
```

优先生成：

```text
SHOT-001-v01
SHOT-001-v02
SHOT-001-v03
```

重点检查：

```text
[ ] 是否 9:16 竖屏
[ ] 是否保持小狗本体形态
[ ] 是否穿衣服
[ ] 是否没有半人身体
[ ] 是否没有人类手掌
[ ] 是否没有双腿站立
[ ] 是否符合工作结束情绪
```

---

# 13. Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 4.0 | 2026 | Updated production package to Identity Card Prompt → Storyboard Prompt → Universal Video Prompt → Model-readable check → COMMAND-005 review |
| 3.0 | 2026 | Revised Jump from anthropomorphic humanoid dog to real dog-form character wearing clothes |
