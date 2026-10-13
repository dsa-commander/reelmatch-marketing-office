# Hooks — how every title, thumbnail line and caption is framed

**The trending title gets us found. The ReelMatch angle is what we're testing.**

**What the channel data actually says (2026-10-13, `studio_performance_review`).** 97 public videos.
Four of them are promoted walkthroughs carrying **350,401 of the channel's 352,064 views**. The other
93 have **1,663 views between them, median 6**. Within those 93: trailer-framed videos median 6,
everything else median 6, and the single organic app-angle video has 50.

So the honest position is: **no framing has been proven to beat another yet.** One video at 50 views
against a median of 6 is encouraging and is not evidence. We lead with the ReelMatch angle because it
is the thing no competitor can copy — not because the numbers have shown it wins.

> An earlier version of this file claimed app-angle videos held a median of 42,503 views against 6.
> That was the median of the four *paid* promos. `by_format` was folding ad results into organic
> figures, and a weekly run planned itself around the mistake. The tool now reports promoted videos
> separately. **When a number looks like four orders of magnitude, check what is in the denominator.**

Guardian rule **V6** enforces this. A title that leads with "N trailers", "official trailers",
"coming in <month>" or "new releases" — without a decision premise — is a REVISE.

## The five formulas

Pick the one that matches the data you have. Fill the `<…>` from tool results only.

| # | Formula | Use when | Hashtags (max 3 on YouTube) |
|---|---|---|---|
| **1 · Swipe or skip** | `Would you swipe right on <title>? <emoji>` | one trending title, a Short | `#<Title> #Shorts #ReelMatch` |
| **2 · Our users decided** | `<N> couples used ReelMatch this week — here's what they agreed on` | `reelmatch_top_matched` / `top_liked` has ≥ 3 titles **and N ≥ 5** — see the floor below | tags of the titles shown |
| **3 · Date-night decider** | `She wants <genre A>, he wants <genre B>. ReelMatch found the one on <platform> tonight.` | `tmdb_streaming_now(mood="date")` | `#DateNight #<Platform> #<Title>` |
| **4 · Trending vs. ours** | `TMDB says these <N> are trending. Our users disagree — here's what they're actually swiping on.` | trending ∩ audience data both available | mix of both lists |
| **5 · Argument settler** | `<N> new releases couples will fight over in <month> — and how to settle it in 10 seconds` | the long-form Top-N countdown | `#NewMovies #<Month><Year> #ReelMatch` |

Formula 2 is the one no competitor can copy. Prefer it whenever the audience data supports it.

### Formula 2 has a floor: never publish a number that makes the app look empty

**`<N>` must be ≥ 5.** The "use when" column above is a floor on how many *titles* carry match data —
it was never a floor on **N itself**, and on 2026-10-13 a run produced "1 couple matched on ReelMatch
this week" and "2 couples matched on ReelMatch this week". Both were accurate, correctly sourced, and
approved by the guardian — the guardian checks voice, claims and safety, and a true number is all
three. It has no concept of a true number that is bad for us.

A title is an advertisement. "1 couple matched this week" advertises that nobody is using the app.

**When the matched count is below 5**, use the larger signal from the same snapshot — likes — and say
so plainly: `<N> ReelMatch users swiped right on <title> this week 🍿`. Same formula, same honesty,
a number that doesn't undersell the product. If *that* is also below 5, fall back to formula 1.

## Rules of the hook

- **First 5 words carry the premise.** "Would you swipe right on…" / "37 couples agreed on…" / "She wants…".
  Not "Top 5…", "New…", "Official…".
- **A number from a tool beats an adjective.** "37 couples" > "lots of couples". "8 likes among 37 users"
  is a real claim; "everyone's obsessed" is not (rule C1).
- **The film's hashtag, not a generic one.** `#ResidentEvil` finds the trending audience; `#horrormovie`
  finds nobody. Three hashtags on YouTube: the film, the format, `#ReelMatch`.
- **One emoji, at the end.** 🍿 is ours. (V4)
- **The description can still list every trailer, cast and release date** — that's where the SEO lives.
  The hook is the title, the first line, and the thumbnail text.
- **Never the same hook twice in a row.** Rotate formulas week to week; the report will show which lands.

## Thumbnail text (≤ 6 words, the same premise)
- Swipe or skip → `SWIPE RIGHT?` over the poster
- Our users decided → `37 COUPLES PICKED THIS`
- Date-night decider → `SHE SAID YES TO THIS`
- Trending vs ours → `TMDB vs REELMATCH`
- Argument settler → `SETTLE IT IN 10 SEC`

## What this is NOT
- Not clickbait. Every premise must be true from tool data (C1) and the video must deliver it.
- Not a reason to drop the trailers. They are the thing people search for — keep them; reframe them.
- Not engagement bait. "Comment which one" is fine as a genuine question; "like if you agree" is P2.

## Measuring it
Every render produces 4 `titleAlternates`. Put one trailer-style and one hook-style title into YouTube
Studio's **Test & Compare** on each upload. `studio_performance_review` will show which wins within 1–2
weeks — then this file gets updated with what the data said, not what we guessed.
