# Wiki Schema

## Domain
TFTable社交媒体做图系统 — 覆盖TFT（云顶之弈）信息图的设计系统、代码架构、渲染流程、数据管线、经验教训和工具链。

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `rendering-pipeline.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- 中英混用，技术术语保留英文，描述用中文

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
---
```

## Tag Taxonomy
- **Tools**: image-studio, scripts, playwright, playwright-render, preflight
- **Design**: design-system, style, theme, typography, color, layout, watermark
- **Data**: api, data-pipeline, tftable-api, cdragon, json
- **Content Types**: tierlist, top5, comp-detail, meta-shift, patch-notes, weekly, cover, unit-card, trait-card, comp-guide
- **Workflow**: rendering, bilingual, multi-page, generation-pipeline
- **Experience**: lesson, bug, anti-pattern, best-practice
- **Infrastructure**: server, cloudflare-tunnel, litellm, proxy

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed,
add it here first, then use it.

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions or minor details
- **Split a page** when it exceeds ~200 lines
- **Archive a page** when fully superseded — move to `_archive/`, remove from index

## Entity Pages
One page per notable entity (tool, system, service). Include:
- Overview / what it is
- Key facts and architecture
- Relationships to other entities ([[wikilinks]])
- Source references

## Concept Pages
One page per concept or topic. Include:
- Definition / explanation
- Current state of knowledge
- Open questions or debates
- Related concepts ([[wikilinks]])

## Comparison Pages
Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table format preferred)
- Verdict or synthesis
- Sources

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the lint report
