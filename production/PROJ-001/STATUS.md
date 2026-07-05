# PROJ-001 — Current Production Status

> Production Status Dashboard
> Project: PROJ-001 — Jump After Work Pilot Project
> Chinese Title: 《跳跳下班啦》
> Status: Ready For Real Video Generation

---

# Current Usable State

PROJ-001 is ready to start real video generation.

The current runtime structure is:

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

The current shot structure is:

```text
Shot 1 — Work Ending
Shot 2 — Clock Out
Shot 3 — Dinner Time
Shot 4 — Supermarket Walk
Shot 5 — Movie Night
Shot 6 — Street Snack
Shot 7 — Night Walk
Shot 8 — Life Begins
```

---

# Ready Files

Use these files directly:

```text
production/PROJ-001/VIDEO-PROMPTS.md
production/PROJ-001/RUNBOOK.md
production/PROJ-001/PRODUCTION-CHECKLIST.md
production/PROJ-001/review/CLIP-REVIEW-GUIDE.md
production/PROJ-001/review/SHOT-REVIEW-TEMPLATE.md
production/PROJ-001/review/ITERATION-LOG.md
production/PROJ-001/review/FINAL-CLIP-SELECTION.md
production/PROJ-001/editing/EDITING-ASSEMBLY.md
production/PROJ-001/editing/CAPTION-TIMING.md
production/PROJ-001/editing/MUSIC-SOUND.md
production/PROJ-001/final/FINAL-EXPORT-CHECKLIST.md
production/PROJ-001/COVER-PACKAGE.md
production/PROJ-001/PUBLISHING-PACKAGE.md
production/PROJ-001/POST-PUBLISH-TRACKER.md
```

---

# Next Real Action

Start video generation:

```text
1. Open production/PROJ-001/VIDEO-PROMPTS.md.
2. Generate Jump-Identity-Card-v02.jpg.
3. Generate PROJ-001-Storyboard-v02.jpg.
4. Upload identity card and storyboard to the video model.
5. Copy the Universal Video Prompt.
6. Set Current Shot: Shot 1 — Work Ending.
7. Generate SHOT-001-v01, SHOT-001-v02 and SHOT-001-v03.
8. Review each result with COMMAND-005 and SHOT-REVIEW-TEMPLATE.md.
9. Record results in ITERATION-LOG.md.
10. Repeat for Shot 2–8.
```

---

# Do Not Fabricate

The following values must remain `TBD` until real production data exists:

```text
generated clip filenames
review pass / fail decisions
approved clip selections
final export result
publishing date
platform metrics
post-publish analytics
next episode decision
```

---

# Completion Gate

The project becomes ready for editing only after:

```text
[ ] all Shot 1–8 clips have at least one reviewed version
[ ] FINAL-CLIP-SELECTION.md has selected clips for Shot 1–8
[ ] selected clips are copied to production/PROJ-001/clips/approved/
[ ] COMMAND-005 returns PASS or PASS WITH MINOR FIXES for final clip continuity
```

The project becomes ready for publishing only after:

```text
[ ] final edit is exported
[ ] FINAL-EXPORT-CHECKLIST.md is complete
[ ] publishing package is reviewed
[ ] cover is finalized
[ ] COMMAND-005 final publishing review passes
```
