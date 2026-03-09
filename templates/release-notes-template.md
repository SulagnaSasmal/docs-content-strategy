# Template: Release Notes

Copy this template for each release. Use one file per release (or one H2 per release in a running changelog, depending on your toolchain). Replace all placeholder text in `[brackets]`.

---

<!--
TEMPLATE INSTRUCTIONS:
- Release notes are for USERS, not the development team — write from the perspective of "what does this mean for someone using the product"
- Every breaking change gets a migration note and a link to a migration guide
- "Fixed" items should state the symptom the user experienced, not the internal bug description
- Omit sections that don't apply rather than writing "None"
- If a change requires user action, make that explicit — bold it, put it first, or use an "Action required" header
- Alphabetize within sections when there are more than 5 items
-->

# [Product name] [version] — [Month Year]

[Optional 1–2 sentence summary for releases with a clear theme or important headline change. Skip for minor/patch releases.]

---

## Action required

<!--
Use this section ONLY when the user must do something before or after upgrading — configuration change, migration, deprecated feature removal, etc.
-->

- **[Breaking change short name]:** [What the user must do and by when. Link to migration guide.]

---

## New features

### [Feature name]

[1–3 sentences: what this feature is, what problem it solves, and how to use it (or where to find the documentation). Do not paste the feature spec — synthesize.]

See [Feature documentation link](link).

### [Feature name]

[Repeat as needed.]

---

## Improvements

- **[Area or component]:** [What changed and what the user will notice. One sentence per item.]
- **[Area or component]:** [Description.]

---

## Fixed

- **[User-visible symptom]:** [What was happening and that it's now resolved. Name the version it was introduced in if known and relevant.]
- **[User-visible symptom]:** [Description.]

---

## Deprecated

- **[Feature or field name]:** Deprecated in [version]. Will be removed in [version]. [Migration path or replacement.]

---

## Known issues

- **[Issue short description]:** [What happens. Workaround, if one exists. Expected fix version, if known.]

---

## Upgrade notes

[If upgrading from the previous version requires steps beyond updating the package version, list them here. Link to a full migration guide if the steps are extensive.]

```bash
[Upgrade command]
```

[Any configuration changes required.]
