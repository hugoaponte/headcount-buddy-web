---
title: HeadcountBuddyBot
---

# HeadcountBuddyBot

HeadcountBuddyBot is the crawler behind Headcount Buddy's tennis reports. If you saw `HeadcountBuddyBot` in your server logs, this page says who we are, what we read and how to reach us.

## What it reads

Public USTA league pages on tennisrecord.com: team pages, match results and players' public match histories, for teams in the USTA Pacific Northwest section. We use them to write match and lineup reports for the captains and players of those teams. We do not read anything behind a login.

## How it reads

- One request at a time, at least 30 seconds apart, and never more than a set number of pages in a day.
- It reads `robots.txt` first and follows it, including any crawl delay it asks for.
- It slows down when asked (a `429` or a `Retry-After`) and backs off when the site is slow or unavailable.
- A page it has read recently is served from our own copy instead of being asked for again.
- If the site answers that it does not want us (`401`, `403` or `451`), the crawler stops completely, and a person on our team looks at it before anything is asked again.

Every request carries our name in its `User-Agent` and our address in its `From` header.

## Contact

Write to [help@headcountbuddy.com](mailto:help@headcountbuddy.com). If you run a site we read and want us to slow down or stop, tell us and we will.
