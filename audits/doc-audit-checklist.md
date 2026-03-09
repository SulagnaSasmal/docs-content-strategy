# Documentation Audit Checklist

Use this checklist to evaluate the quality and coverage of an existing documentation set. Run it quarterly for active doc sets, or when taking over documentation from another writer or team.

This checklist has three sections: coverage, content quality, and findability. Score each item Y (yes), N (no), or N/A. Count the Ns at the end of each section to prioritize work.

---

## Section 1: Coverage

### API and feature coverage

- [ ] Every public API endpoint has a reference page
- [ ] Every CLI command has a reference entry
- [ ] Every configuration option is documented (type, allowed values, default, description)
- [ ] All error codes and messages are documented with causes and fixes
- [ ] All major features have at least one associated how-to guide
- [ ] Breaking changes from the last two versions have migration guides
- [ ] Deprecated features are clearly marked with their removal version and migration path

### User journey coverage

- [ ] A new user can get to a working integration using only the documentation (tested path)
- [ ] The authentication setup process is documented end-to-end (not just that auth exists)
- [ ] There is a troubleshooting section for the most common failure points in the new user flow
- [ ] Admin/operator setup (deployment, configuration, access control) is documented separately from developer setup
- [ ] There is a clear path from "I'm evaluating this product" to "I've made my first API call"

**Coverage score: [Y count] / [total applicable]**

---

## Section 2: Content quality

### Accuracy

- [ ] Code examples are tested against the current product version
- [ ] Parameter names, field names, and error codes match the current API
- [ ] Screenshots and UI references match the current UI (or have been removed in favor of text descriptions)
- [ ] Version numbers and dates in the documentation are current
- [ ] No pages reference deprecated features without noting their deprecation status

### Clarity

- [ ] Headings are specific enough to distinguish pages from each other out of context
- [ ] Every how-to guide has an explicit outcome in its title
- [ ] Steps are numbered and each step has one action and one visible result
- [ ] Prerequisites are stated before steps begin, not discovered mid-guide
- [ ] No page uses "simple", "easy", "just", or "only" to describe a user action
- [ ] Code examples use realistic placeholder values (not `YOUR_VALUE_HERE` or bare integers like `1`)
- [ ] Every code example either runs or is explicitly annotated as a fragment

### Consistency

- [ ] All pages use sentence case headings
- [ ] UI element names match the product exactly (tested by checking against the live product)
- [ ] Terminology is consistent — the same concept is called the same thing on every page
- [ ] Code style is consistent across examples (indentation, quote style, import syntax)

**Quality score: [Y count] / [total applicable]**

---

## Section 3: Findability

### Navigation

- [ ] Navigation depth is three levels or fewer
- [ ] No navigation section has only one item in it
- [ ] The top-level navigation can accommodate the current content without overflow or orphaned pages
- [ ] Related pages are linked from within page bodies, not just adjacent in navigation

### Search

- [ ] The page title contains the exact terms a user would search for to find this page
- [ ] The first paragraph of each page answers the user's question directly (passes the 10-second test)
- [ ] Common alternative terms for key concepts appear in the page body
- [ ] All pages have a meaningful meta description (if your platform supports it)

### Freshness signals

- [ ] Every page has a `last reviewed` or `updated` date visible to users
- [ ] Pages that are intentionally limited in scope say so ("This guide covers X only; for Y, see...")
- [ ] Archived or deprecated pages are clearly marked and redirect to current alternatives
- [ ] The changelog or release notes section is up to date through the current version

**Findability score: [Y count] / [total applicable]**

---

## Prioritization

After scoring, apply this matrix to prioritize fixes:

| Impact | Effort | Priority |
|---|---|---|
| High (blocking user journeys, incorrect information) | Low | Do immediately |
| High | High | Plan for next sprint |
| Low (style inconsistencies, missing details) | Low | Batch into a cleanup pass |
| Low | High | Defer until capacity allows |

High-impact items in the coverage and accuracy sections take precedence over style and consistency fixes. A broken code example costs the user more time than a slightly inconsistent heading case.

---

## Re-audit schedule

| Doc set state | Recommended frequency |
|---|---|
| Active development (feature releases every 1–4 weeks) | Every 4–6 weeks |
| Stable product (major releases 2–4x per year) | Quarterly |
| Mature / legacy (infrequent changes) | Every 6 months or at release |
| Newly inherited documentation | Immediately, then quarterly |
