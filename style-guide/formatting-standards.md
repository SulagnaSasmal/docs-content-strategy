# Formatting Standards

Consistent formatting reduces the cognitive load of reading technical content. These standards apply across all documentation types.

---

## Headings

Use sentence case for all headings — capitalize only the first word and proper nouns.

| Correct | Incorrect |
|---|---|
| Set up your development environment | Set Up Your Development Environment |
| Authentication and authorization | Authentication And Authorization |
| Configure the NexaFlow SDK | Configure The Nexaflow Sdk |

Use headings to signal a change in topic, not to decorate sections that don't need a visual break. Avoid consecutive headings with no body content between them. If you must nest headings, do not skip levels (H2 → H4).

**Heading hierarchy:**

- H1: Page title (one per page, set by the CMS or front matter — do not write `#` headings in body content)
- H2: Major section
- H3: Subsection under an H2
- H4: Use sparingly; if you need H4 frequently, consider splitting the page

---

## Paragraphs

Write short paragraphs. Aim for 2–4 sentences. A paragraph that's longer than 6 sentences almost always contains two or more ideas — split it.

Start each paragraph with the most important sentence. Readers who skim stop at the first sentence of each paragraph.

---

## Lists

Use unordered lists for items that don't have a meaningful sequence:

- Prerequisites for a task
- A set of options, features, or constraints
- Examples

Use ordered lists for steps that must happen in sequence:

1. Install the SDK.
2. Set your API key.
3. Initialize the client.

**List formatting rules:**

- Use a period at the end of each list item that is a complete sentence.
- Don't use a period if the list items are short noun phrases or fragments.
- Be parallel — all items in a list should follow the same grammatical structure.
- Don't nest more than two levels deep.

---

## Tables

Use tables for structured comparisons. Tables are appropriate when:

- You have three or more items, each with the same set of attributes
- A user needs to scan across rows to compare options
- The information is too dense for prose without becoming a wall of text

Don't use tables for two-column key/value lists — a definition list or prose is clearer.

**Table formatting:**
- Keep column headers short (1–3 words)
- Left-align text columns; right-align number columns
- If a cell has no applicable value, write "—" not "N/A" or "None" (unless "None" is a meaningful technical value)

---

## Code

**Inline code:** Use backticks for all of the following, even in the middle of a sentence:
- Command names: `git commit`
- Parameter names: `timeoutMs`
- File paths: `/etc/config.yaml`
- String values: `"application/json"`
- HTTP methods and status codes: `POST`, `400 Bad Request`

**Code blocks:** Use fenced code blocks (triple backtick) for all multi-line code. Always specify the language for syntax highlighting:

````markdown
```js
const result = await workflow.run({ userId: '123' });
```
````

**What to show in code blocks:**
- Show complete, runnable examples when space allows
- If a code block is partial, use comments to indicate what's been omitted — do not use ellipsis (`...`) without a comment explaining what it represents
- Use realistic but clearly fictional values: `user_abc123`, `ord_789xyz`, `nxf_test_...` — not `YOUR_VALUE_HERE` or `REPLACE_ME`

---

## Notes, warnings, and callouts

Use callout formatting sparingly. Overuse of callout boxes trains readers to ignore them.

| Type | Use for | Formatting |
|---|---|---|
| **Note** | Useful context that isn't part of the main flow | `> **Note:** ...` |
| **Important** | Information the user must know to avoid an error | `> **Important:** ...` |
| **Warning** | Risk of data loss, security issue, or irreversible action | `> **Warning:** ...` |
| **Tip** | Optional shortcut or best practice | `> **Tip:** ...` |

Reserve **Warning** for genuinely dangerous actions. If everything has a Warning box, none of them will be read.

---

## Numbers and units

- Spell out numbers zero through nine; use numerals for 10 and above.
- Always include a unit of measurement: `30 seconds`, `10 MB`, `100 requests per minute`.
- Use commas for thousands: `10,000` not `10000`.
- Use MS units (milliseconds = `ms`, seconds = `s`); never mix formats in the same table.

---

## Dates and times

- Use ISO 8601 for machine-readable timestamps: `2026-03-09T14:30:00Z`
- For human-readable dates in prose, write the full month: `March 9, 2026`
- Always specify the timezone when referencing a specific time: `6:00 AM UTC`

---

## Links

- Write descriptive link text — never "click here" or "read more"
- The link text should describe the destination, not the action: "see [Error Handling](../error-handling.md)" not "click here to read about errors"
- Use relative links for internal documentation
- External links should open in the same tab by default; do not force new tabs in Markdown unless your CMS does it automatically for external links

---

## File naming

- Use lowercase and hyphens: `getting-started.md`, `api-reference.md`
- No spaces, underscores, or camelCase in filenames
- Index files should be named `index.md` or `README.md` depending on the toolchain
- Be specific: `authentication.md` is better than `auth.md`
