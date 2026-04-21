---
title: Bilingual Content Workflow
created: 2026-04-21
updated: 2026-04-21
type: workflow
tags: [bilingual, workflow, translation]
---

# Bilingual Content Workflow

> 每种内容类型都出中英双版。

## 流程

```
1. 获取英文数据（API原始数据）
2. 生成英文版图片
3. 翻译关键字段（glossary驱动，不是全文翻译）
4. 生成中文版图片
5. 导出两组图片
```

## 翻译规则

### 必须翻译
- 英雄名、羁绊名、装备名 → 查glossary
- 标题、副标题
- 固定UI文案（"Top 5 Comps" → "阵容推荐Top5"）

### 不翻译
- 数字、百分比
- 英文缩写保留（AD, AP, BIS等）
- 作者署名

### 特殊处理
- "95" → 中文版替换为"传说"（Legendaries的中文称呼）
- "表现"不是"强度"（用户偏好）
- 英文版用TFTable官方英文名，不自己翻译

### 翻译顺序
永远是英文版先，中文版后。因为API数据本身是英文的，减少一次翻译。

## 相关
- [[data-is-truth]] — 翻译走glossary不走记忆
- [[data-gotchas]] — 翻译陷阱
