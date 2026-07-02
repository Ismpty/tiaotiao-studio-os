# CODEX — TiaoTiao Studio OS Codex Guide（Codex 使用指南）

> Runtime Documentation（运行文档）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件定义 Codex 在读取、理解和操作 TiaoTiao Studio OS 时应该遵守的规则。

它的目标是让 Codex 能够正确使用本仓库，而不是把它当成普通文档仓库随意修改。

Codex 应该理解：

- 哪些文件是 Source of Truth
- 哪些内容可以生成
- 哪些内容不能随意修改
- 如何读取 Knowledge、Database、Agents、Workflows、Commands
- 如何执行 TSOS 标准命令
- 如何避免破坏已冻结规划
- 如何保持 Jump / 跳跳 的角色一致性

## English

This file defines how Codex should read, understand and operate TiaoTiao Studio OS.

Codex should treat this repository as an AI Native Studio Operating System, not as a normal document collection.

---

# Core Rule（核心规则）

Codex 必须把 GitHub 仓库视为 TSOS 的唯一事实来源。

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Codex 不能把 Notion 当成最终设定来源。

---

# Codex Reading Order（Codex 读取顺序）

Codex 在执行任何任务前，应该按照以下顺序读取：

```text
1. README.md
2. ARCHITECTURE.md
3. CHANGELOG.md
4. docs/studio-os/RUNTIME.md
5. docs/studio-os/CODEX.md
6. knowledge/README.md
7. knowledge/
8. database/
9. agents/
10. workflows/
11. commands/
12. examples/
```

---

# Required Files Before Action（执行前必读文件）

Codex 在修改或生成内容前，至少应读取：

```text
README.md
ARCHITECTURE.md
CHANGELOG.md
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
```

如果任务涉及 Jump / 跳跳，必须额外读取：

```text
database/characters/CHAR-001.md
database/assets/ASSET-001.md
knowledge/outfit/OUTFIT-001.md
knowledge/color/COLOR-001.md
knowledge/brand-language/BRAND-001.md
```

如果任务涉及视频生产，必须额外读取：

```text
database/projects/PROJ-001.md
commands/COMMAND-001.md
workflows/WORKFLOW-001.md
```

如果任务涉及 Prompt，必须额外读取：

```text
commands/COMMAND-002.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
database/prompts/PROMPT-001.md
```

---

# Repository Layers（仓库层级）

Codex 必须理解 TSOS 当前层级：

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

## 1. Knowledge Layer

路径：

```text
knowledge/
```

作用：

定义稳定规则。

Codex 不得随意改写 Knowledge Nodes。

只有用户明确要求进行系统迭代时，才可以建议修改 Knowledge。

---

## 2. Database Layer

路径：

```text
database/
```

作用：

定义生产记录。

Database Records 应该引用 Knowledge Nodes，而不是重复制造新规则。

---

## 3. Agents Layer

路径：

```text
agents/
```

作用：

定义 AI 角色和执行职责。

Codex 可以读取 Agents 来决定该用什么方式输出。

---

## 4. Workflow Layer

路径：

```text
workflows/
```

作用：

定义执行顺序。

Codex 执行复杂任务时必须按 Workflow 顺序操作。

---

## 5. Command Layer

路径：

```text
commands/
```

作用：

定义用户可直接调用的操作命令。

Codex 应优先通过 Commands 理解用户需求。

---

## 6. Runtime Docs

路径：

```text
docs/studio-os/
```

作用：

定义 TSOS 如何运行。

---

# Command Routing Rules（命令路由规则）

当用户提出任务时，Codex 应根据意图匹配 Command。

| User Intent 用户意图 | Codex Should Use |
|---|---|
| 生产完整《跳跳下班啦》项目 | COMMAND-001 |
| 生成图片 / 视频 Prompt | COMMAND-002 |
| 生成分镜 | COMMAND-003 |
| 生成发布包 | COMMAND-004 |
| 检查一致性 | COMMAND-005 |

---

# Standard Command Execution（标准命令执行）

当用户说：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

Codex 应执行：

