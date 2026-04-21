---
title: "Style: Sunset"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, warm]
---

# Sunset

> Warm sunset gradients with amber and coral, vibrant and energetic

**分类**: 暖色 · **ID**: `sunset`

## Background

```css
background: linear-gradient(165deg, #FFF5EB 0%, #FFE0CC 50%, #FFD0B0 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.55)` |
| `surface-solid` | `#FFFAF5` |
| `card-shadow` | `0 4px 20px rgba(255,87,34,0.06)` |
| `card-radius` | `14px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(255,87,34,0.08)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#3D2010` |
| `text-secondary` | `#6B4030` |
| `text-muted` | `#9B7060` |
| `text-hint` | `#C8A090` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#FF5722` |
| `accent-gradient` | `linear-gradient(135deg, #FF5722, #FF9800)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FF5722` | `rgba(255,87,34,0.10)` | `linear-gradient(160deg, #FF8A65, #FF5722)` |
| A | `#FF9800` | `rgba(255,152,0,0.08)` | `linear-gradient(160deg, #FFB74D, #FF9800)` |
| B | `#26A69A` | `rgba(38,166,154,0.08)` | `linear-gradient(160deg, #4DB6AC, #26A69A)` |
| C | `#90A4AE` | `rgba(144,164,174,0.06)` | `linear-gradient(160deg, #B0BEC5, #78909C)` |

## Chart Line Colors

```css
--line-colors: #FF5722, #FF9800, #FFC107, #26A69A, #EC407A, #42A5F5;
--bar-track: rgba(255,87,34,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

warm radial glow at top corners, opacity 0.06

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-cosmic]] — 同类风格对比
