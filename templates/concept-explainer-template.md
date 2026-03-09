# Template: Concept Explainer

Copy this template when creating a new conceptual page. Replace all placeholder text in `[brackets]`. Remove sections that don't apply.

---

<!--
TEMPLATE INSTRUCTIONS:
- A concept page explains how something works — not how to do something
- Lead with what the user NEEDS to understand to use the feature correctly
- Don't bury the key insight; state it in the first two paragraphs
- Diagrams are high-value here — use ASCII or Mermaid if your toolchain supports it
- Link to how-to guides for "how to use this" — don't duplicate procedural content
- Keep this page focused on ONE concept; if you're explaining two things, split them
-->

# [Concept name — e.g., "How run context works"]

[Opening paragraph: what this concept is and why it matters. Answer the question a developer would ask before clicking on this page.]

[Optional second paragraph: the key insight about this concept that prevents common mistakes. If you have a "this is the most important thing to understand" statement, put it here rather than in a callout box.]

---

## [How it works — or whatever the first major section is]

[Explain the mechanism. Use plain language. If an analogy helps, use it — but be careful that it doesn't fall apart under scrutiny.]

[Include a diagram if the concept has a flow, hierarchy, or sequence that's hard to describe in prose:]

```
[ASCII diagram or Mermaid code block]
```

[Continue explanation. If there are sub-components or variations, introduce them here as H3 sections.]

### [Sub-component or variation]

[Explanation.]

---

## [Key behavior or rule the user must know]

[Important behaviors that affect how the user writes code or configures the system. These are the things that cause bugs if the user doesn't know them.]

---

## [Limitations and constraints]

[What this concept doesn't support. What edge cases exist. This is not an apology — it's useful technical information that saves users time they'd otherwise spend testing the limits themselves.]

---

## Example

[A short, concrete example that shows the concept in action. Enough code or configuration to illustrate the point — not a full tutorial.]

```[language]
[Example]
```

[Annotate the key parts of the example that illustrate the concept.]

---

## Related

- [Link to a how-to guide that puts this concept into practice]
- [Link to the relevant reference page for the API or config related to this concept]
- [Link to adjacent concept pages the user might need]
