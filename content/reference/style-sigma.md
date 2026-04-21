---
title: "Style: Sigma"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Sigma

> TFTable signature style — SigmaSerif headlines + SigmaSans body on warm white, red accent. Used for unit cards, trait cards, and production infographics.

**分类**: 亮色 · **ID**: `sigma`

## Background

```css
background: #FAFAF8;
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.6)` |
| `surface-solid` | `#FFFFFF` |
| `card-shadow` | `0 4px 20px rgba(0,0,0,0.06)` |
| `card-radius` | `12px` |
| `card-backdrop` | `blur(8px)` |
| `border` | `rgba(0,0,0,0.06)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#1a1a1a` |
| `text-secondary` | `#555555` |
| `text-muted` | `#999999` |
| `text-hint` | `#CCCCCC` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#C8392D` |
| `accent-gradient` | `linear-gradient(135deg, #C8392D, #E05050)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FF8F00` | `rgba(255,143,0,0.10)` | `linear-gradient(160deg, #FFB74D, #FF8F00)` |
| A | `#43A047` | `rgba(67,160,71,0.08)` | `linear-gradient(160deg, #66BB6A, #43A047)` |
| B | `#1E88E5` | `rgba(30,136,229,0.08)` | `linear-gradient(160deg, #42A5F5, #1E88E5)` |
| C | `#8E24AA` | `rgba(142,36,170,0.06)` | `linear-gradient(160deg, #AB47BC, #8E24AA)` |

## Chart Line Colors

```css
--line-colors: #C8392D, #43A047, #1E88E5, #FF8F00, #8E24AA, #00BCD4;
--bar-track: rgba(0,0,0,0.06);
```

## Typography

| Role | Font |
|------|------|
| heading | `SigmaSerifHead` |
| body | `SigmaSans` |
| serif-text | `SigmaSerifText` |
| mono | `JetBrains Mono` |
| cjk | `Noto Sans CJK SC` |

## Stat Colors

| Stat | Color |
|------|-------|
| hp | `#e05050` |
| damage | `#ff8c42` |
| abilityPower | `#b06cdd` |
| attackSpeed | `#7a8c20` |
| armor | `#d4a830` |
| magicResist | `#4488cc` |
| mana | `#3399ff` |
| range | `#cc7733` |

## Cost Colors

| Cost | Color |
|------|-------|
| 1 | `#808080` |
| 2 | `#11b288` |
| 3 | `#207ac7` |
| 4 | `#c440da` |
| 5 | `#ffb93b` |

## Typography Rules

- **headline-style**: SigmaSerifHead, font-weight 500, tight line-height (0.95-1.1)
- **body-style**: SigmaSans, font-weight 400-500
- **label-style**: SigmaSerifHead, letter-spacing 0.08-0.12em, uppercase, color text-muted
- **stat-value-style**: SigmaSerifHead, font-size 28px, font-weight 500
- **keyword-highlight**: strong, color accent, font-family SigmaSerifHead

## Decoration

clean, minimal — no patterns, rely on typography hierarchy

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-gradient-tech]] — 同类风格对比
