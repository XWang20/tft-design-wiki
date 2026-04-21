---
title: "Theme: Sakura"
tags: [reference, theme]
---

# Theme: Sakura 樱花蓝粉浅色主题

**类型：** 浅色主题（Light）
**用途：** 樱花粉+蓝色点缀的浅色风格。

基础通用 token 见 [[design-tokens]]。

## CSS Variables

```css
[data-theme="sakura"] {
  /* Background */
  --bg: #FDF5F7;

  /* Card */
  --card-bg: #F2DCDB;
  --card-border: rgba(108, 8, 32, 0.08);

  /* Brand / Accent */
  --brand: #6C0820;
  --accent-2: #5A86CB;

  /* Text */
  --text-primary: #2A1A24;
  --text-secondary: #8A7A9A;

  /* Tier */
  --tier-s: #6C0820;
  --tier-a: #5A86CB;
  --tier-b: #F2AEBC;
  --tier-c: #C8C0D0;

  /* Sparkline / Chart */
  --spark-1: #6C0820;
  --spark-2: #5A86CB;
  --spark-3: #A3284A;
  --spark-4: #3D5D91;
  --spark-5: #E87AA4;
  --spark-6: #FF6F00;
  --spark-7: #00897B;
  --spark-8: #7B1FA2;
}
```

## 色板

| Token | 色值 | 用途 |
|-------|------|------|
| `--bg` | `#FDF5F7` | 淡粉白背景 |
| `--card-bg` | `#F2DCDB` | 卡片背景（粉调） |
| `--card-border` | `rgba(108,8,32,0.08)` | 卡片边框 |
| `--brand` | `#6C0820` | 品牌色（深红） |
| `--accent-2` | `#5A86CB` | 蓝色强调 |
| `--text-primary` | `#2A1A24` | 主文字（深紫棕） |
| `--text-secondary` | `#8A7A9A` | 辅助文字 |

## Tier 系统

| Tier | 色值 | 描述 |
|------|------|------|
| S | `#6C0820` | 深红 |
| A | `#5A86CB` | 蓝 |
| B | `#F2AEBC` | 浅粉 |
| C | `#C8C0D0` | 灰紫 |

## 趋势线/图表色

`#6C0820` · `#5A86CB` · `#A3284A` · `#3D5D91` · `#E87AA4` · `#FF6F00` · `#00897B` · `#7B1FA2`
