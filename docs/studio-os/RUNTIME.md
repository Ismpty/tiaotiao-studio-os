# RUNTIME — TiaoTiao Studio OS Runtime Guide（运行指南）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件定义 TiaoTiao Studio OS 在实际运行时应该如何被读取、调用和执行。

它的目标是让 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具在进入本仓库后，能够理解：

- 应该先读哪些文件
- 什么是 Source of Truth
- 如何调用 Commands
- 如何执行 Workflows
- 如何使用 Agents
- 如何引用 Database Records
- 如何遵守 Knowledge Nodes
- 如何避免随意修改核心设定

## English

This file defines how TiaoTiao Studio OS should be read, called and executed at runtime.

It helps AI tools understand the correct reading order, source of truth, command usage, workflow execution, agent roles, database references and knowledge constraints.

---

# Runtime Principle（运行原则）

TSOS 的运行原则是：

```text
Knowledge Nodes define rules.
Database Records define production entities.
Assets define reference materials.
Prompts define generation modules.
Projects assemble records.
Agents perform creative tasks.
Workflows define execution order.
Commands trigger operations.
```

任何 AI 工具在运行 TSOS 时，都不能绕过这个顺序。

---

# Source of Truth（唯一事实来源）

## Primary Source（主要来源）

GitHub 仓库是 TSOS 的唯一事实来源。

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

也就是说：

- 角色设定以 GitHub 文件为准
- 世界观以 GitHub 文件为准
- Knowledge Nodes 以 GitHub 文件为准
- Database Records 以 GitHub 文件为准
- Agents / Workflows / Commands 以 GitHub 文件为准

Notion 用于管理、查看和同步 Production Records，但不作为最终规则来源。

---

# Runtime Reading Order（运行读取顺序）

AI 工具进入 TSOS 后，必须优先按照以下顺序读取：

```text
1. AGENTS.md
2. CODEX-HANDOFF.md
3. docs/studio-os/START-HERE.md
4. README.md
5. ARCHITECTURE.md
6. CHANGELOG.md
7. knowledge/README.md
8. database/
9. agents/
10. workflows/
11. commands/
12. docs/
13. examples/
```

---

# Required Core Files（核心必读文件）

运行任何正式任务前，至少需要读取：

```text
AGENTS.md
CODEX-HANDOFF.md
docs/studio-os/START-HERE.md
README.md
ARCHITECTURE.md
CHANGELOG.md
knowledge/README.md
```

如果任务与 Jump / 跳跳相关，还必须读取：

```text
database/characters/CHAR-001.md
database/assets/ASSET-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Core System Layers（核心系统层）

TSOS 当前由以下层组成：

```text
knowledge/
database/
agents/
workflows/
commands/
docs/
examples/
```

---

## 1. Knowledge Layer（知识层）

路径：

```text
knowledge/
```

作用：

定义长期稳定的规范。

包括：

```text
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
SHOT-002
MOTIONLANG-001
OUTFIT-001
MUSIC-001
STORYFORMULA-001
BRAND-001
```

规则：

Knowledge Nodes 不能被临时修改。

如果输出内容与 Knowledge 冲突，必须以 Knowledge 为准。

---

## 2. Production Database（生产数据库）

路径：

```text
database/
```

作用：

定义生产中使用的具体记录。

当前核心 Records：

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

规则：

Database Records 负责引用 Knowledge，而不是重复改写 Knowledge。

---

## 3. Agents（智能体层）

路径：

```text
agents/
```

作用：

定义 AI 执行角色。

当前 Agents：

```text
AGENT-001 — Storyboard Agent
AGENT-002 — Prompt Engineer Agent
AGENT-003 — Cinematography Agent
AGENT-004 — Script Agent
AGENT-005 — Editing Agent
AGENT-006 — Publishing Agent
```

规则：

Agents 只能执行任务，不能修改 Source of Truth。

---

## 4. Workflows（工作流层）

路径：

```text
workflows/
```

作用：

定义执行顺序。

当前 Workflows：

```text
WORKFLOW-001 — Jump After Work Production Workflow
WORKFLOW-002 — Short Video Prompt Workflow
WORKFLOW-003 — Storyboard to Video Workflow
WORKFLOW-004 — Publishing Workflow
```

规则：

Workflows 决定 Agents 如何协作。

---

## 5. Commands（命令层）

路径：

```text
commands/
```

作用：

定义用户可直接调用的操作命令。

当前 Commands：

```text
COMMAND-001 — Run Jump After Work Production
COMMAND-002 — Generate Video Prompt Package
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

