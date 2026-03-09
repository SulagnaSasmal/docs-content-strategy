# Audience Analysis

Every documentation decision — structure, depth, vocabulary, tone — depends on knowing who you're writing for. This framework defines how to build and apply audience profiles to a documentation program.

---

## Why documentation fails audience analysis

The most common audience analysis failure in technical documentation is writing for a composite user that doesn't exist: "the developer who needs step-by-step guidance and also wants a deep conceptual explanation and also just wants to scan the reference table." These are three different users in three different states.

The goal is not one persona, but a small set of distinct user types with distinct documentation needs, mapped to the right content at the right point in their journey.

---

## Defining user types

For most API-first and developer-focused software products, three to five user types cover the majority of documentation use cases:

### 1. The evaluator

**Who:** A developer, architect, or technical lead deciding whether to adopt the product.

**What they need:** Enough information to assess fit — capabilities, constraints, architecture, pricing model, security posture, and integration complexity. Not a tutorial; they want signal, not hand-holding.

**Documentation touchpoints:**
- Overview and architecture page
- Authentication and security
- API reference (or conceptual overview of it)
- Changelog (to assess maturity and support quality)

**Failure mode:** Burying key technical constraints in the middle of getting-started guides instead of surfacing them at evaluation stage.

---

### 2. The first-time implementer

**Who:** A developer who has decided to use the product and is setting it up for the first time.

**What they need:** Clear, sequential guidance from zero to "it works." Error messages that explain what went wrong and how to fix it. Realistic sample code that matches their tech stack.

**Documentation touchpoints:**
- Quickstart / getting started guide
- Installation instructions
- Authentication setup
- First integration how-to

**Failure mode:** Quickstarts that skip prerequisites, don't explain what success looks like, or make assumptions about existing setup.

---

### 3. The experienced user / builder

**Who:** A developer who has used the product before and is building something new with it.

**What they need:** Fast access to reference information. They know the concepts; they need the exact parameter name or the error code description. They don't want to read prose to find a method signature.

**Documentation touchpoints:**
- API reference (primary)
- How-to guides for specific tasks
- Changelog (to know about new features)
- Troubleshooting (when something behaves unexpectedly)

**Failure mode:** Reference documentation buried under conceptual content, or poor navigation that forces them to read to find the one fact they need.

---

### 4. The operator / administrator

**Who:** An IT admin, DevOps engineer, or platform team member responsible for deployment, configuration, and ongoing operation. Often not the same person who built the integration.

**What they need:** Deployment requirements, environment configuration, access control setup, monitoring and alerting guidance, upgrade procedures.

**Documentation touchpoints:**
- Deployment and infrastructure guides
- Configuration reference
- Security and permissions model
- Upgrade and migration guides
- Troubleshooting for operational issues

**Failure mode:** Deployment guides written for developers, not operators — assumes application code context that an admin doesn't have.

---

### 5. The end user (for product documentation)

**Who:** A business user who interacts with the product through a UI, not code. Often non-technical.

**What they need:** Task-based guidance ("how do I do X?"), plain-language explanations of what things mean, and clear error recovery guidance.

**Documentation touchpoints:**
- Help center articles
- UI-based how-to guides
- FAQ and troubleshooting
- In-app tooltips and contextual help

**Failure mode:** Writing help docs for end users in developer vocabulary. Or assuming they've read the previous section.

---

## Applying audience profiles

### At the content planning stage

Before adding a page to your documentation plan, answer:
- Which user type(s) will read this page?
- At what stage in their journey?
- What question are they coming in with, and what will they do differently after reading this?

If you can't answer these questions, the page may not need to exist yet.

### At the writing stage

Write each page for one primary user type. It's fine to note that a section "is relevant for operators deploying in multi-tenant environments" — that's a signal, not a full shift in audience. But if you're writing the same page for a first-time implementer and an experienced builder, you'll end up with content that serves neither well.

### At the review stage

Review against the audience: would the intended user understand this without additional context? Is the vocabulary appropriate? Are there assumed prerequisites that aren't stated?

---

## Researching your actual users

Audience profiles are hypotheses until validated. Methods to validate:

- **Support ticket analysis:** Categorize the last 50–100 support tickets by user type and question type. High-volume repeating questions are documentation gaps.
- **Direct interviews:** Talk to 5–10 users from each primary user type. Ask what they do when they get stuck, not what they think of the docs.
- **Search analytics:** What are users searching for that they're not finding? Gaps between search queries and page clicks reveal missing or poorly titled content.
- **Page analytics:** High entry rates with high exit rates on a given page may indicate that users arrived expecting different content.

Run this analysis at least once per quarter when the documentation is actively evolving, and when a major product change ships.
