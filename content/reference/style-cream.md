---
title: "Style: Cream"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Cream

> Warm, approachable, Xiaohongshu-native style with orange accents

**分类**: 亮色 · **ID**: `cream`

## Background

```css
background: linear-gradient(165deg, #FFF9F2 0%, #FFEDD5 50%, #FEE2C5 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.6)` |
| `surface-solid` | `#FFFFFF` |
| `card-shadow` | `0 4px 20px rgba(0,0,0,0.06)` |
| `card-radius` | `14px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(0,0,0,0.06)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#3E2723` |
| `text-secondary` | `#5D4037` |
| `text-muted` | `#8D6E63` |
| `text-hint` | `#BCAAA4` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#FF8F00` |
| `accent-gradient` | `linear-gradient(90deg, #FF8F00, #43A047)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FF8F00` | `rgba(255,143,0,0.10)` | `linear-gradient(160deg, #FFB74D, #FF8F00)` |
| A | `#43A047` | `rgba(67,160,71,0.08)` | `linear-gradient(160deg, #66BB6A, #43A047)` |
| B | `#1E88E5` | `rgba(30,136,229,0.08)` | `linear-gradient(160deg, #42A5F5, #1E88E5)` |
| C | `#8E24AA` | `rgba(142,36,170,0.06)` | `linear-gradient(160deg, #AB47BC, #8E24AA)` |

## Chart Line Colors

```css
--line-colors: #FF8F00, #43A047, #1E88E5, #8E24AA, #f472b6, #34d399, #fb923c, #38bdf8;
--bar-track: rgba(0,0,0,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Decoration

subtle radial-gradient circles at corners, opacity 0.05-0.08

## 相关
- [[design-tokens]] — 全局共享token
- [[style-sigma]] — 同类风格对比
- [[style-gradient-tech]] — 同类风格对比