```text
1. Read commands/COMMAND-003.md
2. Read agents/director/AGENT-001.md
3. Read workflows/WORKFLOW-001.md
4. Read database/projects/PROJ-001.md
5. Read required database records
6. Read required knowledge nodes
7. Generate output using COMMAND-003 format
8. Run consistency check rules
```

---

# Source of Truth Priority（事实来源优先级）

当文件内容发生冲突时，Codex 应按以下优先级判断：

```text
1. README.md
2. ARCHITECTURE.md
3. docs/studio-os/RUNTIME.md
4. commands/
5. workflows/
6. agents/
7. database/
8. knowledge/
9. examples/
10. older conversation context
```

但对于角色、世界观、品牌、风格类内容：

```text
Knowledge Nodes + Database Records
```

优先于临时对话。

---

# Jump Character Rules（Jump 角色规则）

任何涉及 Jump 的生成，Codex 必须保持：

```text
Jump = anthropomorphic fluffy female dog programmer
```

必须遵守：

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
把 Jump 改成其他动物
去掉毛茸茸质感
改成肌肉型体型
改变程序员身份
改变核心品牌色
改成恐怖 / 黑暗 / 赛博朋克角色
```

---

# File Creation Rules（文件创建规则）

Codex 创建新文件时必须遵守目录结构。

## Agents

```text
agents/{role-group}/AGENT-XXX.md
```

示例：

```text
agents/director/AGENT-001.md
agents/prompt-engineer/AGENT-002.md
```

---

## Workflows

```text
workflows/WORKFLOW-XXX.md
```

示例：

```text
workflows/WORKFLOW-001.md
```

---

## Commands

```text
commands/COMMAND-XXX.md
```

示例：

```text
commands/COMMAND-001.md
```

---

## Studio OS Docs

```text
docs/studio-os/{DOC_NAME}.md
```

示例：

```text
docs/studio-os/RUNTIME.md
docs/studio-os/CODEX.md
```

---

## Database Records

```text
database/{category}/{RECORD-ID}.md
```

示例：

```text
database/characters/CHAR-001.md
database/projects/PROJ-001.md
```

---

## Knowledge Nodes

```text
knowledge/{category}/{NODE-ID}.md
```

示例：

```text
knowledge/style/STYLE-001.md
knowledge/brand-language/BRAND-001.md
```

---

# Naming Rules（命名规则）

Codex 必须遵守统一命名规则。

## Database Records

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

## Knowledge Nodes

```text
STYLE-001
COLOR-001
WORLD-001
EMOTION-001
SHOT-001
MOTIONLANG-001
OUTFIT-001
MUSIC-001
STORYFORMULA-001
BRAND-001
```

## Agents

```text
AGENT-001
AGENT-002
AGENT-003
```

## Workflows

```text
WORKFLOW-001
WORKFLOW-002
WORKFLOW-003
```

## Commands

```text
COMMAND-001
COMMAND-002
COMMAND-003
```

---

# Modification Rules（修改规则）

Codex 不得随意修改已有规划。

## Allowed Without Explicit Approval（无需额外批准可做）

Codex 可以：

```text
新增已规划文件
补全文档缺失内容
修正路径错误
修正命名不一致
补充索引
补充引用关系
修复明显格式错误
```

---

## Requires Explicit User Approval（需要用户明确批准）

Codex 修改以下内容前必须获得确认：

```text
修改 Jump 核心设定
修改 TiaoTiao Universe 世界观
修改 Brand Language
删除已有 Database Record
删除 Knowledge Node
改变目录结构
新增未规划的系统层级
改变 Phase Roadmap
改变命名规范
```

---

# Changelog Rules（更新记录规则）

Codex 在完成阶段性工作后，应提醒更新：

```text
CHANGELOG.md
```

但在用户明确表示“等全部完成后再更新 CHANGELOG”时，Codex 应遵守，不要频繁输出 Changelog 片段。

标准 Changelog Commit：

```text
chore(changelog): complete Phase X description
```

---

# Git Commit Rules（提交规则）

Codex 建议 commit message 时，应使用以下格式：

```text
feat(agent): add AGENT-XXX Name
feat(workflow): add WORKFLOW-XXX Name
feat(command): add COMMAND-XXX Name
feat(docs): add runtime documentation
feat(database): add RECORD-ID Name
chore(changelog): complete Phase X
refactor(system): align naming and paths
```

---

# Push Policy（Push 策略）

当用户说：

```text
我还没有 push，等 Phase 完成后再一起 push
```

Codex 必须：

```text
1. 继续输出文件内容
2. 不催促 push
3. 在 Phase 结束后提供待 push 文件清单
4. 提供建议 commit message
```

---

# Notion Policy（Notion 策略）

Codex 应理解：

```text
Production Database Records → GitHub + Notion
Agents / Workflows / Commands / Docs → GitHub only
```

Notion 当前同步范围：

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

Codex 不应主动要求新增：

```text
Agent DB
Workflow DB
Command DB
```

除非用户进入后续专门 Phase。

---

# Consistency Check Requirement（一致性检查要求）

任何正式输出前，Codex 应能调用：

```text
COMMAND-005 — Run Consistency Check
```

检查：

```text
Character
World
Style
Color
Emotion
Motion
Camera
Lighting
Story
Prompt
Brand
Workflow
Publishing
```

最终结果必须明确：

```text
PASS
FAIL
PASS WITH MINOR FIXES
```

---

# Codex Output Standard（Codex 输出标准）

Codex 输出必须：

```text
[ ] 可执行
[ ] 可复制
[ ] 可追溯
[ ] 不空泛
[ ] 不乱改设定
[ ] 不跳过 Source of Truth
[ ] 不省略关键引用
[ ] 有明确文件路径
[ ] 有建议 commit message
```

---

# Standard File Output Format（标准文件输出格式）

Codex 给用户文件内容时，应使用：

```text
File:
path/to/file.md

