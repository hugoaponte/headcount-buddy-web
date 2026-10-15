# How Reminders Work

Headcount Buddy takes care of most reminders on its own — nudging players who haven't committed, confirming the people who are in, and alerting you when a headcount problem needs your attention. Here's what fires automatically, what you can trigger yourself, and what to expect when.

---

## Part 1: RSVP Reminders for Scheduled Events

### Who gets nudged, and when

For practices, scrimmages, and other scheduled events, the assistant automatically nudges anyone who hasn't fully committed — that means people who haven't replied at all, or who answered with a "maybe" or something soft. The nudges go out around two days before the event and again the day before. No action needed from you.

Players who already said YES don't get asked again. Instead, once the event has the players it needs, they get a friendly "it's on, see you there" text as the event approaches — not a re-confirmation request.

> **Example — player who hasn't replied:**
>
> *Headcount Buddy → Jordan:* "Hey Jordan — scrimmage at Riverside Tennis Club is Saturday at 10am and we still need your answer. Are you in? YES / NO / MAYBE"
>
> *Headcount Buddy → Alex (who said YES, event is set):* "Good news — Saturday's scrimmage is on! See you at Riverside at 10am."

### The "it's on" text and the event page

Every "it's on" confirmation ends with a link to a page for that specific event. Open your own link — don't use one someone forwarded, and note the link stops working a while after the event.

The event page shows the kind of event, the team, the date and time, the location, any notes, and who's in (you're listed first; subs are marked), along with the current count — for example, "4 of 4." The page is read-only; you can't change your RSVP from it. If the event has been canceled, it shows as canceled.

**Group chat.** The event page has a "Start a group chat" button. Tap it and your phone opens a group message addressed to everyone else who is in — handy for day-of logistics like "running 10 late" or "court 3, not 5." Headcount Buddy is not in that thread and sends nothing into it; it's entirely your own conversation.

Group chat is on for a team unless the organizer turns it off (there's a "Group chat" setting on the team's admin page). The button shows as greyed out — with a reason — when it's off for the team, when you're not counted in, or when nobody else has a number to text. If a sub from another team is in the event, they're included only while their own team's group chat setting is also on. The page names anyone the group text leaves out, and why.

### Matches are different

League matches get **no automatic nudges at all.** The roster is generally settled before match day, so a "you're still a maybe for Saturday's match" text would just be noise. When you want players to respond, you send the reminder yourself (more on that below). Players who are confirmed still get the "it's on, see you there" text as the match approaches. For everything about how match reminders work, see the matches page.

### Sending a reminder yourself

You can always ask the assistant to send a reminder on demand — to everyone, to a specific group, or to one player by name.

> *You:* "Remind the maybes about Saturday."
> *Headcount Buddy:* "Done — nudged 3 players who were on the fence for Saturday's scrimmage."

> *You:* "Nudge Marcus."
> *Headcount Buddy:* "Sent Marcus a reminder for Saturday."

> *You:* "Remind everyone for Thursday's practice."
> *Headcount Buddy:* "Queued reminders for 7 players. Skipped Dana — she was just reminded a few hours ago. Want me to send her one anyway?"

If someone was already reminded recently, the assistant will tell you and offer to send anyway. Just say yes and it will.

### What players experience

Players get a plain text message — nothing to install, no account to create. The assistant keeps a reasonable gap between reminders to the same person for the same event, so no one feels badgered. All reminders (like all messages from the assistant) are held to sensible local hours and never sent back-to-back; the full details on timing live on the message-timing page.

---

## Part 2: Availability Check-ins for Flexible Events

When you're trying to find a time that works — rather than filling slots for a fixed event — the assistant has its own reminder track.

### The weekly check-in

Each week, players get a text asking which days work for them. They can reply by text or tap through to their personal availability page; either counts. The assistant learns from their answers and uses them to help you find times that work for the group.

If someone keeps ignoring the weekly check-in, the assistant backs off — fewer asks, and eventually none at all — so people who genuinely aren't active aren't pestered. A player can also turn off the automated check-in entirely by texting something like "stop the weekly check-in."

### The organizer's on-demand ask

You can ask the assistant to check on availability for a specific span at any time. That ask goes out with your name attached:

> *Headcount Buddy → Priya:* "Marcus asked me to check on availability for this week — which days work for you?"

This reaches everyone, including players who've turned off the automated weekly check-in. The per-person daily cap and recent-ask guard still apply, and the assistant will name anyone it skips and why.

**When you ask, the assistant will also ask for your own availability** — it won't just quietly pass over you because you're the one asking.

### Reminders for outstanding availability questions

If you've already sent out an availability ask and some players still haven't answered, you can ask the assistant to nudge them:

> *You:* "Remind the people who haven't sent their availability."
> *Headcount Buddy:* "Re-sent the availability question to 4 players who haven't answered yet."

The assistant re-sends each person the exact question they still owe — not a generic reminder — and skips anyone who's already responded.

For matches against another team, you can similarly send an on-demand reminder that re-asks each non-responder for the answer they still owe.

---

## Part 3: Headcount Alerts to You (the Organizer)

Player nudges and organizer alerts are separate tracks. The player nudges chase RSVPs; the alerts below tell *you* when the numbers are off so you can decide what to do.

### The alert schedule

Alerts run on their own checkpoint schedule, measured in hours before the event's start time. (An alert for a morning event can arrive the prior evening.) Here's what happens at each one:

| Hours before start | What triggers an alert |
|---|---|
| **72 hours out** | Only if the event is *over-subscribed* — too many people in for the space. No news here means headcount is fine or low; far out, no alert on a shortfall is normal. |
| **36 hours out** | First possible alert for a *short* headcount. This is deliberately after the player nudges have had time to draw responses. |
| **24 hours out** | Re-checks — alerts again if still short. |
| **16 hours out** | Re-checks — alerts again if still short. The final scheduled checkpoint always fires if the count is off. |

If an RSVP changes the picture between checkpoints — someone drops out or signs up — you'll hear about it right away, without waiting for the next scheduled check.

Far out from the event, no news is normal. If you want to know the live count at any time, just ask.

### The near-start check-in (~12 hours out)

If the event is still short about half a day before it starts, the assistant checks in with you directly:

- **If there's still time to find people** (roughly 6 hours or more to go): the assistant offers to find substitutes or cancel.
- **If it's too late to reliably fill spots**: the assistant asks whether you'd like to cancel or run short.

> *Headcount Buddy → You:* "Saturday's scrimmage is still 2 players short with about 12 hours to go. Want me to look for subs, or would you prefer to cancel?"

This check-in is separate from all the player nudges and only happens when the event hasn't reached its target.

---

## Quick Reference

| What fires automatically | Who it goes to |
|---|---|
| RSVP nudges ~2 days and ~1 day before a scheduled event | Players who haven't fully committed (not matches) |
| "It's on, see you there" as event approaches | Players who said YES, once event is set |
| Headcount over-subscription alert (72 hours out) | Organizer |
| Headcount shortfall alerts (36, 24, 16 hours out) | Organizer |
| Near-start check-in if still short (~12 hours out) | Organizer |
| Weekly availability check-in | Each player (backs off if ignored; can be turned off) |

| What you can trigger yourself | How to ask |
|---|---|
| Remind everyone / the maybes / one player by name | "Remind everyone for Saturday" / "Nudge the maybes" / "Remind Marcus" |
| Send an availability ask on your behalf | "Ask everyone when they're free this week" |
| Nudge players with outstanding availability questions | "Remind the people who haven't answered yet" |
| Get the live headcount | "How many are in for Thursday?" |

---

Questions? Reach out at help@headcountbuddy.com.
