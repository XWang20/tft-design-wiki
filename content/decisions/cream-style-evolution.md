---
title: Cream Style Evolution
created: 2026-04-21
updated: 2026-04-21
type: decision
tags: [visual-identity, color, iteration]
---

# Cream Style Evolution

> 从"那坨黑黑的"到粉紫暖色调，TFTable的视觉识别是怎么来的。

## 风格迭代历史

### Phase 1: 暗色esports（否决）
深色背景，霓虹强调色。电竞网站标配。
- ash评价："那坨黑黑的"
- 教训：竞品都在做的风格不是"安全选择"，是没有辨识度

### Phase 2: Cream暖色（采纳）
暖奶油色背景，棕色文字，橙色强调。
- 灵感来源：小红书原生的视觉调性
- 核心特征：看起来不像"游戏网站"，更像生活方式内容
- ash确认采纳

### Phase 3: 竞品研究（否决）
研究了tactics.tools, lolchess等竞品风格。
- 结论：所有竞品都是暗色 + 蓝紫强调 → 差异化就是不做这个

### Phase 4: 三风格体系（当前）
ash在2026-04-11确认三个official palette：
- **Forest** — 深绿，严肃/竞技
- **Sakura** — 浅粉蓝，清新
- **Sunset** — 暖色深底

原则：**颜色固定，UI组件按内容类型灵活调整。**

### S17 Cosmic 渐变
随Riot官方S17赛季主题（紫粉星云渐变），出了Cosmic风格变体。同系列用同样的紫/薰衣草渐变。

## 关键设计选择的理由

**为什么MiSans不是Noto Sans SC**: Noto在信息图尺寸下笔画细节丢失，MiSans的笔画更粗更清晰。另外MiSans原生支持tabular figures。

**为什么Outfit不是Inter**: Inter是AI生成的头号默认字体。用Outfit的几何感相似但不会一眼"AI味"。

**为什么同系列用同一渐变**: 用户在抖音/小红书刷到多张图时，统一渐变建立系列感。标题字号70-80px@1080w也是为了在feed小图时依然可读。

## 相关
- [[no-dark-theme]] — 暗色否决的完整故事
- [[context-over-defaults]] — 设计选择的原则
