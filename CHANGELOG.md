# CHANGELOG

# Phase 9 — Validation and Test Runs Completed

> Date：2026  
> Status：Completed  
> Scope：Validation / Test Runs / Production Readiness

---

## Summary（总结）

Phase 9 完成了 TiaoTiao Studio OS 第一轮系统验证测试。

本阶段目标是验证 TSOS 是否已经可以真正运行，而不只是停留在系统结构、文档、命令、工作流和智能体定义层。

本轮测试依次运行并验证了：

- COMMAND-003 — Generate Storyboard
- COMMAND-002 — Generate Short Video Prompt
- COMMAND-005 — Run Consistency Check
- COMMAND-004 — Generate Publishing Package
- COMMAND-001 — Run Jump After Work Production

所有测试结果均为：

```text
PASS
```

这说明当前 TSOS 已经具备从分镜、Prompt、一致性检查、发布包到完整生产包的基础运行能力。

---

## Validation Tests Completed（已完成验证测试）

| Test | Command | Target | Path | Result |
|---|---|---|---|---|
| TEST-001 | COMMAND-003 | Storyboard Validation | validation/TEST-001-COMMAND-003-storyboard.md | PASS |
| TEST-002 | COMMAND-002 | Prompt Validation | validation/TEST-002-COMMAND-002-prompt.md | PASS |
| TEST-003 | COMMAND-005 | Consistency Check Validation | validation/TEST-003-COMMAND-005-consistency.md | PASS |
| TEST-004 | COMMAND-004 | Publishing Package Validation | validation/TEST-004-COMMAND-004-publishing.md | PASS |
| TEST-005 | COMMAND-001 | Full Production Package Validation | validation/TEST-005-COMMAND-001-production.md | PASS |

---

## TEST-001 — COMMAND-003 Storyboard Validation

验证目标：

```text
COMMAND-003 是否可以稳定生成《跳跳下班啦》45 秒 9:16 竖屏分镜。
```

验证内容包括：

- Storyboard Summary
- Story Beat Breakdown
- Shot List
- Shot Details
- Camera / Motion / Lighting Mapping
- Prompt Notes
- Continuity Notes
- Validation Checklist

结果：

```text
PASS
```

说明：

```text
COMMAND-003 能够正确调用 AGENT-001，并基于 PROJ-001、CHAR-001、STORY-001、ENV-001、CAM-001、LGT-001、ASSET-001 和相关 Knowledge Nodes 输出稳定分镜。
```

---

## TEST-002 — COMMAND-002 Prompt Validation

验证目标：

```text
COMMAND-002 是否可以基于 TEST-001 分镜结果生成适用于 Kling / Veo / Runway 的短视频 Prompt。
```

验证内容包括：

- Prompt Purpose
- Target Model
- Source Records
- Base Prompt
- Shot-by-shot Prompts
- Model-specific Prompt Validation
- Negative Prompt
- Chinese Production Notes
- Consistency Checklist

结果：

```text
PASS
```

说明：

```text
COMMAND-002 能够正确调用 AGENT-002 和 WORKFLOW-002，并生成可用于 AI 视频生成的模型适配 Prompt。
```

---

## TEST-003 — COMMAND-005 Consistency Check Validation

验证目标：

```text
COMMAND-005 是否可以检查 TEST-001 分镜输出和 TEST-002 Prompt 输出是否符合 TSOS Source of Truth。
```

验证内容包括：

- Character Consistency
- World Consistency
- Visual Style Check
- Color Check
- Emotion Check
- Motion Check
- Camera Check
- Lighting Check
- Story / Brand Check
- Prompt Consistency Check
- Workflow Compliance Check
- Issue List
- Final PASS / FAIL Result

结果：

```text
PASS
```

说明：

```text
COMMAND-005 能够正确检查 Jump 角色一致性、世界观、视觉风格、动作、镜头、灯光、故事公式和品牌语言。
```

---

## TEST-004 — COMMAND-004 Publishing Package Validation

验证目标：

```text
COMMAND-004 是否可以为 PROJ-001 生成适用于小红书的发布包。
```

验证内容包括：

- Publishing Summary
- Platform Strategy
- Title Options
- Caption / Description
- Hashtag Set
- Cover Text Suggestions
- Publishing Time Suggestion
- Pre-Publish Checklist
- Publishing Record
- Post-Publish Review Template
- Brand Safety Check

结果：

```text
PASS
```

说明：

```text
COMMAND-004 能够正确调用 AGENT-006 和 WORKFLOW-004，并生成符合 BRAND-001 的平台发布包。
```

---

## TEST-005 — COMMAND-001 Full Production Package Validation

验证目标：

```text
COMMAND-001 是否可以整合 TEST-001 至 TEST-004，形成完整《跳跳下班啦》Production Package。
```

验证内容包括：

- Project Brief
- Storyboard Output Validation
- Prompt Output Validation
- Cinematography Output Validation
- Script Output Validation
- Editing Output Validation
- Publishing Output Validation
- Final Consistency Checklist
- Next Production Actions
- Phase 9 Validation Summary

结果：

```text
PASS
```

说明：

```text
COMMAND-001 能够正确串联 WORKFLOW-001 和 AGENT-001 至 AGENT-006，并形成完整生产包。
```

---

## Validation Chain（验证链路）

Phase 9 验证链路为：

```text
TEST-001
COMMAND-003
Generate Storyboard
↓
TEST-002
COMMAND-002
Generate Short Video Prompt
↓
TEST-003
COMMAND-005
Run Consistency Check
↓
TEST-004
COMMAND-004
Generate Publishing Package
↓
TEST-005
COMMAND-001
Run Full Production Package
```

---

## Validation Source Records（验证来源记录）

本轮测试默认读取以下 Production Database Records：

```text
CHAR-001 — Jump
EP-001 — Jump After Work
STORY-001 — Work Ends, Adventure Begins
ENV-001 — TiaoTiao Studio Office
MOT-001 — Natural Walking
CAM-001 — Hero Tracking Camera
LGT-001 — Warm Studio Lighting
PROMPT-001 — Jump After Work Master Prompt
ASSET-001 — Jump Character Reference Pack
PROJ-001 — Jump After Work Pilot Project
```

---

## Validation Knowledge Nodes（验证知识节点）

