# Information Architecture Framework

This framework defines how to structure documentation for a software product from scratch. It covers navigation hierarchy, content grouping principles, and the decisions you make before writing a single page.

---

## Why IA matters in docs

Most documentation failures are not writing failures — they are findability failures. A user arrives with a clear question, can't locate the answer in the navigation or through search, and gives up. They either submit a support ticket (costing the company money) or assume the product can't do what they need.

Good information architecture means users reach the right content within two or three clicks from the documentation home page.

---

## The four-part navigation model

Developer documentation typically needs four navigation areas, aligned to the user's intent:

| Area | What the user's question is | Examples |
|---|---|---|
| **Learning** | "What is this and how does it work?" | Overview, key concepts, architecture |
| **Doing** | "How do I accomplish a specific task?" | How-to guides, tutorials, quickstarts |
| **Reference** | "What are the exact parameters, options, and return values?" | API reference, CLI reference, config options |
| **Troubleshooting** | "Something isn't working — why?" | Error code lookup, common issues, FAQ |

This model — popularized by the Diátaxis framework — prevents a common failure mode where docs mix conceptual explanation with step-by-step instructions, making it hard to skim for either purpose.

**Map your content against this model before writing anything:**

| Your content | Probably belongs in |
|---|---|
| "The workflow engine uses an event-driven model..." | Learning (concept) |
| "Configure a retry policy for your workflow" | Doing (how-to) |
| "`NexaFlow({ apiKey, timeoutMs })`" | Reference |
| "My webhook isn't receiving events" | Troubleshooting |

---

## Top-level navigation structure

For a developer-facing documentation site, this is the recommended top-level structure. Not all products need every section.

```
Docs home
├── Getting started          ← Doing (quickstart)
├── Concepts                 ← Learning
│   ├── Overview
│   ├── Architecture
│   └── [Core concept pages]
├── Guides                   ← Doing (task-based how-tos)
│   ├── [Task-based guide pages]
│   └── ...
├── API reference            ← Reference
│   ├── [Resource/class pages]
│   └── ...
├── Troubleshooting          ← Troubleshooting
│   ├── Common errors
│   └── ...
├── What's new               ← Changelog / release notes
└── Support / Contact
```

**Hierarchy rules:**
- Maximum three levels deep in navigation
- A section with only one child page should either promote that page up a level or be merged into a related section
- Do not create a section just to hold one doc

---

## Naming navigation items

Navigation labels must be short and outcome-oriented. Users scan navigation to find the thing that answers their question — not to understand the product's architecture.

| Avoid | Use |
|---|---|
| "NexaFlow SDK Documentation" | "Docs" or just the product name |
| "Workflow Engine Architecture" (top-level) | Move this inside Concepts |
| "Frequently Asked Questions" | "Troubleshooting" or "Common issues" |
| "Release Notes and Changelog" | "What's new" or "Changelog" |
| "Advanced Configuration Options" | "Configuration reference" |

---

## Content grouping principles

**Group by user task, not by feature.** A user looking to handle payment failures doesn't think "I need the webhook section and the error codes section" — they think "I need to handle payment failures." Create a guide around the task and link from it to the reference pages.

**Co-locate decisions.** Information that a user needs at the same moment should be on the same page or one click away. If a user is following a setup guide and gets blocked by an authentication error, the troubleshooting path should be accessible from the setup guide — not buried three levels down.

**Separate concepts from tasks.** A conceptual explanation of how retry logic works belongs in a Concepts page. A step-by-step guide to adding retry logic belongs in a Guides page. They can and should link to each other, but they serve different user intents and should not be on the same page.

---

## Managing doc debt

Documentation accumulates debt the same way code does. Pages become stale. Navigation grows into a graveyard of old feature names. Links rot.

Manage doc debt by:

1. **Auditing quarterly** — see [Doc Audit Checklist](../audits/doc-audit-checklist.md)
2. **Assigning ownership** — every top-level section has an owner responsible for updates when that area of the product changes
3. **Retiring gracefully** — rather than deleting pages, archive them with a clear deprecation notice and a redirect to current content
4. **Tracking coverage gaps** — content written by engineers or support in tickets/Slack is a signal; capture recurring questions in the docs

---

## Search optimization for documentation

External search engines rank documentation differently than they rank marketing pages. Optimize for developers who search with specific technical terms.

- The page title should contain the exact terms a user would type: "Configure retry policies" not "Advanced error handling overview"
- The first paragraph should answer the question directly — the user shouldn't have to read past the intro to know they're on the right page
- Use headings that match the language users use, not internal product terminology
- Include common alternative phrases in the body: if the official term is "workflow trigger" but users also search for "event listener" or "webhook handler", use those terms in context
