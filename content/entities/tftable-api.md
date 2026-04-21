---
title: TFTable API
created: 2026-04-21
updated: 2026-04-21
type: entity
tags: [tftable-api, api, data-pipeline]
sources: [raw/workspace/image-studio/core/data_fetcher.py]
---

# TFTable API

tftable.cc的Next.js数据源。通过解析`__NEXT_DATA__` JSON获取TFT游戏数据。

## 数据获取方式
从HTML页面中提取`__NEXT_DATA__`脚本标签中的JSON：
```python
curl tftable.cc/zh/comps → parse __NEXT_DATA__ → JSON
```

## 本地缓存
数据缓存到`/tmp/`，超过4小时自动刷新：

| 缓存文件 | 来源页面 |
|----------|---------|
| `/tmp/tft_set17.html` | tftable.cc set17数据 |
| `/tmp/tftable_meta.html` | 元数据统计 |
| `/tmp/tftable_comps.html` | 阵容列表 |
| `/tmp/tftable_daily.html` | 每日数据 |
| `/tmp/tftable_entities.json` | 实体数据 |
| `/tmp/tftable_comp_cards.json` | 阵容卡片 |

## 可用函数
- `fetch_comp_list()` — 全部英雄
- `fetch_traits()` — 全部羁绊
- `fetch_meta_stats()` — 元数据统计
- `fetch_comp_stats()` — 阵容统计
- `fetch_daily_stats()` — 每日数据
- `fetch_comp_detail(slug)` — 单阵容详情
- `fetch_composition_list()` — 阵容列表

## 多语言
支持 zh/en/ko/fr/ja

## 需要代理
请求需要通过HTTP代理`127.0.0.1:7890`

## 相关
- [[data-pipeline]] — 数据如何流入渲染
- [[image-studio]] — 使用data_fetcher的主系统
- [[cdragon]] — 图片资源备用源
