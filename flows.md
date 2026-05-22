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
> **Headcount Buddy →** Hi! I'm Headcount Buddy, an agent for sports groups. Reply START to opt in — after that, I'll text you about your group's games, scrimmages and other events. Reply HELP for help, STOP to opt out. Msg & data rates may apply.
>
> **Bob →** START
>
> **Headcount Buddy →** You're in! Headcount Buddy will text you about games, scrimmages and other events once your organizer adds you to a group. Msg frequency varies, msg & data rates may apply. Reply HELP for help, STOP to opt out.

After Bob replies `START`, we record his consent. No message is sent to him until that point.

### Organizer enrolls a player who hasn't opted in yet

This is the captain's experience. Mike opens his dashboard and adds Bob to the Lake Tigers roster by entering Bob's name and phone number.

- Mike fills in the form and saves.
- **No SMS is sent to Bob.** Bob is in the roster but has no opt-in on record.
- The dashboard shows Bob as "pending — waiting for opt-in."
- Mike tells Bob in person or in their group chat: *"Hey Bob, text START to +1 (425) 552-8339 to get on the team's RSVP system."*
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

`INFO` or `HELP` returns a brief summary, the START/STOP keywords, links to Terms/Privacy, and the support email. The same reply ships regardless of your opt-in state — opted in, opted out, or never engaged:

> **Bob →** HELP
>
> **Headcount Buddy →** Headcount Buddy helps sports groups coordinate games, scrimmages and other events. Reply START to opt in, STOP to opt out. Problem or feedback? Just text or email help@headcountbuddy.com. Msg & data rates may apply. <site>/legal/terms <site>/legal/privacy

Once opted in, `HELP` is also where users learn about the feedback channel — anything you text after that is automatically captured. You can email support at any time instead.

### Sending feedback

Once opted in, you can text feedback in plain words — no special keyword required. It goes to the team that builds Headcount Buddy, not to your organizer.

> **Bob →** the reminders come way too late to be useful, would love them the night before
>
> **Headcount Buddy →** Thanks Bob — I've passed that along to our team. Appreciate you flagging it.

### ALPHA tester signup (alpha-period only)

While Headcount Buddy is in early development, organizers interested in running a test group can sign up for our alpha tester list. **`ALPHA` is processed only after you've opted in** — if you text `ALPHA` before opting in, we'll send you the same welcome message as any other unknown reply (asking you to text `START` first). Opt in via `START`, then reply `ALPHA`:

> **Jane →** START
>
> **Headcount Buddy →** You're in! Headcount Buddy will text you about games, scrimmages and other events once your organizer adds you to a group. Msg frequency varies, msg & data rates may apply. Reply HELP for help, STOP to opt out.
>
> **Jane →** ALPHA
>
> **Headcount Buddy →** You're on the Headcount Buddy alpha-tester list — we'll text you when we open up. Reply HELP for help, STOP to opt out.

Texting `ALPHA` a second time confirms you're already on the list without sending duplicate messages later:

> **Jane →** ALPHA
>
> **Headcount Buddy →** You're already on the Headcount Buddy alpha-tester list. We'll text you when we open up. Reply HELP for help, STOP to opt out.

### Quick reference

| Reply | What happens |
|---|---|
| `START` / `UNSTOP` | Opt in to receive messages (or re-opt-in after a previous opt-out). |
| `ALPHA` | Sign up for the alpha-tester list. Processed only after you've opted in; pre-opt-in `ALPHA` is treated like any other unknown reply. |
| `STOP`, `STOPALL`, `QUIT`, `UNSUBSCRIBE`, `CANCEL`, `END`, `OPTOUT`, `REVOKE` | Opt out. We will not text you again until you reply `START`. |
| `INFO`, `HELP` | Receive a summary + links to this site. |
| Anything else | We reply based on what we know about you. If you're not yet opted in, we'll prompt you to. |

---

## Functional flows — what the service does once enrolled (in active development; below is what your experience will look like once we open up the full service)

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

### More flows

We're working on additional coordination flows beyond core RSVP and headcount. We'll add them here as they ship.

---

**⚠️ Early development.** Headcount Buddy is in active development and not yet generally available. The service may be intermittent (responses delayed or unavailable) and may contain bugs.
