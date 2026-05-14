# Headcount Buddy

An SMS helper for amateur sports teams.

> **⚠️ Early development.** Headcount Buddy is in active development and not yet generally available. The service may be intermittent (responses delayed or unavailable) and may contain bugs. To be added to the alpha tester list, **text `ALPHA` to +1 (833) 962-0311**.

We handle the operational chaos of running a team — RSVPs, headcount, who's confirmed for Saturday's match — so captains stop chasing texts and players have a frictionless experience. Players never install an app: they text our number, the assistant texts them back.

## Who this is for

Captains and managers of amateur sports teams. Starting with USTA tennis, expanding to softball, pickleball, and similar in 2026. The captain is the buyer and primary user; teammates are passive beneficiaries who interact entirely via SMS.

## How it works

- A team captain enrolls their team and players (name, phone) in a simple dashboard.
- Each player texts `JOIN` to the team's Headcount Buddy number to opt in. Captains tell players the number directly — we never text anyone before they've opted in.
- Once a player has opted in and a captain has added them to a roster, the assistant texts them about practices, matches, and headcount.
- Anyone can text `STOP` at any time to opt out, or `INFO` to see this page.

See [`flows.md`](flows.md) for example conversations.

## What this is, technically

Headcount Buddy is a single SMS-first AI assistant powered by:

- **Anthropic Claude (`claude-sonnet-4-6`)** — the language model that reads inbound messages and decides what to do or say. We use the Claude API directly with tool-use, not an agent framework.
- **Twilio** — SMS delivery (inbound webhooks for replies; toll-free number for the demo period).
- **Python + FastAPI** — the backend service.
- **PostgreSQL** — durable state: teams, rosters, events, RSVPs, message history, consent records.

The assistant has two roles internally — one that handles captain-facing interactions, one for player-facing — both driven by Claude with role-specific prompts. Architecturally separating them makes it easy to constrain what each role is allowed to do.

The product owns the *operational layer* (headcount, comms about events, schedule sync). It is not a scorekeeping app, not a stats app, and not a replacement for the platforms teams already use. We integrate with TeamSnap, GameChanger, and league schedules where it makes sense.

## AI usage and limits

Headcount Buddy uses an AI language model to generate responses. The AI is not always right. Captains should sanity-check anything important — schedule confirmations, communications about a specific player, etc. We log every model decision so anything weird can be traced back and reviewed.

Player data sent to Anthropic for processing is not used to train Anthropic's models, per their commercial terms. See the [privacy policy](legal/privacy.md) for full data-sharing details.

## Status

In active development. Running a small private pilot with USTA tennis teams in 2026. Not generally available yet.

## Policies and info

- [Service info / what messages you'll get](info.md)
- [Privacy policy](legal/privacy.md)
- [Terms of service](legal/terms.md)
- [Example message flows](flows.md)

## Contact

**headcountbuddy@gmail.com** — questions, feedback, or to be notified when we open up more broadly.
