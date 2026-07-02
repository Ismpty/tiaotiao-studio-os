# WORKFLOW-003 — Storyboard to Video Workflow（分镜到视频工作流）

> Canonical Workflow Template（官方工作流模板）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Storyboard to Video Workflow 是 TiaoTiao Studio OS 的分镜到视频生成工作流。

它用于把已经完成的 Storyboard Output 转化为可执行的视频镜头生成包，包括镜头拆分、视频提示词、摄影参数、动作连续性、灯光一致性、负面提示词和片段组装规则。

这个 Workflow 不负责重新写故事，也不负责重新设计角色。

它只负责把已经确认的分镜内容转化为可生成、可检查、可组装的视频片段。

## English

Storyboard to Video Workflow transforms approved storyboard outputs into executable AI video generation packages.

It converts storyboard shots into video prompts, cinematography instructions, motion continuity rules, lighting requirements, negative prompts and assembly notes.

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 将分镜转化为可直接生成的视频镜头
- 保持 Jump 角色一致性
- 保持镜头之间动作连续
- 保持办公室环境、灯光、色彩一致
- 避免 AI 视频生成中的角色漂移
- 避免镜头之间风格不统一
- 让视频片段可以进入剪辑阶段

---

# Default Project（默认项目）

本 Workflow 默认服务：

```text
PROJ-001 — Jump After Work Pilot Project
```

---

# Required Database Records（必需数据库记录）

| Database | Record | Purpose |
|---|---|---|
| Character DB | CHAR-001 | Jump 角色身份 |
| Episode DB | EP-001 | 剧集设定 |
| Story DB | STORY-001 | 故事目标 |
| Environment DB | ENV-001 | 场景环境 |
| Motion DB | MOT-001 | 动作连续性 |
| Camera DB | CAM-001 | 镜头语言 |
| Lighting DB | LGT-001 | 灯光一致性 |
| Prompt DB | PROMPT-001 | 主提示词 |
| Asset DB | ASSET-001 | 角色参考资产 |
| Project DB | PROJ-001 | 项目目标 |

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
| AGENT-002 | Prompt Agent |
| AGENT-003 | Cinematography Agent |
| AGENT-005 | Editing Agent |

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Storyboard Input Review
↓
2. Shot Segmentation
↓
3. Video Prompt Generation
↓
4. Cinematography Enhancement
↓
5. Motion Continuity Setup
↓
6. Lighting and Style Lock
↓
7. Negative Prompt Setup
↓
8. Video Clip Generation Package
↓
9. Clip Review
↓
10. Assembly Notes
```

---

# Stage 1 — Storyboard Input Review（分镜输入检查）

## Input（输入）

读取：

```text
Storyboard Output
PROJ-001
CHAR-001
STORY-001
ASSET-001
```

## Task（任务）

检查分镜是否已经具备：

- 镜头编号
- 镜头名称
- 镜头时长
- 叙事功能
- 画面描述
- 角色动作
- 镜头语言
- 灯光要求
- 负面提示词
- 连续性备注

## Output（输出）

```text
Storyboard Review Result
```

## Required Check（必须检查）

```text
[ ] 是否存在完整 Shot List
[ ] 每个镜头是否有明确故事功能
[ ] 每个镜头是否引用 CHAR-001
[ ] 每个镜头是否引用 ASSET-001
[ ] 是否没有新增未确认设定
```

---

# Stage 2 — Shot Segmentation（镜头拆分）

## Task（任务）

将分镜拆成独立视频生成单元。

每个视频片段应包含：

```text
Shot ID
Shot Name
Duration
Start State
Action
End State
Camera
Motion
Lighting
Environment
Continuity Notes
```

## Output（输出）

```text
Video Shot Units
```

---

# Video Shot Unit Template（视频镜头单元模板）

```text
Shot ID:
Shot Name:
Duration:
Story Function:
Start State:
Action:
End State:
Character:
Environment:
Camera:
Motion:
Lighting:
Asset Reference:
Continuity Notes:
```

---

# Stage 3 — Video Prompt Generation（视频提示词生成）

## Agent（执行智能体）

```text
AGENT-002 — Prompt Agent
```

## Input（输入）

读取：

```text
Video Shot Units
PROMPT-001
CHAR-001
ENV-001
MOT-001
CAM-001
LGT-001
ASSET-001
STYLE-001
COLOR-001
BRAND-001
```

## Task（任务）

为每个镜头生成视频 Prompt。

必须包含：

- Duration
- Subject
- Start Frame
- Action
- End Frame
- Camera Movement
- Motion Description
- Lighting
- Style
- Negative Prompt

## Output（输出）

```text
Shot-by-Shot Video Prompts
```

---

# Standard Video Prompt Template（标准视频提示词模板）

```text
Duration:
6–8 seconds

