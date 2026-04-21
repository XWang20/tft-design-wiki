---
title: Script Generation vs AI Generation
created: 2026-04-21
updated: 2026-04-21
type: comparison
tags: [scripts, image-studio, generation-pipeline, comparison]
sources: [raw/workspace/social-media/PRD_IMAGE_TOOL.md, raw/workspace/social-media/PRD_IMAGE_STUDIO_V2.md]
---

# Script Generation vs AI Generation

两种信息图生成方式的对比。

## 对比

| 维度 | 脚本方式 | AI方式 (Image Studio) |
|------|---------|----------------------|
| **代码位置** | `social-media/scripts/` | `image-studio/` |
| **HTML生成** | Python f-string拼接 | LLM生成完整HTML |
| **灵活性** | 固定模板，改样式要改代码 | 每次生成全新HTML |
| **一致性** | 高（同脚本输出一致） | 需要QA自检 |
| **开发速度** | 快（复制改改） | 快（描述即可） |
| **维护成本** | 高（85个独立脚本，大量重复） | 低（规则在system prompt） |
| **数据集成** | 手动读JSON | data_fetcher自动获取 |
| **多模型** | N/A | Claude/GPT/Gemini |
| **迭代** | 改代码重跑 | 对话式编辑 |
| **成本** | 0（本地运行） | API调用费用 |

## 历史演进
1. **Phase 1**: 纯脚本方式，每种内容一个`.py`文件
2. **Phase 2**: PRD_IMAGE_TOOL.md — 计划做模板引擎（Style × Template × Data），未完全实现
3. **Phase 3**: PRD_IMAGE_STUDIO_V2.md — AI原生方式，Claude生成HTML

## 当前状态
两种方式并存：
- 稳定的、高频的内容类型用脚本（tier list, comp detail等）
- 新类型、一次性内容用Image Studio

## 相关
- [[image-studio]] — AI方式的实体页
- [[scripts-architecture]] — 脚本方式的架构
- [[rendering-pipeline]] — 两者共享的渲染层
