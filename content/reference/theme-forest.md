---
title: "Theme: Forest"
tags: [reference, theme]
---

# Theme: Forest 森林绿深色主题

**类型：** 深色主题（Dark）
**用途：** 自然/森林感深色风格。

基础通用 token 见 [[design-tokens]]。

## CSS Variables

```css
[data-theme="forest"] {
  /* Background */
  --bg: #0F2A1D;

  /* Card */
  --card-bg: #1A3D2B;
  --card-border: rgba(174, 195, 176, 0.15);

  /* Brand / Accent */
  --brand: #E3EED4;
  --accent-1: #AEC3B0;
  --accent-2: #6B9071;

  /* Text */
  --text-primary: #E3EED4;
  --text-secondary: #6B9071;

  /* Tier */
  --tier-s: #E3EED4;
  --tier-a: #AEC3B0;
  --tier-b: #6B9071;
  --tier-c: #375534;

  /* Sparkline / Chart */
  --spark-1: #E3EED4;
  --spark-2: #AEC3B0;
  --spark-3: #6B9071;
  --spark-4: #93D8A0;
  --spark-5: #FFD740;
  --spark-6: #FF8A65;
  --spark-7: #81D4FA;
  --spark-8: #CE93D8;
}
```

## 色板

| Token | 色值 | 用途 |
|-------|------|------|
| `--bg` | `#0F2A1D` | 深绿背景 |
| `--card-bg` | `#1A3D2B` | 卡片背景 |
| `--card-border` | `rgba(174,195,176,0.15)` | 卡片边框 |
| `--brand` | `#E3EED4` | 品牌/主色（淡绿白） |
| `--accent-1` | `#AEC3B0` | 强调色1（灰绿） |
| `--accent-2` | `#6B9071` | 强调色2（中绿） |
| `--text-primary` | `#E3EED4` | 主文字 |
| `--text-secondary` | `#6B9071` | 辅助文字 |

## Tier 系统

| Tier | 色值 | 描述 |
|------|------|------|
| S | `#E3EED4` | 淡绿白 |
| A | `#AEC3B0` | 灰绿 |
| B | `#6B9071` | 中绿 |
| C | `#375534` | 深绿 |

## 趋势线/图表色

`#E3EED4` · `#AEC3B0` · `#6B9071` · `#93D8A0` · `#FFD740` · `#FF8A65` · `#81D4FA` · `#CE93D8`
