# Technical Documentation Content Strategy & Style Guide

This repository contains the content strategy framework, editorial style guide, documentation templates, and audit tools I use to build and maintain developer and product documentation at scale.

It is both a practical reference for day-to-day writing decisions and a strategic framework for planning, organizing, and measuring documentation quality across a product portfolio.

---

## What's in here

| Section | Purpose |
|---|---|
| [Style Guide](style-guide/) | Decisions about voice, tone, formatting, naming, and code examples |
| [Content Strategy](content-strategy/) | Information architecture, audience models, doc type taxonomy, and success metrics |
| [Templates](templates/) | Ready-to-use structural templates for the most common doc types |
| [Audits](audits/) | Checklists and scorecards for evaluating existing documentation |

---

## Who this is for

This framework is designed for technical writing teams that:

- Support software products with both developer-facing API docs and end-user guides
- Work in a docs-as-code environment (Markdown, Git, CI/CD)
- Need a shared standard that multiple writers can apply consistently
- Are evaluating or improving their documentation against user and business outcomes

Individual writers can use the style guide and templates immediately. Documentation leads and managers will find the content strategy and audit sections most useful for program-level decisions.

---

## Philosophy

Good documentation is a product, not a byproduct. It answers specific questions for specific users at specific points in their journey, and it degrades gracefully when it's outdated — it either signals clearly that something may have changed, or it's accurate enough that users can still move forward.

The decisions in this framework follow three principles:

1. **Users first.** Start with what the user needs to accomplish, not with what the product does. Structure and vocabulary should match user mental models, not internal product architecture.

2. **Less is more.** Users don't read technical documentation; they scan it looking for the thing they need. Shorter, clearer, more navigable content serves them better than comprehensive prose.

3. **Ownership requires measurement.** You cannot improve what you don't measure. The metrics and audit frameworks here are designed to surface problems before they become user complaints.

---

## Repository layout

```
docs-content-strategy/
├── style-guide/
│   ├── voice-and-tone.md
│   ├── formatting-standards.md
│   ├── naming-conventions.md
│   └── code-examples.md
├── content-strategy/
│   ├── ia-framework.md
│   ├── doc-types.md
│   ├── audience-analysis.md
│   └── metrics.md
├── templates/
│   ├── api-reference-template.md
│   ├── how-to-guide-template.md
│   ├── concept-explainer-template.md
│   └── release-notes-template.md
└── audits/
    ├── doc-audit-checklist.md
    └── content-health-scorecard.md
```

---

## Using this framework with a new product

1. Start with [Audience Analysis](content-strategy/audience-analysis.md) — identify who you're writing for before you plan structure or content.
2. Review the [Doc Types](content-strategy/doc-types.md) reference to decide which content types your product needs.
3. Use the [IA Framework](content-strategy/ia-framework.md) to plan navigation and hierarchy.
4. Write to the [Voice and Tone](style-guide/voice-and-tone.md) standards from day one — retrofitting voice is expensive.
5. Apply [Templates](templates/) when creating new docs to enforce structure without starting from blank pages.
6. Schedule a quarterly [Audit](audits/doc-audit-checklist.md) once the docs are live.
