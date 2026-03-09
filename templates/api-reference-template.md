# Template: API Reference Page

Copy this template when creating a new API reference page. Remove sections that don't apply. Replace all placeholder text in `[brackets]`.

---

<!-- 
TEMPLATE INSTRUCTIONS:
- One page per resource, class, or logical grouping of related methods
- Keep prose minimal — this is a lookup document
- Every parameter gets a row in the table, even optional ones
- Use sentence case for field descriptions
- Omit sections that don't apply rather than leaving empty tables
-->

# [Resource name]

[One-sentence description of what this resource or class represents and what it's used for.]

---

## [Method name]

[One-sentence description of what this method does.]

```[language]
[method signature]
```

### Parameters

| Parameter | Type | Required | Default | Description |
|---|---|---|---|---|
| `[param]` | [type] | Yes / No | — | [Description in present tense, ending in period.] |

### Returns

```ts
{
  [field]: [type];  // [description]
}
```

[Optional: short prose explanation if the return structure needs context.]

### Errors

| Code | Meaning |
|---|---|
| `[error_code]` | [Plain English explanation of when this occurs.] |

### Example

```[language]
[Minimal, runnable example showing the most common use case. Use sample data from naming conventions.]
```

---

## [Next method name]

[Repeat the method block for each method in this class or resource group.]

---

## Related

- [Link to relevant concept page]
- [Link to related how-to guide]
- [Link to related reference page]
