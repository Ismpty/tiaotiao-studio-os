# INDEX — TiaoTiao Studio OS Navigation Index（导航索引）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 TiaoTiao Studio OS 的导航索引。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- TSOS 当前有哪些系统层
- 每一层放在哪里
- 每一层应该什么时候读取
- 每个核心文件的用途是什么
- 用户提出任务时应该如何快速定位文件
- 如何避免在仓库中迷路

## English

This file is the navigation index for TiaoTiao Studio OS.

It helps AI tools quickly locate system layers, runtime files, commands, workflows, agents, database records and knowledge nodes.

---

# Source of Truth（唯一事实来源）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

所有正式规则、记录、命令、工作流、智能体和运行文档，都以 GitHub 文件为准。

---

# Recommended Reading Order（推荐读取顺序）

AI 工具进入仓库后，建议按以下顺序读取：

```text
1. AGENTS.md
2. CODEX-HANDOFF.md
3. docs/studio-os/START-HERE.md
4. README.md
5. ARCHITECTURE.md
6. CHANGELOG.md
7. docs/studio-os/INDEX.md
8. docs/studio-os/RUNTIME.md
9. docs/studio-os/CODEX.md
10. docs/studio-os/COMMANDS.md
11. docs/studio-os/WORKFLOWS.md
12. docs/studio-os/AGENTS.md
13. docs/studio-os/PROMPT-RUNTIME-RULES.md
14. knowledge/README.md
15. database/
16. commands/
17. workflows/
18. agents/
19. examples/
```

---

# System Layers（系统层级）

TSOS 当前由以下系统层组成：

```text
knowledge/
database/
agents/
workflows/
commands/
docs/studio-os/
examples/
```

Fastest direct-use guide:

```text
docs/studio-os/START-HERE.md
```

---

# 1. Knowledge Layer（知识层）

## Path

```text
knowledge/
```

## Purpose

Knowledge Layer 定义长期稳定的创作规则。

它回答：

```text
这个世界是什么？
角色视觉风格是什么？
品牌语言是什么？
镜头语言是什么？
动作语言是什么？
音乐语言是什么？
故事公式是什么？
```

## Core Files

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

## When to Read

当任务涉及以下内容时，必须读取 Knowledge：

```text
视觉风格
品牌语言
世界观
角色情绪
镜头语言
动作语言
服装系统
音乐方向
故事公式
```

## Rule

Knowledge Nodes 不应被临时修改。

---

# 2. Production Database（生产数据库）

## Path

```text
database/
```

## Purpose

Production Database 定义具体生产记录。

它回答：

```text
角色是谁？
剧集是什么？
故事是什么？
场景是什么？
动作是什么？
镜头是什么？
灯光是什么？
Prompt 是什么？
资产参考是什么？
项目是什么？
```

## Core Records

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

## When to Read

当任务涉及具体生产内容时，必须读取 Database Records。

例如：

```text
生成跳跳分镜
生成跳跳 Prompt
生成发布包
检查角色一致性
生成项目生产包
```

## Rule

Database Records 应引用 Knowledge Nodes，不应重复制造新规则。

---

# 3. Agents（智能体层）

## Path

```text
agents/
```

## Purpose

Agents 定义 AI 创作角色。

它回答：

```text
谁来做分镜？
谁来写 Prompt？
谁来设计摄影？
谁来写脚本？
谁来设计剪辑？
谁来做发布？
```

## Core Agents

```text
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
agents/cinematographer/AGENT-003.md
agents/writer/AGENT-004.md
agents/editor/AGENT-005.md
agents/publisher/AGENT-006.md
```

## Agent Index

| Agent | Role | Path |
|---|---|---|
| AGENT-001 | Storyboard Agent | agents/director/AGENT-001.md |
| AGENT-002 | Prompt Engineer Agent | agents/prompt-engineer/AGENT-002.md |
| AGENT-003 | Cinematography Agent | agents/cinematographer/AGENT-003.md |
| AGENT-004 | Script Agent | agents/writer/AGENT-004.md |
| AGENT-005 | Editing Agent | agents/editor/AGENT-005.md |
| AGENT-006 | Publishing Agent | agents/publisher/AGENT-006.md |