本轮测试默认读取以下 Knowledge Nodes：

```text
STYLE-001 — Cinematic Documentary
COLOR-001 — Fire Dragon Fruit Palette
WORLD-001 — TiaoTiao Universe
EMOTION-001 — Freedom
SHOT-001 — Hero Tracking Shot
MOTIONLANG-001 — Natural Walking Language
OUTFIT-001 — Programmer Outfit System
MUSIC-001 — Lifestyle Music Language
STORYFORMULA-001 — Work Ends, Adventure Begins
BRAND-001 — TiaoTiao Studio Brand Language
```

---

## Validation Result Summary（验证结果总结）

```text
TEST-001:
PASS

TEST-002:
PASS

TEST-003:
PASS

TEST-004:
PASS

TEST-005:
PASS
```

整体结果：

```text
Phase 9 Validation Result:
PASS
```

---

## Issues Found（发现问题）

```text
Critical Issues:
None

Major Issues:
None

Minor Issues:
None
```

---

## Production Readiness（生产可用性）

Phase 9 验证后，TSOS 当前具备以下生产能力：

```text
[PASS] Can generate storyboard
[PASS] Can generate model-ready video prompts
[PASS] Can run consistency checks
[PASS] Can generate publishing package
[PASS] Can assemble full production package
[PASS] Can preserve Jump character consistency
[PASS] Can preserve TSOS Source of Truth
[PASS] Can follow runtime commands
[PASS] Can follow workflow sequence
[PASS] Can use agents correctly
```

---

## Current System Status（当前系统状态）

```text
TSOS Status:
Readable
Navigable
Callable
Executable
Validated
Production-ready for PROJ-001 pilot workflow
```

---

## Next Phase（下一阶段）

建议下一阶段：

```text
Phase 10 — Production Output and Real Asset Generation
```

Phase 10 目标：

开始真正进入生产，不再只是文档验证。

优先级：

1. Generate actual shot-by-shot Kling / Veo / Runway prompts
2. Produce first video clips
3. Run COMMAND-005 on generated clips
4. Create first cover image package
5. Generate final publishing copy
6. Publish first PROJ-001 test content
7. Record post-publish metrics

---

## Change Type（变更类型）

- Added validation test files
- Validated COMMAND-003 storyboard output
- Validated COMMAND-002 prompt output
- Validated COMMAND-005 consistency check
- Validated COMMAND-004 publishing package
- Validated COMMAND-001 full production package
- Confirmed Phase 9 PASS result
- Confirmed PROJ-001 production workflow readiness

---

## Status

```text
Phase 9 Validation and Test Runs: Completed
Ready for Phase 10 Production Output and Real Asset Generation
```


# Phase 8 — Index and Navigation Layer Completed

> Date：2026  
> Status：Completed  
> Scope：Index / Navigation / Architecture Update

---

## Summary（总结）

Phase 8 完成了 TiaoTiao Studio OS 的索引与导航层。

本阶段目标是让 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具进入仓库后，能够快速理解：

- 系统有哪些层
- 每层放在哪里
- 应该先读什么
- 用户任务应该路由到哪个 Command
- Command 对应哪个 Workflow
- Workflow 调用哪些 Agents
- Database Records 和 Knowledge Nodes 如何被引用
- 示例输出在哪里查看

现在 TSOS 已经具备完整的导航入口，不再只是文件堆叠，而是一个可被 AI 工具快速定位、读取和执行的系统。

```text
Knowledge Nodes
+
Production Database
+
AI Agents
+
Workflow Templates
+
Operating Commands
+
Runtime Docs
+
Examples
+
Navigation Index
=
Navigable AI Native Studio OS
```

---

## Navigation Files Added（新增导航文件）

| File | Path | Status |
|---|---|---|
| Studio OS Index | docs/studio-os/INDEX.md | Active |
| Commands Index | commands/README.md | Active |
| Workflows Index | workflows/README.md | Active |
| Agents Index | agents/README.md | Active |
| Examples Index | examples/README.md | Active |
| Database Index | database/README.md | Active |

---

## Updated Core Files（已更新核心文件）

| File | Purpose | Status |
|---|---|---|
| README.md | Updated final repository structure and runtime entry points | Updated |
| ARCHITECTURE.md | Updated Phase 4–8 system architecture | Updated |
| CHANGELOG.md | Added Phase 8 checkpoint | Updated |

---

## Navigation Layer Purpose（导航层职责）

### docs/studio-os/INDEX.md

作为 Studio OS 的主导航索引。

它帮助 AI 工具快速定位：

- Knowledge Layer
- Production Database
- Agents
- Workflows
- Commands
- Runtime Docs
- Examples

---

### commands/README.md

作为 `commands/` 目录索引。

它帮助 AI 工具理解：

- 当前有哪些 Operating Commands
- 每个 Command 何时使用
- 每个 Command 调用哪些 Workflow / Agent
- 每个 Command 的标准输出

---

### workflows/README.md

作为 `workflows/` 目录索引。

它帮助 AI 工具理解：

- 当前有哪些 Workflow Templates
- 每个 Workflow 的使用场景
- Workflow 和 Command 的映射关系
- Workflow 和 Agent 的映射关系

---

### agents/README.md

作为 `agents/` 目录索引。

它帮助 AI 工具理解：

- 当前有哪些 AI Agents
- 每个 Agent 的职责
- 每个 Agent 的目录位置
- Agent 与 Command / Workflow 的关系

---

### examples/README.md

作为 `examples/` 目录索引。

它帮助 AI 工具理解：

- 当前有哪些示例输出
- 示例对应哪个 Command
- 示例应该何时参考
- Examples 只是格式参考，不是 Source of Truth

---

### database/README.md

作为 `database/` 目录索引。

它帮助 AI 工具理解：

- 当前 10 个 Production Database Records
- 每个 Record 的文件路径
- 每个 Record 对应的 Notion DB
- Database 与 Knowledge / Commands / Workflows 的映射关系

---

## Architecture Updated（架构已更新）

`ARCHITECTURE.md` 已新增 Phase 4–8 架构说明。

当前 TSOS 系统结构为：

```text
knowledge/
↓
database/
↓
agents/
↓
workflows/
↓
commands/
↓
docs/studio-os/
↓
examples/
```

Phase 4–8 已完成层级：

