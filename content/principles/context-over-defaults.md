---
title: Context Over Defaults
created: 2026-04-21
updated: 2026-04-21
type: principle
tags: [visual-identity, anti-pattern, ai-generation]
---

# Context Over Defaults

> 每个设计决策都应该能追溯到具体的品牌、受众或内容语境。

## 从Impeccable学到的

Impeccable的核心洞察：LLM生成的UI之所以看起来"AI味"，是因为模型总是选统计上最常见的默认值。Inter字体、紫色渐变、圆角卡片、深色模式 — 这些不是因为它们好，而是因为训练数据里它们出现最多。

同样的道理适用于TFT信息图：

### 不要因为"好看"选风格
Cream主题不是因为暖色"好看"才选的。是因为：
1. 小红书/抖音的受众偏好明亮、干净的视觉
2. 竞品（tactics.tools, lolchess）都用暗色，差异化
3. ash（设计负责人）明确否决了暗色（"那坨黑黑的"）

### 不要因为"流行"选字体
MiSans不是随便选的。是因为：
1. 中文渲染清晰度在信息图尺寸下优于Noto Sans SC
2. 免费商用
3. 数字等宽（tabular figures原生支持）

### AI生成时的特别警惕
[[image-studio]]用LLM生成HTML。模型的第一反应永远是Inter + 紫色渐变 + 暗色。系统提示词里有~500行规则就是为了对抗这个倾向。但规则永远不够 — 关键是每次生成后问：**"这看起来像AI做的吗？如果是，哪里暴露了？"**

## 相关
- [[no-dark-theme]] — 一个具体的context-driven决策
- [[ai-vs-scripts]] — AI生成需要更多设计约束
