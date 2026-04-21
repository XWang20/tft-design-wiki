---
title: Subtraction First
created: 2026-04-21
updated: 2026-04-21
type: principle
tags: [layout, anti-pattern, visual-identity]
---

# Subtraction First

> 信息图的问题几乎都是"太多"而不是"太少"。

## Impeccable设计原则在TFT做图中的应用

从Impeccable skill学到的核心：**每个元素都必须有存在的理由。** 在TFT信息图的语境下：

### 不嵌套卡片
卡片里套卡片是视觉噪音。一层容器足够。

### 4pt网格对齐
所有间距是4的倍数。不是8，不是任意数。4pt网格让眼睛舒服但你说不出为什么。

### 左对齐为主
居中对齐看起来"设计感"更强，但信息密集的图表读起来更累。左对齐让眼睛有固定的起点。

### tabular-nums
数字列必须等宽对齐。`font-variant-numeric: tabular-nums`。没有这个，0.72和0.8看起来不在同一列。

### 单一强调色
一张图只有一个强调色。如果什么都在强调，就什么都没在强调。

### 单层渐变
背景最多一层渐变。两层以上的渐变 = 视觉混乱。

### 最小14px
这是底线。低于14px在手机上完全看不清。与其缩小字号塞更多内容，不如砍内容。

## 相关
- [[rewrite-over-patch]] — 当减法不够时，推倒重来
- [[no-dark-theme]] — 减法思维的一个具体决策
