---
title: Image Studio
created: 2026-04-21
updated: 2026-04-21
type: entity
tags: [image-studio, server, generation-pipeline]
sources: [raw/workspace/image-studio/README.md, raw/workspace/image-studio/PRD.md]
---

# Image Studio

AI驱动的TFT信息图生成器。核心理念：**不是模板引擎**，每次由LLM（Claude/GPT/Gemini）生成全新HTML，Playwright渲染为PNG。

## 架构

```
Browser (React+Tailwind) → FastAPI Backend → LLM API (via LiteLLM) + Playwright
```

- 后端：FastAPI，端口8765，提供REST API + SSE流式生成 + WebSocket
- 前端：React + Vite + Tailwind，打包后由FastAPI serve
- 渲染：[[playwright-renderer]] 将HTML转PNG
- AI：通过LiteLLM proxy（localhost:4141）调用多模型
- 部署：自托管 + [[cloudflare-tunnel]]

## 可用模型
- `claude-sonnet-4.6`（默认）
- `claude-opus-4.6`
- `gpt-5.4`
- `gemini-3.1-pro`, `gemini-3-flash`

## V2 三阶段流程
1. **Research & Confirm** — 获取数据，生成skeleton，用户确认
2. **Generate & QA** — LLM生成HTML，自动QA检查
3. **Feedback & Learn** — 用户反馈，lessons写入memory

## 系统提示词
`claude_client.py`中有~500行系统提示，包含：
- 完整[[design-system]]
- 所有[[lessons-and-bugs]]
- 10种内容类型的HTML参考结构
- 18条关键规则

## API端点（V1）
| 端点 | 功能 |
|------|------|
| POST `/api/generate` | 生成信息图 |
| POST `/api/generate-stream` | SSE流式生成 |
| POST `/api/edit` | 编辑已有HTML |
| GET `/api/preview/{id}` | 预览 |
| GET `/api/export/{id}` | 导出PNG |

## 相关
- [[rendering-pipeline]] — 渲染细节
- [[data-pipeline]] — 数据获取
- [[design-system]] — 设计规范
- [[lessons-and-bugs]] — 踩坑记录
