# Database — Production Database Index（生产数据库索引）

> Navigation Index（导航索引）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 `database/` 目录的索引文件。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- 当前有哪些 Production Database Records
- 每个数据库记录放在哪里
- 每个记录负责什么
- 每个记录与 Notion DB 如何对应
- 每个记录应引用哪些 Knowledge Nodes
- 什么时候应该读取哪个记录
- 如何避免重复定义角色、故事、镜头、灯光和品牌规则

## English

This file is the index for the `database/` directory.

It helps AI tools understand available production database records, their locations, Notion DB mapping, knowledge references and usage rules.

---

# Database Layer Role（数据库层作用）

Production Database 是 TSOS 的生产实体层。

```text
Knowledge Nodes
↓
Database Records
↓
Projects
↓
Agents
↓
Workflows
↓
Commands
↓
Output
```

Knowledge Nodes 定义长期规则。  
Database Records 定义具体生产对象。  
Project Records 组合多个 Database Records 进入实际生产。

---

# Source of Truth（唯一事实来源）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Database Records 必须以 GitHub 文件为准。

Notion 用于可视化管理和同步，但不能覆盖 GitHub Source of Truth。

---

# Current Production Database Records（当前生产数据库记录）

当前 TSOS 有 10 个核心 Production Database Records：

```text
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
```

---

# Database Index（数据库索引）

| Database | Record | File | Notion DB |
|---|---|---|---|
| Character DB | CHAR-001 | characters/CHAR-001.md | Character DB |
| Episode DB | EP-001 | episodes/EP-001.md | Episode DB |
| Story DB | STORY-001 | stories/STORY-001.md | Story DB |
| Environment DB | ENV-001 | environments/ENV-001.md | Environment DB |
| Motion DB | MOT-001 | motions/MOT-001.md | Motion DB |
| Camera DB | CAM-001 | cameras/CAM-001.md | Camera DB |
| Lighting DB | LGT-001 | lighting/LGT-001.md | Lighting DB |
| Prompt DB | PROMPT-001 | prompts/PROMPT-001.md | Prompt DB |
| Asset DB | ASSET-001 | assets/ASSET-001.md | Asset DB |
| Project DB | PROJ-001 | projects/PROJ-001.md | Project DB |

---

# Directory Structure（目录结构）

```text
database/
├── README.md
├── characters/
│   └── CHAR-001.md
├── episodes/
│   └── EP-001.md
├── stories/
│   └── STORY-001.md
├── environments/
│   └── ENV-001.md
├── motions/
│   └── MOT-001.md
├── cameras/
│   └── CAM-001.md
├── lighting/
│   └── LGT-001.md
├── prompts/
│   └── PROMPT-001.md
├── assets/
│   └── ASSET-001.md
└── projects/
    └── PROJ-001.md
```

---

# CHAR-001 — Jump

## File

```text
database/characters/CHAR-001.md
```

## Notion DB

```text
Character DB
```

## 中文说明

CHAR-001 是 Jump / 跳跳 的官方角色记录。

它定义 Jump 的核心身份、角色气质、视觉识别、角色约束和生产使用规则。

## Use When（使用场景）

当任务涉及：

```text
Jump 角色
跳跳外观
角色一致性
角色 Prompt
角色分镜
角色封面
角色视频生成
```

必须读取：

```text
CHAR-001
```

## Key References

```text
ASSET-001
OUTFIT-001
COLOR-001
BRAND-001
STYLE-001
```

## Never Do

```text
不得把 Jump 改成人类
不得改成其他动物
不得去掉毛茸茸质感
不得改成肌肉型角色
不得改变程序员身份
```

---

# EP-001 — Jump After Work

## File

```text
database/episodes/EP-001.md
```

## Notion DB

```text
Episode DB
```

## 中文说明

EP-001 是《跳跳下班啦》的官方剧集记录。

它定义该系列的默认剧集方向、核心情绪、内容边界和生产目标。

## Use When（使用场景）

当任务涉及：

```text
跳跳下班啦
系列内容
剧集规划
短视频生产
系列风格
系列延展
```

必须读取：

```text
EP-001
```

## Key References

```text
CHAR-001
STORY-001
PROJ-001
BRAND-001
STORYFORMULA-001
```

---

# STORY-001 — Work Ends, Adventure Begins

## File

```text
database/stories/STORY-001.md
```

## Notion DB

```text
Story DB
```

## 中文说明

STORY-001 是《跳跳下班啦》的核心故事记录。

它定义“下班，就是冒险的开始”的故事结构和情绪路径。

