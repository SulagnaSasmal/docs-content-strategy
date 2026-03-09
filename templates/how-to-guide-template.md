# Template: How-to Guide

Copy this template when creating a new task-based guide. Replace all placeholder text in `[brackets]`. Remove sections that don't apply.

---

<!--
TEMPLATE INSTRUCTIONS:
- Title must start with an imperative verb: "Configure", "Set up", "Troubleshoot", "Add"
- Prerequisites list everything the user must have DONE before starting — not just installed
- Each step is one action with a visible result
- If a decision point exists (two valid approaches), present it as a decision before the steps diverge, not as a note buried in step 4
- Keep the guide under 15 steps if possible; longer tasks should be broken into phases or sub-guides
-->

# [Imperative verb + outcome — e.g., "Set up webhook signature verification"]

[2–3 sentence intro. State: what this guide covers, what the user will be able to do when finished, and any key constraints or caveats that affect whether this guide applies to them.]

---

## Prerequisites

Before you begin:

- [Prerequisite 1 — be specific: "You have an API key with `webhooks:write` scope"]
- [Prerequisite 2 — link to setup guides where appropriate]
- [Prerequisite 3]

---

## [Phase 1 heading — optional, use for tasks with 10+ steps]

### Step 1: [Short verb phrase describing the step outcome]

[Explain what to do. Use second person and present tense. If this step requires a decision, present options explicitly.]

```[language]
[Code, command, or config example for this step]
```

[Optional: note a common mistake or clarify expected behavior at this step.]

### Step 2: [Short verb phrase]

[Step instruction.]

```[language]
[Code example if applicable]
```

Expected output:
```
[What the user should see if this step succeeded]
```

### Step 3: [Short verb phrase]

[Repeat as needed.]

---

## Verify it worked

[Tell the user exactly how to confirm the task is complete. Don't end with a step that has no verification — the user should have clear evidence of success before moving on.]

```[language]
[Verification command or code snippet]
```

You should see:
```
[Expected output that confirms success]
```

---

## Troubleshoot common issues

**[Symptom: what went wrong, using the user's vocabulary]**  
[Cause. Fix.]

**[Another symptom]**  
[Cause. Fix.]

---

## Next steps

- [Link to the next logical task in the user's journey]
- [Link to related reference page for deeper detail]
- [Link to related guide if the user wants to extend what they just built]