规则：

Commands 是运行 TSOS 的入口。

---

# Runtime Command Usage（命令调用方式）

用户可以通过以下方式调用 TSOS：

```text
Run COMMAND-001.
```

```text
运行 COMMAND-002，生成身份卡 + 故事板 + 通用视频 Prompt。
```

```text
运行 COMMAND-003，生成 45 秒竖屏分镜。
```

```text
运行 COMMAND-004，生成小红书发布包。
```

```text
运行 COMMAND-005，检查这个 Prompt 是否符合跳跳设定。
```

---

# Command Routing（命令路由）

AI 工具必须根据用户意图选择正确 Command。

| User Intent 用户意图 | Command |
|---|---|
| 完整生产一条《跳跳下班啦》视频 | COMMAND-001 |
| 生成图片 / 视频 Prompt | COMMAND-002 |
| 生成分镜 | COMMAND-003 |
| 生成发布标题、正文、标签 | COMMAND-004 |
| 检查是否符合设定 | COMMAND-005 |

---

# Runtime Execution Example（运行示例）

## User Input

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

## Runtime Should Execute

```text
1. Read commands/COMMAND-003.md
2. Read workflows/WORKFLOW-001.md
3. Read agents/director/AGENT-001.md
4. Read database/projects/PROJ-001.md
5. Read database/characters/CHAR-001.md
6. Read database/stories/STORY-001.md
7. Read database/environments/ENV-001.md
8. Read database/assets/ASSET-001.md
9. Read required Knowledge Nodes
10. Output storyboard using COMMAND-003 format
```

---

# Default Runtime Project（默认运行项目）

除非用户明确指定其他项目，默认项目为：

```text
PROJ-001 — Jump After Work Pilot Project
```

默认角色为：

```text
CHAR-001 — Jump
```

默认剧集为：

```text
EP-001 — Jump After Work
```

默认故事为：

```text
STORY-001 — Work Ends, Adventure Begins
```

---

# Runtime Safety Rules（运行安全规则）

AI 工具在运行 TSOS 时必须遵守：

```text
[ ] 不得临时修改 Jump 的核心身份
[ ] 不得临时修改 TiaoTiao Universe 世界观
[ ] 不得临时修改 Brand Language
[ ] 不得新增未确认的 Master Knowledge
[ ] 不得绕过 Database Records
[ ] 不得绕过 ASSET-001
[ ] 不得省略一致性检查
[ ] 不得把 Notion 当成唯一事实来源
[ ] 不得随意改变已冻结 Roadmap
```

---

# Jump Runtime Rules（Jump 运行规则）

任何涉及 Jump 的任务，都必须保持：

```text
Jump = real dog-form character wearing programmer-style dog clothes
```

必须引用：

```text
CHAR-001
ASSET-001
OUTFIT-001
COLOR-001
BRAND-001
```

禁止：

```text
把 Jump 改成人类
去掉毛茸茸质感
改成其他动物
改成肌肉型角色
改成黑暗恐怖角色
改成赛博朋克角色
去掉程序员身份
```

---

# Prompt Runtime Rules（Prompt 运行规则）

任何生成 Prompt 的任务，必须：