## When to Read

当任务需要执行具体创作职责时，读取对应 Agent。

## Rule

Agents 只能执行任务，不能修改 Source of Truth。

---

# 4. Workflows（工作流层）

## Path

```text
workflows/
```

## Purpose

Workflows 定义执行顺序。

它回答：

```text
完整生产流程怎么走？
Prompt 生成流程怎么走？
分镜如何转视频？
发布包如何生成？
```

## Core Workflows

```text
workflows/WORKFLOW-001.md
workflows/WORKFLOW-002.md
workflows/WORKFLOW-003.md
workflows/WORKFLOW-004.md
```

## Workflow Index

| Workflow | Purpose | Path |
|---|---|---|
| WORKFLOW-001 | Jump After Work Production Workflow | workflows/WORKFLOW-001.md |
| WORKFLOW-002 | Short Video Prompt Workflow | workflows/WORKFLOW-002.md |
| WORKFLOW-003 | Storyboard to Video Workflow | workflows/WORKFLOW-003.md |
| WORKFLOW-004 | Publishing Workflow | workflows/WORKFLOW-004.md |

## When to Read

当任务需要多个步骤协作时，必须读取 Workflow。

## Rule

Workflow 决定执行顺序，不覆盖 Knowledge 或 Database。

---

# 5. Commands（命令层）

## Path

```text
commands/
```

## Purpose

Commands 是 TSOS 的操作入口。

它回答：

```text
用户一句话应该触发哪个系统命令？
```

## Core Commands

```text
commands/COMMAND-001.md
commands/COMMAND-002.md
commands/COMMAND-003.md
commands/COMMAND-004.md
commands/COMMAND-005.md
```

## Command Index

| Command | Purpose | Path |
|---|---|---|
| COMMAND-001 | Run Jump After Work Production | commands/COMMAND-001.md |
| COMMAND-002 | Generate Video Prompt Package | commands/COMMAND-002.md |
| COMMAND-003 | Generate Storyboard | commands/COMMAND-003.md |
| COMMAND-004 | Generate Publishing Package | commands/COMMAND-004.md |
| COMMAND-005 | Run Consistency Check | commands/COMMAND-005.md |

## When to Read

当用户提出任务时，优先根据意图路由到 Command。

## Rule

Commands 是入口，不是自由发挥提示词。

---

# 6. Runtime Docs（运行文档层）

## Path

```text
docs/studio-os/
```

## Purpose

Runtime Docs 说明 TSOS 如何被 AI 工具读取和运行。

