# Naming Conventions

Consistent naming reduces ambiguity and helps users build accurate mental models of the product. These conventions apply to UI text, documentation headings, API field references, and code identifiers in examples.

---

## Product and feature names

- Use the official product name exactly as registered: "NexaFlow", not "Nexaflow", "nexaflow", or "NF"
- Feature names follow the product's naming standard for the first reference on a page; subsequent references can be shortened if unambiguous
- Do not invent informal abbreviations for product features — if the product team hasn't shortened it, don't do it in docs

---

## APIs

**Endpoints:** describe by resource and action, not by HTTP method in prose:
- "Create a workflow" (not "POST /workflows")
- "List runs" (not "GET /runs")

In reference tables, show the method: `POST /v2/workflows`

**Field names:** always use the exact field name from the API response in inline code, even if it looks awkward in prose:
- "The `startedAt` field contains..." (not "the start time")

**IDs:** show ID prefixes in examples consistently — don't use raw UUIDs in sample payloads. Use a prefix that signals the resource type:
- Users: `usr_abc123`
- Workflows: `wf_abc123`
- Runs: `run_abc123`
- Orders: `ord_abc123`

This matches the pattern used by Stripe, Plaid, and other API-first companies — it's familiar to developers and makes logs easier to read.

---

## UI elements

Reference UI elements by their exact label in bold, followed by the type of element if it isn't obvious:

| Element | How to reference |
|---|---|
| Button | Click **Save changes** |
| Menu item | Select **Settings > API Keys** |
| Tab | Go to the **Overview** tab |
| Text field | In the **Name** field, enter a display name |
| Toggle | Turn on **Two-factor authentication** |
| Checkbox | Select **Notify on failure** |

Do not describe the visual appearance of UI elements ("the blue button", "the dropdown on the right"). Labels change less often than visual design; descriptions of appearance become incorrect after redesigns.

---

## Actions (verbs)

Be consistent in how you describe user actions:

| Use | Instead of |
|---|---|
| "Select" (from a list or menu) | "Choose", "pick" |
| "Click" (buttons, links) | "Hit", "press", "tap" (except on mobile) |
| "Enter" (in a text field) | "Type", "input", "put in" |
| "Turn on / turn off" (toggles) | "Enable/disable", "toggle", "flip" |
| "Run" (a command) | "Execute", "fire" |
| "Create" (a resource) | "Make", "add" (reserve "add" for optional additions to existing groups) |
| "Delete" (permanent removal) | "Remove" (use "remove" for reversible operations) |

---

## Procedures and tasks

Name how-to guides with the task the user is completing, not the feature:

| Correct | Incorrect |
|---|---|
| "Set up two-factor authentication" | "Two-factor authentication" |
| "Create your first workflow" | "Workflow creation" |
| "Troubleshoot connection failures" | "Connection failure troubleshooting" |

Use an imperative verb phrase — "Set up", "Create", "Configure", "Troubleshoot" — not a gerund ("Setting up") or noun phrase.

---

## Error messages

Error messages in documentation should match the exact text the user sees in the product. If the error text changes, the documentation must change too — this is a strong argument for pulling error messages from a shared content file.

When documenting an error, always include:
- The exact error code or message string (in inline code)
- What it means in plain English
- The most common cause
- The fix or next step

---

## Version references

When referencing a specific version, write it as: "NexaFlow SDK v2.3", not "version 2.3" or "v2.3.0" (omit the patch unless the patch is relevant to the fix being documented).

When describing version-gated features, use a consistent "Available in" note:

> **Available in SDK v2.2 and later.** Earlier versions do not support parallel blocks.
