# Notes for Muse — Proper 29 (Year A) is handled by Claude

**From:** Claude (working with Abraham in the Poimen's Pulpit Service OS project)
**Date:** 2026-11-15
**Status:** Proper 29 (Christ the King, Sunday 2026-11-22) devotions are built and published by Claude. **You do not need to execute anything for Proper 29.** Please do not rebuild, regenerate, or overwrite any of it.

## What Claude has done

1. Branch `proper-29` from `main`, with Chinese and English devotions for the reading week Mon 11-16 – Sat 11-21:
   - `year-a/proper-29/index.html` and `year-a/proper-29/{mon,tue,wed,thu,fri,sat}/index.html` — title 「我們什麼時候見你？」, 本週金句「王把自己藏在最小的人中間。」
   - `en/year-a/proper-29/…` — title "When Did We See You?", nail "The King hides among the least." The English was written in English, not translated.
   - Markdown source copies: `year-a/proper-29/md/zh.md` and `en.md`.
2. Updated `index.html`, `en/index.html`, `today/index.html`, `en/today/index.html`, `rss.xml` for Proper 29.
3. Sunday sermon, reader version (no page numbers or slide cues): `year-a/proper-29/sermon/` and `en/year-a/proper-29/sermon/`, linked from both week pages.
4. Readings (RCL Year A, Proper 29, Track 1): Ezekiel 34:11-16, 20-24; Psalm 100; Ephesians 1:15-23; Matthew 25:31-46. Saturday: Parashat Vayetzei (Gen 28:10–32:3), Haftarah Hosea 12:13–14:10 (Ashkenazi), verified for Shabbat 2026-11-21 (11 Kislev 5787).

## Publishing

Abraham asked for Proper 29 to go live **Sunday 2026-11-15 at 6:00 pm (America/New_York)**. Claude merges `proper-29` into `main` at that time; Cloudflare deploys to devotions.wordnspirit.com. Do not add a separate scheduled push.

## Please do not

- Do not edit, regenerate, or force-push anything under `year-a/proper-29/` or `en/year-a/proper-29/`.
- Do not merge `proper-29` yourself, and do not change the Proper 29 entries in the home pages, `today` routers, or `rss.xml`.

## Please do

When you come into this repository, **report to Abraham in your work group** that Claude built and published Proper 29 (Chinese and English), and that you left it untouched. For anything else here, branch from `main` and stay clear of the files above.

## Today router (fixed 2026-11-15)

`today/index.html` and `en/today/index.html` send readers to today's page. On Sunday they used to send readers to `{week}/sermon/`, which does not exist for weeks without a sermon page, so readers saw a blank page. Now: Monday–Saturday → that day's page; Sunday → the next week's overview if it is already listed, otherwise the sermon page only when the week is marked `s:1`, otherwise the week overview. When you add a week, add `{m:"YYYY-MM-DD",p:"/year-a/proper-NN/"}` (Monday date) to both routers, and add `s:1` only if that week really has a `sermon/` page. A `404.html` now links back to the home pages.

## Weekly workflow and the two sites (from Proper 29 on — replaces the Proper 25 instructions)

Order of work each week: study → theological map → Sunday sermon (zh + en) → two songs → sermon theater on sermon.wordnspirit.com (slides, PowerPoint, PDF) → Mon–Sat devotions written backward from the sermon (zh, then en written in English) → publish.

| | Sermon theater | Devotions |
|---|---|---|
| Site | sermon.wordnspirit.com | devotions.wordnspirit.com |
| Repo | `AbrahamChan1965/lectionary-sermon-` | `AbrahamChan1965/devotions` (this repo) |
| Content | Projected slides, PowerPoint 16:9 / 4:3, PDF | Mon–Sat devotions + Sunday sermon reader version (`{week}/sermon/`) |
| Ready by | **Friday** of the week before, on the `{week}-preview` branch | **Friday** of the week before, on a week branch (e.g. `proper-29`, `advent-1`) |
| Goes live | **Monday 00:00 (America/New_York)**, merged automatically by a weekly scheduled task; previous week moves to 藏經室 | **Same moment, Monday 00:00**: devotions and the Sunday sermon page go out together in one merge |

(Changed 2026-11-17: both sites now go live together at Monday 00:00 by schedule. The earlier "Sunday afternoon" release is retired. Do not add another scheduled push.)

Songs: Muse fetches them from the Google Drive song folder and publishes to music.wordnspirit.com, the sermon theater song page, and YouTube (see `MUSE_NOTE.md` in the lectionary-sermon repo).
