---
description: >
  Use Qualia's Recipient Intelligence tools when composing messages, emails,
  or outreach for a specific person. Triggers on: "draft a message to [person]",
  "write an email to [name]", "adapt this for [recipient]", "how should I
  communicate with [name]", or any request involving writing to or for a
  specific named individual. Use when recipient context matters — not for
  generic writing tasks.
---

# Qualia — Recipient Intelligence

You have access to three Qualia MCP tools. Use them in sequence when composing
for a specific recipient.

## Workflow

**Step 1 — Profile the recipient** (`qualia_profile_person`)
Call this first with a sample of the recipient's writing (emails, messages,
LinkedIn posts) or their name if interaction history exists. Returns their
communication archetype, preferred information density, tone register, and
relationship state.

**Step 2 — Adapt the draft** (`qualia_adapt_message`)
Pass the draft message and the recipient profile from Step 1. Returns a
structurally adapted version — not surface-level rewording, but actual
reordering and reframing toward how this person processes information.

**Step 3 — Analyze or draft a reply** (`qualia_analyze_message` / `qualia_draft_reply`)
Optional but useful for inbound messages. `qualia_analyze_message` classifies
intent, tone, and risks of an incoming message. `qualia_draft_reply` returns
a full intelligence packet for crafting a response — start here for replies.

## Behavioral rules

- Always run Step 1 before Step 2. Adapting without a profile is generic
  rewriting, not Recipient Intelligence.
- If the user provides text samples from the recipient, pass them directly
  to `qualia_profile_person` — don't summarize.
- Describe profiling outputs in plain language, not technical or framework terms.
- If the recipient is unknown (cold contact, no writing sample), say so
  clearly: cold-contact profiling is thinner and the adapted output should
  reflect that.
- Keep the adapted message in the user's voice, not a generic "professional"
  voice. Ask for a sample of the user's own writing if voice fidelity matters.

## Authentication

First-time use prompts OAuth sign-in to qualiaai.co. A Qualia account is
required. API documentation and sandbox: qualiaai.co/developers
