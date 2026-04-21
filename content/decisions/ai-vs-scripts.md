---
title: AI Generation vs Templates
created: 2026-04-21
updated: 2026-04-21
type: decision
tags: [ai-generation, scripts, architecture, iteration]
---

# AI Generation vs Templates

> 两种做图方式并存，各有适用场景。

## 演进历史

### Phase 1: 纯脚本（2026年3月前）
每种内容类型一个Python脚本。f-string拼HTML，Playwright截图。
- 优点：一致性高，成本零
- 痛点：85个脚本，大量复制粘贴，改风格要改每个脚本

### Phase 2: 模板引擎构想（PRD_IMAGE_TOOL）
计划做 Style × Template × Data = Image 的模板系统。
- 没完全实现 — 发现模板的灵活性不够

### Phase 3: AI原生（Image Studio）
核心洞察：**不是模板引擎，每次由LLM生成全新HTML。**

Claude/GPT根据设计规范 + 数据生成完整HTML页面，Playwright渲染。
- 优点：灵活，新内容类型不需要写代码
- 痛点：需要~500行系统提示词约束质量，QA成本高

## 当前策略

| 场景 | 方式 | 理由 |
|------|------|------|
| 高频固定内容（tier list, comp detail） | 脚本 | 一致性比灵活性重要 |
| 新类型、一次性内容 | Image Studio | 不值得写专门脚本 |
| 实验新风格 | Image Studio | 快速迭代 |
| 正式发布的系列图 | 脚本 | 品牌一致性 |

## 未解决的问题
- 脚本间85处代码重复（COST_COLORS、icon URL helpers等）
- Image Studio的QA自检不够可靠（曾输出编造的数据）
- 没有共享utility模块

## 相关
- [[context-over-defaults]] — AI生成需要对抗默认审美
- [[rendering-pipeline]] — 两种方式共享的渲染层
