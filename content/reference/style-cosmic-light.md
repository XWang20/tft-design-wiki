---
title: "Style: Cosmic Light"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Cosmic Light

> Clean celestial theme with lavender accents and soft gradients

**分类**: 亮色 · **ID**: `cosmic_light`

## Background

```css
background: linear-gradient(165deg, #F8F6FF 0%, #EDE7F6 50%, #E1D5F0 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.7)` |
| `surface-solid` | `#FFFFFF` |
| `card-shadow` | `0 4px 24px rgba(124,77,255,0.08)` |
| `card-radius` | `16px` |
| `card-backdrop` | `blur(12px)` |
| `border` | `rgba(124,77,255,0.08)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#1A1035` |
| `text-secondary` | `#4A3F6B` |
| `text-muted` | `#7E6FA0` |
| `text-hint` | `#B0A3C8` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#7C4DFF` |
| `accent-gradient` | `linear-gradient(135deg, #7C4DFF, #E040FB)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#fbbf24` | `rgba(251,191,36,0.12)` | `linear-gradient(160deg, #fcd34d, #f59e0b)` |
| A | `#a78bfa` | `rgba(167,139,250,0.10)` | `linear-gradient(160deg, #c4b5fd, #8b5cf6)` |
| B | `#60a5fa` | `rgba(96,165,250,0.08)` | `linear-gradient(160deg, #93c5fd, #3b82f6)` |
| C | `#9ca3af` | `rgba(156,163,175,0.08)` | `linear-gradient(160deg, #d1d5db, #6b7280)` |

## Chart Line Colors

```css
--line-colors: #7C4DFF, #E040FB, #00BCD4, #FF7043, #66BB6A, #FFC107;
--bar-track: rgba(124,77,255,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

subtle star/dot pattern at 0.04 opacity

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-sigma]] — 同类风格对比
