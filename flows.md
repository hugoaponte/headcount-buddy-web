---
title: Headcount Buddy — example message flows
---

# Example message flows

These are sample conversations between Headcount Buddy and a player or an organizer (a team captain, coach, club manager, or scrimmage organizer — whoever runs the group). Anything you receive from us will look like one of these patterns. We never send proactive messages to a player who has not first texted `START`.

This page is split in two sections, both listed below: **basic flows** cover opt-in, opt-out, and account management — these are implemented today and govern every interaction with Headcount Buddy. **Functional flows** show what the service will do once a player is enrolled — these describe the design and are not yet implemented.

In the examples below we use "Mike" as the organizer (in his case, a USTA tennis captain) and "Bob" as a player. The same flows apply whether Mike is a formal team captain, a softball coach, or someone who organizes Saturday pickup tennis.

In the transcripts below:

- **Player / Organizer →** is a message *from* a person *to* Headcount Buddy.
- **Headcount Buddy →** is our reply.

---

## Basic flows — opt-in and account management

These flows are implemented and govern every interaction with the service.

### Player joins the service

Bob's captain Mike has told Bob to text the team's Headcount Buddy number to opt in.

> **Bob →** hello
>
> **Headcount Buddy →** Hi! I'm Headcount Buddy, an agent for sports groups. When your organizer adds you, I'll text about games, scrimmages and other events. Reply START to opt in. Reply HELP for help, STOP to opt out. Msg & data rates may apply.
>
> **Bob →** START
>
> **Headcount Buddy →** You're in — Headcount Buddy. I'll text you about games, scrimmages and other events once your organizer adds you to a group. Msg frequency varies, msg & data rates may apply. Reply HELP for help, STOP to opt out.

After Bob replies `START`, we record his consent. No message is sent to him until that point.

### Captain enrolls a player who hasn't opted in yet

This is the captain's experience. Mike opens his dashboard and adds Bob to the Lake Tigers roster by entering Bob's name and phone number.

- Mike fills in the form and saves.
- **No SMS is sent to Bob.** Bob is in the roster but has no opt-in on record.
- The dashboard shows Bob as "pending — waiting for opt-in."
- Mike tells Bob in person or in their group chat: *"Hey Bob, text START to +1-833-962-0311 to get on the team's RSVP system."*
- Bob does so (see the previous flow).

### Player opts out

Any player can opt out at any time from any state.

> **Bob →** STOP
>
> **Headcount Buddy →** You're opted out of Headcount Buddy. Reply START to resubscribe.

After this, no proactive messages go to Bob unless he texts `START`. The organizer sees his status change in the dashboard.

`STOPALL`, `QUIT`, `UNSUBSCRIBE`, `CANCEL`, `END`, `OPTOUT`, and `REVOKE` all do the same thing as `STOP`.

Note: your mobile carrier may also block messages on top of our own opt-out, and may keep them blocked until you reply `START`. Because of that, the confirmation you actually see for `STOP` (or `START`) may be sent by your carrier rather than by us, and may differ from the wording above. Carrier behavior varies and we don't control it.

### INFO / HELP

> **Bob →** INFO
>
> **Headcount Buddy →** Headcount Buddy helps sports groups coordinate games, scrimmages and other events. Got feedback or a problem with the service? Just text it here and I'll pass it to our team. Terms: <site>/legal/terms  Privacy: <site>/legal/privacy  More: <site>/info  Msg & data rates may apply. Reply STOP to opt out.

`HELP` works the same way. (The feedback line appears once you're opted in — it's how you reach the team that builds the service.)

### Sending feedback

Once opted in, you can text feedback in plain words — no special keyword. It goes to the team that builds Headcount Buddy, not to your organizer.

> **Bob →** the reminders come way too late to be useful, would love them the night before
>
> **Headcount Buddy →** Thanks Bob — I've passed that along to our team. Appreciate you flagging it.

### ALPHA tester signup (alpha-period only)

While Headcount Buddy is in early development, anyone can request to be on the alpha tester list.

> **Jane →** ALPHA
>
> **Headcount Buddy →** You're on the Headcount Buddy alpha list — we'll text you when we open up. Msg frequency varies, msg & data rates may apply. Reply HELP for help, STOP to opt out.

Texting `ALPHA` also counts as opt-in, so we can text the tester back when alpha access opens up. `ALPHA` works unless you're *currently* opted out — if you've opted out, reply `START` to come back first, then `ALPHA`.

### Quick reference

| Reply | What happens |
|---|---|
| `START` / `UNSTOP` | Opt in to receive messages (or re-opt-in after a previous opt-out). |
| `ALPHA` | Opt in AND request the alpha tester list — works unless you're currently opted out. |
| `STOP`, `STOPALL`, `QUIT`, `UNSUBSCRIBE`, `CANCEL`, `END`, `OPTOUT`, `REVOKE` | Opt out. We will not text you again until you reply `START`. |
| `INFO`, `HELP` | Receive a summary + links to this site. |
| Anything else | We reply based on what we know about you. If you're not yet opted in, we'll prompt you to. |

---

## Functional flows — what the service does once enrolled (not yet implemented)

These describe the operational work the service will handle for enrolled, opted-in players. They are part of the product design and not yet running.

### RSVP request and response

This is what we expect a typical RSVP exchange to look like once the assistant ships.

> **Headcount Buddy → Bob:** Hi Bob! Lake Tigers practice this Sat 10/12 at 9am, City Park courts. Reply YES, NO, or MAYBE. Or tell me anything else — happy to relay to Mike.
>
> **Bob →** yes
>
> **Headcount Buddy →** Got it, you're in for Saturday. See you there.

A more nuanced reply also works:

> **Headcount Buddy → Bob:** Hi Bob! Lake Tigers practice this Sat 10/12 at 9am, City Park courts. Reply YES, NO, or MAYBE.
>
> **Bob →** yes, but I can skip if you've got enough people
>
> **Headcount Buddy →** Got it — you're a yes, willing to skip if we have plenty. I'll let Mike know if it gets tight.

### Headcount management

The captain is informed about state and can give instructions.

> **Headcount Buddy → Mike:** Just got one more RSVP — Saturday's practice is on with 5 players for 2 courts.
>
> **Mike →** Let's do one court only.
>
> **Headcount Buddy →** On it. Bob is a yes but said he'd skip if needed — asking him now.
>
> *(A minute later)*
>
> **Headcount Buddy → Mike:** Done. Bob is skipping. We have 4 for one court.

---

**⚠️ Early development.** Headcount Buddy is in active development and not yet generally available. The service may be intermittent (responses delayed or unavailable) and may contain bugs.
