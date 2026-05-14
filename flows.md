---
title: Headcount Buddy — example message flows
---

# Example message flows

> **⚠️ Early development.** These flows describe the system as designed. Each flow below is marked as **implemented** or **planned**. The service may be intermittent during this period.

These are sample conversations between Headcount Buddy and a player or captain. Anything you receive from us will look like one of these patterns. We never send proactive messages to a player who has not first texted `JOIN`.

In the transcripts below:

- **Player / Captain →** is a message *from* a person *to* Headcount Buddy.
- **Headcount Buddy →** is our reply.

Each flow is implemented or planned as noted.

---

## Flow 1 — Player joins the service (implemented)

Bob's captain Mike has told Bob to text the team's Headcount Buddy number to opt in.

> **Bob →** hello
>
> **Headcount Buddy →** Hi! I'm Headcount Buddy, an SMS helper for sports teams. When your captain adds you, I'll text about RSVPs & headcount. Reply JOIN to opt in, INFO for details, STOP anytime. Msg & data rates may apply.
>
> **Bob →** JOIN
>
> **Headcount Buddy →** You're in. I'll text you when your captain adds you to a roster, and about RSVPs & headcount once you're on one. Reply STOP anytime to opt out.

After Bob replies `JOIN`, we record his consent. No message is sent to him until that point.

---

## Flow 2 — Captain enrolls a player who hasn't opted in yet (implemented)

This is the captain's experience. Mike opens his dashboard and adds Bob to the Lake Tigers roster by entering Bob's name and phone number.

- Mike fills in the form and saves.
- **No SMS is sent to Bob.** Bob is in the roster but has no opt-in on record.
- The dashboard shows Bob as "pending — waiting for opt-in."
- Mike tells Bob in person or in their group chat: *"Hey Bob, text JOIN to +1-833-962-0311 to get on the team's RSVP system."*
- Bob does so (see Flow 1).

---

## Flow 3 — RSVP request and response (planned, not yet implemented)

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

---

## Flow 4 — Headcount management (planned, not yet implemented)

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

## Flow 5 — Player opts out (implemented)

Any player can opt out at any time from any state.

> **Bob →** STOP
>
> **Headcount Buddy →** You're opted out of Headcount Buddy. We won't text you again. Reply JOIN to resubscribe.

After this, no proactive messages go to Bob ever again unless he texts `JOIN`. The captain sees his status change in the dashboard.

`STOPALL`, `QUIT`, `UNSUBSCRIBE`, `CANCEL`, and `END` all do the same thing as `STOP`.

---

## Flow 6 — INFO / HELP (implemented)

> **Bob →** INFO
>
> **Headcount Buddy →** Headcount Buddy helps sports teams coordinate RSVPs & headcount by SMS. Terms: <site>/legal/terms  Privacy: <site>/legal/privacy  More: <site>/info  Reply STOP to opt out.

`HELP` works the same way.

---

## Flow 7 — ALPHA tester signup (implemented, alpha-period only)

While Headcount Buddy is in early development, anyone can request to be on the alpha tester list.

> **Jane →** ALPHA
>
> **Headcount Buddy →** You're on the Headcount Buddy alpha list. We'll text you when we open up. Reply STOP anytime to opt out, INFO for details.

Texting `ALPHA` also counts as opt-in (`last_consent_sms_at` is recorded), so we can text the tester back when alpha access opens up.

---

## Quick reference

| Reply | What happens |
|---|---|
| `JOIN` | Opt in to receive messages (or re-opt-in after a previous opt-out). |
| `ALPHA` | Opt in AND request to be on the alpha tester list. |
| `STOP`, `STOPALL`, `QUIT`, `UNSUBSCRIBE`, `CANCEL`, `END` | Opt out. We will not text you again. |
| `INFO`, `HELP` | Receive a summary + links to this site. |
| Anything else | We reply based on what we know about you. If you're not yet opted in, we'll prompt you to. |
