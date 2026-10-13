# Active channels — what the team may produce for

Only produce content for channels marked **live**. Producing for a channel that doesn't exist wastes a
review cycle and clutters the approval queue.

| Channel | Status | Handle / notes |
|---|---|---|
| YouTube (long-form + Shorts) | **live** | @reelmatchapp — the main channel; the studio renders and can upload here |
| YouTube Community posts | **live** | polls between uploads; no API — drafted for manual posting |
| YouTube comment replies | **live · automated** | `community-agent` drafts, you ✅ from Telegram, gateway posts — 10:00 & 18:00 daily |
| Instagram (Reels + captions) | **live** | same Short cross-posted; no API wired yet, so posted manually |
| TikTok | **not yet** | account not created — do NOT generate TikTok items |
| X / Twitter | **not yet** | do NOT generate X items |

## Weekly mix — a week of Shorts, produced in one go

**Every run renders 5 Shorts and schedules them on 5 consecutive days.** Shorts are the app-discovery
engine and the channel needs a daily rhythm, so the office produces a week of them at once rather than
one at a time. One approval tap then covers the whole week.

| Every week | Mix |
|---|---|
| **5 YouTube Shorts** | 5 different titles, one per day on consecutive days, 09:00 |
| 1 Instagram caption | cut from the strongest of the five |
| 1 Community poll | on a day between two Shorts |
| **Long-form** | **even ISO weeks only**, in addition — a Top-5 countdown |

**Render all five in ONE call.** `studio_render_short` takes a list:
`studio_render_short(tmdb_ids=[{id, media_type} × 5])` returns a `shorts[]` array with one entry per
title, each with its own `metadata_file`. Five separate calls waste 4 render start-ups and risk the run
timing out — one call, five videos.

Five distinct titles: never five Shorts about the same film, and never a title that already went out
(check `studio_recent_videos`). Work out the ISO week with `date +%V` to decide whether the long-form
is due, and say so in the run summary. If the user asks for a specific format, that overrides this.

**Long-form is big.** A rendered countdown is 300–900 MB, over Telegram's 50 MB bot-upload cap, so the
approval card carries the **thumbnail** plus a note and a link rather than the video. Review the title,
description, chapters and thumbnail there; watch the video itself in the studio UI at localhost:3456.
A long-form render also takes 5–15 minutes, against 2–6 for a Short — don't kill it.

When a channel moves to live, add it here — the agents read this file, so nothing else needs changing.

## Outreach — live, monthly, not part of the weekly mix

Press pitches, guest posts and resource links to people who have already covered "how do we decide what
to watch". Runs once a month via `RM · 8 Outreach batch`, drafted by `outreach-scout`, rules in
`knowledge/OUTREACH.md`, record in `logs/outreach.jsonl`. The office drafts; the human sends. Do not
produce outreach items in a weekly run.

## Instagram carousels — live, weekly

One carousel a week, on a fixed day, **in place of** that day's single-image queue post, so the posting
volume does not change. The first of each month is the previous month's genre round-up; the other weeks
rotate through the angles in `social/carousel.py` (trending, new, short, hidden, by streaming service).
Rendered by `social.carousel`, hosted on R2, published by `RM · 9 Publish carousel`.

Carousels lead Instagram on engagement and saves; Reels lead on reach. They are complements — the
carousel is for the audience you have, the Reel is for the one you do not.
