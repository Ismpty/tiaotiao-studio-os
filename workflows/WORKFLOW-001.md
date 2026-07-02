# WORKFLOW-001 — Jump After Work Production Workflow（跳跳下班啦生产工作流）

> Canonical Workflow Template（官方工作流模板）  
> Version：1.0  
> Status：Active

---

# Definition（定义）

## 中文

Jump After Work Production Workflow 是 TiaoTiao Studio OS 的第一个完整生产工作流模板。

它用于把 TSOS 中已经建立的 Knowledge Nodes、Database Records 和 AI Agents 串联起来，形成一套可重复执行的短视频生产流程。

这个 Workflow 不负责新增世界观、不修改角色设定、不改变品牌方向。

它只负责规定：

从项目开始，到分镜、提示词、摄影、脚本、剪辑、发布，应该按照什么顺序执行。

## English

Jump After Work Production Workflow is the first complete production workflow template in TiaoTiao Studio OS.

It connects Knowledge Nodes, Database Records and AI Agents into a repeatable short-video production process.

It does not create new canon, modify characters or change brand direction.

---

# Workflow Goal（工作流目标）

本工作流的目标是：

- 让《跳跳下班啦》系列可以稳定生产
- 让每次创作都引用同一套 TSOS 记录
- 避免每次重新解释角色、风格、镜头、灯光和品牌语言
- 让 AI Agents 按固定顺序协作
- 让内容从创意进入可执行生产流程
- 让 GitHub 成为工作流的唯一事实来源

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
| Episode DB | EP-001 | 跳跳下班啦剧集设定 |
| Story DB | STORY-001 | 下班冒险故事 |
| Environment DB | ENV-001 | 跳跳工作室办公室 |
| Motion DB | MOT-001 | 自然行走动作 |
| Camera DB | CAM-001 | 主角跟拍镜头 |
| Lighting DB | LGT-001 | 温暖工作室灯光 |
| Prompt DB | PROMPT-001 | 主提示词模块 |
| Asset DB | ASSET-001 | Jump 角色参考资产 |
| Project DB | PROJ-001 | 试播项目记录 |

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
| AGENT-004 | Script Agent |
| AGENT-005 | Editing Agent |
| AGENT-006 | Publishing Agent |

---

# Workflow Overview（工作流总览）

标准执行顺序：

```text
1. Project Setup
↓
2. Storyboard Planning
↓
3. Prompt Generation
↓
4. Cinematography Planning
↓
5. Script Writing
↓
6. Editing Planning
↓
7. Publishing Planning
↓
8. Final Consistency Check
```

---

# Stage 1 — Project Setup（项目初始化）

## Input（输入）

读取：

```text
PROJ-001
CHAR-001
EP-001
STORY-001
ASSET-001
```

## Task（任务）

确认本次项目的：

- 主角
- 剧集
- 故事
- 情绪
- 项目目标
- 平台方向
- 生产范围

## Output（输出）

```text
Project Brief
```

## Required Check（必须检查）

```text
[ ] 是否使用 PROJ-001
[ ] 是否使用 CHAR-001
[ ] 是否使用 EP-001
[ ] 是否使用 STORY-001
[ ] 是否使用 ASSET-001
[ ] 是否没有新增未确认设定
```

---

# Stage 2 — Storyboard Planning（分镜规划）

## Agent（执行智能体）

```text
AGENT-001 — Storyboard Agent
```

## Input（输入）

读取：

```text
PROJ-001
PROMPT-001
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
ASSET-001
```

## Task（任务）

生成：

- 故事节奏拆解
- 镜头列表
- 每个镜头的叙事功能
- 每个镜头的画面描述
- 每个镜头使用的角色、环境、动作、镜头、灯光和资产引用

## Output（输出）

```text
Storyboard Output
```

## Required Check（必须检查）

```text
[ ] 每个镜头是否有故事功能
[ ] Jump 是否保持角色一致
[ ] 是否引用 ASSET-001
[ ] 是否符合 STORYFORMULA-001
[ ] 是否符合 BRAND-001
```

---

# Stage 3 — Prompt Generation（提示词生成）

## Agent（执行智能体）

```text
AGENT-002 — Prompt Agent
```

## Input（输入）

读取：

