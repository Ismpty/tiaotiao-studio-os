# Reference Library（参考素材库）

> Source Capture Layer
>
> Status：Active

---

# Purpose（用途）

Reference Library 存放外部素材、创作者研究、平台案例、摄影参考、音乐参考、服装参考和视觉参考。

它不是最终规则层。

正式、可复用、可直接进入模型工作流的规则，必须先从 Reference 提炼，再晋升到：

```text
knowledge/
```

---

# Source of Truth Rule（事实来源规则）

```text
GitHub = Source of Truth
Notion = Visual Management Layer
```

Reference 文件也必须先记录在 GitHub。

Notion 可以同步这些素材条目用于看板、筛选、标签和视觉管理，但不能覆盖 GitHub 中的记录。

---

# Canonicalization Rule（晋升规则）

外部参考进入 `knowledge/` 前，必须满足：

- 有明确来源或采集记录
- 不直接复制平台原文作为模型 Prompt
- 已提炼为可复用的镜头、风格、动作、音乐或叙事规则
- 已提炼为可复用的基础画面参数、场景调度、转场、镜头、风格、动作、音乐或叙事规则
- 模型可读，不依赖内部原始 ID
- 兼容 Jump / 跳跳真实狗形角色规则
- 兼容黑白粗铅笔分镜规则和颜色标注系统

---

# Current Reference Areas（当前参考区域）

```text
reference/animation/
reference/architecture/
reference/creators/
reference/fashion/
reference/movies/
reference/music/
reference/photography/
```
