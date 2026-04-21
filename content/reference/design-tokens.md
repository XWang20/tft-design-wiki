---
title: Design Tokens
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [color, typography, layout, visual-identity]
sources: [social-media/design-tokens.css, image-studio/web/src/index.css]
---

# Design Tokens

## 风格版索引

| 主题 | 类型 | 用途 |
|------|------|------|
| [[theme-warm]] | 浅色 | 小红书/抖音（默认） |
| [[theme-dark]] | 深色 | Twitter/Reddit |
| [[theme-cosmic-light]] | 浅色 | 宇宙淡紫风 |
| [[theme-dreamy]] | 浅色 | 梦幻柔色 |
| [[theme-gods]] | 深色 | 科幻/神话 |
| [[theme-forest]] | 深色 | 森林绿 |
| [[theme-sakura]] | 浅色 | 樱花蓝粉 |
| [[theme-sunset]] | 深色 | 日落沙滩 |

> 查阅型参考。关于**为什么**这样选，看 [[cream-style-evolution]] 和 [[context-over-defaults]]。

## Canvas

| Token | Value | 备注 |
|-------|-------|------|
| `--canvas-w` | `1080px` | 抖音/小红书竖图标准 |
| `--canvas-h` | `1440px` | 3:4比例 |
| `--canvas-scale` | `2` | 实际输出2160×2880 |

## Spacing (4pt Grid)

| Token | Value |
|-------|-------|
| `--space-2xs` | `4px` |
| `--space-xs` | `8px` |
| `--space-sm` | `12px` |
| `--space-md` | `16px` |
| `--space-lg` | `24px` |
| `--space-xl` | `32px` |
| `--space-2xl` | `48px` |
| `--space-page` | `32px` |

**WHY 4pt**: 见 [[subtraction-first]] — 所有间距是4的倍数，视觉节奏一致。

## Typography

**字体**:
- Display/Body: `'Outfit', 'Noto Sans CJK SC', sans-serif`
- 中文正式图: **MiSans**（不是Noto Sans SC — 见 [[cream-style-evolution]] 原因）
- 英文: Outfit（不是Inter — 避免AI味）

**字号 (~1.25 major third)**:

| Token | Value | 用途 |
|-------|-------|------|
| `--text-2xs` | `9px` | hex百分比，脚注小字 |
| `--text-xs` | `11px` | 脚注，caption |
| `--text-sm` | `13px` | body small，trait标签 |
| `--text-base` | `15px` | body，名字 |
| `--text-lg` | `17px` | 卡片标题 |
| `--text-xl` | `24px` | 分区标题 |
| `--text-2xl` | `32px` | KPI数字 |
| `--text-3xl` | `40px` | 页面标题 |

**⚠️ 最小14px** — 低于此在手机上不可读。见 [[subtraction-first]]。

**Weights**: 400 (regular), 600 (medium), 700 (bold), 900 (black)

## Colors — Warm Theme (小红书/抖音)

### Background
| Token | Value |
|-------|-------|
| `--bg-start` | `#FFF8F0` (cream) |
| `--bg-mid` | `#FFE8D6` (apricot) |
| `--bg-end` | `#FFECD2` (peach) |
| `--bg-gradient` | `linear-gradient(160deg, ...)` |

### Text (brown-tinted neutrals)
| Token | Value | 用途 |
|-------|-------|------|
| `--text-primary` | `#3E2723` | 标题，核心数据 |
| `--text-secondary` | `#5D4037` | body，标签 |
| `--text-muted` | `#8D6E63` | caption，KPI标签 |
| `--text-faint` | `#BCAAA4` | 脚注，时间戳 |

### Surface (glassmorphism卡片)
| Token | Value |
|-------|-------|
| `--surface-card` | `rgba(255,255,255,0.6)` |
| `--surface-card-solid` | `rgba(255,255,255,0.82)` |
| `--surface-card-blur` | `8px` |

### Accents
| Token | Value | 用途 |
|-------|-------|------|
| `--accent` | `#FF8F00` | 品牌橙，CTA |
| `--accent-light` | `#FFB74D` | hover，装饰 |
| `--accent-blue` | `#1E88E5` | 次要数据 |
| `--accent-red` | `#E53935` | 下跌/负面 |
| `--accent-green` | `#43A047` | 上涨/正面 |

## Colors — Dark Theme (Twitter/Reddit)

| Token | Value |
|-------|-------|
| `--bg-start` | `#0A0B12` |
| `--surface-card` | `#161925` |
| `--text-primary` | `#E8E6E3` |
| `--accent` | `#E0B55A` |

**⚠️** 暗色主题仅用于Twitter/Reddit。小红书/抖音永ban暗色。见 [[no-dark-theme]]。

## Tier Colors (SABC)

### Warm Theme
| Tier | Flat | Gradient |
|------|------|----------|
| S | `#FF8F00` | `linear-gradient(160deg, #FFD180, #FF8F00)` |
| A | `#43A047` | `linear-gradient(160deg, #A5D6A7, #43A047)` |
| B | `#1E88E5` | `linear-gradient(160deg, #90CAF9, #1E88E5)` |
| C | `#8E24AA` | `linear-gradient(160deg, #CE93D8, #8E24AA)` |

### Dark Theme
S `#E0B55A` · A `#38C97B` · B `#3E6FE0` · C `#A78BFA`

### Thresholds
S ≥ 0.70 · A ≥ 0.365 · B ≥ 0.15 · C < 0.15

**⚠️** 阈值不能硬编码 — 见 [[data-gotchas]] tier阈值条目。

## Unit Cost Colors

| Cost | design-tokens.css | 暗色变体 |
|------|-------------------|---------|
| 1 | `#808080` | `#9ca3af` |
| 2 | `#11b288` | `#4ade80` |
| 3 | `#207ac7` | `#60a5fa` |
| 4 | `#c440da` | `#c084fc` |
| 5 | `#ffb93b` | `#fbbf24` |

## Trait Tier Colors
| Tier | Color | Name |
|------|-------|------|
| 1 | `#8B7355` | bronze |
| 2 | `#B0BEC5` | silver |
| 3 | `#E0B55A` | gold |
| 4 | `#E0B55A` | chromatic |

## Buff/Nerf Colors (红涨绿跌)
| Type | Color |
|------|-------|
| Buff ▲ | `#c62828` |
| Nerf ▼ | `#2e7d32` |

## Component Tokens
| Token | Value |
|-------|-------|
| `--card-radius` | `14px` |
| `--card-padding` | `14px 16px` |
| `--hex-size` | `66px` |
| `--unit-icon` | `72px` |
| `--item-icon` | `20px` |
| `--trait-icon` | `16px` |

## 备选风格
Image Studio有9个备选theme JSON（sunset, tarot_gold, glassmorphism, gradient_tech, bold_editorial, heatmap, serif_quote, neon等），各有独立的tier/accent/bg配色。详见 `image-studio/styles/` 目录。

## 相关
- [[cream-style-evolution]] — 为什么选这些颜色
- [[context-over-defaults]] — 为什么选这些字体
- [[subtraction-first]] — spacing和最小字号的原则依据