| Phase | Layer | Status |
|---|---|---|
| Phase 4 | AI Agents | Completed |
| Phase 5 | Workflow Templates | Completed |
| Phase 6 | Operating Commands | Completed |
| Phase 7 | Runtime Docs and Examples | Completed |
| Phase 8 | Index and Navigation Layer | Completed |

---

## README Updated（README 已更新）

`README.md` 已更新最终仓库结构。

新增内容包括：

- Repository Structure
- System Layer Overview
- Quick Start
- Current Default Project
- Navigation Entry Points
- Source of Truth
- Runtime Safety

---

## Current Navigation Entry Points（当前导航入口）

| Need | File |
|---|---|
| Understand full system | docs/studio-os/INDEX.md |
| Understand runtime behavior | docs/studio-os/RUNTIME.md |
| Guide Codex usage | docs/studio-os/CODEX.md |
| Find command usage | commands/README.md |
| Find workflow usage | workflows/README.md |
| Find agent usage | agents/README.md |
| Find database records | database/README.md |
| Find example outputs | examples/README.md |

---

## Recommended Reading Order（推荐读取顺序）

AI 工具进入仓库后，推荐读取顺序为：

```text
1. README.md
2. ARCHITECTURE.md
3. CHANGELOG.md
4. docs/studio-os/INDEX.md
5. docs/studio-os/RUNTIME.md
6. docs/studio-os/CODEX.md
7. docs/studio-os/COMMANDS.md
8. docs/studio-os/WORKFLOWS.md
9. docs/studio-os/AGENTS.md
10. knowledge/README.md
11. database/README.md
12. commands/README.md
13. workflows/README.md
14. agents/README.md
15. examples/README.md
```

---

## Source of Truth Confirmed（事实来源确认）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

GitHub 负责：

```text
Knowledge Nodes
Database Records
Agents
Workflows
Commands
Runtime Docs
Examples
Architecture
Changelog
Navigation Indexes
```

Notion 负责：

```text
Visual management
Database browsing
Production record visibility
```

---

## Default Production Stack Confirmed（默认生产栈确认）

当前默认项目：

```text
PROJ-001 — Jump After Work Pilot Project
```

默认生产链路：

```text
CHAR-001
+
EP-001
+
STORY-001
+
ENV-001
+
MOT-001
+
CAM-001
+
LGT-001
+
PROMPT-001
+
ASSET-001
=
PROJ-001
```

默认执行链路：

```text
PROJ-001
↓
COMMAND-001
↓
WORKFLOW-001
↓
AGENT-001
↓
AGENT-002
↓
AGENT-003
↓
AGENT-004
↓
AGENT-005
↓
AGENT-006
↓
COMMAND-005
```

---

## Runtime Safety Confirmed（运行安全确认）

任何 AI 工具运行 TSOS 时不得：

```text
change Jump's core identity
change TiaoTiao Universe worldbuilding
change Brand Language
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
invent unapproved canon
treat Notion as the source of truth
```

正式输出前，建议运行：

```text
COMMAND-005 — Run Consistency Check
```

---

## Current Architecture Status（当前架构状态）

```text
TSOS Architecture Status:
Readable
Navigable
Callable
Executable
Extensible
```

---

## Next Phase（下一阶段）

建议下一阶段：

```text
Phase 9 — Validation and Test Runs
```

Phase 9 目标：

开始真正运行 TSOS，验证 Commands、Workflows、Agents、Database Records 和 Knowledge Nodes 是否能组合成稳定输出。

优先级：

1. Run COMMAND-003 — Generate Storyboard
2. Run COMMAND-002 — Generate Short Video Prompt
3. Run COMMAND-005 — Consistency Check
4. Run COMMAND-004 — Generate Publishing Package
5. Run COMMAND-001 — Full Production Package
6. Record validation findings
7. Fix issues if needed

---

## Change Type（变更类型）

- Added Studio OS navigation index
- Added commands index
- Added workflows index
- Added agents index
- Added examples index
- Added database index
- Updated architecture for Phase 4–8
- Updated README final repository structure
- Confirmed navigation entry points
- Confirmed runtime reading order
- Completed first navigation layer

---

## Status

```text
Phase 8 Index and Navigation Layer: Completed
Ready for Phase 9 Validation and Test Runs
```


# Phase 7 — Runtime Docs and Examples Completed

> Date：2026  
> Status：Completed  
> Scope：Runtime Documentation / Examples

---

## Summary（总结）

Phase 7 完成了 TiaoTiao Studio OS 的 Runtime Docs 和 Examples 层。

本阶段目标是让 TSOS 不只是拥有 Knowledge、Database、Agents、Workflows 和 Commands，而是进一步具备可被 ChatGPT、Codex、Cursor、Claude 等 AI 工具读取、理解和执行的运行说明。

现在 TSOS 已经从“结构完整”进入“可运行、可调用、可参考示例”的阶段。

```text
Knowledge Nodes
+
Database Records
+
AI Agents
+
Workflow Templates
+
Operating Commands
+
Runtime Docs
+
Examples
=
Readable and Executable AI Native Studio OS
```

---

## Runtime Docs Added（新增运行文档）

| Document | Path | Status |
|---|---|---|
| RUNTIME | docs/studio-os/RUNTIME.md | Active |
| CODEX | docs/studio-os/CODEX.md | Active |
| COMMANDS | docs/studio-os/COMMANDS.md | Active |
| WORKFLOWS | docs/studio-os/WORKFLOWS.md | Active |
| AGENTS | docs/studio-os/AGENTS.md | Active |

---

## Runtime Docs Purpose（运行文档职责）

### RUNTIME.md

定义 TSOS 的整体运行方式。

包括：

- Source of Truth
- Runtime reading order
- Core system layers
- Command usage
- Runtime safety rules
- Notion / Git policy
- Standard runtime response format

---

### CODEX.md

定义 Codex 如何读取和操作 TSOS。

包括：

- Codex reading order
- File creation rules
- Modification rules
- Command routing
- Git commit rules
- Push policy
- Notion policy
- Failure handling

---

### COMMANDS.md

定义 Operating Commands 的使用方式。

包括：

- Current command index
- Command routing table
- Command expected outputs
- Multi-command usage
- Command safety rules
- Command failure handling

---

