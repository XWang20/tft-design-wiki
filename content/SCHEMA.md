# Wiki Schema

## Domain
TFTable做图体系 — 涵盖设计思想、架构决策、经验教训和工作流。
重点是**为什么**这样做，不是**具体参数是什么**。

## Architecture: Three Knowledge Layers

```
wiki/
├── principles/    # Layer 1: 设计哲学，核心原则，不变的东西
├── decisions/     # Layer 2: 架构决策，为什么选了A不选B，历史演进
├── pitfalls/      # Layer 3: 踩坑记录，带完整上下文的bug故事
├── workflows/     # Layer 4: 工作流程，操作性知识
├── reference/     # Layer 5: 按需查阅的技术细节（不是默认加载）
```

**Layer 1 — Principles**: 不会过时的设计智慧。读完应该能做出对的设计判断。
**Layer 2 — Decisions**: 每个重大决策的WHY。为什么禁暗色？为什么不用模板引擎？
**Layer 3 — Pitfalls**: 完整的bug故事 — 谁发现的，怎么错的，为什么会错，怎么修的。
**Layer 4 — Workflows**: 从数据到图片的具体流程，操作手册。
**Layer 5 — Reference**: CSS tokens、API路径、脚本清单等。需要时查，不需要记。

## Reference层的定位
Design tokens（颜色、字号、间距）非常重要，但它们是**查阅型知识**，不是**理解型知识**。
放在`reference/`里，按需查阅，不跟principles混在一起。

**不属于Wiki的**：
- ❌ 具体的proxy端口号（属于env config）
- ❌ 脚本文件的完整列表（属于filesystem discovery）

**属于reference/的**：
- ✅ 颜色token表（palette、cost colors、tier colors）
- ✅ 字号/间距规范（4pt grid的具体数值）
- ✅ API端点和数据结构
- ✅ 脚本的功能索引（不是文件列表，是"做什么用哪个"）

## Conventions
- File names: lowercase, hyphens, no spaces
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md`
- Every action must be appended to `log.md`
- 中英混用，技术术语保留英文

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: principle | decision | pitfall | workflow | reference
tags: [from taxonomy below]
sources: []
---
```

## Tag Taxonomy
- **Design**: visual-identity, anti-pattern, layout, typography, color
- **Architecture**: rendering, data, ai-generation, scripts, infra
- **Quality**: bug, gotcha, validation, testing
- **Process**: workflow, bilingual, multi-page, iteration
- **Domain**: tft, content-type, translation

## Page Quality Rules
- Every page must answer "WHY" — if it only answers "WHAT", it belongs in reference/
- Bug stories must include: who found it, what went wrong, root cause, fix
- Principles must include: the reasoning, not just the rule
- Decisions must include: what was rejected and why
- Keep pages scannable — readable in 30 seconds
