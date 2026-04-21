---
title: Lessons and Bugs
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [lesson, bug, anti-pattern, best-practice]
sources: [raw/workspace/social-media/LESSONS.md, raw/workspace/image-studio/LESSONS.md]
---

# Lessons and Bugs

做图过程中积累的所有经验教训和bug记录。**这是最关键的操作文档。**

## 核心原则
1. **所有数据来自API，永远不硬编码**
2. **所有中文翻译来自glossary，不凭记忆翻**
3. **重写优于修补**（rewrite > patch）
4. **做减法优于放大字体**（reduce info > enlarge font）

## 数据Bug（最常见）

| Bug | 原因 | 修复 |
|-----|------|------|
| 错误的英雄数据 | 用了错误的数据源/字段 | 统一用data_fetcher |
| Cost显示错误 | 7费英雄API返回cost=5 | 特殊处理7费 |
| 召唤物出现 | cost=11没过滤 | 过滤cost>7 |
| Slug不匹配 | 不同源用不同slug | 建SLUG_MAP |
| 硬编码名字 | 手写了英雄/羁绊名 | 必须从API获取 |
| 翻译错误 | 凭记忆翻译 | 必须用glossary |

## 渲染Bug

| Bug | 原因 | 修复 |
|-----|------|------|
| Emoji豆腐块 | headless Chromium不支持emoji | [[preflight]]替换为SVG |
| 字体太小看不清 | 没遵守最小字号 | 最小14px |
| 图片比例错 | 视口设置不对 | 固定1080×1440 @2x |
| `/tmp/`缓存丢失 | 系统清理了缓存 | 加stale检测 |

## 设计教训

### 字号锁定
- 最小14px，无例外
- 标题70-80px（@1080w）
- 锁定字号比例，不随内容伸缩

### Impeccable设计原则
- 4pt网格对齐
- 左对齐为主
- 不嵌套卡片
- `tabular-nums`对齐数字
- 单一强调色
- 单层渐变

### 暗色主题
**永久禁止**在小红书等平台使用暗色主题。历史教训："那坨黑黑的"被ash否决。

### 强度显示
- 用"表现"不用"强度"
- 数值用小数（如0.72），不用百分比

### 趋势曲线
- 用Catmull-Rom平滑
- 不用折线

## 工作流教训

### Discord发图
必须用Discord API直接curl发送，不能通过普通消息附件。

### 羊刀 = Guinsoo's
使用玩家俗称，不用官方全名。

### "95" → "传说"
中文版用"传说"替代"95"指代传说级单位。

## CSS设计Token标准（@2x）
```css
:root {
  --fs-hero: 80px;
  --fs-h1: 56px;
  --fs-h2: 44px;
  --fs-body: 36px;
  --fs-sm: 28px;
  --fs-xs: 24px;
  /* spacing */
  --sp-xs: 8px;
  --sp-sm: 12px;
  --sp-md: 16px;
  --sp-lg: 24px;
  --sp-xl: 32px;
}
```

## 相关
- [[design-system]] — 设计规范
- [[rendering-pipeline]] — 渲染流程
- [[data-pipeline]] — 数据源规范
- [[content-types]] — 各类型特有的坑