```text
[ ] 引用 Source Records
[ ] 在 Source References 中引用 ASSET-001
[ ] 在模型可见 Prompt 中把 ASSET-001 转写成自然语言角色描述
[ ] 包含 Negative Prompt
[ ] 说明目标模型
[ ] 保持角色一致
[ ] 保持视觉风格一致
[ ] 保持品牌语言一致
```

Prompt 默认调用：

```text
COMMAND-002
WORKFLOW-002
AGENT-002
PROMPT-001
```

---

# Storyboard Runtime Rules（分镜运行规则）

任何生成分镜的任务，必须：

```text
[ ] 引用 STORYFORMULA-001
[ ] 引用 CHAR-001
[ ] 引用 ASSET-001
[ ] 引用 ENV-001
[ ] 引用 CAM-001
[ ] 引用 LGT-001
[ ] 输出 Shot List
[ ] 输出 Shot Details
[ ] 输出 Continuity Checklist
```

Storyboard 默认调用：

```text
COMMAND-003
AGENT-001
WORKFLOW-001
```

---

# Publishing Runtime Rules（发布运行规则）

任何生成发布包的任务，必须：

```text
[ ] 引用 BRAND-001
[ ] 避免标题党
[ ] 避免职场焦虑
[ ] 避免强营销腔
[ ] 生成标题
[ ] 生成正文
[ ] 生成标签
[ ] 生成封面文案
[ ] 生成发布前检查清单
[ ] 生成发布后复盘模板
```

Publishing 默认调用：

```text
COMMAND-004
WORKFLOW-004
AGENT-006
```

---

# Consistency Runtime Rules（一致性检查规则）

任何正式输出前，必须能够调用：

```text
COMMAND-005 — Run Consistency Check
```

检查对象包括：

```text
Storyboard
Prompt
Script
Editing Plan
Publishing Package
Generated Image
Generated Video
Project Package
```

最终结果必须输出：

```text
PASS
FAIL
PASS WITH MINOR FIXES
```

---

# Notion Runtime Policy（Notion 运行策略）

Notion 当前只同步 Production Database Records：

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

以下内容暂不同步 Notion：

```text
Agents
Workflows
Commands
Runtime Docs
Examples
```

原因：

```text
Agents, Workflows and Commands are operating instructions.
GitHub is the source of truth for runtime behavior.
```

---

# Git Runtime Policy（Git 运行策略）

所有结构性更新都应提交到 GitHub。

建议提交规范：

```text
feat(agent): add AGENT-XXX Name
feat(workflow): add WORKFLOW-XXX Name
feat(command): add COMMAND-XXX Name
feat(docs): add runtime documentation
chore(changelog): update phase checkpoint
```

---

# Runtime Output Standard（运行输出标准）

所有正式输出必须做到：

```text
[ ] 可执行
[ ] 可追溯
[ ] 可复用
[ ] 有明确来源
[ ] 有一致性检查
[ ] 不空泛
[ ] 不随意改设定
[ ] 不脱离 TSOS Source of Truth
```

---

# Standard Runtime Response Format（标准运行回复格式）

当用户调用 Command 时，输出建议使用：

```text
# COMMAND-XXX Output

## Source Records

## Execution Summary

## Output

## Consistency Checklist

## Next Actions
```

---

# Runtime Failure Handling（运行失败处理）

当用户要求与 TSOS 冲突时，必须这样处理：

```text
1. 标记冲突
2. 说明冲突的 Source of Truth
3. 不直接执行错误修改
4. 提供符合 TSOS 的替代方案
```

示例：

```text
Issue Found:
The request changes Jump from a real dog-form character into a human.

Source of Truth:
CHAR-001
ASSET-001

Action:
Cannot apply this change under current TSOS rules.
```

---

# Runtime Summary（运行总结）

TSOS 当前运行逻辑为：

```text
User Command
↓
Operating Command
↓
Workflow Template
↓
AI Agent
↓
Database Records
↓
Knowledge Nodes
↓
Production Output
↓
Consistency Check
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial runtime guide |
