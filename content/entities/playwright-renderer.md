---
title: Playwright Renderer
created: 2026-04-21
updated: 2026-04-21
type: entity
tags: [playwright-render, rendering]
sources: [raw/workspace/image-studio/core/renderer.py]
---

# Playwright Renderer

所有TFTable信息图的最终渲染器。HTML → PNG 的核心。

## 规格
- **视口**: 1080×1440
- **设备缩放**: 2x（输出2160×2880）
- **浏览器**: Chromium headless
- **字体注入**: Sigma字体系列（SigmaSerif/SigmaSans）通过base64 @font-face注入

## 多页支持
检测内容高度 > 视口高度时，自动分页截图：
- 检测 `.scrollHeight`
- 按视口高度分割
- 输出 `v0_page0.png`, `v0_page1.png`, ...

## 单例模式
`Renderer`类是单例，避免重复启动浏览器。

## 两种渲染方法
- `render_html_to_png(html, path)` — 保存到磁盘
- `render_html_to_bytes(html)` — 返回bytes（用于API响应）

## Playwright环境变量
`PLAYWRIGHT_BROWSERS_PATH=/home/xing/.cache/ms-playwright`

## 相关
- [[image-studio]] — 调用渲染器的主系统
- [[rendering-pipeline]] — 完整渲染流程
- [[preflight]] — 渲染前HTML清洗
