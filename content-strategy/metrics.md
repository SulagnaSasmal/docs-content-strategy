# Documentation Metrics

You cannot manage what you don't measure. This framework defines the metrics that indicate documentation quality and team effectiveness, how to collect them, and how to use them to make decisions.

---

## Why metrics matter in docs programs

Documentation teams often operate on gut instinct and anecdote — "the quickstart feels too long" or "we keep hearing that authentication is confusing." These signals are real but unreliable. Metrics provide evidence that separates signal from noise and justifies investment in specific improvements.

The goal is not to track everything. The goal is to track a small set of meaningful indicators that reveal whether documentation is actually helping users do things.

---

## Tier 1: Outcome metrics (most important)

These metrics indicate whether documentation is achieving its purpose.

### Docs-deflected support volume

**What it measures:** How many support tickets, Slack threads, or community forum posts ask questions that are answered in the documentation.

**How to collect:** Tag incoming support requests. Count the proportion that match documented content. Track trend over time.

**Target:** Downward trend in docs-deflectable questions as coverage improves.

**Signal for action:** A spike in a specific question type means coverage is missing, the existing page isn't findable, or the existing page doesn't actually answer the question.

---

### Task completion rate

**What it measures:** What percentage of users who start a documented task complete it successfully.

**How to collect:** Instrument quickstarts and key how-to guides with page progression tracking. Track step-level drop-off in tutorials if your analytics platform supports it.

**Target:** >70% completion for a core quickstart is a reasonable baseline; best-in-class is >85%.

**Signal for action:** Drop-off at a specific step means that step is confusing, broken, or requires unstated prerequisites.

---

### Time to first success

**What it measures:** How long it takes a new user to reach a working integration or complete a key task from first landing in the documentation.

**How to collect:** Combine session analytics with product event data (e.g., "first API call made"). Median is more useful than mean here.

**Target:** Depends on product complexity. Set a baseline from current data and measure improvement over time.

**Signal for action:** If TTS is growing despite the product not getting more complex, documentation is getting harder to use.

---

## Tier 2: Quality indicators (leading metrics)

These metrics are easier to collect than outcome metrics and can serve as early warning signals.

### Page search exit rate

**What it measures:** The proportion of users who arrive at a page via search and immediately leave. High exit rate = content doesn't match what the user expected.

**How to collect:** Site analytics (GA4, Segment, or equivalent).

**Target:** <40% exit rate on high-traffic reference and how-to pages.

---

### Page-level feedback score (thumbs up/down)

**What it measures:** Whether users found a given page helpful.

**How to collect:** Add a "Was this helpful? Yes / No" widget on every page. Record negative feedback with an optional reason field.

**Target:** Track trend. Industry baseline for developer docs is roughly 60–70% positive.

**Signal for action:** Pages consistently below 50% positive need investigation — don't just rewrite them, talk to users first.

---

### Coverage ratio

**What it measures:** What percentage of documented API endpoints, CLI commands, or product features have at least one how-to guide.

**How to collect:** Maintain a coverage matrix. Map features/endpoints to documentation pages. Calculate ratio.

**Target:** 100% reference coverage for public APIs. >80% how-to coverage for top-used features.

---

### Freshness ratio

**What it measures:** What percentage of pages were reviewed or confirmed accurate within the last 90 days.

**How to collect:** Add a `last-reviewed` field to front matter. Script extracts pages where this is > 90 days old.

**Target:** >80% freshness for core pages (quickstart, auth, API reference). Long-tail pages can tolerate 6-month cycles.

---

## Tier 3: Efficiency metrics (team health)

These measure how well the documentation team operates.

### Time from code freeze to docs publish

**What it measures:** The lag between a feature being done and its documentation being live.

**Target:** Docs ship in the same release as the feature. Lag beyond one sprint should trigger a process conversation, not just a rewrite.

---

### Writer cycle time

**What it measures:** How long it takes from a documentation request to a published page.

**How to collect:** Track in your project management tool. Categorize by doc type — a new API reference page should take less time than a deep how-to guide.

**Signal for action:** Cycle times above team average on a specific writer or doc type may indicate unclear scope, tooling problems, or insufficient SME access.

---

## Putting metrics into practice

**Don't start measuring everything at once.** Pick one Tier 1 metric and instrument it properly. Use it to drive one quarter of work. Add a second metric when the first is stable.

**Socialize the data.** Share metrics with product, engineering, and support teams. Documentation quality is a shared responsibility — showing teams that their features account for 40% of docs-deflectable support tickets changes the conversation about documentation investment.

**Set baselines before setting targets.** Run 60–90 days of measurement before committing to a target number. Setting targets before baselines leads to either trivially easy goals or unreachable ones.

**Use metrics to start conversations, not end them.** A low page score is a symptom. The diagnosis requires talking to users.