```text
Storyboard Output
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

生成：

- 图片 Prompt
- 视频 Prompt
- 镜头 Prompt
- 角色一致性 Prompt
- 负面提示词
- 模型适配版本

## Output（输出）

```text
Prompt Output
```

## Required Check（必须检查）

```text
[ ] 是否保持 Jump 是拟人化小狗
[ ] 是否保留毛茸茸质感
[ ] 是否引用 ASSET-001
[ ] 是否禁止赛博朋克、恐怖、游戏感
[ ] 是否适配目标模型
```

---

# Stage 4 — Cinematography Planning（摄影方案）

## Agent（执行智能体）

```text
AGENT-003 — Cinematography Agent
```

## Input（输入）

读取：

```text
Storyboard Output
Prompt Output
CAM-001
LGT-001
ENV-001
STYLE-001
COLOR-001
SHOT-001
BRAND-001
```

## Task（任务）

生成：

- 镜头焦段方案
- 机位高度
- 运镜方案
- 构图方案
- 景深规则
- 灯光关系
- AI 视觉增强提示词

## Output（输出）

```text
Cinematography Output
```

## Required Check（必须检查）

```text
[ ] 镜头是否服务故事
[ ] 是否使用自然可信运镜
[ ] 是否符合 CAM-001
[ ] 是否符合 LGT-001
[ ] 是否保持电影感真实
[ ] 是否避免极端广角和游戏感镜头
```

---

# Stage 5 — Script Writing（脚本写作）

## Agent（执行智能体）

```text
AGENT-004 — Script Agent
```

## Input（输入）

读取：

```text
PROJ-001
EP-001
STORY-001
CHAR-001
Storyboard Output
Cinematography Output
STORYFORMULA-001
BRAND-001
EMOTION-001
MUSIC-001
```

## Task（任务）

生成：

- 开场 Hook
- 旁白脚本
- 字幕脚本
- 角色对白或内心独白
- 结尾金句
- 中英文版本可选

## Output（输出）

```text
Script Output
```

## Required Check（必须检查）

```text
[ ] 文案是否温暖真实
[ ] 是否避免职场焦虑
[ ] 是否符合 BRAND-001
[ ] 是否符合 STORYFORMULA-001
[ ] 是否适合短视频节奏
```

---

# Stage 6 — Editing Planning（剪辑规划）

## Agent（执行智能体）

```text
AGENT-005 — Editing Agent
```

## Input（输入）

读取：

```text
Storyboard Output
Prompt Output
Cinematography Output
Script Output
MUSIC-001
EMOTION-001
BRAND-001
```

## Task（任务）

生成：

- 剪辑时间线
- 镜头时长
- 转场方式
- 字幕时间点
- 旁白时间点
- 音乐进入退出
- 环境音建议
- 导出备注

## Output（输出）

```text
Editing Output
```

## Required Check（必须检查）

```text
[ ] 开头 3 秒是否清晰
[ ] 字幕是否不遮挡 Jump
[ ] 音乐是否不压过情绪
[ ] 是否保留情绪停顿
[ ] 是否避免过度快切
[ ] 是否适合短视频平台
```

---

# Stage 7 — Publishing Planning（发布规划）

## Agent（执行智能体）

```text
AGENT-006 — Publishing Agent
```

## Input（输入）

读取：

```text
PROJ-001
Script Output
Editing Output
BRAND-001
STYLE-001
COLOR-001
```

## Task（任务）

生成：

- 平台标题
- 正文简介
- 标签组
- 封面文案
- 发布时间建议
- 发布前检查清单
- 发布后复盘指标

## Output（输出）

```text
Publishing Output
```

## Required Check（必须检查）

```text
[ ] 标题是否不标题党
[ ] 文案是否不制造焦虑
[ ] 标签是否相关
[ ] 封面文案是否简洁
[ ] 是否符合 BRAND-001
[ ] 是否保留 Jump 的温暖角色气质
```

---

# Stage 8 — Final Consistency Check（最终一致性检查）

## Input（输入）

读取所有阶段输出：

```text
Project Brief
Storyboard Output
Prompt Output
Cinematography Output
Script Output
Editing Output
Publishing Output
```

## Task（任务）

最终检查：

```text
[ ] Jump 身份是否一致
[ ] Jump 外观是否参考 ASSET-001
[ ] 世界观是否符合 WORLD-001
[ ] 风格是否符合 STYLE-001
[ ] 色彩是否符合 COLOR-001
[ ] 情绪是否符合 EMOTION-001
[ ] 故事是否符合 STORYFORMULA-001
[ ] 镜头是否符合 SHOT-001 / CAM-001
[ ] 动作是否符合 MOTIONLANG-001 / MOT-001
[ ] 灯光是否符合 LGT-001
[ ] 音乐是否符合 MUSIC-001
[ ] 文案是否符合 BRAND-001
[ ] 是否没有新增未确认设定
```

## Output（输出）

```text
Final Production Package
```

---

# Final Production Package（最终生产包）

完整工作流最终应输出：

```text
1. Project Brief
2. Storyboard Output
3. Prompt Output
4. Cinematography Output
5. Script Output
6. Editing Output
7. Publishing Output
8. Final Consistency Checklist
```

---

# Standard Command Template（标准调用模板）

使用本 Workflow 时，可以输入：

```text
Run WORKFLOW-001 for PROJ-001.

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

Use Agents:
AGENT-001
AGENT-002
AGENT-003
AGENT-004
AGENT-005
AGENT-006

Output:
Complete production package.
```

---

# Workflow Rules（工作流规则）

## Must Do（必须）

- 必须按阶段顺序执行
- 必须读取现有 TSOS 记录
- 必须保持 GitHub 为 Source of Truth
- 必须保留角色一致性
- 必须保留品牌一致性
- 必须输出可执行内容
- 必须完成最终一致性检查

---

## Never Do（禁止）

- 不得跳过 Database Records
- 不得跳过 Knowledge Nodes
- 不得临时修改 Jump 人设
- 不得临时新增世界观
- 不得改变品牌语言
- 不得为了效率省略一致性检查
- 不得输出无法执行的空泛建议

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
agents/writer/AGENT-004.md
agents/editor/AGENT-005.md
agents/publisher/AGENT-006.md
```

---

# Usage Scope（应用范围）

适用于：

- Jump After Work short video production
- AI video generation workflow
- Storyboard production
- Prompt production
- Cinematography planning
- Script writing
- Editing planning
- Publishing planning
- Series pilot production
- Workflow validation

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial canonical workflow template |