---
title: Rendering Pipeline
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [rendering, generation-pipeline, playwright-render]
sources: [raw/workspace/image-studio/core/renderer.py, raw/workspace/social-media/scripts/preflight.py]
---

# Rendering Pipeline

从数据到最终PNG的完整流程。

## 流程

```
数据(JSON) → HTML生成 → Preflight清洗 → Playwright渲染 → PNG输出
```

### Step 1: 数据准备
- [[data-pipeline]]获取JSON数据到`/tmp/`
- 或者[[image-studio]]的data_fetcher实时获取

### Step 2: HTML生成
两种方式：
1. **脚本方式**（social-media/scripts/）: Python f-string拼接HTML，每个脚本独立
2. **AI方式**（[[image-studio]]）: LLM根据设计规范生成完整HTML

### Step 3: Preflight清洗
[[preflight]]脚本处理：
- Emoji → SVG替换
- 图片onerror注入
- 字体fallback CSS注入
- 未知Unicode字符检测

### Step 4: Playwright渲染
[[playwright-renderer]]执行：
- 设置1080×1440视口，2x缩放
- 注入字体（base64 @font-face）
- 截图（检测是否需要多页）
- 输出PNG到指定路径

## 字体嵌入方式
- **Outfit**: base64 woff2直接嵌入HTML的`<style>`标签
- **MiSans**: CDN加载
- **Sigma系列**: renderer.py中注入

## 图片资源URL
| 类型 | CDN路径 |
|------|---------|
| 英雄头像 | `tftable.cc/set17/avatar-webp/{uid}.webp` |
| 道具图标 | `tftable.cc/set17/item-webp/{iid}.webp` |
| 羁绊图标 | `tftable.cc/set17/trait-webp/{tid}.webp` |
| 强化符文 | 类似路径 |

## 脚本方式的共享模式
每个脚本都复制粘贴了以下内容（无共享模块）：
- `COST_COLORS` 字典
- `unit_icon_url()`, `item_icon_url()`, `trait_icon_url()` 函数
- Tier阈值逻辑
- Logo base64编码

## 已知问题
- `/tmp/`缓存会被系统清理，需要重新获取
- 脚本间大量代码重复，无共享utility模块
- 字体base64使脚本文件巨大（gen_xhs_html.py约180KB）

## 相关
- [[design-system]] — 视觉规范
- [[image-studio]] — AI生成方式
- [[data-pipeline]] — 数据来源
- [[content-types]] — 各类型渲染细节
