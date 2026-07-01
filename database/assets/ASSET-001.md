# ASSET-001 — Studio Asset Management（Studio 资产管理规范）

> **Canonical Asset Record（官方资产规范）**

# Overview（概述）

## Purpose（用途）

### 中文

Asset Database 用于管理 TiaoTiao Studio 所有数字资产，是整个 Studio 的资源索引中心。

它不负责创作，而负责管理、追踪和复用。

### English

The Asset Database manages all digital assets and serves as the central index of reusable resources.

---

# Asset Categories（资产分类）

角色（Character）

场景（Environment）

动作（Motion）

Prompt

图片（Image）

视频（Video）

音乐（Music）

字体（Font）

Logo

模板（Template）

---

# Asset Information（资产信息）

每个 Asset 必须包含：

* Asset ID
* Asset Name
* Asset Type
* Version
* Storage Path
* Source
* License
* Status

---

# Storage Rules（存储规范）

GitHub：

保存 Markdown。

Cloud：

保存原始素材。

Notion：

保存索引。

---

# Naming Convention（命名规范）

统一格式：

```text
TYPE-编号-名称

例如：

IMG-001-Jump-Office

VID-008-Surfing

PSD-002-Cover
```

---

# Lifecycle（生命周期）

Draft

↓

Review

↓

Approved

↓

Published

↓

Archived

---

# Related Database（关联数据库）

Character

Episode

Project

Prompt

---

# Changelog（更新记录）

Version 1.0

---

