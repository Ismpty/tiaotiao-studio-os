# START HERE — TiaoTiao Studio OS Direct Use Guide

> Runtime Documentation
> Status: Active
> Purpose: shortest path for using TSOS directly

---

# What This System Does

TiaoTiao Studio OS is a production operating system for the Jump / 跳跳 short-video IP.

The current main series is Little Security Guard and His Ancient Friends: Jump works as the little security guard in an AI Museum, and Chinese cultural relics become her ancient friends.

It can also generate identity cards, storyboards and video prompt packages for custom subjects such as humans, animals, plants, products, scene subjects or new IP characters when `Custom Subject Mode` is used.

It helps an AI tool or human operator generate repeatable production outputs:

```text
storyboard
video prompt package
video generation plan
editing plan
publishing package
consistency review
```

The current default project is:

```text
PROJ-001 — Little Security Guard and His Ancient Friends
《小保安和他的古人朋友们》
```

---

# Non-Negotiable Rules

Always follow:

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Jump / 跳跳 must remain:

```text
a real dog-form character wearing clothes
```

Storyboards must remain:

```text
black-and-white rough pencil line art
with colored annotation system
```

Model-facing prompts must be:

```text
natural language descriptions
not raw internal IDs
```

Custom Subject Mode must use:

```text
SUBJECT-001 expanded into natural language
not Jump-only dog-form rules
```

Relic friends must use:

```text
RELIC-001 expanded into natural language
Chinese cultural relic source retained
no horror, cyberpunk, Western fantasy or disrespect toward cultural heritage
```

---

# Fastest Way To Use TSOS

## 1. Generate A Complete Production Package

Use when you want the whole Little Security Guard project package:

```text
Run COMMAND-001.
```

This routes through:

```text
commands/COMMAND-001.md
workflows/WORKFLOW-001.md
agents/
database/projects/PROJ-001.md
```

## 2. Generate The Video Prompt Package

Use when you need prompts for AI video generation:

```text
Run COMMAND-002.
```

Required output structure:

```text
Identity Card Prompt
↓
Storyboard Prompt
↓
Universal Video Prompt
↓
Model-readable check
↓
COMMAND-005 review
```

For non-Jump subjects, specify:

```text
Subject Mode:
Custom Subject Mode

Subject Type:
Human / Animal / Plant / Object / Scene Subject / Mascot / Other
```

## 3. Generate Storyboard

Use when you need the shot plan first:

```text
Run COMMAND-003.
```

Storyboard style must be:

```text
black-and-white rough pencil line art
minimal detail
clear silhouettes
colored annotations retained
```

## 4. Generate Publishing Package

Use when the video is ready for platform publishing:

```text
Run COMMAND-004.
```

## 5. Check Any Output

Use before production, generation, review, export or publishing:

```text
Run COMMAND-005.
```

---

# Required Reading For AI Tools

Before changing or generating formal output, read:

```text
AGENTS.md
CODEX-HANDOFF.md
docs/studio-os/START-HERE.md
README.md
docs/studio-os/RUNTIME.md
docs/studio-os/COMMANDS.md
```

For prompt generation, also read:

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
commands/COMMAND-002.md
workflows/WORKFLOW-002.md
agents/prompt-engineer/AGENT-002.md
knowledge/subject-identity/SUBJECT-001.md
knowledge/museum-relic-friends/RELIC-001.md
knowledge/visual-parameters/VISUALPARAM-001.md
knowledge/scene-blocking/BLOCKING-001.md
```

For storyboard generation, also read:

```text
commands/COMMAND-003.md
agents/director/AGENT-001.md
workflows/WORKFLOW-001.md
knowledge/subject-identity/SUBJECT-001.md
knowledge/museum-relic-friends/RELIC-001.md
knowledge/transition-language/TRANSITION-001.md
knowledge/visual-parameters/VISUALPARAM-001.md
knowledge/scene-blocking/BLOCKING-001.md
```

For consistency review, also read:

```text
commands/COMMAND-005.md
```

---

# Current Production Boundary

PROJ-001 has documentation for production, editing, publishing and post-publish tracking.

Current project status lives in:

```text
production/PROJ-001/STATUS.md
```

Some files intentionally contain `TBD`.

Do not fabricate:

```text
generated video clip results
final clip selections
export outcomes
publishing dates
platform metrics
post-publish analytics
```

Only replace `TBD` after real assets, review decisions or platform data exist.

---

# Direct Use Checklist

Before handing output to a model or publishing workflow, check:

```text
[ ] GitHub source files were read
[ ] Notion was not treated as canonical
[ ] Subject Mode is clear: Jump Mode or Custom Subject Mode
[ ] Jump remains a real dog-form character wearing clothes
[ ] Jump remains the AI Museum little security guard, not a human security guard
[ ] Relic friends follow RELIC-001 and retain Chinese cultural source identity
[ ] Custom Subject follows the approved identity card and does not inherit Jump-only rules
[ ] model-facing prompt does not rely on raw internal IDs
[ ] base visual parameters are explicit and model-readable
[ ] complex spatial scenes use an overhead blocking map when needed
[ ] storyboard uses black-and-white rough pencil line art
[ ] colored annotation system is preserved
[ ] transitions have a visible carrier, clear anchor and continuity logic
[ ] COMMAND-005 review is included
[ ] unknown real-world production values remain TBD
```
