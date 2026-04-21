---
title: "Style: Glassmorphism"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, mixed]
---

# Glassmorphism

> Frosted glass cards on gradient backgrounds, modern overlay style

**分类**: 混合 · **ID**: `glassmorphism`

## Background

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

## Surface

| Token | Value |
|-------|-------|
| `surface` | `rgba(255,255,255,0.15)` |
| `surface-solid` | `rgba(255,255,255,0.25)` |
| `card-shadow` | `0 8px 32px rgba(0,0,0,0.15)` |
| `card-radius` | `20px` |
| `card-backdrop` | `blur(20px) saturate(180%)` |
| `border` | `rgba(255,255,255,0.20)` |

## Text

| Token | Value |
|-------|-------|
| `text` | `#FFFFFF` |
| `text-secondary` | `rgba(255,255,255,0.85)` |
| `text-muted` | `rgba(255,255,255,0.60)` |
| `text-hint` | `rgba(255,255,255,0.35)` |

## Accent

| Token | Value |
|-------|-------|
| `accent` | `#FFFFFF` |
| `accent-gradient` | `—` |

## Tier Colors

| Tier | Color | Background | Gradient |
|------|-------|------------|----------|
| S | `#FFD700` | `rgba(255,215,0,0.20)` | `—` |
| A | `#FFFFFF` | `rgba(255,255,255,0.15)` | `—` |
| B | `rgba(255,255,255,0.70)` | `rgba(255,255,255,0.08)` | `—` |
| C | `rgba(255,255,255,0.45)` | `rgba(255,255,255,0.04)` | `—` |

## Typography

| Role | Font |
|------|------|
| heading | `Outfit` |
| body | `Outfit` |
| cjk | `Noto Sans CJK SC` |

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]] — 同类风格对比
- [[style-cosmic]] — 同类风格对比
