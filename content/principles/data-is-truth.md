---
title: Data is Truth
created: 2026-04-21
updated: 2026-04-21
type: principle
tags: [data, bug, gotcha]
---

# Data is Truth

> 所有数据必须来自API，永远不要硬编码。所有中文翻译必须来自glossary。

这是TFTable做图体系的第一原则，也是被违反最多的原则。

## 为什么这条规则存在

TFT每个patch都在变 — 英雄费用会调整，羁绊会重做，装备会改名。任何硬编码的数据都会在下个patch变成bug。更隐蔽的是：即使当前patch的数据，不同API源之间也有不一致。

## 典型违反案例

**7费英雄返回cost=5**: API设计上7费英雄的cost字段实际返回5（因为5是shop中的最高费用）。直接用API的cost字段显示就会出错。需要特殊处理。

**召唤物cost=11**: 召唤物在数据中cost=11，如果不过滤就会出现在英雄列表里。

**Slug不匹配**: tftable用一套slug，CDragon用另一套。直接拼URL会404。必须维护SLUG_MAP。

**凭记忆翻译**: "蚂蚱"的官方翻译是"玛尔扎哈"，"龙王"是"奥瑞利安·索尔"。凭记忆写永远会出错。

## 推论

- 每个数据字段都要确认来源
- 翻译走glossary，不走记忆
- 新赛季第一次出图要全量验证数据源
- [[data-gotchas]]记录了所有已知的数据陷阱

## 相关
- [[data-gotchas]] — 具体的数据陷阱清单
- [[rewrite-over-patch]] — 为什么推倒重来比修补好