### WORKFLOWS.md

定义 Workflow Templates 的使用方式。

包括：

- Current workflow index
- Workflow routing
- Workflow / Command mapping
- Workflow / Agent mapping
- Standard workflow execution rule
- Workflow safety rules

---

### AGENTS.md

定义 AI Agents 的使用方式。

包括：

- Current agent index
- Agent responsibilities
- Agent / Command mapping
- Agent / Workflow mapping
- Agent source of truth rule
- Agent safety rules
- Agent collaboration chain

---

## Examples Added（新增示例）

| Example | Path | Status |
|---|---|---|
| COMMAND-001 Output Example | examples/COMMAND-001-output.md | Active |
| COMMAND-002 Prompt Example | examples/COMMAND-002-prompt.md | Active |
| COMMAND-003 Storyboard Example | examples/COMMAND-003-storyboard.md | Active |

---

## Examples Purpose（示例职责）

### COMMAND-001-output.md

展示运行完整生产流程后，最终 Production Package 应该长什么样。

覆盖：

- Project Brief
- Storyboard Output
- Prompt Output
- Cinematography Output
- Script Output
- Editing Output
- Publishing Output
- Final Consistency Checklist
- Next Production Actions

---

### COMMAND-002-prompt.md

展示短视频 Prompt Package 的标准输出格式。

覆盖：

- Prompt Purpose
- Target Model
- Source Records
- Base Prompt
- Kling / Veo / Runway Prompt
- Negative Prompt
- Chinese Production Notes
- Consistency Checklist
- Usage Notes

---

### COMMAND-003-storyboard.md

展示 45 秒竖屏分镜的标准输出格式。

覆盖：

- Storyboard Summary
- Story Beat Breakdown
- Shot List
- Shot Details
- Camera / Motion / Lighting Mapping
- Prompt Notes
- Continuity Checklist
- Next Production Actions

---

## README Updated（README 已更新）

README.md 已新增 Runtime Entry Points 说明。

新增内容包括：

- Runtime Entry Points
- Source of Truth
- Runtime Docs
- Operating Commands
- Runtime Layer Structure
- Default Runtime Project
- Examples
- Runtime Safety Rule

---

## Runtime Layer Completed（运行层完成）

Phase 7 后，TSOS 当前运行层结构为：

```text
knowledge/
↓
database/
↓
agents/
↓
workflows/
↓
commands/
↓
docs/studio-os/
↓
examples/
```

---

## Runtime Reading Order Confirmed（运行读取顺序确认）

AI 工具进入 TSOS 后，推荐读取顺序为：

```text
1. README.md
2. ARCHITECTURE.md
3. CHANGELOG.md
4. docs/studio-os/RUNTIME.md
5. docs/studio-os/CODEX.md
6. docs/studio-os/COMMANDS.md
7. docs/studio-os/WORKFLOWS.md
8. docs/studio-os/AGENTS.md
9. knowledge/README.md
10. knowledge/
11. database/
12. agents/
13. workflows/
14. commands/
15. examples/
```

---

## Runtime Source of Truth Confirmed（运行事实来源确认）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Production Database Records：

```text
GitHub + Notion
```

Operating layers：

```text
Agents
Workflows
Commands
Runtime Docs
Examples
```

统一策略：

```text
GitHub only
```

---

## Default Runtime Commands（默认运行命令）

当前 TSOS 可以通过以下命令直接调用：

```text
COMMAND-001 — Run Jump After Work Production
COMMAND-002 — Generate Short Video Prompt
COMMAND-003 — Generate Storyboard
COMMAND-004 — Generate Publishing Package
COMMAND-005 — Run Consistency Check
```

---

## Runtime Safety Rules Confirmed（运行安全规则确认）

任何 AI 工具运行 TSOS 时不得：

```text
change Jump's core identity
change TiaoTiao Universe worldbuilding
change Brand Language
skip ASSET-001
skip Knowledge Nodes
skip Database Records
skip consistency checks
invent unapproved canon
treat Notion as the source of truth
```

---

## Standard Runtime Logic（标准运行逻辑）

TSOS 当前标准运行逻辑为：

```text
User Request
↓
Command Routing
↓
Workflow Execution
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

## Phase 7 File Structure（Phase 7 文件结构）

```text
docs/
└── studio-os/
    ├── RUNTIME.md
    ├── CODEX.md
    ├── COMMANDS.md
    ├── WORKFLOWS.md
    └── AGENTS.md

