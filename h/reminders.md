# How Reminders Work

Headcount Buddy handles three kinds of reminders automatically — nudges to players about upcoming events, availability check-ins for flexible scheduling, and alerts to you when headcount is off. Here's what each one does and when you'll see it.

---

## 1. RSVP reminders for scheduled events

### What players receive (and when)

As an event approaches, the assistant texts players who still need to reply — without you having to chase anyone. The nudge schedule is fixed to the event's start time:

- **One week out** — players who haven't replied yet (or said maybe) get a friendly heads-up that the event is coming.
- **Three days out** — same group gets a follow-up with the current confirmed headcount, giving them context to make a decision.
- **Forty-eight hours out** — a more direct nudge to anyone still uncommitted, with a clear signal that a reply is needed soon.

Players who have already said **yes** are not asked to re-confirm at the early checkpoints. At forty-eight hours they receive a warm "see you there" message with the event details — just a reminder of what's happening, not a request to respond again.

**Example — a player who said yes:**
> *Headcount Buddy:* Hey Priya — just a heads-up, Saturday's scrimmage at Riverside Tennis Club is in two days. You're all set. See you there!

**Example — a player who hasn't replied:**
> *Headcount Buddy:* Hi Marcus — just checking in on Saturday's scrimmage at Riverside (2pm). Are you in? Reply YES, NO, or MAYBE.

**Example — a player who said maybe:**
> *Headcount Buddy:* Hi Jordan — Saturday's scrimmage is in 3 days and we have 6 confirmed so far. You're still down as a maybe — can you lock in a yes or no?

No one needs to install anything. Players just reply to a text. The assistant keeps a cushion between reminders to the same person for the same event, so no one gets bombarded.

> Reminders — like all messages — are sent during reasonable local hours. The full timing rules are covered on the message-timing page.

### Sending a reminder yourself

You don't have to wait for the automatic schedule. At any point you can ask the assistant to send a reminder on demand:

- **Everyone:** *"Remind everyone about Saturday's practice."*
- **A specific group:** *"Remind the maybes for Thursday."*
- **One person by name:** *"Nudge Victor about the scrimmage."*

**Example exchange:**
> *You:* Remind the maybes for Saturday.
> *Headcount Buddy:* On it — queued reminders for 3 players (Amol, Jordan, and Reina). One note: Marcus was reminded a couple hours ago, so I held off on him. Want me to send his anyway?
> *You:* Yeah, go ahead.
> *Headcount Buddy:* Done — sent to Marcus too.

When you name a specific person, the assistant sends to them right away regardless of how recently they were last messaged about that event. When you send to a group by status, normal spacing rules apply — and the assistant will tell you if anyone was skipped and offer to send anyway.

### The organizer check-in when you're short

Separate from the player nudges, the assistant watches your headcount and checks in with **you** when an event is still short close to start:

**About twelve hours before the event**, if you still don't have enough players, the assistant sends you a message:

> *Headcount Buddy:* Saturday's scrimmage is still 2 players short and starts in 12 hours. Want me to look for subs, or would you rather cancel or run short?

If there are still **six or more hours** until start, you'll be offered the option to find substitutes or cancel. Inside that window, finding subs in time becomes less feasible, so the assistant instead asks whether to cancel or go ahead short.

This check-in only goes to you — players don't see it — and it only fires if the event is still below your target at that point.

---

## 2. Availability check-ins

### The weekly check-in (for players)

When you're building a flexible or "find a time" event, every player on the roster gets a weekly text asking about their availability. They can reply directly or update their personal availability page — either way counts.

**Example:**
> *Headcount Buddy:* Hey Sam — which days work for you next week? Reply with the days that work, or tap here to update your availability.

The assistant doesn't flood anyone. Each person has a daily cap on how many availability asks they receive, and if someone was already asked about a span recently, a duplicate ask is suppressed automatically.

If a player keeps ignoring the check-in week after week, the cadence backs off — less frequent asks, then none from the automated schedule. A player can also turn it off directly:

> *Sam:* Stop the weekly check-in.
> *Headcount Buddy:* Got it — I won't send you automatic availability check-ins anymore.

### When the organizer asks on demand

Even if a player has turned off automatic check-ins, you can still reach them by asking the assistant to check availability on your behalf:

> *You:* Ask everyone about next week's availability.
> *Headcount Buddy:* On it — sending availability asks for next week to the roster. What works for you?

When this comes from you, the message players receive makes that clear:

> *Headcount Buddy:* Hi Ravi — Hugo asked me to check on availability for this week. Which days work for you?

Notice that the assistant also asks **you** for your own times in the same reply — since you're on the roster too, your availability matters for the scheduling picture.

### On-demand reminders for flexible events

If you've already sent out availability asks and some people still haven't replied, you can ask the assistant to follow up with just the non-responders:

> *You:* Remind the people who haven't sent their availability.
> *Headcount Buddy:* Sent follow-ups to 4 people who haven't replied yet. (Skipped Priya and Sam, who already answered.)

The assistant re-sends each person the specific question they still owe — the original "when are you free?" for anyone who never responded, or the more focused "does this window work?" for anyone who was asked about a particular time and hasn't answered.

For a match against another team, you can also send an on-demand reminder that re-sends each non-responder the question they still owe.

---

## 3. Headcount alerts to you

### How the alert schedule works

Alongside the player nudges, the assistant runs a separate track just for you: periodic headcount checkpoints that flag when your event is over- or under-subscribed.

The checkpoints run at these hours before the event's start time:

| Hours before start | What triggers an alert |
|---|---|
| **72 hours** | Only if the event is *over-subscribed* (too many yes RSVPs) |
| **36 hours** | First time a *short* headcount can trigger an alert |
| **24 hours** | Re-checks; alerts again if still off |
| **16 hours** | Re-checks; alerts again if still off |
| **~12 hours** | The organizer check-in described above (short-only) |

**A few things to know:**

- **You won't hear about a shortfall before 36 hours out.** Far in advance, no news is normal — the player reminders are still working. If you're curious, just ask: *"What's the headcount for Saturday?"* and you'll get a live count.
- **The over-subscription alert starts earlier (72 hours)** because having too many players confirmed is something you may want to act on before the reminders have fully run.
- **After the 36-hour window opens**, each checkpoint re-checks and sends you a fresh alert if the count is still off.
- **The final checkpoint always fires** if you're still short or over.

**Example — short headcount alert:**
> *Headcount Buddy:* Heads-up: Thursday's practice is still 2 players short (6 confirmed, need 8). It starts in 24 hours. Let me know if you want to reach out to anyone.

**Example — over-subscribed alert:**
> *Headcount Buddy:* Just a heads-up: Saturday's scrimmage has 14 confirmed but you've got room for 12. Want me to put someone on the waitlist?

### Alerts triggered by RSVPs

You don't have to wait for a scheduled checkpoint. If an RSVP comes in between checkpoints and it changes the picture — pushing you over your target or dropping you below it — the assistant reads the live state and flags it to you right away.

---

## Quick reference

| Reminder type | Who receives it | Automatic? | On demand? |
|---|---|---|---|
| RSVP nudges (1 week, 3 days, 48 hours) | Unsettled players | ✓ | ✓ |
| "See you there" heads-up (48 hours) | Players who said yes | ✓ | — |
| Short-event organizer check-in (~12 hours) | You | ✓ | — |
| Weekly availability check-in | Players | ✓ | ✓ |
| Non-responder availability follow-up | Players who haven't replied | — | ✓ |
| Headcount alerts | You | ✓ | — |

---

Questions or want to get your team set up? Reach out at **help@headcountbuddy.com**.
