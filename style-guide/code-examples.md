# Code Examples

Code examples are often the most-read part of any developer documentation. A bad example costs the user time and erodes trust. These standards define what good examples look like and how to maintain them.

---

## Principles

### Show intent, not just syntax

An example should demonstrate something a real user would actually do, not just prove that a method exists.

**Weak** — shows that a method exists:
```js
client.workflows.get('wf_123');
```

**Strong** — shows how you'd use it:
```js
// Check whether a workflow exists before triggering it
const exists = await nf.workflows.get('welcome-flow').catch(() => null);
if (!exists) {
  throw new Error('Workflow not found — check that it has been registered');
}
await nf.events.emit('user.signup', { userId: newUser.id });
```

### Make them runnable

A developer should be able to copy an example, replace the placeholder values, and have it work. If an example requires significant setup that isn't described nearby, add a prerequisite note or link.

### Fail gracefully

Show error handling in examples where failures are likely — network calls, file I/O, authentication. An example without error handling teaches bad patterns.

---

## Sample data conventions

Use consistent, clearly fictional placeholder values. Do not use real-looking email addresses, phone numbers, or IDs.

| Data type | Use | Avoid |
|---|---|---|
| API key | `nxf_test_abc123...` | `YOUR_API_KEY_HERE`, real-looking keys |
| User ID | `usr_test_001`, `usr_abc123` | `1`, `john`, real UUIDs |
| Email | `user@example.com`, `dev@example.com` | Real-looking personal emails |
| URL | `https://api.example.com/...` | Internal URLs, real production endpoints |
| Names | `Alice`, `Acme Corp` | Real person names, real company names |
| Phone | `+1-555-000-0000` | Real phone numbers |

Use `example.com` as the domain for all example URLs — it's an IANA reserved domain for documentation purposes.

---

## Language coverage

When an SDK or API supports multiple languages, show examples in each supported language. Use tabs if your documentation platform supports them. If not, pick the most common language for the primary example and link to a reference for others.

The order of language tabs should reflect your user analytics — most-used language first. As a default starting point: JavaScript/TypeScript, Python, then others.

---

## Comments in code

Use comments to explain *why*, not *what* — the code already shows what. Reserve comments for:
- Explaining a non-obvious choice
- Flagging a value the user must replace
- Noting a limitation or gotcha

```js
// Replace 'welcome-flow' with the ID you used when calling workflow.register()
const result = await nf.runs.list({ workflowId: 'welcome-flow' });

// workflow.run() blocks until the run completes — use events for production
await workflow.run({ userId: '123' });
```

Do not over-comment obvious code:
```js
// Bad: over-commented
const nf = new NexaFlow({ apiKey: process.env.NEXAFLOW_API_KEY }); // create client
const result = await workflow.run({ userId: '123' }); // run the workflow
```

---

## Keeping examples accurate

Stale code examples are one of the most common complaints in developer docs. Treat code examples like code, not prose:

1. **Test examples** — run them, or have CI run them, against the current version of the SDK. A broken example is worse than no example.
2. **Pin version numbers** — if an example works differently in v1 vs v2, say so explicitly.
3. **Update on breaking changes** — when a method is renamed or a parameter changes, update the examples in the same PR as the code.
4. **Flag deprecated patterns** — if an example shows a v1 pattern that still works but will break at EOL, add a note: `// NexaFlow SDK v1 — see migration guide for v2 equivalent`

---

## Long vs. short examples

**Short examples** (3–15 lines): Good for API reference — one method, one purpose, no surrounding context.

**Long examples** (16–50+ lines): Good for quickstarts, tutorials, and end-to-end scenarios where a reader needs to understand how pieces fit together. These should be in a dedicated examples repository or an `/examples` directory, not inline in a reference page.

For reference documentation, link to the full example rather than embedding it:

> For a complete end-to-end example, see [examples/node/order-fulfillment.js](../examples/node/).

---

## Accessibility in code examples

- Provide plain-text descriptions for complex diagrams or architecture illustrations that accompany code
- If your documentation platform renders code with syntax highlighting, verify it passes color contrast requirements
- Do not convey meaning through color alone in inline comments ("the red part", "the highlighted section")
