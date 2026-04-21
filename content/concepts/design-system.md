---
title: Design System
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [design-system, style, theme, color, typography, layout]
sources: [raw/workspace/social-media/DESIGN.md, raw/workspace/social-media/DESIGN_SYSTEM.md]
---

# Design System

TFTable信息图的完整视觉规范体系。

## 输出规格
- **画布**: 1080×1440 @2x（实际输出2160×2880 PNG）
- **背景**: `#FAFAF8`（cream系列）
- **截图**: `full_page=False`，固定视口尺寸

## 24主题系统

### Tier 1 Active（正在使用）
| 主题 | 描述 |
|------|------|
| **Cream** | 暖奶油色，主力风格。`#FFF8F0→#FFE8D6→#FFECD2` |
| **Gradient Tech** | 浅灰蓝科技感 |
| **Graphite** | 深色石墨 |

### Tier 2 @uisavior参考（9个）
Bold Editorial, Minimal Spec, UI Education, Swatch Board, Flowchart, Serif Quote, Japan Grid, Brutalist, Editorial

### Tier 3 备选（12个）
Micro-Rule, Amber Dark, Neon Cyber, Cosmic, Tarot Gold, Pastel Pop, Hextech, Tier List, Ink Wash, Glassmorphism, Patch Notes, Heatmap

## 字体
- **主字体**: Outfit（英文），通过base64 woff2嵌入HTML
- **中文**: MiSans（不是Noto Sans SC！），从CDN加载
- **数字**: `font-variant-numeric: tabular-nums`

## 字号系统（@2x）
| Token | 大小 | 用途 |
|-------|------|------|
| `--fs-hero` | 80px | 标题（1080w时70-80px） |
| `--fs-h1` | 56px | 一级标题 |
| `--fs-h2` | 44px | 二级标题 |
| `--fs-body` | 36px | 正文 |
| `--fs-sm` | 28px | 小字 |
| `--fs-xs` | 24px | 最小字号 |
| 最小值 | 14px | **永远不低于14px** |

## Cost颜色（通用不变）
| 费用 | 颜色 |
|------|------|
| 1 | `#808080` 灰 |
| 2 | `#11b288` 绿 |
| 3 | `#207ac7` 蓝 |
| 4 | `#c440da` 紫 |
| 5 | `#ffb93b` 金 |

## Tier颜色
- S: 金橙
- A: 绿
- B: 蓝
- C: 紫

## 组件规范
- **卡片容器**: 圆角，阴影，白底或渐变底
- **Tier徽章**: 彩色方块+字母
- **英雄头像**: 六边形或方形，边框颜色=cost颜色
- **Sparkline**: Catmull-Rom平滑曲线，SVG内联
- **水印**: 左下=来源credit，右下=`@TFTable`

## 永久禁止
- ❌ 暗色主题（"永ban暗色"，"那坨黑黑的"被否决）
- ❌ Emoji（headless Chromium不支持）
- ❌ 暗夜金 Dark Gold（"这辈子不想再看见"）
- ❌ 嵌套卡片
- ❌ 多层渐变

## 相关
- [[theme-system]] — 24主题详细CSS tokens
- [[rendering-pipeline]] — 设计如何落地为图片
- [[lessons-and-bugs]] — 设计踩坑
- [[content-types]] — 各内容类型的设计规范
