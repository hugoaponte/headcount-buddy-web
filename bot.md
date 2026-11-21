---
title: HCBBot
---

# HCBBot

HCBBot is Headcount Buddy's web crawler. If you saw `HCBBot` in your server logs, this page says who we are, how we crawl and how to reach us.

## What it reads

A small number of public websites with sports results and schedules, for the teams and players who use Headcount Buddy. It reads only public pages, never anything behind a login.

## How it crawls

- One request at a time, spaced well apart, with a daily limit.
- It reads `robots.txt` first and follows it, including any crawl delay it asks for.
- It slows down when asked (a `429` or a `Retry-After`) and backs off when a site is slow or unavailable.
- A page it has read recently comes from our own copy instead of being asked for again.
- If a site answers that it does not want us (`401`, `403` or `451`), the crawler stops completely, and a person on our team looks at it before anything is asked again.

Every request carries our name in its `User-Agent` and our address in its `From` header.

## Contact

Write to [help@headcountbuddy.com](mailto:help@headcountbuddy.com). If you run a site we read and want us to slow down or stop, tell us and we will.
