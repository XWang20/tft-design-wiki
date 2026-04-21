---
title: "Theme: Gods"
tags: [reference, theme]
---

# Theme: Gods 深色科幻主题

**类型：** 深色主题（Dark）
**用途：** 科幻/神话感深色风格，深蓝黑背景。

基础通用 token 见 [[design-tokens]]。

## CSS Variables

```css
[data-theme="gods"] {
  /* Background */
  --bg: #0c0e1a;
  --bg-gradient: linear-gradient(175deg, #0c0e1a 0%, #111428 50%, #0a0c16 100%);

  /* Accent */
  --accent-gold: #fbbf24;
  --accent-blue: #06b6d4;

  /* Text */
  --text-primary: #e8e6e3;
  --text-secondary: #9ca3af;
  --text-tertiary: #6b7280;
  --text-muted: #4b5563;

  /* Tier */
  --tier-s: #fbbf24;
  --tier-a: #34d399;
  --tier-b: #22d3ee;
  --tier-c: #94a3b8;

  /* Cost */
  --cost-1: #9ca3af;
  --cost-2: #4ade80;
  --cost-3: #60a5fa;
  --cost-4: #c084fc;
  --cost-5: #fbbf24;

  /* Sparkline / Chart */
  --spark-1: #fbbf24;
  --spark-2: #f472b6;
  --spark-3: #34d399;
  --spark-4: #22d3ee;
  --spark-5: #a78bfa;
  --spark-6: #fb923c;
  --spark-7: #38bdf8;
  --spark-8: #4ade80;
}
```

## 色板

| Token | 色值 | 用途 |
|-------|------|------|
| `--bg` | `#0c0e1a` | 深蓝黑背景 |
| `--accent-gold` | `#fbbf24` | 金色强调 |
| `--accent-blue` | `#06b6d4` | 青蓝强调 |
| `--text-primary` | `#e8e6e3` | 主文字 |
| `--text-secondary` | `#9ca3af` | 副文字 |
| `--text-tertiary` | `#6b7280` | 辅助文字 |
| `--text-muted` | `#4b5563` | 弱化文字 |

## Tier 系统

| Tier | 色值 | 描述 |
|------|------|------|
| S | `#fbbf24` | 金 |
| A | `#34d399` | 翠绿 |
| B | `#22d3ee` | 青蓝 |
| C | `#94a3b8` | 灰蓝 |

## 费用色

| Cost | 色值 |
|------|------|
| 1 | `#9ca3af` |
| 2 | `#4ade80` |
| 3 | `#60a5fa` |
| 4 | `#c084fc` |
| 5 | `#fbbf24` |

## 趋势线/图表色

`#fbbf24` · `#f472b6` · `#34d399` · `#22d3ee` · `#a78bfa` · `#fb923c` · `#38bdf8` · `#4ade80`
