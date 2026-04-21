---
title: "Style: Sakura"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Sakura

> Soft pink and blush tones inspired by cherry blossoms, feminine and elegant

**分类**: 亮色 · **ID**: `sakura`

## Background

```css
background: linear-gradient(165deg, #FFF5F7 0%, #FFE4E8 50%, #FDD5DC 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.6)` |
| `surface-solid` | `#FFFBFC` |
| `card-shadow` | `0 4px 20px rgba(233,30,99,0.06)` |
| `card-radius` | `16px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(233,30,99,0.06)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#3D1F28` |
| `text-secondary` | `#6B3A4A` |
| `text-muted` | `#9B6B7D` |
| `text-hint` | `#C8A0B0` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#E91E63` |
| `accent-gradient` | `linear-gradient(135deg, #E91E63, #9C27B0)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#E91E63` | `rgba(233,30,99,0.10)` | `linear-gradient(160deg, #F06292, #E91E63)` |
| A | `#AB47BC` | `rgba(171,71,188,0.08)` | `linear-gradient(160deg, #CE93D8, #AB47BC)` |
| B | `#7986CB` | `rgba(121,134,203,0.08)` | `linear-gradient(160deg, #9FA8DA, #5C6BC0)` |
| C | `#B0A0A8` | `rgba(176,160,168,0.06)` | `linear-gradient(160deg, #D0C4C8, #B0A0A8)` |

## Chart Line Colors

```css
--line-colors: #E91E63, #AB47BC, #5C6BC0, #EC407A, #F48FB1, #CE93D8;
--bar-track: rgba(233,30,99,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

petal shapes scattered at corners, opacity 0.05

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-sigma]] — 同类风格对比
