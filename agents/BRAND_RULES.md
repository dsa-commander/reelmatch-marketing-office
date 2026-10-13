# ReelMatch Brand & Policy Rules

The Brand Guardian checks every draft against these. Each rule has an ID so rejections can cite it.

## Voice
- **V1** Lead with the pain point: "Stop arguing about what to watch." The app is the punchline, not the pitch.
- **V2** Casual, warm, a little cheeky. Never corporate ("leverage", "seamless", "revolutionary").
- **V3** Talk to couples, roommates, friend groups — people deciding *together*. Never "find your perfect match" (dating connotation).
- **V4** One emoji max in a title, three max in a caption. 🍿 is the house emoji.
- **V5** Always spell it **ReelMatch** (capital R, capital M, one word).

- **V6** The title, first caption line and `thumbnail_text` all carry ONE of the five premises in
  `knowledge/HOOKS.md` (swipe decision, our users decided, date-night decider, trending-vs-ours, argument
  settler). Channel data: trailer-only titles median 5 views. "5 Trailers Coming in September" → REVISE
  with the formula to use. "37 couples agreed on this" with a number from the run's tools → ok. A hook whose
  number does not appear in the tool data → C1, not V6.

## Claims
- **C1** No invented numbers. Only cite figures that came from a tool result in this run (TMDB rating, ReelMatch like/match counts, YouTube analytics).
- **C2** Never claim a title is "on Netflix" etc. unless `watch_providers`/`watch_on` from a tool said so.
- **C3** Never promise features the app doesn't have (see ReelMatch_Product_Context.md for what exists).
- **C4** Pricing is never mentioned in organic content.

## Platform policy
- **P1** YouTube "reused content": every trailer compilation must add transformative value — commentary, ranking rationale, info cards, a ReelMatch angle. Titles/descriptions must reflect that added value, not just "TRAILER".
- **P2** No engagement bait ("like if you agree", "comment 1 or 2"). Community polls are fine.
- **P3** No fake urgency ("only today", "before it's gone") unless a real release date supports it.
- **P4** Hashtags: max 5 on YouTube, max 8 on Instagram/TikTok. Always include #ReelMatch.
- **P5** Nothing that could be read as manipulated engagement or spam (no mass comments, no asking people to comment on other channels' videos).

## Safety / legal
- **S1** Trailers are used under the studios' promotional distribution; never re-host full films or leaked footage.
- **S4 Content ID.** Most rights holders allow their trailer in a compilation; a few **block it
  globally**, and one such trailer takes the whole video down with it — YouTube gives no warning, the
  video simply becomes invisible. Seen 2026-09-25: a 5-film countdown blocked in 249 regions because of
  the **Neagley** trailer alone (the Resident Evil, Monster and Love Hypothesis claims on the same video
  said "no impact"). Rules: never put **Neagley** in a compilation; uploads stay **private with a
  publishAt** so `/youtube/check-blocks` can catch a block before it goes public; if one is found,
  re-render without the claimed title rather than trimming — a trim leaves a jump cut, wrong chapters
  and a title promising more films than the video has. A Short about a single title is far lower risk
  than a compilation, because there is only one claimant to please.
- **S2** No user data, user names, or anything identifying a ReelMatch user in any content. Aggregates only ("hundreds of couples matched on…").
- **S3** No content about titles rated for adults only (TMDB `adult: true`).

## Output contract
Verdict must be one of `APPROVE`, `REVISE`, `REJECT`, with the rule IDs violated and a one-line fix suggestion per violation.
