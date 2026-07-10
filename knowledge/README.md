# TiaoTiao Studio Knowledge System

> Single Source of Truth for all reusable creative knowledge.

---

# Purpose（用途）

## 中文

Knowledge Layer 是整个 TiaoTiao Studio OS 的核心知识层。

这里存放的是**可复用、不会因为某一个项目而改变的知识**。

例如：

- 摄影风格
- 品牌色
- 世界观
- 情绪系统
- 镜头语言

Character、Episode、Project 等数据库不应重复描述这些知识，而应引用这里的标准。

---

## English

The Knowledge Layer contains reusable and canonical knowledge shared across all productions.

Production databases should reference these knowledge nodes instead of duplicating them.

---

# Knowledge Libraries（知识库）

| Library | Description | Status |
|----------|-------------|--------|
| Style | Visual language and aesthetics | ✅ |
| Color | Brand color system | ✅ |
| World | World building | ✅ |
| Emotion | Emotional framework | ✅ |
| Subject Identity | Generic identity card grammar | ✅ |
| Museum Relic Friends | AI Museum relic-friend character grammar | ✅ |
| Visual Parameters | AIGC base image / video parameter grammar | ✅ |
| Scene Blocking | Overhead scene blocking and spatial choreography | ✅ |
| Camera Language | Cinematic shot language | ✅ |
| Transition Language | Reusable video transition grammar | ✅ |
| Motion Language | Motion principles | ✅ |
| Outfit | Character outfit system | ✅ |
| Music | Music language | ✅ |
| Story Formula | Storytelling framework | ✅ |
| Brand Language | Brand values and tone | ✅ |

---

# Current Knowledge Nodes（当前知识节点）

## Style

- STYLE-001 — Cinematic Documentary

## Color

- COLOR-001 — Fire Dragon Fruit Palette

## World

- WORLD-001 — TiaoTiao Universe

## Emotion

- EMOTION-001 — Freedom

## Subject Identity

- SUBJECT-001 — Generic Subject Identity Card Grammar

## Museum Relic Friends

- RELIC-001 — AI Museum Relic Friends Grammar

## Visual Parameters

- VISUALPARAM-001 — AIGC Base Visual Parameter Grammar

## Scene Blocking

- BLOCKING-001 — Overhead Scene Blocking Map

## Camera Language

- SHOT-001 — Hero Tracking Shot
- SHOT-002 — Six-View Scene Lock

## Transition Language

- TRANSITION-001 — Universal AI Video Transition Grammar

## Motion Language

- MOTIONLANG-001 — Natural Walking Language

## Outfit

- OUTFIT-001 — Programmer Outfit System

## Music

- MUSIC-001 — Lifestyle Music Language

## Story Formula

- STORYFORMULA-001 — Work Ends, Adventure Begins

## Brand Language

- BRAND-001 — TiaoTiao Studio Brand Language

---

# Design Principles（设计原则）

Every Knowledge Node must be:

- Canonical（官方）
- Reusable（可复用）
- Model Agnostic（模型无关）
- Version Controlled（版本管理）
- Referenced instead of duplicated（引用而不是复制）

---

# Relationship（引用关系）

Knowledge Layer

↓

Character

↓

Episode

↓

Story

↓

Environment

↓

Prompt

↓

Project

---

# Naming Convention（命名规范）

STYLE-001

COLOR-001

WORLD-001

EMOTION-001

SUBJECT-001

RELIC-001

VISUALPARAM-001

BLOCKING-001

SHOT-001

SHOT-002

TRANSITION-001

MOTIONLANG-001

OUTFIT-001

MUSIC-001

STORYFORMULA-001

BRAND-001

---

# Changelog（更新记录）

| Version | Date | Changes |
|---------|------|----------|
| 1.5 | 2026 | Added RELIC-001 AI Museum Relic Friends Grammar |
| 1.4 | 2026 | Added SUBJECT-001 Generic Subject Identity Card Grammar |
| 1.3 | 2026 | Added BLOCKING-001 Overhead Scene Blocking Map |
| 1.2 | 2026 | Added VISUALPARAM-001 AIGC Base Visual Parameter Grammar |
| 1.1 | 2026 | Added TRANSITION-001 Universal AI Video Transition Grammar |
| 1.0 | 2026 | Initial Knowledge Index |
