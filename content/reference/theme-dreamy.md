---
title: "Theme: Dreamy"
tags: [reference, theme]
---

# Theme: Dreamy 梦幻柔色主题

**类型：** 浅色主题（Light）
**用途：** 柔和梦幻风格，浅蓝紫渐变背景。

基础通用 token 见 [[design-tokens]]。

## CSS Variables

```css
[data-theme="dreamy"] {
  /* Background */
  --bg-gradient: linear-gradient(175deg, #f0eaff 0%, #e8f0ff 30%, #f5f0ff 60%, #eae4f8 100%);

  /* Accent */
  --accent-gold: #e67e5a;
  --accent-blue: #70a8c8;

  /* Text */
  --text-primary: #3a2e50;
  --text-secondary: #5a4e70;
  --text-tertiary: #8a80a0;
  --text-muted: #b0a8c0;

  /* Tier */
  --tier-s: #f0a050;
  --tier-a: #7ec8b8;
  --tier-b: #88b4e0;
  --tier-c: #b0b8c4;

  /* Cost */
  --cost-1: #a0aab8;
  --cost-2: #60c8a0;
  --cost-3: #70a8e0;
  --cost-4: #b888d8;
  --cost-5: #e8a850;

  /* Sparkline / Chart */
  --spark-1: #f0a050;
  --spark-2: #e88098;
  --spark-3: #a0b0e8;
  --spark-4: #70c8b8;
  --spark-5: #d0a0e0;
  --spark-6: #f0c060;
  --spark-7: #80c8e8;
  --spark-8: #c890d8;
}
```

## 色板

| Token | 色值 | 用途 |
|-------|------|------|
| `--accent-gold` | `#e67e5a` | 暖橘强调 |
| `--accent-blue` | `#70a8c8` | 柔蓝强调 |
| `--text-primary` | `#3a2e50` | 主文字 |
| `--text-secondary` | `#5a4e70` | 副文字 |
| `--text-tertiary` | `#8a80a0` | 辅助文字 |
| `--text-muted` | `#b0a8c0` | 弱化文字 |

## Tier 系统

| Tier | 色值 | 描述 |
|------|------|------|
| S | `#f0a050` | 暖橘 |
| A | `#7ec8b8` | 薄荷绿 |
| B | `#88b4e0` | 柔蓝 |
| C | `#b0b8c4` | 浅灰 |

## 费用色

| Cost | 色值 |
|------|------|
| 1 | `#a0aab8` |
| 2 | `#60c8a0` |
| 3 | `#70a8e0` |
| 4 | `#b888d8` |
| 5 | `#e8a850` |

## 趋势线/图表色

`#f0a050` · `#e88098` · `#a0b0e8` · `#70c8b8` · `#d0a0e0` · `#f0c060` · `#80c8e8` · `#c890d8`
