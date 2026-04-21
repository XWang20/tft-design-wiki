---
title: Preflight
created: 2026-04-21
updated: 2026-04-21
type: entity
tags: [preflight, rendering]
sources: [raw/workspace/social-media/scripts/preflight.py]
---

# Preflight

HTML渲染前的自动清洗脚本。解决headless Chromium无法渲染emoji等问题。

## 功能
1. **Emoji替换** — 将Unicode emoji替换为SVG图片
2. **图片onerror注入** — 给所有`<img>`加`onerror="this.style.display='none'"`
3. **字体安全CSS** — 注入字体fallback
4. **未知Unicode检测** — 捕获会渲染成豆腐块的字符

## 使用
在[[playwright-renderer]]渲染前调用，确保HTML可以干净渲染。

## 相关
- [[rendering-pipeline]] — preflight在流程中的位置
- [[lessons-and-bugs]] — emoji是常见坑