Subject:
Jump, an anthropomorphic fluffy female dog programmer, slim body, friendly warm expression, soft realistic fur texture, default programmer outfit, Fire Dragon Fruit Pink brand accents, consistent with ASSET-001.

Start Frame:
Describe the opening state of the shot.

Action:
Describe the exact movement or action.

End Frame:
Describe how the shot should end.

Camera:
Hero tracking camera, 35mm lens, eye-level framing, natural camera movement, cinematic documentary style.

Motion:
Natural movement, realistic weight transfer, grounded foot contact, soft body mechanics, subtle tail movement.

Lighting:
Warm Studio Lighting, practical desk lamp, soft screen glow, golden-hour window spill, gentle shadows.

Environment:
TiaoTiao Studio Office, warm modern creator studio, realistic programmer workspace.

Mood:
Freedom, warmth, relaxation, everyday joy.

Style:
Cinematic documentary realism, lifestyle storytelling, natural color balance, realistic depth.

Negative Prompt:
Do not change Jump's species, no human version, no sliding feet, no robotic motion, no game animation, no cyberpunk lighting, no horror mood, no extreme wide-angle distortion.
```

---

# Stage 4 — Cinematography Enhancement（摄影增强）

## Agent（执行智能体）

```text
AGENT-003 — Cinematography Agent
```

## Input（输入）

读取：

```text
Shot-by-Shot Video Prompts
CAM-001
LGT-001
SHOT-001
STYLE-001
```

## Task（任务）

为每个视频 Prompt 增强摄影信息：

- Lens
- Camera Height
- Camera Movement
- Frame Size
- Composition
- Depth of Field
- Cinematic Notes

## Output（输出）

```text
Cinematography-Enhanced Video Prompts
```

---

# Cinematography Add-on Template（摄影增强模板）

```text
Lens:
35mm

Camera Height:
Eye level

Camera Movement:
Natural hero tracking / side tracking / rear follow / gentle push-in

Composition:
Jump occupies 35–45% of frame, environment occupies 55–65%, clear forward space, no obstruction.

Depth of Field:
Natural depth, soft background falloff, clear subject separation.

Cinematic Notes:
Warm cinematic documentary realism, subtle handheld energy, realistic depth compression.
```

---

# Stage 5 — Motion Continuity Setup（动作连续性设置）

## Input（输入）

读取：

```text
MOT-001
MOTIONLANG-001
Storyboard Output
```

## Task（任务）

为镜头之间建立连续性。

检查：

- Jump 起始位置
- Jump 结束位置
- 行走方向
- 手部动作
- 尾巴动作
- 表情变化
- 背包状态
- 电脑是否关闭
- 门是否打开
- 光线是否连续

## Output（输出）

```text
Motion Continuity Map
```

---

# Motion Continuity Checklist（动作连续性检查表）

```text
[ ] Shot 起始动作是否接上上一镜头
[ ] Shot 结束动作是否能接下一镜头
[ ] Jump 是否没有瞬移
[ ] 脚步是否没有滑动
[ ] 身体重心是否真实
[ ] 尾巴动作是否自然
[ ] 表情变化是否合理
[ ] 背包 / 道具状态是否连续
```

---

# Stage 6 — Lighting and Style Lock（灯光与风格锁定）

## Input（输入）

读取：

```text
LGT-001
STYLE-001
COLOR-001
ENV-001
```

## Task（任务）

锁定所有镜头的视觉一致性：

- 暖色工作室灯光
- 屏幕柔光
- 台灯实用光
- 傍晚窗光
- 火龙果粉点缀
- 真实电影感
- 生活方式叙事

## Output（输出）

```text
Lighting and Style Lock Notes
```

---

# Visual Lock Rules（视觉锁定规则）

```text
[ ] 所有镜头保持暖色室内光
[ ] 不出现赛博朋克蓝光
[ ] 不出现恐怖片高反差
[ ] 不出现过度 RGB 灯效
[ ] 不改变办公室空间基调
[ ] 不改变 Jump 服装主视觉
[ ] 不改变品牌色点缀
[ ] 不出现游戏渲染感
```

---

# Stage 7 — Negative Prompt Setup（负面提示词设置）

## Task（任务）

为每个镜头生成负面提示词。

负面提示词必须覆盖：

- 角色错误
- 动作错误
- 镜头错误
- 灯光错误
- 风格错误
- 环境错误
- 品牌错误

## Output（输出）

```text
Shot Negative Prompt Set
```

---

# Standard Video Negative Prompt（标准视频负面提示词）

```text
Do not change Jump's species, do not turn Jump into a human, do not remove fluffy fur, do not make Jump muscular, do not change outfit, do not remove Fire Dragon Fruit Pink accents, do not use horror, violence, dark dystopian mood, cyberpunk blue lighting, neon sci-fi glow, game animation, robotic movement, sliding feet, floating body, mechanical tail movement, impossible motion, extreme wide-angle distortion, drone orbit, FPS camera, artificial camera shake, over-saturated RGB lights, messy office, cold corporate office, inconsistent environment, aggressive expression, cheap CGI look.
```

---

# Stage 8 — Video Clip Generation Package（视频片段生成包）

## Task（任务）

为每个镜头输出完整生成包。

## Output（输出）

```text
Video Clip Generation Package
```

---

# Clip Package Template（片段生成包模板）

```text
# Shot Video Package

