# CODEX-HANDOFF — Current Development State

## Current State

TiaoTiao Studio OS is being developed as a production-ready AI-native creative operating system for the Jump / 跳跳 short-video IP.

The current confirmed architecture is:

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

All canonical rules, records, agents, workflows, commands, runtime docs and examples must be maintained in GitHub first.

Notion can be used for visual management, dashboards and synchronization, but it must not override GitHub files.

## Current Runtime Structure

Canonical runtime paths:

```text
knowledge/
database/
agents/
workflows/
commands/
docs/studio-os/
examples/
validation/
production/
```

The canonical knowledge directory is lowercase:

```text
knowledge/
```

Do not recreate or reference `Knowledge/` as a runtime path.

## Prompt Runtime Architecture

All future video prompt packages must use:

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

This replaces the older structure where Shot 1–6 each had long duplicated video prompts.

## Key Runtime Rule

Internal TSOS IDs are allowed inside GitHub documents, review records, changelogs and Notion references.

Model-facing prompts must not rely on raw internal IDs.

Before model use, internal IDs must be translated into complete natural language descriptions that the model can understand.

## Jump Character Rule

Jump / 跳跳 must remain a real dog-form character wearing clothes.

Required:

- real dog body form
- four-legged dog anatomy
- fluffy fur
- programmer-style dog clothing
- small backpack / badge / collar charm allowed
- dragon-fruit pink accent details allowed

Forbidden:

- humanoid body
- human hands
- human arms
- human legs
- bipedal human standing pose
- human body proportions
- turning into a human
- turning into another animal
- losing fluffy fur

## Storyboard Rule

Storyboards must be black-and-white rough pencil line art with minimal details and clear silhouettes.

Colored annotation system remains required:

```text
Red = camera movement
Blue = dog / character movement
Yellow = prop interaction
Green = lighting / mood
Purple = continuity / transition
```

## Camera Language Update

The camera-language knowledge layer now includes:

```text
SHOT-001 — Hero Tracking Shot
SHOT-002 — Six-View Scene Lock
```

`SHOT-002` was adapted from the user-provided Douyin note about AI camera language and scene consistency.

Use `SHOT-002` when a storyboard or video prompt needs to keep scene layout, light direction, color, props and character appearance stable while changing camera position.

## Completed Prompt Runtime Upgrade

The following system files have already been aligned with the new prompt runtime architecture:

- `docs/studio-os/PROMPT-RUNTIME-RULES.md`
- `commands/COMMAND-002.md`
- `commands/COMMAND-005.md`
- `workflows/WORKFLOW-002.md`
- `workflows/WORKFLOW-003.md`
- `agents/director/AGENT-001.md`
- `agents/prompt-engineer/AGENT-002.md`
- `ARCHITECTURE.md`
- `README.md`
- `CHANGELOG.md`
- `production/PROJ-001/VIDEO-PROMPTS.md`
- `examples/`
- `validation/`

## Completed Repository Structure Cleanup

The knowledge layer has been normalized to the documented lowercase runtime path:

```text
knowledge/
```

This keeps the actual repository structure aligned with README, INDEX, RUNTIME, commands, workflows and agent references.

## Completed Runtime Quickstart Pass

TSOS now has a direct-use entry guide:

```text
docs/studio-os/START-HERE.md
```

The following runtime entry docs route AI tools through it:

- `README.md`
- `docs/studio-os/INDEX.md`
- `docs/studio-os/RUNTIME.md`
- `docs/studio-os/CODEX.md`

This guide defines:

- fastest command routing
- required reading for AI tools
- prompt runtime architecture
- Jump character constraints
- storyboard style constraints
- current production boundary
- direct-use checklist

## Current PROJ-001 State

PROJ-001 — Jump After Work Pilot Project / 《跳跳下班啦》 has production docs for:

- current status dashboard
- prompt package
- storyboard package
- cover package
- publishing package
- production checklist
- editing assembly
- caption timing
- music and sound
- final export checklist
- review templates
- iteration logs
- post-publish tracker

Current production status file:

```text
production/PROJ-001/STATUS.md
```

Some production files intentionally contain TBD values.

Do not fabricate final clip selections, review decisions, export outcomes, platform metrics or post-publish data.

Only replace TBD values after real production assets or real publishing data exist.

## Immediate Continuation Point

If the user asks to continue system development:

1. Read `AGENTS.md` and this file first.
2. Read `docs/studio-os/START-HERE.md`.
3. Run `git status --short`.
4. Check whether the requested file is already aligned with:
   - GitHub Source of Truth
   - Notion Visual Management Layer
   - model-readable prompt rules
   - Jump real dog-form rule
   - black-and-white rough pencil storyboard rule
   - colored annotation system
5. Prefer updating existing OS files rather than creating new files.

Recommended next work:

```text
Run a focused readiness pass on runtime docs, examples, validation records or PROJ-001 production records only when the user asks for that area.
```

Do not repeat the already completed WORKFLOW-002 prompt runtime upgrade unless the user explicitly requests a revision.