examples/
├── COMMAND-001-output.md
├── COMMAND-002-prompt.md
└── COMMAND-003-storyboard.md
```

---

## Next Phase（下一阶段）

建议下一阶段：

```text
Phase 8 — Index and Navigation Layer
```

Phase 8 目标：

建立完整索引层，让 Codex / ChatGPT / Cursor 可以更快定位文件和调用系统。

优先级：

1. Update root README.md final structure
2. Update ARCHITECTURE.md with Phase 4–7 layers
3. Add docs/studio-os/INDEX.md
4. Add commands/README.md
5. Add workflows/README.md
6. Add agents/README.md
7. Add examples/README.md
8. Add database/README.md if needed

---

## Change Type（变更类型）

- Added runtime documentation
- Added Codex operating guide
- Added commands guide
- Added workflows guide
- Added agents guide
- Added command output examples
- Updated README runtime entry points
- Confirmed runtime reading order
- Confirmed GitHub as runtime source of truth
- Completed first executable runtime documentation layer

---

## Status

```text
Phase 7 Runtime Docs and Examples: Completed
Ready for Phase 8 Index and Navigation Layer
```


# Phase 6 — Operating Commands Completed

> Date：2026  
> Status：Completed  
> Scope：Operating Commands

---

## Summary（总结）

Phase 6 完成了 TiaoTiao Studio OS 第一批核心 Operating Commands。

本阶段目标是让 TSOS 不只是拥有 Knowledge、Database、Agents 和 Workflows，而是进一步形成可以直接调用的标准操作命令。

现在用户可以通过固定命令快速启动：

- 完整生产流程
- 短视频 Prompt 生成
- 分镜生成
- 发布包生成
- 一致性检查

这意味着 TSOS 已经具备从“系统结构”进入“可调用操作系统”的能力。

```text
Knowledge Nodes
+
Database Records
+
AI Agents
+
Workflow Templates
+
Operating Commands
=
Callable AI Native Studio OS
```

---

## Completed Commands（已完成命令）

| Command | Name | Path | Status |
|---|---|---|---|
| COMMAND-001 | Run Jump After Work Production | commands/COMMAND-001.md | Active |
| COMMAND-002 | Generate Short Video Prompt | commands/COMMAND-002.md | Active |
| COMMAND-003 | Generate Storyboard | commands/COMMAND-003.md | Active |
| COMMAND-004 | Generate Publishing Package | commands/COMMAND-004.md | Active |
| COMMAND-005 | Run Consistency Check | commands/COMMAND-005.md | Active |

---

## Command Responsibilities（命令职责）

### COMMAND-001 — Run Jump After Work Production

用于启动《跳跳下班啦》的完整生产流程。

覆盖：

- Project Brief
- Storyboard Output
- Prompt Output
- Cinematography Output
- Script Output
- Editing Output
- Publishing Output
- Final Consistency Checklist

---

### COMMAND-002 — Generate Short Video Prompt

用于生成可直接复制执行的短视频图片 / 视频 / 封面 / 分镜 Prompt。

覆盖：

- Prompt Purpose
- Target Model
- Source Records
- Base Prompt
- Model-Specific Prompt
- Negative Prompt
- Consistency Checklist
- Usage Notes

---

### COMMAND-003 — Generate Storyboard

用于生成可生产的短视频分镜。

覆盖：

- Storyboard Summary
- Story Beat Breakdown
- Shot List
- Shot Details
- Camera / Motion / Lighting Mapping
- Prompt Notes
- Continuity Checklist
- Next Production Actions

---

### COMMAND-004 — Generate Publishing Package

用于生成平台发布包。

覆盖：

- Publishing Summary
- Platform Strategy
- Title Options
- Caption / Description
- Hashtag Set
- Cover Text Suggestions
- Publishing Time Suggestion
- Pre-Publish Checklist
- Publishing Record
- Post-Publish Review Template
- Brand Safety Check

---

### COMMAND-005 — Run Consistency Check

用于检查任意输出是否符合 TSOS Source of Truth。

覆盖：

- Character Consistency
- World Consistency
- Visual Style Check
- Color Check
- Emotion Check
- Motion Check
- Camera Check
- Lighting Check
- Story / Brand Check
- Workflow Compliance Check
- Issue List
- Fix Suggestions
- Final PASS / FAIL Result

---

## Default Command Source Records（默认命令来源记录）

Phase 6 Commands 默认读取以下 Production Database Records：

- CHAR-001 — Jump
- EP-001 — Jump After Work
- STORY-001 — Work Ends, Adventure Begins
- ENV-001 — TiaoTiao Studio Office
- MOT-001 — Natural Walking
- CAM-001 — Hero Tracking Camera
- LGT-001 — Warm Studio Lighting
- PROMPT-001 — Jump After Work Master Prompt
- ASSET-001 — Jump Character Reference Pack
- PROJ-001 — Jump After Work Pilot Project

---

## Default Knowledge Constraints（默认知识约束）

Phase 6 Commands 默认受以下 Knowledge Nodes 约束：

- STYLE-001 — Cinematic Documentary
- COLOR-001 — Fire Dragon Fruit Palette
- WORLD-001 — TiaoTiao Universe
- EMOTION-001 — Freedom
- SHOT-001 — Hero Tracking Shot
- MOTIONLANG-001 — Natural Walking Language
- OUTFIT-001 — Programmer Outfit System
- MUSIC-001 — Lifestyle Music Language
- STORYFORMULA-001 — Work Ends, Adventure Begins
- BRAND-001 — TiaoTiao Studio Brand Language

---

## Default Workflow References（默认工作流引用）

Phase 6 Commands 默认调用以下 Workflow Templates：

```text
COMMAND-001 → WORKFLOW-001
COMMAND-002 → WORKFLOW-002
COMMAND-003 → WORKFLOW-001 / WORKFLOW-003
COMMAND-004 → WORKFLOW-004
COMMAND-005 → WORKFLOW-001 / WORKFLOW-002 / WORKFLOW-003 / WORKFLOW-004
```

---

## Default Agent References（默认智能体引用）

Phase 6 Commands 默认调用以下 AI Agents：

```text
COMMAND-001
→ AGENT-001 + AGENT-002 + AGENT-003 + AGENT-004 + AGENT-005 + AGENT-006

COMMAND-002
→ AGENT-002

COMMAND-003
→ AGENT-001

COMMAND-004
→ AGENT-006

COMMAND-005
→ Checks outputs from all Agents
```

---

## Command File Structure（命令文件结构）

```text
commands/
├── COMMAND-001.md
├── COMMAND-002.md
├── COMMAND-003.md
├── COMMAND-004.md
└── COMMAND-005.md
```

---

## Command Naming Rule Confirmed（命令命名规则确认）

Command 文件统一使用以下规则：

```text
Command ID = COMMAND-XXX
File Name = COMMAND-XXX.md
Directory = commands/
Page H1 = COMMAND-XXX + Human-readable Name
```

Example：

```text
Command ID:
COMMAND-001

GitHub File:
commands/COMMAND-001.md

Page H1:
# COMMAND-001 — Run Jump After Work Production（运行跳跳下班啦完整生产流程）
```

---

## Notion Status（Notion 状态）

Phase 6 暂不新增 Notion Command DB。

原因：

```text
Commands are operating instructions, not production database records.
GitHub is the source of truth for command behavior.
```

当前策略：

```text
Operating Commands → GitHub only
Production Records → GitHub + Notion
```

以后如果需要可视化 Command 面板，可以在后续 Phase 中单独新增 Command DB。

---

## Operating System Layer Completed（操作系统层完成）

现在 TSOS 已经形成第一套完整 AI Native Studio 操作系统层：

```text
Knowledge Layer
↓
Production Database
↓
Asset Reference
↓
Prompt System
↓
Project Assembly
↓
AI Agents
↓
Workflow Templates
↓
Operating Commands
↓
Repeatable Studio Production
```

---

## Standard User Command Examples（标准用户调用示例）

```text
Run COMMAND-001.
```

```text
运行 COMMAND-002，生成小红书 9:16 Kling 视频 Prompt。
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