Shot ID:
Shot Name:
Duration:
Target Model:
Aspect Ratio:
Source Records:

Video Prompt:

Cinematography Add-on:

Negative Prompt:

Continuity Notes:

Review Checklist:
```

---

# Target Model Notes（目标模型备注）

## Kling

适合：

- 人物动作
- 镜头运动
- 生活化短镜头

重点写清：

```text
动作起点
动作终点
镜头运动
角色连续性
```

---

## Veo

适合：

- 电影感
- 复杂环境
- 自然运动
- 连续叙事

重点写清：

```text
场景情绪
电影语言
动作节奏
空间关系
```

---

## Runway

适合：

- 镜头片段
- 视觉测试
- 图片转视频
- 局部动作生成

重点写清：

```text
主体不要变形
动作不要过度
镜头不要漂移
```

---

# Stage 9 — Clip Review（片段检查）

## Task（任务）

每个生成片段必须检查：

```text
[ ] Jump 是否保持小狗身份
[ ] 毛发是否清晰
[ ] 身体是否苗条
[ ] 服装是否一致
[ ] 动作是否自然
[ ] 脚步是否不滑
[ ] 镜头是否稳定可信
[ ] 灯光是否符合 LGT-001
[ ] 环境是否符合 ENV-001
[ ] 情绪是否符合 EMOTION-001
[ ] 是否可接入下一镜头
```

## Output（输出）

```text
Clip Review Notes
```

---

# Stage 10 — Assembly Notes（组装备注）

## Agent（执行智能体）

```text
AGENT-005 — Editing Agent
```

## Input（输入）

读取：

```text
Approved Video Clips
Editing Output
MUSIC-001
BRAND-001
```

## Task（任务）

输出：

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
1. Storyboard Review Result
2. Video Shot Units
3. Shot-by-Shot Video Prompts
4. Cinematography-Enhanced Video Prompts
5. Motion Continuity Map
6. Lighting and Style Lock Notes
7. Shot Negative Prompt Set
8. Video Clip Generation Package
9. Clip Review Notes
10. Video Assembly Notes
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-003 for PROJ-001.

Input:
Storyboard Output from AGENT-001

Use:
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
PROJ-001

Use Agents:
AGENT-002
AGENT-003
AGENT-005

Target Model:
Kling / Veo / Runway

Output:
Shot-by-shot video generation package.
```

---

# Workflow Rules（工作流规则）

## Must Do（必须）

- 必须基于已确认分镜
- 必须逐镜头输出视频生成包
- 必须引用 ASSET-001
- 必须保持 Jump 角色一致
- 必须保持动作连续
- 必须保持灯光统一
- 必须包含负面提示词
- 必须输出片段检查标准

---

## Never Do（禁止）

- 不得重新改写故事
- 不得重新设计 Jump
- 不得忽略分镜顺序
- 不得省略连续性检查
- 不得省略负面提示词
- 不得生成无法执行的视频提示词
- 不得使用与品牌冲突的风格

---

# Related Files（关联文件）

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
agents/editor/AGENT-005.md
```

---

# Usage Scope（应用范围）

适用于：

- Storyboard to Video
- AI Video Generation
- Shot Prompt Production
- Clip Review
- Motion Continuity Check
- Cinematography Enhancement
- Video Assembly
- Series Production

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical workflow template |