---
title: "Style: Neon Cyber"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, dark]
---

# Neon Cyber

> Dark cyberpunk theme with neon cyan/magenta accents for data-heavy content

**分类**: 暗色 · **ID**: `neon`

## Background

```css
background: linear-gradient(165deg, #0A1628 0%, #0D1B2A 50%, #1B2838 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.04)` |
| `surface-solid` | `#162032` |
| `card-shadow` | `0 4px 24px rgba(0,0,0,0.3)` |
| `card-radius` | `12px` |
| `card-backdrop` | `blur(16px)` |
| `border` | `rgba(34,211,238,0.12)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#E0E8F0` |
| `text-secondary` | `#A0B0C0` |
| `text-muted` | `#607080` |
| `text-hint` | `#405060` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#22D3EE` |
| `accent-gradient` | `linear-gradient(135deg, #22D3EE, #E040FB)` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FFD700` | `rgba(255,215,0,0.12)` | `linear-gradient(160deg, #FFE44D, #FFD700)` |
| A | `#22D3EE` | `rgba(34,211,238,0.10)` | `linear-gradient(160deg, #67E8F9, #06B6D4)` |
| B | `#A78BFA` | `rgba(167,139,250,0.08)` | `linear-gradient(160deg, #C4B5FD, #8B5CF6)` |
| C | `#6B7280` | `rgba(107,114,128,0.08)` | `linear-gradient(160deg, #9CA3AF, #4B5563)` |

## Chart Line Colors

```css
--line-colors: #22D3EE, #E040FB, #FFD700, #34D399, #FB923C, #F472B6;
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

horizontal scan lines at 0.03 opacity, subtle glow on accent elements

## 相关
- [[design-tokens]] — 全局共享token
- [[style-graphite]] — 同类风格对比
- [[style-midnight]] — 同类风格对比
