# Doc Types

This reference defines the documentation types used in this framework, what each type is for, and how to choose the right type for a given piece of content.

The type shapes the structure, voice, and success criteria of a doc before you write a word.

---

## The four primary doc types

### 1. Concept (Learning)

**Purpose:** Build the reader's understanding of a system, principle, or mechanism. Not "how to do X" but "how X works."

**When to use:**
- The user needs context before they can use a feature correctly
- A common misconception needs to be addressed
- The product's architecture or data model needs explanation

**Structure:**
1. What this thing is (one-sentence definition)
2. Why it exists or why it matters
3. How it works (can include diagrams, architecture descriptions)
4. Key distinctions or edge cases that affect usage
5. Links to related how-to guides and reference pages

**What a concept page is NOT:** a feature announcement, a procedural walkthrough, or a reference list.

**Example titles:**
- "How workflows are versioned"
- "Understanding run context and template evaluation"
- "Retry policies: how backoff works"

---

### 2. How-to guide (Doing)

**Purpose:** Help the user complete a specific task. Assumes they understand the basics; focuses on the steps.

**When to use:**
- There's a concrete, achievable outcome the user wants
- The task has multiple steps that must happen in order
- The task has failure modes that need to be addressed

**Structure:**
1. Title: "How to [verb + outcome]"
2. Brief intro: what this guide covers and what the user will be able to do after
3. Prerequisites
4. Numbered steps — each step is one action with a clear outcome
5. Verification: how the user can confirm it worked
6. Next steps or related tasks

**What a how-to is NOT:** an explanation of why something works (link out to a concept page instead).

**Example titles:**
- "Add retry logic to a failing step"
- "Set up webhook signature verification"
- "Replay a failed run from the dead-letter queue"

---

### 3. Reference (Looking up)

**Purpose:** Give the user accurate, complete, and scannable information about a specific interface, configuration option, or data structure.

**When to use:**
- The user knows what they want; they need the exact parameter name, type, or allowed values
- Completeness matters more than narrative — every option, every field, every error code

**Structure:**
- One resource, method, class, or config object per page (or one per H2 section in a group)
- Description line (one sentence maximum)
- Parameter/property table: name, type, required/optional, default, description
- Return value
- Error codes
- Minimal examples (show usage, not a tutorial)

**What a reference page is NOT:** a tutorial or conceptual explanation. Keep prose minimal; if a concept needs more than a sentence to explain, link to a concept page.

**Example titles:**
- `NexaFlow` client (class reference)
- `WorkflowDefinition` schema
- Error codes

---

### 4. Troubleshooting / FAQ

**Purpose:** Help the user recover from a failure or answer a specific question with no preamble.

**When to use:**
- Error messages or codes need an explanation and a fix
- A behavior surprises users frequently (shows up in support tickets, Slack, or community forums)
- There's a common setup mistake with a clear solution

**Structure:**
1. Symptom or question as the H2 heading (use the language users actually use)
2. Cause (brief)
3. Fix / resolution (numbered steps if multiple)
4. Verification
5. "If this didn't solve it": escalation path

**What a troubleshooting page is NOT:** a reference list with no fixes, or a place to document every edge case that nobody will read.

---

## Secondary doc types

### Quickstart / tutorial

A longer, narrative walkthrough designed to get a new user to a working result as fast as possible. Uses a realistic, end-to-end scenario. Different from a how-to in that it's designed for first-time users building understanding, not experienced users completing a task.

- Introduce concepts in passing, but don't stop to explain them fully
- Keep it under 20 minutes; link to deeper content for users who want to understand more
- Always end with a verification step and a "what's next" section

### Release notes

Structured change communication. Not a marketing announcement and not a changelog dump. Good release notes tell users:
- What changed and where to find it
- Whether they need to do anything (migration, configuration change, deprecation)
- What was fixed and what known issues remain

See the [Release Notes Template](../templates/release-notes-template.md) for the standard format.

### Migration guide

A targeted how-to for users upgrading from one version to another. Covers only what changed between the versions — not a repeat of the full documentation.

Structure: list breaking changes, show before/after code for each, provide a migration checklist at the end.

---

## Choosing the right doc type

Ask these questions to identify the right type:

1. **Is the user trying to accomplish something or understand something?**
   - Accomplish something → How-to guide
   - Understand something → Concept page

2. **Is the user looking up a specific detail they already know they need?**
   - Yes → Reference

3. **Is the user stuck and trying to fix something?**
   - Yes → Troubleshooting

4. **Is the user completely new and needs a guided walkthrough?**
   - Yes → Quickstart or tutorial

5. **Am I trying to communicate a change to existing users?**
   - Yes → Release notes or migration guide

If your content doesn't fit cleanly into one of these types, it's usually a sign that the scope is too broad and the content should be split into two or more pages.