## Use When（使用场景）

当任务涉及：

```text
故事结构
分镜
脚本
剧情节奏
情绪转折
故事公式应用
```

必须读取：

```text
STORY-001
```

## Key References

```text
STORYFORMULA-001
EMOTION-001
BRAND-001
EP-001
PROJ-001
```

---

# ENV-001 — TiaoTiao Studio Office

## File

```text
database/environments/ENV-001.md
```

## Notion DB

```text
Environment DB
```

## 中文说明

ENV-001 是 Jump 的默认工作环境记录。

它定义 TiaoTiao Studio Office 的空间特征、道具、光线、氛围和叙事作用。

## Use When（使用场景）

当任务涉及：

```text
办公室场景
工作室环境
写代码场景
下班场景
室内镜头
环境 Prompt
```

必须读取：

```text
ENV-001
```

## Key References

```text
CHAR-001
STYLE-001
COLOR-001
LGT-001
BRAND-001
```

---

# MOT-001 — Natural Walking

## File

```text
database/motions/MOT-001.md
```

## Notion DB

```text
Motion DB
```

## 中文说明

MOT-001 是 Jump 的自然行走动作资产。

它定义 Jump 在下班、散步、旅行、离开办公室等生活化场景中的默认动作方式。

## Use When（使用场景）

当任务涉及：

```text
行走动作
下班离开
动作连续性
视频生成
运动提示词
角色移动
```

必须读取：

```text
MOT-001
```

## Key References

```text
MOTIONLANG-001
EMOTION-001
CAM-001
STYLE-001
```

## Never Do

```text
不得滑步
不得漂浮
不得机器人动作
不得游戏动画感
```

---

# CAM-001 — Hero Tracking Camera

## File

```text
database/cameras/CAM-001.md
```

## Notion DB

```text
Camera DB
```

## 中文说明

CAM-001 是 Jump 的默认主角跟拍镜头资产。

它定义 35mm、平视、自然跟拍、环境叙事和生活方式电影感的镜头规范。

## Use When（使用场景）

当任务涉及：

```text
镜头设计
跟拍镜头
分镜摄影
视频 Prompt
电影感画面
镜头连续性
```

必须读取：

```text
CAM-001
```

## Key References

```text
SHOT-001
STYLE-001
EMOTION-001
BRAND-001
```

---

# LGT-001 — Warm Studio Lighting

## File

```text
database/lighting/LGT-001.md
```

## Notion DB

```text
Lighting DB
```

## 中文说明

LGT-001 是 Jump 工作室和办公室场景的默认灯光资产。

它定义温暖室内光、台灯、屏幕柔光、傍晚窗光和柔和阴影。

## Use When（使用场景）

当任务涉及：

```text
灯光设计
办公室灯光
温暖室内场景
视频 Prompt
摄影方案
封面视觉
```

必须读取：

```text
LGT-001
```

## Key References

```text
ENV-001
STYLE-001
COLOR-001
BRAND-001
```

## Never Do

```text
不得使用冷蓝赛博朋克灯光
不得使用恐怖片高反差
不得使用过度 RGB 灯效
不得使用舞台聚光灯
```

---

# PROMPT-001 — Jump After Work Master Prompt

## File

```text
database/prompts/PROMPT-001.md
```

## Notion DB

```text
Prompt DB
```

## 中文说明

PROMPT-001 是《跳跳下班啦》的主提示词模块。

它用于把角色、故事、场景、动作、镜头、灯光、资产和品牌语言组合成稳定可复用的 Prompt。

## Use When（使用场景）

当任务涉及：

```text
AI Prompt
视频 Prompt
图片 Prompt
角色一致性 Prompt
分镜 Prompt
封面 Prompt
```

必须读取：

```text
PROMPT-001
```

## Key References

```text
CHAR-001
ASSET-001
ENV-001
MOT-001
CAM-001
LGT-001
STYLE-001
BRAND-001
```

---

# ASSET-001 — Jump Character Reference Pack

## File

```text
database/assets/ASSET-001.md
```

## Notion DB

```text
Asset DB
```

## 中文说明

ASSET-001 是 Jump 的角色参考资产包。

它用于保证 Jump 在图片、视频、封面、分镜和 AI 生成流程中的视觉一致性。

## Use When（使用场景）

当任务涉及：

```text
Jump 角色一致性
角色参考图
图片生成
视频生成
封面设计
分镜生产
Prompt 约束
```

必须读取：

```text
ASSET-001
```

## Key References

