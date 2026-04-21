---
title: "Theme: Cosmic Light"
tags: [reference, theme]
---

# Theme: Cosmic Light 淡紫主题

**类型：** 浅色主题（Light）
**用途：** 宇宙/星空感浅色风格，带星星粒子装饰。

基础通用 token 见 [[design-tokens]]。

## CSS Variables

```css
[data-theme="cosmic-light"] {
  /* Background */
  --bg-gradient: linear-gradient(175deg, #f8f4ff 0%, #f0e8ff 20%, #f5efff 45%, #ede4fb 70%, #f8f2ff 100%);

  /* Accent */
  --accent-gold: #d97706;
  --accent-purple: #8b5cf6;

  /* Text */
  --text-primary: #2d1b4e;
  --text-secondary: #4a3370;
  --text-tertiary: #7c6a9a;
  --text-muted: #a99bc0;

  /* Card */
  --card-bg: rgba(255, 255, 255, 0.65);
  --card-backdrop: blur(8px);
  --card-border: 1px solid rgba(140, 100, 200, 0.12);
  --card-left-border: 4px solid #8b5cf6;

  /* Top bar */
  --top-bar: linear-gradient(90deg, #f59e0b, #8b5cf6);

  /* Tier */
  --tier-s: #fbbf24;
  --tier-a: #a78bfa;
  --tier-b: #60a5fa;
  --tier-c: #9ca3af;

  /* Cost */
  --cost-1: #9ca3af;
  --cost-2: #4ade80;
  --cost-3: #60a5fa;
  --cost-4: #c084fc;
  --cost-5: #fbbf24;

  /* Sparkline / Chart */
  --spark-1: #fbbf24;
  --spark-2: #f472b6;
  --spark-3: #a78bfa;
  --spark-4: #60a5fa;
  --spark-5: #34d399;
  --spark-6: #fb923c;
  --spark-7: #38bdf8;
  --spark-8: #e879f9;
}
```

## 色板

| Token | 色值 | 用途 |
|-------|------|------|
| `--bg-gradient` | `#f8f4ff → #f0e8ff → #f5efff → #ede4fb → #f8f2ff` | 175° 淡紫渐变背景 |
| `--accent-gold` | `#d97706` | 金色强调 |
| `--accent-purple` | `#8b5cf6` | 紫色强调 |
| `--text-primary` | `#2d1b4e` | 深紫主文字 |
| `--text-secondary` | `#4a3370` | 中紫副文字 |
| `--text-tertiary` | `#7c6a9a` | 浅紫辅助 |
| `--text-muted` | `#a99bc0` | Footer 文字 |
| `--card-bg` | `rgba(255,255,255,0.65)` | 磨砂玻璃卡片 |
| `--card-left-border` | `#8b5cf6` | 卡片左侧紫色边框 |
| `--top-bar` | `#f59e0b → #8b5cf6` | 顶部金紫渐变条 |

## Tier 系统

| Tier | 色值 | 描述 |
|------|------|------|
| S | `#fbbf24` | 金 |
| A | `#a78bfa` | 紫 |
| B | `#60a5fa` | 蓝 |
| C | `#9ca3af` | 灰 |

## 费用色

| Cost | 色值 |
|------|------|
| 1 | `#9ca3af` |
| 2 | `#4ade80` |
| 3 | `#60a5fa` |
| 4 | `#c084fc` |
| 5 | `#fbbf24` |

## 趋势线/图表色

`#fbbf24` · `#f472b6` · `#a78bfa` · `#60a5fa` · `#34d399` · `#fb923c` · `#38bdf8` · `#e879f9`
