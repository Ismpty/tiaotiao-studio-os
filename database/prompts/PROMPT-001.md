# PROMPT-001 — TiaoTiao Studio Prompt Standard（TSOS 提示词标准）

> **Canonical Prompt Record（官方 Prompt 规范）**
> Version：1.0
> Status：Active

# Overview（概述）

## Purpose（用途）

### 中文

本规范定义了 TiaoTiao Studio 所有 AI 图像、视频、动画 Prompt 的统一编写方式。

所有 Prompt 必须遵循模块化组合，不允许临时拼接。

### English

This document defines the unified prompt standard for all AI-generated images, videos and animations used in TiaoTiao Studio.

---

# Prompt Structure（Prompt 结构）

标准 Prompt 由六个模块组成：

```text
Subject（主体）
        ↓
Action（动作）
        ↓
Environment（环境）
        ↓
Camera（摄影）
        ↓
Lighting（灯光）
        ↓
Style（风格）
```

示例：

```text
Jump（主体）
+
Natural Walking（动作）
+
Studio Office（环境）
+
Hero Tracking Shot（摄影）
+
Golden Hour（灯光）
+
Cinematic Documentary（风格）
```

---

# Style Standard（风格标准）

默认风格：

* Cinematic
* Photorealistic
* Documentary
* High Detail
* Natural Lighting

---

# Negative Prompt（负面提示）

禁止出现：

* Plastic Texture（塑料质感）
* Cartoon Face（卡通脸）
* Horror Style（恐怖风）
* Low Resolution（低清晰度）
* Over Saturation（过饱和）
* Unrealistic Anatomy（错误人体比例）

---

# Prompt Version（版本管理）

每个 Prompt 必须记录：

* Version（版本）
* Author（作者）
* Model（模型）
* Date（日期）

---

# Related Database（关联数据库）

* Character
* Motion
* Environment
* Camera
* Lighting

---

# Changelog（更新记录）

| Version | Date | Changes                 |
| ------- | ---- | ----------------------- |
| 1.0     | 2026 | 创建 TSOS Prompt Standard |

---