Commit:
commit message
```

然后输出完整 Markdown。

---

# Runtime Failure Handling（运行失败处理）

当用户请求与 TSOS 冲突时，Codex 必须：

```text
1. 标记 Issue Found
2. 指出冲突的 Source of Truth
3. 不执行错误修改
4. 给出符合 TSOS 的替代方案
```

示例：

```text
Issue Found:
The request changes Jump from an anthropomorphic fluffy dog into a human.

Source of Truth:
CHAR-001
ASSET-001

Result:
Cannot apply this change under current TSOS rules.
```

---

# Codex Should Not Do（Codex 禁止行为）

Codex 不得：

```text
随意重构目录
随意删除文件
随意改命名规则
随意新增 DB
随意修改 Roadmap
把 Notion 当作最终设定来源
忽略 GitHub Source of Truth
把 Jump 改成人类
省略 ASSET-001
省略 Negative Prompt
省略一致性检查
```

---

# Codex Should Do（Codex 应该行为）

Codex 应该：

```text
先读系统文件
按 Command 路由任务
按 Workflow 执行流程
按 Agent 输出内容
按 Database 读取实体
按 Knowledge 保持规范
按 COMMAND-005 检查一致性
在 Phase 结束时整理文件清单
```

---

# Example Codex Task（Codex 任务示例）

## User Input

```text
运行 COMMAND-002，生成小红书 9:16 Kling 视频 Prompt。
```

## Codex Should Read

```text
commands/COMMAND-002.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
database/projects/PROJ-001.md
database/characters/CHAR-001.md
database/assets/ASSET-001.md
database/prompts/PROMPT-001.md
knowledge/style/STYLE-001.md
knowledge/color/COLOR-001.md
knowledge/brand-language/BRAND-001.md
```

## Codex Should Output

```text
# COMMAND-002 Output

## Prompt Purpose
## Target Model
## Source Records
## Base Prompt
## Model-Specific Prompt
## Negative Prompt
## Consistency Checklist
## Usage Notes
```

---

# Codex Runtime Summary（Codex 运行总结）

Codex 在 TSOS 中的正确执行逻辑是：

```text
User Request
↓
Command Routing
↓
Workflow Reading
↓
Agent Behavior
↓
Database References
↓
Knowledge Constraints
↓
Output Generation
↓
Consistency Check
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial Codex operating guide |