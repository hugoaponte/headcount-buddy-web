# Headcount Buddy

An agent for organizers of amateur sports groups — team captains, club managers, coaches, and the people who run pickup games and scrimmages. Initially available through SMS; WhatsApp, iMessage, and email planned for later.

We handle the operational chaos of getting players to events — RSVPs, headcount, who's confirmed for Saturday's match or scrimmage — so organizers stop chasing texts and players have a frictionless experience. Players never install an app: they text our number, the agent texts them back.

Read more [about headcount buddy](h/about.md) and how it [works](index.md).

---

## What this is, technically

Headcount Buddy is a messaging AI assistant, currently enabled on SMS, powered by:

- **Anthropic** — Claude Code as the sidekick for code generation; the Anthropic SDK + Sonnet 4.6 + API powering the agent that reads inbound messages and decides what to do or say. Sonnet also runs in a pipeline to generate the [help docs](h/index.md) from the code.
- **Voyage AI** — text embeddings powering retrieval (RAG) over the public help docs, so the agent answers "how does X work?" from the docs.
- **APScheduler** — handling time-triggered events (RSVP reminders, headcount checkpoints, payment relay).
- **Twilio** — SMS delivery (inbound webhooks for replies).
- **Python + FastAPI** — the backend service.
- **PostgreSQL** — durable state: teams, rosters, events, RSVPs, message history, consent records.

## AI usage and limits

Headcount Buddy uses an AI language model to generate responses. The AI is not always right. Organizers should sanity-check anything important — schedule confirmations, communications about a specific player, etc. We log every model decision so anything weird can be traced back and reviewed.

Player data sent to Anthropic for processing is not used to train Anthropic's models, per their commercial terms. See the [privacy policy](legal/privacy.md) for full data-sharing details.

## Status

In active development. Running a small private pilot with tennis scrimmage groups and USTA tennis teams in 2026. Not generally available yet. This repository holds the public documentation only; the application code is not publicly available.

## Policies and info

- [Privacy policy](legal/privacy.md)
- [Terms of service](legal/terms.md)

## Contact

**help@headcountbuddy.com** — questions, feedback, or to be notified when we open up more broadly.

---

**⚠️ Early development.** Headcount Buddy is in active development and not yet generally available. The service may be intermittent (responses delayed or unavailable) and may contain bugs.
