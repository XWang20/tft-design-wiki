---
title: Preflight Checks
created: 2026-04-21
updated: 2026-04-21
type: pitfall
tags: [validation, gotcha, rendering]
---

# Preflight Checks

> 出图前必须跑的检查。每条都是一个曾经漏过的bug。

## 中文字体缺失
**症状**: 中文变成方块/回退到serif
**检查**: 确认MiSans已安装且CSS正确引用
**根因**: Docker/headless环境不自带中文字体

## Emoji豆腐块
**症状**: emoji显示为方块
**检查**: preflight脚本扫描HTML中的emoji并替换为SVG
**根因**: Headless Chromium没有emoji字体

## 图片404
**症状**: 英雄/装备/trait图标不显示
**检查**: CDragon slug是否与tftable slug一致，检查SLUG_MAP
**根因**: [[data-gotchas]]中的slug不一致问题

## 颜色对比度
**症状**: 文字在背景上看不清
**检查**: 浅色背景 + 浅色icon? 需要CSS filter
**根因**: Trait icon默认浅色

## 内容溢出
**症状**: 文字被截断，layout挤压
**检查**: 实际数据下的最长名字测试（"奥瑞利安·索尔" 是6个中文字+标点）
**做法**: 不要缩字号，[[subtraction-first]]

## 数据新鲜度
**症状**: 显示上个patch的数据
**检查**: `/tmp/`缓存的stale检测
**做法**: 出图前强制refresh

## 相关
- [[data-gotchas]] — 完整的数据陷阱清单
- [[subtraction-first]] — 内容溢出的正确应对