## Next Phase（下一阶段）

建议下一阶段：

```text
Phase 7 — Templates / Examples / Runtime Docs
```

Phase 7 目标：

建立可直接给 Codex、ChatGPT、Cursor 或其他 AI 工具读取的运行说明与示例。

优先级：

1. README update — explain commands / workflows / agents usage
2. docs/RUNTIME.md — how to operate TSOS
3. docs/CODEX.md — how Codex should read and use TSOS
4. examples/COMMAND-001-output.md — sample production output
5. examples/COMMAND-002-prompt.md — sample prompt output
6. examples/COMMAND-003-storyboard.md — sample storyboard output

---

## Change Type（变更类型）

- Added operating commands
- Added full production command
- Added short video prompt command
- Added storyboard command
- Added publishing package command
- Added consistency check command
- Confirmed Command naming rule
- Confirmed GitHub as Command source of truth
- Completed first callable operating layer

---

## Status

```text
Phase 6 Operating Commands: Completed
Ready for Phase 7 Runtime Docs and Examples
```

# Phase 5 — Workflow Templates Completed

> Date：2026  
> Status：Completed  
> Scope：Workflow Templates

---

## Summary（总结）

Phase 5 完成了 TiaoTiao Studio OS 第一批核心 Workflow Templates。

本阶段目标是让 TSOS 不只是拥有 Knowledge、Database 和 Agents，而是进一步形成可直接执行的标准化生产流程。

现在 TSOS 已经具备从项目启动到提示词生成、视频生成、剪辑发布的完整工作流模板。

```text
Knowledge Nodes
+
Database Records
+
AI Agents
+
Workflow Templates
=
Executable AI Native Studio Operating System
```

---

## Completed Workflows（已完成工作流）

| Workflow | Name | Path | Status |
|---|---|---|---|
| WORKFLOW-001 | Jump After Work Production Workflow | workflows/WORKFLOW-001.md | Active |
| WORKFLOW-002 | Short Video Prompt Workflow | workflows/WORKFLOW-002.md | Active |
| WORKFLOW-003 | Storyboard to Video Workflow | workflows/WORKFLOW-003.md | Active |
| WORKFLOW-004 | Publishing Workflow | workflows/WORKFLOW-004.md | Active |

---

## Workflow Responsibilities（工作流职责）

### WORKFLOW-001 — Jump After Work Production Workflow

用于把《跳跳下班啦》的完整生产流程串联起来。

覆盖：

- Project Setup
- Storyboard Planning
- Prompt Generation
- Cinematography Planning
- Script Writing
- Editing Planning
- Publishing Planning
- Final Consistency Check

---

### WORKFLOW-002 — Short Video Prompt Workflow

用于把 TSOS 数据库记录和知识节点转化为可执行的 AI 图片 / 视频 Prompt。

覆盖：

- Prompt task setup
- Source record collection
- Shot context extraction
- Prompt variable mapping
- Base prompt generation
- Model adaptation
- Negative prompt generation
- Consistency check

---

### WORKFLOW-003 — Storyboard to Video Workflow

用于把已完成分镜转化为可生成的视频镜头包。

覆盖：

- Storyboard input review
- Shot segmentation
- Video prompt generation
- Cinematography enhancement
- Motion continuity setup
- Lighting and style lock
- Video clip generation package
- Clip review
- Assembly notes

---

### WORKFLOW-004 — Publishing Workflow

用于把完成的视频内容转化为不同平台的发布包。

覆盖：

- Publish asset review
- Platform selection
- Title generation
- Caption / description generation
- Hashtag generation
- Cover text planning
- Publishing time planning
- Pre-publish checklist
- Post-publish review

---

## Default Workflow Source Records（默认工作流来源记录）

Phase 5 Workflows 默认读取以下 Production Database Records：

- CHAR-001 — Jump
- EP-001 — Jump After Work
- STORY-001 — Work Ends, Adventure Begins
- ENV-001 — TiaoTiao Studio Office
- MOT-001 — Natural Walking
- CAM-001 — Hero Tracking Camera
- LGT-001 — Warm Studio Lighting
- PROMPT-001 — Jump After Work Master Prompt
- ASSET-001 — Jump Character Reference Pack
- PROJ-001 — Jump After Work Pilot Project

---

## Default Knowledge Constraints（默认知识约束）

Phase 5 Workflows 默认受以下 Knowledge Nodes 约束：

- STYLE-001 — Cinematic Documentary
- COLOR-001 — Fire Dragon Fruit Palette
- WORLD-001 — TiaoTiao Universe
- EMOTION-001 — Freedom
- SHOT-001 — Hero Tracking Shot
- MOTIONLANG-001 — Natural Walking Language
- OUTFIT-001 — Programmer Outfit System
- MUSIC-001 — Lifestyle Music Language
- STORYFORMULA-001 — Work Ends, Adventure Begins
- BRAND-001 — TiaoTiao Studio Brand Language

---

## Default Agent Chain（默认智能体链路）

Phase 5 Workflows 默认调用以下 AI Agents：

```text
AGENT-001 — Storyboard Agent
↓
AGENT-002 — Prompt Agent
↓
AGENT-003 — Cinematography Agent
↓
AGENT-004 — Script Agent
↓
AGENT-005 — Editing Agent
↓
AGENT-006 — Publishing Agent
```

---

## Workflow File Structure（工作流文件结构）

```text
workflows/
├── WORKFLOW-001.md
├── WORKFLOW-002.md
├── WORKFLOW-003.md
└── WORKFLOW-004.md
```

---

## Workflow Naming Rule Confirmed（工作流命名规则确认）

Workflow 文件统一使用以下规则：

```text
Workflow ID = WORKFLOW-XXX
File Name = WORKFLOW-XXX.md
Directory = workflows/
Page H1 = WORKFLOW-XXX + Human-readable Name
```

Example：

```text
Workflow ID:
WORKFLOW-001

GitHub File:
workflows/WORKFLOW-001.md

Page H1:
# WORKFLOW-001 — Jump After Work Production Workflow（跳跳下班啦生产工作流）
```

---

## Notion Status（Notion 状态）

Phase 5 暂不新增 Notion Workflow DB。

原因：

```text
Workflows are execution templates, not production database records.
GitHub is the source of truth for workflow behavior.
```

