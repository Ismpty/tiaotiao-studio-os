# Examples — Command Output Examples Index（命令输出示例索引）

> Navigation Index（导航索引）  
> Version：1.0  
> Status：Active

---

# Purpose（目的）

## 中文

本文件是 `examples/` 目录的索引文件。

它用于帮助 ChatGPT、Codex、Cursor、Claude 或其他 AI 工具快速理解：

- 当前有哪些 Command 输出示例
- 每个示例对应哪个 Command
- 每个示例展示什么标准格式
- 什么时候应该参考这些示例
- 示例和正式 Source of Truth 的区别
- 如何根据示例输出更稳定的生产内容

## English

This file is the index for the `examples/` directory.

It helps AI tools understand available command output examples, their related commands, expected formats and usage boundaries.

---

# Example Layer Role（示例层作用）

Examples 是 TSOS 的输出参考层。

```text
Command
↓
Workflow
↓
Agent
↓
Output
↓
Example Reference
```

Examples 不定义规则。  
Examples 只展示标准输出应该长什么样。

正式规则仍然来自：

```text
Knowledge Nodes
Database Records
Commands
Workflows
Agents
Runtime Docs
```

---

# Current Examples（当前示例）

```text
COMMAND-001-output.md
COMMAND-002-prompt.md
COMMAND-003-storyboard.md
```

---

# Example Index（示例索引）

| Example | Related Command | Primary Use |
|---|---|---|
| COMMAND-001-output.md | COMMAND-001 | 完整生产包示例 |
| COMMAND-002-prompt.md | COMMAND-002 | 短视频 Prompt 示例 |
| COMMAND-003-storyboard.md | COMMAND-003 | 分镜输出示例 |

---

# COMMAND-001-output.md

## File

```text
examples/COMMAND-001-output.md
```

## Related Command

```text
COMMAND-001 — Run Jump After Work Production
```

## Purpose

该示例展示运行完整生产流程后，最终 Production Package 应该如何组织。

## Covers

```text
Project Brief
Storyboard Output
Prompt Output
Cinematography Output
Script Output
Editing Output
Publishing Output
Final Consistency Checklist
Next Production Actions
```

## Use When

当需要参考完整项目输出格式时使用。

例如：

```text
运行 COMMAND-001。
```

```text
做一条完整的《跳跳下班啦》视频生产包。
```

```text
从分镜、Prompt、脚本、剪辑到发布全部生成。
```

---

# COMMAND-002-prompt.md

## File

```text
examples/COMMAND-002-prompt.md
```

## Related Command

```text
COMMAND-002 — Generate Video Prompt Package
```

## Purpose

该示例展示短视频 AI Prompt Package 的标准输出格式。

## Covers

```text
Source References
Prompt Task Brief
Identity Card Prompt
Storyboard Prompt
Universal Video Prompt
Model-readable Check Report
COMMAND-005 Review Result
Usage Notes
```

## Use When

当需要参考 Prompt 输出格式时使用。

例如：

```text
运行 COMMAND-002，生成身份卡 + 故事板 + 通用视频 Prompt。
```

```text
生成小红书 9:16 视频提示词。
```

```text
给分镜生成可逐镜头执行的 Universal Video Prompt。
```

---

# COMMAND-003-storyboard.md

## File

```text
examples/COMMAND-003-storyboard.md
```

## Related Command

```text
COMMAND-003 — Generate Storyboard
```

## Purpose

该示例展示 45 秒竖屏短视频分镜的标准输出格式。

## Covers

```text
Storyboard Summary
Story Beat Breakdown
Shot List
Shot Details
Camera / Motion / Lighting Mapping
Prompt Notes
Continuity Checklist
Next Production Actions
```

## Use When

当需要参考分镜输出格式时使用。

例如：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

```text
把这个故事拆成 6 个镜头。
```

```text
生成可进入 AI 视频制作的 Storyboard。
```

---

# Example Usage Rules（示例使用规则）

使用 Examples 时必须记住：

```text
Examples are output references.
Examples are not source of truth.
Examples should not override Database Records.
Examples should not override Knowledge Nodes.
Examples should not replace Commands, Workflows or Agents.
```

---

# Source of Truth Priority（事实来源优先级）

当 Example 与正式规则冲突时，优先级为：

```text
1. Knowledge Nodes
2. Database Records
3. Commands
4. Workflows
5. Agents
6. Runtime Docs
7. Examples
```

Examples 只用于参考格式，不用于覆盖规则。

---

# When to Read Examples（什么时候读取示例）

AI 工具在以下场景应该读取 Examples：

```text
[ ] 不确定 Command 输出格式
[ ] 需要生成类似结构的正式输出
[ ] 需要参考完整 Production Package
[ ] 需要参考 Prompt Package
[ ] 需要参考 Storyboard Output
[ ] 需要保持输出结构稳定
```

---

# When Not to Use Examples（什么时候不要依赖示例）

以下情况不能只依赖 Examples：

```text
[ ] 判断 Jump 角色设定
[ ] 判断世界观
[ ] 判断品牌语言
[ ] 判断 Knowledge Rules
[ ] 判断 Database Record 内容
[ ] 修改 Source of Truth
[ ] 新增系统文件
```

这些必须读取正式文件：

```text
knowledge/
database/
commands/
workflows/
agents/
docs/studio-os/
```

---

# Example Runtime Flow（示例运行流程）

当用户说：

```text
运行 COMMAND-003，生成 45 秒小红书竖屏分镜。
```

AI 工具应该：

```text
1. Read commands/COMMAND-003.md
2. Read agents/director/AGENT-001.md
3. Read required Database Records
4. Read required Knowledge Nodes
5. Read examples/COMMAND-003-storyboard.md for output format reference
6. Generate new storyboard output
7. Run consistency checklist
```

---

# Example Safety Rules（示例安全规则）

Examples 不得用于：

```text
修改 Jump 核心身份
修改 TiaoTiao Universe 世界观
修改 Brand Language
绕过 ASSET-001
绕过 Knowledge Nodes
绕过 Database Records
改变命名规则
改变目录结构
```

---

# Related Runtime Docs（相关运行文档）

使用 Examples 时应参考：

```text
docs/studio-os/INDEX.md
docs/studio-os/RUNTIME.md
docs/studio-os/COMMANDS.md
docs/studio-os/WORKFLOWS.md
docs/studio-os/AGENTS.md
```

---

# Related Directories（相关目录）

```text
examples/
commands/
workflows/
agents/
database/
knowledge/
docs/studio-os/
```

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial examples index |
