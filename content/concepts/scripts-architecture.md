---
title: Scripts Architecture
created: 2026-04-21
updated: 2026-04-21
type: concept
tags: [scripts, generation-pipeline, rendering]
sources: []
---

# Scripts Architecture

`social-media/scripts/`下85个Python脚本的架构模式。

## 通用模式
每个脚本都是独立的，遵循相同模式：

```python
# 1. 加载JSON数据
with open("/tmp/strength_trends.json") as f:
    data = json.load(f)

# 2. 构建HTML（f-string拼接）
html = f"""<!DOCTYPE html>
<html><head><style>
  @font-face {{ font-family: 'Outfit'; src: url(data:...) }}
  /* 完整CSS */
</style></head>
<body>
  <!-- 完整页面 -->
</body></html>"""

# 3. Playwright渲染
with sync_playwright() as p:
    browser = p.chromium.launch()
    page = browser.new_page(viewport={"width":1080,"height":1440},
                            device_scale_factor=2)
    page.set_content(html)
    page.screenshot(path="output/xxx.png")
```

## 脚本清单（按类型）

### 阵容类
| 脚本 | 输出 |
|------|------|
| `gen_tierlist_s17.py` + 6变体 | Tier list不同风格 |
| `gen_s_tier_s17.py` | Top 5详情 |
| `gen_all_comps_s17.py` | 全阵容分页 |
| `gen_comp_detail_s17.py` | 单阵容详情（最复杂） |
| `gen_comp_spotlight.py` | 阵容聚焦 |

### 趋势类
| 脚本 | 输出 |
|------|------|
| `gen_meta_shift_s17.py` | 版本变动 |
| `gen_patch_shift.py` | 跨版本对比 |
| `gen_trends_chart.py` | 趋势图 |

### 报告类
| 脚本 | 输出 |
|------|------|
| `gen_weekly_s17.py` | 周报 |
| `gen_daily_s17.py` | 日报 |
| `gen_cover_s17.py` | 封面 |

### 平台特定
| 脚本 | 输出 |
|------|------|
| `gen_xhs_html.py` | 小红书 |
| `gen_boons_thumbnail.py` | YouTube缩略图 |

### 特殊内容
| 脚本 | 输出 |
|------|------|
| `gen_pbe_update.py` + v2-v6 | PBE补丁笔记（6版迭代！） |
| `gen_mort_day*.py` | Mort直播笔记 |
| `gen_s16_review.py` + v2-v4 | S16赛季回顾 |
| `gen_s17_announce.py` + v2-v3 | S17公告 |

### 工具
| 脚本 | 功能 |
|------|------|
| `preflight.py` | [[preflight]] HTML清洗 |
| `tier_thresholds.py` | 动态tier阈值计算 |

## 代码重复问题
**无共享模块**。以下内容在每个脚本中复制粘贴：
- `COST_COLORS = {1:'#808080', 2:'#11b288', 3:'#207ac7', 4:'#c440da', 5:'#ffb93b'}`
- `unit_icon_url()`, `item_icon_url()`, `trait_icon_url()`
- Outfit字体base64数据
- Logo base64编码
- Tier阈值
- Playwright启动代码

## 版本演进
多个脚本有v1-v6的迭代版本（如`gen_pbe_update.py`到v6），反映设计迭代过程。

## 相关
- [[rendering-pipeline]] — 渲染流程
- [[data-pipeline]] — 数据来源
- [[content-types]] — 各类型规格
- [[lessons-and-bugs]] — 脚本开发中的坑
