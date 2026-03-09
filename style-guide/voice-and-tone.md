# Voice and Tone

This guide defines the editorial voice for all product documentation. Voice is who we are as communicators — it's consistent. Tone is how we adjust to context — it varies.

---

## Voice

Our documentation voice has four characteristics:

### 1. Direct

Don't warm up to the point. Lead with what the user needs. Cut filler phrases that add length without adding meaning.

| Instead of | Write |
|---|---|
| "In order to get started, you will need to..." | "To get started," |
| "Please note that the following behavior may occur..." | State the behavior directly |
| "It is worth mentioning that..." | State it |

### 2. Precise

Use specific, accurate language. Avoid hedging with vague approximations when the correct detail is available.

| Instead of | Write |
|---|---|
| "The API returns some data about the user" | "The API returns the user's name, email, and account status" |
| "This might cause issues" | "This causes a 401 error" |
| "soon" / "shortly" / "later" | Use a version number, date, or specific condition |

### 3. Instructional

Documentation exists to help someone do something. Keep the user's task in frame, not the product's architecture.

| Instead of | Write |
|---|---|
| "The system processes payments using a two-phase commit protocol" | "When a payment fails, you receive a `payment.failed` webhook event" |
| "Our platform supports multiple authentication methods" | "You can authenticate with an API key, OAuth 2.0, or a session token" |

### 4. Respectful of the user's time

Assume the user is competent and in a hurry. Do not over-explain obvious concepts, add disclaimers for edge cases that rarely happen, or repeat information that's a click away.

---

## Tone by context

Voice stays constant. Tone adjusts based on what the user is doing.

| Context | Tone | Example |
|---|---|---|
| Getting started / quickstart | Encouraging, brisk | "You now have a working integration. Here's what to try next." |
| API reference | Neutral, precise | "Returns 200 on success. Returns 404 if the resource does not exist." |
| Error messages / troubleshooting | Calm, helpful | "This usually means the API key is missing its required scope. Check..." |
| Warning / destructive action | Clear, serious | "This action is permanent. Deleted data cannot be recovered." |
| Release notes | Factual, compact | "Fixed: pagination cursor no longer resets after filtering." |

Avoid:
- Enthusiastic marketing language in technical content ("Best-in-class!", "Seamlessly")
- Excessive apology in error messages ("We're sorry, but unfortunately...")
- Condescension disguised as helpfulness ("Simply do X", "Just add Y")

---

## Person and pronoun

| Context | Use |
|---|---|
| Instructions, procedures | Second person: "you" |
| Product behavior | Third person or passive: "the API returns", "the file is created" |
| Referring to our company/product | Third person: "NexaFlow", "the SDK" — not "we sent you" in reference docs |

Do not use first person plural ("we", "our") in technical reference content. It reads as marketing and makes the docs feel like they speak for the company rather than helping the user.

---

## Contractions

Use contractions in instructional and conceptual content where they make the writing feel natural: "you'll", "it's", "don't", "you're".

Avoid contractions in API reference, warning notices, and legal or compliance content, where precision matters more than conversational tone.

---

## Inclusive language

| Avoid | Use instead |
|---|---|
| "master" / "slave" | "primary" / "replica" or "main" / "secondary" |
| "whitelist" / "blacklist" | "allowlist" / "blocklist" |
| "dummy" data | "example" or "sample" data |
| Gendered pronouns for hypothetical users | "they / their" or restructure to avoid |
| "simple", "easy", "just", "only" | Remove or rephrase — what's simple to one person is a blocker to another |

---

## Reading level

Target a 7th–9th grade reading level for conceptual and instructional content. Use a tool like Hemingway Editor to check. API reference content naturally reads higher — that's acceptable, but avoid unnecessary complexity in sentences describing what a field does.

Test your content against this question: could a competent developer who doesn't speak English as their first language understand this without ambiguity?
