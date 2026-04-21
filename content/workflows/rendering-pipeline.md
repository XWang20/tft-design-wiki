---
title: Rendering Pipeline
created: 2026-04-21
updated: 2026-04-21
type: workflow
tags: [rendering, scripts, architecture]
---

# Rendering Pipeline

> 从数据到最终图片的完整路径。

## 核心流程

```
Data Source (tftable API)
    ↓
data_fetcher.py — 获取、缓存、预处理
    ↓
[脚本模式] Python脚本 → f-string拼HTML
[AI模式] Image Studio → LLM生成HTML
    ↓
Playwright headless Chromium → 截图
    ↓
（可选）后处理 — 拼图、水印
    ↓
输出 .png
```

## 两条路径

### 脚本路径
`scripts/*.py` → 每个脚本对应一种内容类型。数据从`data_fetcher`获取，HTML通过f-string模板生成。

优点：完全可控，一致性高
缺点：85+脚本，大量重复代码

### Image Studio路径
`image-studio/` → Express服务器 + LLM。发送数据 + 设计规范，LLM返回完整HTML。

优点：灵活，新类型无需写代码
缺点：需要~500行系统提示词，QA成本高

## Playwright配置要点
- viewport宽度1080px（抖音/小红书竖图标准）
- 高度auto，按内容撑开
- `deviceScaleFactor: 2` 输出2x分辨率
- 字体：必须预装MiSans + Outfit

## 相关
- [[ai-vs-scripts]] — 两种路径的选择依据
- [[preflight]] — 截图前的检查
