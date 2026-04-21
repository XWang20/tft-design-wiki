---
title: "Style: Ocean"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, cool]
---

# Ocean

> Deep blue ocean tones with teal accents, calm and professional

**分类**: 冷色 · **ID**: `ocean`

## Background

```css
background: linear-gradient(165deg, #F0F7FF 0%, #D6E8F7 50%, #C0D8EF 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.6)` |
| `surface-solid` | `#F8FBFF` |
| `card-shadow` | `0 4px 20px rgba(2,119,189,0.06)` |
| `card-radius` | `14px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(2,119,189,0.08)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#0D2137` |
| `text-secondary` | `#2A4A6B` |
| `text-muted` | `#5A7A9B` |
| `text-hint` | `#8AA8C5` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#0277BD` |
| `accent-gradient` | `linear-gradient(135deg, #0277BD, #00ACC1)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FF8F00` | `rgba(255,143,0,0.10)` | `linear-gradient(160deg, #FFB74D, #FF8F00)` |
| A | `#0277BD` | `rgba(2,119,189,0.08)` | `linear-gradient(160deg, #29B6F6, #0277BD)` |
| B | `#00897B` | `rgba(0,137,123,0.08)` | `linear-gradient(160deg, #26A69A, #00897B)` |
| C | `#78909C` | `rgba(120,144,156,0.06)` | `linear-gradient(160deg, #90A4AE, #607D8B)` |

## Chart Line Colors

```css
--line-colors: #0277BD, #00ACC1, #FF8F00, #00897B, #7B1FA2, #C62828;
--bar-track: rgba(2,119,189,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

wave pattern at bottom, opacity 0.04

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-cosmic]] — 同类风格对比
