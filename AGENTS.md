# AGENTS.md — TiaoTiao Studio OS Codex Instructions

## Project

This repository is the source of truth for TiaoTiao Studio OS.

TiaoTiao Studio OS is an AI-native creative production system for building repeatable short-video workflows around the IP character Jump / 跳跳.

## Source of Truth Rule

GitHub is the source of truth.

Notion is only the visual management layer.

Do not treat Notion as the canonical source.

## Current Main Project

PROJ-001 — Jump After Work Pilot Project

Chinese title:
《跳跳下班啦》

## Core Character Rule

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
- becoming a plain naked pet dog

## Prompt Runtime Rule

Internal database IDs are allowed inside GitHub documents, review records, changelogs, and Notion references.

But model-facing prompts must not rely on raw internal IDs.

Forbidden in model-facing prompts:
- consistent with ASSET-001
- follow CHAR-001
- use STYLE-001
- match BRAND-001

Required:
Translate internal IDs into complete natural language descriptions that AI models can understand.

## Video Prompt Architecture

All future video prompt packages must use this structure:

1. Identity Card Prompt
2. Storyboard Prompt
3. Universal Video Prompt

Do not create separate long prompts for every shot when a storyboard already exists.

Shot details belong to the storyboard.

Video prompt should stay compact and refer to:
- uploaded identity card
- uploaded storyboard
- current shot name

## Storyboard Style Rule

All storyboards must use:

- black-and-white line art
- rough pencil lines
- minimal details
- fast dynamic sketching
- simple anatomy
- clear silhouette
- lightweight unfinished storyboard feeling
- early fight choreography / director previs sketch feeling when action-heavy

Do not use:
- full-color concept art
- polished illustration
- realistic final render
- children's picture book style
- fully colored comic style

## Storyboard Color Annotation System

Even though the storyboard body is black-and-white pencil sketch, dynamic annotations must remain colored:

- Red: camera movement
- Blue: character / dog movement
- Yellow: prop interaction
- Green: lighting / mood
- Purple: continuity / transition

## Default Story Rule for Jump After Work

The series should not spend most of the time showing only the act of leaving work.

Default ratio:

- Office / clock-out part: 10%–20%
- After-work life montage: 80%–90%

After-work life examples:
- dinner
- supermarket
- movie night
- street snack
- night walk
- going home
- bath
- bedtime relaxation
- weekend outdoor life

## Current Completed Updates

The current prompt runtime upgrade has been completed and committed.

Completed system updates:

- `docs/studio-os/PROMPT-RUNTIME-RULES.md` defines model-facing prompt runtime rules.
- `commands/COMMAND-002.md` generates the Identity Card Prompt, Storyboard Prompt and Universal Video Prompt package.
- `commands/COMMAND-005.md` reviews model-readability, storyboard style, colored annotations and prompt runtime compliance.
- `workflows/WORKFLOW-002.md` follows Identity Card Prompt → Storyboard Prompt → Universal Video Prompt → Model-readable check → COMMAND-005 review.
- `workflows/WORKFLOW-003.md` uses uploaded identity card, uploaded storyboard and universal video prompt as the video generation runtime.
- `agents/director/AGENT-001.md` owns black-and-white rough pencil storyboard structure and colored annotation requirements.
- `agents/prompt-engineer/AGENT-002.md` owns model-readable prompt package generation.
- `ARCHITECTURE.md`, `README.md` and `CHANGELOG.md` document the Prompt Runtime Layer.
- `production/PROJ-001/VIDEO-PROMPTS.md` follows the new prompt runtime architecture.
- The canonical knowledge directory is lowercase `knowledge/`.

## Next Tasks

Continue OS development from the current point.

Priority tasks:

1. Keep the repository structure aligned with documented runtime paths.
   - Use `knowledge/`, `database/`, `agents/`, `workflows/`, `commands/`, `docs/studio-os/`, `examples/`, `validation/` and `production/`.
   - Do not introduce alternate directory names for canonical runtime layers.

2. Continue PROJ-001 only from real production state.
   - Do not fabricate final clip, publishing, analytics or post-publish values.
   - Keep TBD values where real generated clips, review decisions or platform metrics do not exist yet.

3. For any new video prompt package, use:
   - Identity Card Prompt
   - Storyboard Prompt
   - Universal Video Prompt
   - Model-readable check
   - COMMAND-005 review

4. Before generating or revising model-facing prompts, verify:
   - no raw internal IDs are required by the model
   - Jump remains a real dog-form character wearing clothes
   - storyboard style remains black-and-white rough pencil line art
   - colored annotation system remains present
   - GitHub remains Source of Truth and Notion remains only Visual Management Layer

5. If asked to continue system development, first check:
   - `CODEX-HANDOFF.md`
   - `git status --short`
   - whether the requested files are already aligned with the prompt runtime architecture

## Editing Rules

When editing files:

- Keep the repository structure clean.
- Use Markdown.
- Do not invent unrelated systems.
- Keep naming consistent.
- Do not rename existing database IDs unless explicitly required.
- Do not create too many new files unless necessary.
- Prefer updating existing OS files.

## Commit Style

Use conventional commit style.

Examples:

- refactor(workflow): update short video prompt workflow
- refactor(command): add prompt runtime checks
- docs(os): document prompt runtime layer
- chore(changelog): record prompt architecture update

## Final Output Expected

After making changes, summarize:

1. Files changed
2. What changed
3. Any assumptions
4. Suggested commit message