## Core Docs

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
```

## Runtime Docs Index

| Doc | Purpose |
|---|---|
| INDEX.md | Navigation index |
| RUNTIME.md | Runtime guide |
| CODEX.md | Codex operating guide |
| COMMANDS.md | Commands guide |
| WORKFLOWS.md | Workflows guide |
| AGENTS.md | Agents guide |

## When to Read

当 AI 工具不确定怎么运行 TSOS 时，先读取 Runtime Docs。

---

# 7. Examples（示例层）

## Path

```text
examples/
```

## Purpose

Examples 展示命令输出应该长什么样。

## Core Examples

```text
examples/COMMAND-001-output.md
examples/COMMAND-002-prompt.md
examples/COMMAND-003-storyboard.md
```

## Example Index

| Example | Purpose |
|---|---|
| COMMAND-001-output.md | 完整生产包示例 |
| COMMAND-002-prompt.md | 短视频 Prompt 示例 |
| COMMAND-003-storyboard.md | 分镜输出示例 |

## When to Read

当需要输出格式参考时，读取 Examples。

---

# Task Routing Quick Guide（任务路由速查）

| User Task 用户任务 | Read First | Then Read |
|---|---|---|
| 完整生产一条视频 | COMMAND-001 | WORKFLOW-001 + all agents |
| 生成视频 Prompt Package | COMMAND-002 | WORKFLOW-002 + AGENT-002 |
| 生成分镜 | COMMAND-003 | AGENT-001 + WORKFLOW-001 |
| 分镜转视频 | WORKFLOW-003 | AGENT-002 + AGENT-003 |
| 生成发布包 | COMMAND-004 | WORKFLOW-004 + AGENT-006 |
| 检查一致性 | COMMAND-005 | relevant Database + Knowledge |
| 检查 Jump 是否偏离 | COMMAND-005 | CHAR-001 + ASSET-001 |
| 更新系统文档 | docs/studio-os/INDEX.md | RUNTIME + CODEX |
| 给 Codex 使用说明 | CODEX.md | RUNTIME.md |

---

# Default Jump Production Stack（默认跳跳生产栈）

任何涉及 Jump / 跳跳 的任务，默认读取：

```text
CHAR-001
ASSET-001
OUTFIT-001
COLOR-001
BRAND-001
```

具体路径：

```text
database/characters/CHAR-001.md
database/assets/ASSET-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/color/COLOR-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Default Project Stack（默认项目栈）

当前默认项目为：

```text
PROJ-001 — Jump After Work Pilot Project
```

默认读取：

```text
database/projects/PROJ-001.md
database/episodes/EP-001.md
database/stories/STORY-001.md
database/characters/CHAR-001.md
database/assets/ASSET-001.md
```

---

# Default Prompt Stack（默认提示词栈）

生成 Prompt 时默认读取：

```text
commands/COMMAND-002.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
database/prompts/PROMPT-001.md
database/characters/CHAR-001.md
database/assets/ASSET-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Default Storyboard Stack（默认分镜栈）

生成分镜时默认读取：

```text
commands/COMMAND-003.md
agents/director/AGENT-001.md
database/projects/PROJ-001.md
database/stories/STORY-001.md
database/characters/CHAR-001.md
database/environments/ENV-001.md
database/cameras/CAM-001.md
database/lighting/LGT-001.md
database/assets/ASSET-001.md
knowledge/story-formula/STORYFORMULA-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Default Publishing Stack（默认发布栈）

生成发布包时默认读取：

```text
commands/COMMAND-004.md
workflows/WORKFLOW-004.md
agents/publisher/AGENT-006.md
database/projects/PROJ-001.md
database/assets/ASSET-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Default Consistency Stack（默认一致性检查栈）

运行一致性检查时默认读取：

```text
commands/COMMAND-005.md
database/characters/CHAR-001.md
database/assets/ASSET-001.md
database/projects/PROJ-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/world/WORLD-001.md
knowledge/emotion/EMOTION-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Navigation Rules（导航规则）

AI 工具必须遵守：

```text
[ ] 先判断用户任务类型
[ ] 再选择 Command
[ ] 再读取 Workflow
[ ] 再读取 Agent
[ ] 再读取 Database Records
[ ] 再读取 Knowledge Nodes
[ ] 最后生成输出
[ ] 正式输出前可运行 COMMAND-005
```

---

# Never Do（禁止）

AI 工具不得：

```text
跳过 Source of Truth
只凭对话记忆生成
把 Notion 当最终来源
临时改 Jump 设定
临时改世界观
临时改品牌语言
绕过 ASSET-001
绕过 Knowledge Nodes
绕过 Database Records
改变命名规则
改变目录结构
```

---

# Final Summary（总结）

TSOS 的导航逻辑是：

```text
User Intent
↓
Command
↓
Workflow
↓
Agent
↓
Database Record
↓
Knowledge Node
↓
Output
↓
Consistency Check
```

本文件用于让任何 AI 工具快速定位正确文件，并避免随意创作或误改系统结构。

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial Studio OS navigation index |
