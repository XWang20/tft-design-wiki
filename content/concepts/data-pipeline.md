---
title: Data Pipeline
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [data-pipeline, api, tftable-api, json]
sources: [raw/workspace/image-studio/core/data_fetcher.py]
---

# Data Pipeline

TFT游戏数据从源头到渲染的完整流转。

## 核心原则
> **所有数据必须来自API，永远不要硬编码。所有中文翻译必须来自glossary。**

这是最重要的规则。违反此规则是最常见的bug来源。

## 数据流

```
tftable.cc → curl(带proxy) → /tmp/*.json → 脚本/Image Studio → HTML
```

## 数据源

### 主源：TFTable API
[[tftable-api]]通过解析Next.js页面的`__NEXT_DATA__`获取：
- 阵容列表、详情、统计
- 英雄、羁绊、道具数据
- 每日/每周统计

### 备用源：CDragon
[[cdragon]]用于：
- 图片资源fallback
- PBE新内容

### 本地缓存
| 文件 | 数据 | 过期时间 |
|------|------|---------|
| `/tmp/strength_trends.json` | 强度趋势 | 手动 |
| `/tmp/all_comp_details.json` | 阵容详情 | 手动 |
| `/tmp/all_comp_hex.json` | 阵容站位 | 手动 |
| `/tmp/s17_name_maps.json` | 名称映射 | 手动 |
| `/tmp/cards_latest.json` | 最新卡片 | 手动 |
| `/tmp/tft_set17.html` | Set17数据 | 4h |

## Tier阈值
动态计算（`tier_thresholds.py`），基于gap分析：
- S ≥ 0.70
- A ≥ 0.365
- B ≥ 0.15
- C = 其余

以"shurima"阵容作为B级边界锚点。

## 已知坑
- 7费英雄API返回cost=5（需要特殊处理）
- 召唤物cost=11（需要过滤）
- slug在不同数据源间不一致，需要SLUG_MAP映射
- `/tmp/`文件会被系统清理
- 需要HTTP代理`127.0.0.1:7890`访问API

## 相关
- [[tftable-api]] — 主数据源详情
- [[rendering-pipeline]] — 数据如何变成图片
- [[lessons-and-bugs]] — 数据相关的bug记录
