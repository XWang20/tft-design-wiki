---
title: "Style: Midnight"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, dark]
---

# Midnight

> Deep navy dark theme with gold accents, luxurious and premium feel

**分类**: 暗色 · **ID**: `midnight`

## Background

```css
background: linear-gradient(165deg, #0F1923 0%, #162233 50%, #1A2940 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.05)` |
| `surface-solid` | `#1E2D40` |
| `card-shadow` | `0 4px 24px rgba(0,0,0,0.3)` |
| `card-radius` | `12px` |
| `card-backdrop` | `blur(16px)` |
| `border` | `rgba(255,179,0,0.10)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#E8EEF4` |
| `text-secondary` | `#B0C0D0` |
| `text-muted` | `#6888A0` |
| `text-hint` | `#405868` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#FFB300` |
| `accent-gradient` | `linear-gradient(135deg, #FFB300, #FF6F00)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FFB300` | `rgba(255,179,0,0.12)` | `linear-gradient(160deg, #FFD54F, #FFB300)` |
| A | `#4FC3F7` | `rgba(79,195,247,0.10)` | `linear-gradient(160deg, #81D4FA, #29B6F6)` |
| B | `#81C784` | `rgba(129,199,132,0.08)` | `linear-gradient(160deg, #A5D6A7, #66BB6A)` |
| C | `#78909C` | `rgba(120,144,156,0.06)` | `linear-gradient(160deg, #90A4AE, #546E7A)` |

## Chart Line Colors

```css
--line-colors: #FFB300, #4FC3F7, #FF7043, #66BB6A, #AB47BC, #78909C;
--bar-track: rgba(255,255,255,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

subtle star field dots, opacity 0.03

## 相关
- [[design-tokens]] — 全局共享token
- [[style-graphite]] — 同类风格对比
- [[style-cosmic]] — 同类风格对比
