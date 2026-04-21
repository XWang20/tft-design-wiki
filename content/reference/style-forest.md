---
title: "Style: Forest"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Forest

> Natural earthy greens with warm wood tones, organic and grounded feel

**分类**: 亮色 · **ID**: `forest`

## Background

```css
background: linear-gradient(165deg, #F5F7F2 0%, #E8EDE3 50%, #DCE4D5 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.65)` |
| `surface-solid` | `#FAFBF8` |
| `card-shadow` | `0 4px 20px rgba(45,125,70,0.06)` |
| `card-radius` | `14px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(45,125,70,0.08)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#1B2E1B` |
| `text-secondary` | `#3D5C3D` |
| `text-muted` | `#6B8A6B` |
| `text-hint` | `#9AB09A` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#2D7D46` |
| `accent-gradient` | `linear-gradient(135deg, #2D7D46, #8B6914)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#D4A017` | `rgba(212,160,23,0.10)` | `linear-gradient(160deg, #E8B82F, #D4A017)` |
| A | `#2D7D46` | `rgba(45,125,70,0.08)` | `linear-gradient(160deg, #43A047, #2D7D46)` |
| B | `#5D8AA8` | `rgba(93,138,168,0.08)` | `linear-gradient(160deg, #7BA7C2, #5D8AA8)` |
| C | `#8E8E8E` | `rgba(142,142,142,0.06)` | `linear-gradient(160deg, #ABABAB, #8E8E8E)` |

## Chart Line Colors

```css
--line-colors: #2D7D46, #D4A017, #5D8AA8, #C0392B, #8B6914, #607D8B;
--bar-track: rgba(45,125,70,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

leaf/branch SVG patterns at edges, opacity 0.04

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-sigma]] — 同类风格对比
