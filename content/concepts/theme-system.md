---
title: Theme System
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [theme, style, design-system, color]
sources: [raw/workspace/social-media/STYLE_GUIDE.md, raw/workspace/image-studio/UISAVIOR_STYLES.md]
---

# Theme System

24主题的CSS token体系。原则：**颜色固定，UI组件按内容类型灵活调整。**

## 三个确认风格（ash 2026-04-11确认）

### Forest（森林暗绿）
深绿色调，适合严肃/竞技内容。

### Sakura（樱花粉蓝）
浅粉蓝色调，轻盈清新。

### Sunset（日落暖色）
暖色系，深色底。

每个palette都有完整token集：bg, card, accent, text, tier colors, 8条趋势线颜色。

## Cream系列（当前主力）
S17赛季主风格：
- 背景渐变：`#FFF8F0 → #FFE8D6 → #FFECD2`
- 文字棕色：`#3E2723 / #5D4037 / #8D6E63`
- 强调橙：`#FF8F00`
- compCost系统：每张阵容卡的`--c-accent`由cost决定

## @uisavior参考风格（13种分析）
来自Twitter @uisavior的设计分析，每种都有完整CSS token：
1. Bold Editorial Poster — 大字排版
2. Minimal Spec Sheet — 瑞士网格
3. UI Education Card — Bad vs Good对比
4. Swatch Board — 暗色token展示
5. Technical Flowchart — 决策树
6. Editorial Serif — 杂志风
7. Gradient Tech — 浅灰蓝（已在用）
8. Japanese Grid — 中性模块
9. Brutalist — 黑+红极简
10. Dark Swatch Wall — 暗色网格
11. Modern Editorial Serif — 暖灰+单色
12. Micro-Rule Card — 冷灰，红绿对比
13. S17 Cosmic Gradient — 紫粉星云（Riot官方S17风格）

## 相关
- [[design-system]] — 主设计系统
- [[lessons-and-bugs]] — 风格踩坑记录
