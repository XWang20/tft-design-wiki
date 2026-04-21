---
title: CDragon
created: 2026-04-21
updated: 2026-04-21
type: entity
tags: [cdragon, data-pipeline]
sources: []
---

# CDragon

Community Dragon，TFT/LoL社区数据源。作为[[tftable-api]]的备用图片资源。

## 用途
- 当tftable CDN图片不可用时的fallback
- 中文翻译对照来源
- PBE（测试服）新内容的图片来源

## CDN路径
- 英雄头像: `raw.communitydragon.org/pbe/plugins/...`
- 道具图标: 类似路径
- 羁绊图标: 类似路径

## 注意
- CDragon的slug/路径不总是和tftable一致，需要SLUG_MAP映射
- 优先使用tftable CDN，CDragon只作fallback

## 相关
- [[tftable-api]] — 主数据源
- [[data-pipeline]] — 数据流
