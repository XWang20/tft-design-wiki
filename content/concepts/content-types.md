---
title: Content Types
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [tierlist, top5, comp-detail, meta-shift, patch-notes, weekly, cover, unit-card, trait-card, comp-guide, content-types]
sources: [raw/workspace/image-studio/LAYOUT_REFERENCE.md]
---

# Content Types

TFTable生产的所有信息图类型及其规格。

## 10种内容类型

### 1. Tier List（阵容梯队）
- 脚本：`gen_tierlist_s17.py`及变体（warm, cosmic, purple, gods, dreamy）
- 内容：所有阵容按S/A/B/C分层，六边形头像
- 多版本风格迭代

### 2. Top 5（S级阵容详情）
- 脚本：`gen_s_tier_s17.py`及变体
- 内容：前5名阵容的完整英雄阵容+装备
- Comp Overview只展示Top 5

### 3. Comp Detail（阵容详细卡）
- 脚本：`gen_comp_detail_s17.py`（最复杂的脚本，611行）
- 内容：单阵容完整信息 — 趋势曲线、英雄+装备、站位、对局数据
- 实时从tftable获取matchup数据

### 4. Meta Shift（版本变动）
- 脚本：`gen_meta_shift_s17.py`
- 内容：上升/下降阵容对比，前后柱状图+delta

### 5. Patch Notes（补丁笔记）
- 多页（5页），1:1画布
- 涵盖：羁绊变更、英雄变更（四宫格布局）、道具、强化符文、bug修复、总结
- 红涨绿跌（红=增强，绿=削弱）

### 6. Weekly Report（周报）
- 脚本：`gen_weekly_s17.py`, `gen_weekly_report.py`等
- 多页（3页）
- 内容：本周阵容变化趋势

### 7. Cover（封面图）
- 脚本：`gen_cover_s17.py`
- 内容：Top 5排名+紫色渐变风格
- 用于社媒帖子第一张图

### 8. Unit Card（英雄卡）
- 画布：1080×auto
- 单层渐变：cost颜色 → `#FAFAF8`
- 内容：属性+技能描述+关键词高亮
- 关键词高亮色：生命值=红，AD=橙，AP=紫，攻速=橄榄，护甲=金，魔抗=蓝

### 9. Trait Card（羁绊卡）
- 画布：1080×1440，多页
- 成员grid用`inline-block`（不是flex）
- 成员固定在底部（`margin-top:auto`）

### 10. Comp Guide（阵容攻略）
- 多页（3页）
- 完整攻略：阵容、装备、站位、打法

## 双语输出
每种内容都生成`_cn.png`和`_en.png`两版：
- 中文版：用"传说"替代"95"（传说级单位）
- 英文版：使用TFTable官方英文名
- 中文字体：MiSans
- 英文字体：Outfit

## 多页规划
| 类型 | 页数 |
|------|------|
| Patch Notes | 5 |
| Comp Guide | 3 |
| Weekly | 3 |
| 其余 | 1 |

## 相关
- [[design-system]] — 所有类型的视觉基础
- [[rendering-pipeline]] — 如何渲染
- [[scripts-architecture]] — 脚本代码架构
