---
title: "Style: Minimal Spec"
created: 2026-04-21
updated: 2026-04-21
type: reference
tags: [visual-identity, color, light]
---

# Minimal Spec

> Swiss grid, technical document, precise and clean

**分类**: 亮色 · **ID**: `minimal_spec`

## Background

<div style="width:100%;height:60px;border-radius:8px;background:#FFFFFF;border:1px solid rgba(128,128,128,0.15);margin:8px 0;"></div>


```css
background: #FFFFFF;
```

## Surface & Card

<table>
<tr><td>surface</td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#F8F8F8;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span></td><td><code>#F8F8F8</code></td></tr>
<tr><td>surface-solid</td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#FFFFFF;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span></td><td><code>#FFFFFF</code></td></tr>
<tr><td>border</td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#EEEEEE;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span></td><td><code>#EEEEEE</code></td></tr>
<tr><td>card-shadow</td><td></td><td><code>none</code></td></tr>
<tr><td>card-radius</td><td></td><td><code>4px</code></td></tr>
<tr><td>card-backdrop</td><td></td><td><code>—</code></td></tr>
</table>

## Text

<div style="display:flex;gap:12px;flex-wrap:wrap;margin:12px 0;">
<div style="text-align:center;"><div style="width:80px;height:44px;background:#FFFFFF;border-radius:6px;border:1px solid rgba(128,128,128,0.15);display:flex;align-items:center;justify-content:center;"><span style="color:#333333;font-weight:600;font-size:14px;">Aa</span></div><div style="font-size:11px;color:#888;margin-top:4px;">Primary<br/><code style="font-size:10px;">#333333</code></div></div>
<div style="text-align:center;"><div style="width:80px;height:44px;background:#FFFFFF;border-radius:6px;border:1px solid rgba(128,128,128,0.15);display:flex;align-items:center;justify-content:center;"><span style="color:#666666;font-weight:600;font-size:14px;">Aa</span></div><div style="font-size:11px;color:#888;margin-top:4px;">Secondary<br/><code style="font-size:10px;">#666666</code></div></div>
<div style="text-align:center;"><div style="width:80px;height:44px;background:#FFFFFF;border-radius:6px;border:1px solid rgba(128,128,128,0.15);display:flex;align-items:center;justify-content:center;"><span style="color:#999999;font-weight:600;font-size:14px;">Aa</span></div><div style="font-size:11px;color:#888;margin-top:4px;">Muted<br/><code style="font-size:10px;">#999999</code></div></div>
<div style="text-align:center;"><div style="width:80px;height:44px;background:#FFFFFF;border-radius:6px;border:1px solid rgba(128,128,128,0.15);display:flex;align-items:center;justify-content:center;"><span style="color:#CCCCCC;font-weight:600;font-size:14px;">Aa</span></div><div style="font-size:11px;color:#888;margin-top:4px;">Hint<br/><code style="font-size:10px;">#CCCCCC</code></div></div>
</div>

## Accent

<div style="display:flex;gap:16px;align-items:center;margin:12px 0;">
<div style="text-align:center;"><div style="width:64px;height:36px;border-radius:6px;background:#333333;"></div><div style="font-size:11px;color:#888;margin-top:4px;">Accent<br/><code style="font-size:10px;">#333333</code></div></div>
</div>

## Tier Colors

<div style="display:flex;gap:12px;flex-wrap:wrap;margin:12px 0;">
<div style="text-align:center;"><div style="width:64px;height:44px;border-radius:8px;background:#333333;display:flex;align-items:center;justify-content:center;"><span style="color:white;font-weight:900;font-size:20px;text-shadow:0 1px 3px rgba(0,0,0,0.3);">S</span></div><div style="font-size:10px;color:#888;margin-top:4px;"><code>#333333</code></div></div>
<div style="text-align:center;"><div style="width:64px;height:44px;border-radius:8px;background:#666666;display:flex;align-items:center;justify-content:center;"><span style="color:white;font-weight:900;font-size:20px;text-shadow:0 1px 3px rgba(0,0,0,0.3);">A</span></div><div style="font-size:10px;color:#888;margin-top:4px;"><code>#666666</code></div></div>
<div style="text-align:center;"><div style="width:64px;height:44px;border-radius:8px;background:#999999;display:flex;align-items:center;justify-content:center;"><span style="color:white;font-weight:900;font-size:20px;text-shadow:0 1px 3px rgba(0,0,0,0.3);">B</span></div><div style="font-size:10px;color:#888;margin-top:4px;"><code>#999999</code></div></div>
<div style="text-align:center;"><div style="width:64px;height:44px;border-radius:8px;background:#CCCCCC;display:flex;align-items:center;justify-content:center;"><span style="color:white;font-weight:900;font-size:20px;text-shadow:0 1px 3px rgba(0,0,0,0.3);">C</span></div><div style="font-size:10px;color:#888;margin-top:4px;"><code>#CCCCCC</code></div></div>
</div>

<table>
<tr><th>Tier</th><th>Color</th><th>Row BG</th><th>Gradient</th></tr>
<tr><td><strong>S</strong></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#333333;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>#333333</code></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:rgba(0,0,0,0.06);border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>rgba(0,0,0,0.06)</code></td><td>— </td></tr>
<tr><td><strong>A</strong></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#666666;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>#666666</code></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:rgba(0,0,0,0.04);border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>rgba(0,0,0,0.04)</code></td><td>— </td></tr>
<tr><td><strong>B</strong></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#999999;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>#999999</code></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:rgba(0,0,0,0.02);border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>rgba(0,0,0,0.02)</code></td><td>— </td></tr>
<tr><td><strong>C</strong></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:#CCCCCC;border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>#CCCCCC</code></td><td><span style="display:inline-block;width:20px;height:20px;border-radius:4px;background:rgba(0,0,0,0.01);border:1px solid rgba(128,128,128,0.2);vertical-align:middle;"></span> <code>rgba(0,0,0,0.01)</code></td><td>— </td></tr>
</table>

## Typography

<table><tr><th>Role</th><th>Font</th></tr>
<tr><td>heading</td><td><code>Outfit</code></td></tr>
<tr><td>body</td><td><code>Outfit</code></td></tr>
<tr><td>cjk</td><td><code>Noto Sans CJK SC</code></td></tr>
</table>

## 相关
- [[design-tokens]] — 全局共享token
- [[style-cream]]
- [[style-sigma]]