当前策略：

```text
Workflow Templates → GitHub only
Production Records → GitHub + Notion
```

以后如果需要可视化 Workflow 面板，可以在后续 Phase 中单独新增 Workflow DB。

---

## Production System Completed（生产系统能力完成）

现在 TSOS 已经形成第一套完整 AI Native Studio 生产系统：

```text
Knowledge Layer
↓
Production Database
↓
Asset Reference
↓
Prompt System
↓
Project Assembly
↓
AI Agents
↓
Workflow Templates
↓
Repeatable Content Production
```

---

## Next Phase（下一阶段）

建议下一阶段：

```text
Phase 6 — Operating Commands
```

Phase 6 目标：

建立可直接调用的标准命令，让之后你可以用一句话启动完整流程。

优先级：

1. COMMAND-001 — Run Jump After Work Production
2. COMMAND-002 — Generate Short Video Prompt
3. COMMAND-003 — Generate Storyboard
4. COMMAND-004 — Generate Publishing Package
5. COMMAND-005 — Run Consistency Check

---

## Change Type（变更类型）

- Added workflow templates
- Added standard production workflow
- Added short video prompt workflow
- Added storyboard to video workflow
- Added publishing workflow
- Confirmed Workflow naming rule
- Confirmed GitHub as Workflow source of truth
- Completed first executable workflow layer

---

## Status

```text
Phase 5 Workflow Templates: Completed
Ready for Phase 6 Operating Commands
```


# Phase 4 — AI Agents Completed

> Date：2026  
> Status：Completed  
> Scope：AI Agent Definitions

---

## Summary（总结）

Phase 4 完成了 TiaoTiao Studio OS 第一批基础 AI Agents 的定义。

本阶段目标是让 TSOS 不只是保存角色、故事、镜头、灯光、提示词和项目记录，而是进一步具备可复用的 AI 创作工作流能力。

现在 TSOS 已经具备以下完整工作链路：

```text
Database Records
+
Knowledge Nodes
+
AI Agents
=
Repeatable Production Workflow
```

---

## Completed Agents（已完成智能体）

| Agent | Role Group | Path | Status |
|---|---|---|---|
| AGENT-001 — Storyboard Agent | Director | agents/director/AGENT-001.md | Active |
| AGENT-002 — Prompt Agent | Prompt Engineer | agents/prompt-engineer/AGENT-002.md | Active |
| AGENT-003 — Cinematography Agent | Cinematographer | agents/cinematographer/AGENT-003.md | Active |
| AGENT-004 — Script Agent | Writer | agents/writer/AGENT-004.md | Active |
| AGENT-005 — Editing Agent | Editor | agents/editor/AGENT-005.md | Active |
| AGENT-006 — Publishing Agent | Publisher | agents/publisher/AGENT-006.md | Active |

---

## Agent Chain（智能体工作链路）

Phase 4 建立了以下标准创作链路：

```text
AGENT-001 Storyboard Agent
↓
AGENT-002 Prompt Agent
↓
AGENT-003 Cinematography Agent
↓
AGENT-004 Script Agent
↓
AGENT-005 Editing Agent
↓
AGENT-006 Publishing Agent
```

---

## Default Production Source（默认生产来源）

所有 Agents 默认读取以下 Database Records：

- CHAR-001 — Jump
- EP-001 — Jump After Work
- STORY-001 — Work Ends, Adventure Begins
- ENV-001 — TiaoTiao Studio Office
- MOT-001 — Natural Walking
- CAM-001 — Hero Tracking Camera
- LGT-001 — Warm Studio Lighting
- PROMPT-001 — Jump After Work Master Prompt
- ASSET-001 — Jump Character Reference Pack
- PROJ-001 — Jump After Work Pilot Project

---

## Default Knowledge References（默认知识引用）

所有 Agents 默认受以下 Knowledge Nodes 约束：

- STYLE-001 — Cinematic Documentary
- COLOR-001 — Fire Dragon Fruit Palette
- WORLD-001 — TiaoTiao Universe
- EMOTION-001 — Freedom
- SHOT-001 — Hero Tracking Shot
- MOTIONLANG-001 — Natural Walking Language
- OUTFIT-001 — Programmer Outfit System
- MUSIC-001 — Lifestyle Music Language
- STORYFORMULA-001 — Work Ends, Adventure Begins
- BRAND-001 — TiaoTiao Studio Brand Language

---

## Agent Responsibilities（智能体职责）

### AGENT-001 — Storyboard Agent

负责将 Project、Story、Character、Environment、Camera、Motion、Lighting 和 Asset 记录转化为可生产的分镜方案。

---

### AGENT-002 — Prompt Agent

负责将 TSOS Database Records、Knowledge Nodes 和其他 Agent 输出转化为可执行的 AI 图片、视频、分镜、封面和角色一致性 Prompt。

---

### AGENT-003 — Cinematography Agent

负责生成镜头、构图、机位、焦段、景深、运镜和灯光关系方案，保证视觉语言符合 TSOS 电影感规范。

---

### AGENT-004 — Script Agent

负责生成短视频脚本、旁白、字幕、对白、开场 Hook 和结尾金句，保证文案符合 TiaoTiao Studio 的温暖品牌语气。

---

### AGENT-005 — Editing Agent

负责生成剪辑时间线、镜头时长、转场、字幕节奏、旁白节奏、音乐进入退出和成片节奏方案。

---

### AGENT-006 — Publishing Agent

负责生成平台发布方案，包括标题、简介、标签、封面文案、发布时间建议、发布前检查清单和发布后复盘指标。

---

## Naming Rule Confirmed（命名规则确认）

Agent 文件统一使用以下规则：

```text
Agent ID = AGENT-XXX
File Name = AGENT-XXX.md
Directory = agents/{role-group}/
Page H1 = AGENT-XXX + Human-readable Name
```

Example：

```text
Agent ID:
AGENT-001

GitHub File:
agents/director/AGENT-001.md

Page H1:
# AGENT-001 — Storyboard Agent（分镜智能体）
```

---

## Notion Status（Notion 状态）

Phase 4 暂不新增 Notion Agent DB。

原因：

```text
Agents are workflow definitions, not production database records.
GitHub is the source of truth for agent behavior.
```

当前策略：