```text
CHAR-001
OUTFIT-001
COLOR-001
STYLE-001
BRAND-001
```

## Required Rule

任何涉及 Jump 的生成任务都必须引用：

```text
ASSET-001
```

---

# PROJ-001 — Jump After Work Pilot Project

## File

```text
database/projects/PROJ-001.md
```

## Notion DB

```text
Project DB
```

## 中文说明

PROJ-001 是《跳跳下班啦》的第一个试播项目记录。

它将角色、剧集、故事、环境、动作、镜头、灯光、提示词和资产组合成一个完整生产项目。

## Use When（使用场景）

当任务涉及：

```text
完整生产流程
项目生产包
分镜生成
视频生成
发布规划
项目复盘
```

必须读取：

```text
PROJ-001
```

## Key References

```text
CHAR-001
EP-001
STORY-001
ENV-001
MOT-001
CAM-001
LGT-001
PROMPT-001
ASSET-001
```

---

# Database and Knowledge Mapping（数据库与知识映射）

| Database Record | Key Knowledge References |
|---|---|
| CHAR-001 | STYLE-001, COLOR-001, OUTFIT-001, BRAND-001 |
| EP-001 | WORLD-001, EMOTION-001, STORYFORMULA-001, BRAND-001 |
| STORY-001 | STORYFORMULA-001, EMOTION-001, BRAND-001 |
| ENV-001 | STYLE-001, COLOR-001, BRAND-001 |
| MOT-001 | MOTIONLANG-001, EMOTION-001 |
| CAM-001 | SHOT-001, STYLE-001 |
| LGT-001 | STYLE-001, COLOR-001 |
| PROMPT-001 | STYLE-001, COLOR-001, WORLD-001, BRAND-001 |
| ASSET-001 | CHAR-001, OUTFIT-001, COLOR-001, BRAND-001 |
| PROJ-001 | All core records |

---

# Database and Command Mapping（数据库与命令映射）

| Command | Required Database Records |
|---|---|
| COMMAND-001 | All 10 core records |
| COMMAND-002 | CHAR-001, STORY-001, ENV-001, MOT-001, CAM-001, LGT-001, PROMPT-001, ASSET-001, PROJ-001 |
| COMMAND-003 | PROJ-001, CHAR-001, EP-001, STORY-001, ENV-001, MOT-001, CAM-001, LGT-001, PROMPT-001, ASSET-001 |
| COMMAND-004 | EP-001, STORY-001, PROMPT-001, ASSET-001, PROJ-001 |
| COMMAND-005 | All 10 core records |

---

# Database and Workflow Mapping（数据库与工作流映射）

| Workflow | Required Database Records |
|---|---|
| WORKFLOW-001 | All 10 core records |
| WORKFLOW-002 | CHAR-001, STORY-001, ENV-001, MOT-001, CAM-001, LGT-001, PROMPT-001, ASSET-001, PROJ-001 |
| WORKFLOW-003 | All 10 core records |
| WORKFLOW-004 | EP-001, STORY-001, PROMPT-001, ASSET-001, PROJ-001 |

---

# Naming Rule（命名规则）

Database Records 必须遵守：

```text
Record ID = PREFIX-XXX
File Name = PREFIX-XXX.md
Notion Title = PREFIX-XXX only
Page H1 = PREFIX-XXX + Human-readable Name
```

示例：

```text
GitHub File:
database/projects/PROJ-001.md

Notion Title:
PROJ-001

Page H1:
# PROJ-001 — Jump After Work Pilot Project（跳跳下班啦试播项目）
```

---

# Notion Sync Rule（Notion 同步规则）

当前 Notion 同步范围：

```text
Character DB
Episode DB
Story DB
Environment DB
Motion DB
Camera DB
Lighting DB
Prompt DB
Asset DB
Project DB
```

Notion 主标题必须只写 Record ID：

```text
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
```

不要写：

```text
Jump
跳跳
📖 STORY-001 — Work Ends, Adventure Begins
```

---

# Database Safety Rules（数据库安全规则）

AI 工具不得：

```text
临时修改 Database Record ID
临时修改 Jump 核心身份
临时新增未经确认的 Database Record
删除现有记录
绕过 ASSET-001
把 Notion 当成最终事实来源
重复定义 Knowledge Rules
改变目录结构
改变命名规范
```

---

# Required Runtime Docs（相关运行文档）

使用 Database Records 时应参考：

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
```

---

# Related Directories（相关目录）

```text
database/
knowledge/
commands/
workflows/
agents/
docs/studio-os/
examples/
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial production database index |