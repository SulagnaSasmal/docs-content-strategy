# Content Health Scorecard

This scorecard gives a documentation set a single composite score based on five dimensions. Use it to communicate documentation health to product managers, engineering leads, and stakeholders who need a summary view — not the full audit detail.

Run alongside the [Doc Audit Checklist](doc-audit-checklist.md), which gives the actionable item-level view.

---

## Scoring dimensions

Rate each dimension 1–5 using the criteria below. Be honest — a score inflated to look good is a score that can't drive improvement.

---

### Dimension 1: Coverage

Does the documentation cover what users need?

| Score | Criteria |
|---|---|
| **5** | All public API and feature surfaces documented. New user journey fully covered. Operator and admin use cases covered separately from developer use cases. |
| **4** | ≥90% of API and features documented. New user journey works end to end. Minor gaps in operator/admin coverage. |
| **3** | Core features and top-20 endpoints documented. New user can get started but hits undocumented edge cases. Operator coverage thin. |
| **2** | Significant gaps — major features or common workflows are undocumented. Users routinely find the limits of the docs. |
| **1** | Documentation covers less than 50% of the product surface. Most user journeys require support ticket escalation. |

**Coverage score:** ___

---

### Dimension 2: Accuracy

Is the documentation correct?

| Score | Criteria |
|---|---|
| **5** | All code examples testable and verified against current version. All field names, error codes, and UI references match the product. No known stale pages. |
| **4** | Code examples verified for core flows. Minor discrepancies in edge-case reference pages. Reviewed within last 60 days. |
| **3** | Core examples work. Some parameter names or UI references outdated. Known stale pages present but not blocking. |
| **2** | Multiple stale pages on critical paths. Users report incorrect information via feedback or support. |
| **1** | Code examples regularly fail. Documentation reflects a previous major version of the product in key sections. |

**Accuracy score:** ___

---

### Dimension 3: Clarity

Is the documentation easy to understand and act on?

| Score | Criteria |
|---|---|
| **5** | All how-tos have clear outcome-focused titles, numbered steps, and verification. Concepts explain "why" as well as "what." Voice consistent throughout. |
| **4** | Most how-tos are task-based. Occasional conceptual content mixed into procedures. Voice mostly consistent. |
| **3** | Some useful content but structure varies widely across pages. Users can find answers but often need to scan past irrelevant content. |
| **2** | Documentation is dense, inconsistently structured, or uses jargon without explanation. Users frequently need support despite finding the right page. |
| **1** | Documentation reads as feature specs or internal notes. Not structured for user consumption. |

**Clarity score:** ___

---

### Dimension 4: Findability

Can users get to the content they need within 2–3 clicks?

| Score | Criteria |
|---|---|
| **5** | Navigation is ≤3 levels deep, organized by user task, and stable. Search returns correct results for common queries. All pages have meaningful titles and first paragraphs that confirm the right landing. |
| **4** | Navigation has occasional depth or labeling issues. Search mostly works. A few pages with misleading titles. |
| **3** | Navigation is feature-oriented rather than task-oriented. Users can find content but it takes effort. Search has significant gaps. |
| **2** | Navigation has grown organically without a clear model. Users rely on external search engines or Ctrl+F to navigate. Significant orphaned pages. |
| **1** | No coherent navigation structure. Content is discoverable only if you already know where to look. |

**Findability score:** ___

---

### Dimension 5: Freshness

Is the documentation kept current?

| Score | Criteria |
|---|---|
| **5** | Docs ship with features. All pages reviewed within 90 days. Deprecation notices present for all end-of-life features. |
| **4** | Docs ship within one sprint of features. >80% of pages reviewed within 90 days. Deprecation mostly current. |
| **3** | Some documentation lag (1–2 releases behind). Core paths current; edge cases may be stale. |
| **2** | Documentation frequently 1+ major versions behind. Users encounter outdated guidance on common paths. |
| **1** | Documentation has not been systematically updated in 6+ months. Cannot be trusted as a source of truth for current behavior. |

**Freshness score:** ___

---

## Composite score

Add the five dimension scores and calculate the total.

| Total | Health status | Recommended action |
|---|---|---|
| 23–25 | Excellent | Maintenance mode — monitor metrics, address as issues arise |
| 18–22 | Good | Targeted improvements — address lowest-scoring dimension |
| 13–17 | Fair | Structured remediation plan — prioritize accuracy and coverage first |
| 8–12 | Poor | Significant investment needed — audit, prioritize, and allocate dedicated time |
| 5–7 | Critical | Documentation is a liability — escalate to product/engineering leadership |

**Total score:** ___ / 25  
**Health status:** ___

---

## Scorecard history

Track scores over quarters to show trend direction. A stable "Fair" is less concerning than a trend from "Good" to "Fair" to "Poor."

| Quarter | Coverage | Accuracy | Clarity | Findability | Freshness | Total |
|---|---|---|---|---|---|---|
| [Q1 YYYY] | | | | | | |
| [Q2 YYYY] | | | | | | |
| [Q3 YYYY] | | | | | | |
| [Q4 YYYY] | | | | | | |

---

## Notes

[Space for qualitative context that explains the scores — major launches, resource constraints, process changes, or specific known issues that account for a dimension's score.]
