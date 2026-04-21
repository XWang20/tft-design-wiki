---
title: Data Gotchas
created: 2026-04-21
updated: 2026-04-21
type: pitfall
tags: [data, bug, gotcha, tft]
---

# Data Gotchas

TFT数据源中所有已知的陷阱。每条都是一个真实的bug。

## API数据陷阱

### 7费英雄cost=5
**发现者**: 出图时英雄费用显示错误
**原因**: tftable API中7费英雄的cost字段返回5（shop最高费用）
**修复**: 特殊处理，单独判断7费单位
**教训**: 不要假设API字段的语义

### 召唤物cost=11
**发现者**: 英雄列表中出现奇怪的单位
**原因**: 召唤物在数据中用cost=11标记
**修复**: 过滤cost>7的实体
**教训**: 永远检查数据边界

### Slug不一致
**发现者**: 图片404
**原因**: tftable用`nunu-willump`，CDragon用`nunu`；trait slug也有不同
**修复**: 维护SLUG_MAP映射表
**教训**: 跨源数据不要假设ID一致

### builds字段的陷阱
**发现者**: 装备显示错误
**原因**: `builds`有多种字段 — `items`, `itemIds`, `components`含义不同
**教训**: 读API文档，不猜字段含义。容易搞混的字段要记录。

### Tier阈值不能硬编码
**发现者**: 新patch后tier分布不合理
**原因**: 强度分布每patch变化，硬编码阈值会失效
**修复**: `tier_thresholds.py`动态计算，用gap分析法，以特定阵容（shurima）作为B级锚点
**教训**: 统计边界必须动态计算

### 强度score算法
```
score = perf * (0.6 + 0.4 * min(sqrt(games/15), 1.0))
```
游戏数少的阵容要降权。不是简单的win rate排序。

## 渲染陷阱

### Emoji = 豆腐块
**原因**: headless Chromium没有emoji字体
**修复**: [[preflight]]脚本将emoji替换为SVG
**教训**: 在headless环境测试所有特殊字符

### /tmp/缓存消失
**原因**: 系统清理临时目录
**修复**: data_fetcher加stale检测，过期自动重新获取
**教训**: 不要依赖/tmp/的持久性

### trait icon在浅色背景上不可见
**原因**: trait icon默认是白色/浅色
**修复**: CSS filter `brightness(0.35)` 让icon在浅色背景上可见
**教训**: 图片资源的颜色不要假设，要测试在目标背景上的效果

## 翻译陷阱

### 不存在的官方翻译
| 俗称 | 官方翻译 | 容易写错 |
|------|---------|---------|
| 蚂蚱 | 玛尔扎哈 | 蚂蚱/马尔扎哈 |
| 龙王 | 奥瑞利安·索尔 | 龙王 |
| 羊刀 | 鬼索的狂暴之刃 | 直接写"羊刀" |

**规则**: 正式图用官方翻译，社媒文案可用俗称。翻译永远查glossary。

## 相关
- [[data-is-truth]] — 为什么这些陷阱重要
- [[rendering-pipeline]] — 渲染相关陷阱的上下文
