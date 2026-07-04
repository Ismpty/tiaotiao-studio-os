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

The following files were recently updated or should exist:

- docs/studio-os/PROMPT-RUNTIME-RULES.md
- commands/COMMAND-002.md
- agents/prompt-engineer/AGENT-002.md
- production/PROJ-001/VIDEO-PROMPTS.md

## Next Tasks

Continue OS development from the current point.

Priority tasks:

1. Update workflows/WORKFLOW-002.md
   - Convert Short Video Prompt Workflow to the new structure:
     Identity Card Prompt
     ↓
     Storyboard Prompt
     ↓
     Universal Video Prompt
     ↓
     Model-readable check
     ↓
     COMMAND-005 review

2. Update commands/COMMAND-005.md
   - Add checks for:
     model-readable prompts
     no raw internal IDs in model-facing prompt
     storyboard black-and-white pencil style
     color annotation system
     identity card existence
     universal video prompt structure

3. Update workflows/WORKFLOW-003.md
   - Align Storyboard to Video Workflow with identity card + storyboard + universal video prompt.

4. Update agents/director/AGENT-001.md
   - Add responsibility for black-and-white pencil storyboard structure and color annotations.

5. Update ARCHITECTURE.md
   - Add Prompt Runtime Layer.

6. Update README.md
   - Add current OS operating structure.

7. Update CHANGELOG.md
   - Record the new prompt runtime architecture.

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
