# CODEX-HANDOFF — Current Development State

## Current State

TiaoTiao Studio OS is being upgraded from a static content database into a production-ready AI-native creative operating system.

The latest confirmed architecture is:

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

## Recently Established Rule

All video prompt packages now use:

```text
Identity Card Prompt
+
Storyboard Prompt
+
Universal Video Prompt
```

This replaces the older structure where Shot 1–6 each had long duplicated video prompts.

## Key Runtime Rule

Internal IDs are allowed for system management, but model-facing prompts must be written in natural language.

## Jump Character Rule

Jump / 跳跳 is a real dog-form character wearing clothes.

No humanoid body.

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

## User Preference

The user prefers practical, directly usable Markdown files.

Do not over-create new files.

Prefer updating existing OS files.

## Immediate Continuation Point

We just updated:

```text
docs/studio-os/PROMPT-RUNTIME-RULES.md
commands/COMMAND-002.md
agents/prompt-engineer/AGENT-002.md
```

Next file to update:

```text
workflows/WORKFLOW-002.md
```

Goal:

Update `WORKFLOW-002 — Short Video Prompt Workflow` so it follows:

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