```text
Agent Definitions → GitHub only
Production Records → GitHub + Notion
```

以后如果需要 Agent 管理面板，可以在后续 Phase 中单独新增 Agent DB。

---

## Phase 4 Completed Files（Phase 4 完成文件）

```text
agents/
├── director/
│   └── AGENT-001.md
├── prompt-engineer/
│   └── AGENT-002.md
├── cinematographer/
│   └── AGENT-003.md
├── writer/
│   └── AGENT-004.md
├── editor/
│   └── AGENT-005.md
└── publisher/
    └── AGENT-006.md
```

---

## Production Workflow Completed（生产工作流完成）

现在 TSOS 已经形成第一条完整 AI Native Studio 生产链：

```text
Knowledge Layer
↓
Database Records
↓
Prompt / Project Assembly
↓
AI Agents
↓
Storyboard
↓
Prompt
↓
Cinematography
↓
Script
↓
Editing
↓
Publishing
```

---

## Next Phase（下一阶段）

Phase 5 将在 Phase 4 完成后开始。

建议下一阶段：

```text
Phase 5 — Workflow Templates
```

Phase 5 目标：

建立可直接执行的工作流模板，让 Agents 能够按照固定输入输出格式协作。

优先级：

1. WORKFLOW-001 — Jump After Work Production Workflow
2. WORKFLOW-002 — Short Video Prompt Workflow
3. WORKFLOW-003 — Storyboard to Video Workflow
4. WORKFLOW-004 — Publishing Workflow

---

## Change Type（变更类型）

- Added AI Agent definitions
- Added role-based agent directory structure
- Confirmed Agent naming rule
- Confirmed GitHub as Agent source of truth
- Completed first AI production agent chain

---

## Status

```text
Phase 4 AI Agents: Completed
Ready for Phase 5 Workflow Templates
```

# Phase 3 Checkpoint — Database Population Review

> Date：2026  
> Status：Completed  
> Scope：Database Population / Knowledge Reference Update

---

## Summary（总结）

Phase 3 完成了 TiaoTiao Studio OS 第一批核心 Production Database Records 的建立与更新。

本阶段目标不是继续扩展 Knowledge Layer，而是让 Database Records 正式引用已经完成的 Master Knowledge Nodes，从而实现：

```text
Knowledge Layer
↓
Production Database
↓
Project Assembly
```

现在 TSOS 已经具备从知识规范到生产项目的第一条完整链路。

---

## Completed Database Records（已完成数据库记录）

| Database | Record | Status |
|---|---|---|
| Character DB | CHAR-001 — Jump | Completed |
| Episode DB | EP-001 — Jump After Work | Completed |
| Story DB | STORY-001 — Work Ends, Adventure Begins | Completed |
| Environment DB | ENV-001 — TiaoTiao Studio Office | Completed |
| Motion DB | MOT-001 — Natural Walking | Completed |
| Camera DB | CAM-001 — Hero Tracking Camera | Completed |
| Lighting DB | LGT-001 — Warm Studio Lighting | Completed |
| Prompt DB | PROMPT-001 — Jump After Work Master Prompt | Completed |
| Asset DB | ASSET-001 — Jump Character Reference Pack | Completed |
| Project DB | PROJ-001 — Jump After Work Pilot Project | Completed |

---

## Knowledge References Applied（已应用知识引用）

The completed database records now reference the following Master Knowledge Nodes:

- STYLE-001 — Cinematic Documentary
- COLOR-001 — Fire Dragon Fruit Palette
- WORLD-001 — TiaoTiao Universe
- EMOTION-001 — Freedom
- SHOT-001 — Hero Tracking Shot
- MOTIONLANG-001 — Natural Walking Language
- OUTFIT-001 — Programmer Outfit System
- MUSIC-001 — Lifestyle Music Language
- STORYFORMULA-001 — Work Ends, Adventure Begins
- BRAND-001 — TiaoTiao Studio Brand Language

---

## Notion Sync Status（Notion 同步状态）

| Notion DB | Record | Status |
|---|---|---|
| Character DB | CHAR-001 | Synced |
| Episode DB | EP-001 | Synced |
| Story DB | STORY-001 | Synced |
| Environment DB | ENV-001 | Synced |
| Motion DB | MOT-001 | Synced |
| Camera DB | CAM-001 | Synced |
| Lighting DB | LGT-001 | Synced |
| Prompt DB | PROMPT-001 | Synced |
| Asset DB | ASSET-001 | Synced |
| Project DB | PROJ-001 | Synced |

---

## Naming Rule Confirmed（命名规则确认）

Notion database title fields now follow the frozen rule:

```text
Notion Title = Record ID only
GitHub Filename = Record ID.md
Page H1 = Record ID + Human-readable Name
Database Properties = Human-readable description
```

Example:

```text
Notion Title:
PROJ-001

GitHub File:
database/projects/PROJ-001.md

Page H1:
# PROJ-001 — Jump After Work Pilot Project（跳跳下班啦试播项目）
```

---

## Production Chain Completed（生产链路完成）

The first full TSOS production chain is now complete:

```text
CHAR-001
+
EP-001
+
STORY-001
+
ENV-001
+
MOT-001
+
CAM-001
+
LGT-001
+
PROMPT-001
+
ASSET-001
=
PROJ-001
```

This means TiaoTiao Studio OS can now assemble a real short-video project using stable database records instead of rewriting character, style, story, camera or lighting rules every time.

---

## Next Phase（下一阶段）

Phase 4 will begin after this checkpoint.

Next planned phase:

```text
Phase 4 — AI Agents
```

Phase 4 goal:

Build reusable AI Agent definitions that can read TSOS database records and help generate:

- scripts
- storyboards
- image prompts
- video prompts
- cover concepts
- project plans
- production checklists

---

## Change Type（变更类型）

- Added database records
- Updated database-to-knowledge references
- Synced Notion database records
- Confirmed naming convention
- Completed first production chain

---

## Status

```text
Phase 3 Database Population: Completed
Ready for Phase 4 AI Agents
```

## TSOS v1.0

### Sprint 1

- Database Schema completed

### Sprint 2

- Repository Structure completed

### Sprint 3

- Repository Foundation completed

---

## Change Rules

All structural changes require a new version.

Never modify Architecture during a Sprint.

New ideas go to Backlog.
