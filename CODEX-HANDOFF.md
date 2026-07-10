# CODEX-HANDOFF — Current Development State

## Current State

TiaoTiao Studio OS is being developed as a production-ready AI-native creative operating system for the Jump / 跳跳 short-video IP.

The current main project has pivoted to:

```text
PROJ-001 — Little Security Guard and His Ancient Friends
《小保安和他的古人朋友们》
```

Jump is the little security guard. The ancient friends are Chinese cultural relics, ancient painting figures, artifacts and mythic motifs awakened inside an AI Museum.

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
reference/
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

External creator studies and source captures live in:

```text
reference/
```

Reference files are staging records. Do not treat them as canonical Knowledge Nodes until source material has been captured, reviewed and translated into TSOS model-readable rules.

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
- dog-size AI Museum little security guard outfit or approved dog clothing
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

## AI Museum Relic Friends Update

The new main story engine is:

```text
AI Museum closes
↓
Jump patrols as the little security guard
↓
Chinese relic friend awakens
↓
Ancient logic misunderstands modern museum rules
↓
Absurd museum incident escalates
↓
Jump resolves it with serious dog-form kindness
```

Canonical knowledge node:

```text
knowledge/museum-relic-friends/RELIC-001.md
```

Rules:

- Ancient friends must come from Chinese cultural relics, ancient paintings, artifacts, vessels, figurines, books, calligraphy or mythic motifs.
- They must retain source identity, material, pattern, dynasty feeling and cultural character.
- Comedy should be absurd and warm, not disrespectful toward cultural heritage.
- AI Museum should be warm, real and intelligent, not cyberpunk, horror or tomb-raiding.
- Jump must never become a human security guard.

## Generic Subject Identity Update

TSOS now supports two subject modes:

```text
Jump Mode
Custom Subject Mode
```

Jump Mode continues to use `CHAR-001`, `ASSET-001`, `OUTFIT-001` and the Jump dog-form rules above.

Custom Subject Mode uses:

```text
knowledge/subject-identity/SUBJECT-001.md
```

It can generate identity cards, storyboards and video prompt packages for humans, animals, plants, objects, products, scene subjects, mascots or new IP characters.

Model-facing Custom Subject prompts must describe the subject in natural language. They must not rely on `SUBJECT-001` as a raw internal ID, and they must not inherit Jump-only dog-form rules unless the user explicitly asks for that.

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

## Transition Language Update

The transition-language knowledge layer now includes:

```text
TRANSITION-001 — Universal AI Video Transition Grammar
```

`TRANSITION-001` was adapted from the user-provided Douyin note by `末鹿` about AI video transition prompts.

Use `TRANSITION-001` when a storyboard, prompt package or review needs reusable shot-to-shot transition logic, including light / shadow, action occlusion, camera movement, natural material, emotional flashback, time passage, spatial crossing and classical editing transitions.

COMMAND-003 now requires `Transition To Next Shot`.

COMMAND-005 now includes a dedicated `Transition Check`.

## Visual Parameter Update

The visual-parameters knowledge layer now includes:

```text
VISUALPARAM-001 — AIGC Base Visual Parameter Grammar
```

`VISUALPARAM-001` was adapted from the user-provided Douyin note reference by `赛博阿智pro` about AIGC basic visual parameters for AI short drama production.

The Douyin short link resolved to note ID:

```text
7657167225338987919
```

The page content was blocked by an anti-crawler JavaScript challenge during capture, so exact slide-level extraction and OCR remain pending.

Use `VISUALPARAM-001` when a prompt package, storyboard or review needs structured control over format, shot size, camera height, lens, composition, depth of field, lighting, color, texture, motion and continuity locks.

COMMAND-002 now requires visual parameters to be model-readable.

COMMAND-003 now includes visual parameter requirements in shot details.

COMMAND-005 now includes a dedicated `Visual Parameter Check`.

## Scene Blocking Update

The scene-blocking knowledge layer now includes:

```text
BLOCKING-001 — Overhead Scene Blocking Map
```

`BLOCKING-001` was adapted from the user-provided Douyin video reference attributed to `一帆老师` about using one overhead scene blocking map to avoid ineffective AI video generation attempts.

The Douyin short link resolved to video ID:

```text
7658676046082909425
```

The page content was blocked by an anti-crawler JavaScript challenge during capture, so exact video transcription and frame extraction remain pending.

Use `BLOCKING-001` when a prompt package, storyboard or review involves multi-person dialogue, complex walking paths, chase scenes, action blocking, camera switching or one-take camera movement.

COMMAND-002 now supports uploaded overhead scene blocking maps for complex spatial scenes.

COMMAND-003 now includes blocking map requirements in shot details when needed.

COMMAND-005 now includes a dedicated `Scene Blocking Check`.

## Creator Reference Update

The reference layer now includes:

```text
reference/creators/DLHU827-CAMERA-STUDY.md
reference/creators/MOLU-TRANSITION-STUDY.md
reference/creators/CYBER-AZHI-VISUAL-PARAMETER-STUDY.md
reference/creators/YIFAN-OVERHEAD-BLOCKING-STUDY.md
```

These are source-capture staging files for external creator studies.

`reference/creators/DLHU827-CAMERA-STUDY.md` is the source-capture file for the Douyin account `DLHU827`.

Current status:

```text
Collection Indexed / Item Content Pending
```

The user provided the Douyin collection link:

```text
https://v.douyin.com/Vtb6L7Mw1Mw/
```

It resolves to Mix ID:

```text
7643424899830122534
```

The collection metadata and all 36 episode item IDs have been indexed in `reference/creators/DLHU827-CAMERA-STUDY.md`.

Do not claim the camera and viewpoint language has been fully extracted until each item is opened, screenshot, exported, or otherwise reviewed.

`reference/creators/MOLU-TRANSITION-STUDY.md` records the source metadata, note ID and 35 source image URI fingerprints for the `末鹿` transition note.

The visible category architecture has been promoted into `knowledge/transition-language/TRANSITION-001.md`, but image-level OCR of all source slides is still pending.

`reference/creators/CYBER-AZHI-VISUAL-PARAMETER-STUDY.md` records the source capture boundary for the `赛博阿智pro` visual-parameter note.

The source theme has been promoted into `knowledge/visual-parameters/VISUALPARAM-001.md`, but full note body, slide images and OCR remain pending.

`reference/creators/YIFAN-OVERHEAD-BLOCKING-STUDY.md` records the source capture boundary for the `一帆老师` overhead blocking map video.

The source theme has been promoted into `knowledge/scene-blocking/BLOCKING-001.md`, but full video transcript, frames and original diagrams remain pending.

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

PROJ-001 — Little Security Guard and His Ancient Friends / 《小保安和他的古人朋友们》 has production docs for:

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
