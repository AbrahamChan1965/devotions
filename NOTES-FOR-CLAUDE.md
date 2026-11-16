# Notes for Claude — /today shows a blank white page on Sundays (Proper 28)

**From:** Muse (via Abraham)
**Date:** 2026-11-15 (Sunday, Proper 28)
**Status:** Please check. Muse is not touching anything — this note is the only change.

## What Abraham reported

Opening "今日靈修" (`/today`) shows a blank white page — both the Chinese version
(devotions.wordnspirit.com/today) and the English version (/en/today).
The page looks empty / unconnected.

## What Muse verified (read-only, 2026-11-15 ~20:15 EST)

- `/today` and `/en/today` both return HTTP 200 (the no-JS fallback link list
  renders in a text fetch).
- The today router maps the visitor's local date to a day page:
  `D = ['mon','tue','wed','thu','fri','sat','sermon']`. Today is Sunday
  2026-11-15, the 7th day of Proper 28 week (Monday 2026-11-09), so
  diff = 6 and the destination is `/year-a/proper-28/sermon/`
  (and `/en/year-a/proper-28/sermon/`).
- That sermon page does not exist: both URLs return HTTP 404, and `main`
  has no Proper 28 sermon file. The sermon page is on hold by Abraham's
  decision.
- So with JavaScript on, `/today` redirects visitors to a missing page —
  the blank white screen Abraham sees. The English router has the same
  structure (`D` array and Proper 29 entry included).

## Please check

1. Confirm this is the cause (visit `/today` in a real browser with JS on,
   both languages).
2. Fix the router so a Sunday with no sermon page does not land on a 404:
   fall back to something that exists (e.g. Saturday's devotional, or the
   week page). Apply the same guard to the English router (`en/today`).
3. Same trap ahead: next Sunday 2026-11-22 (Christ the King / Proper 29) —
   Proper 29 also has no sermon page yet. Make sure `/today` does not go
   blank that Sunday too.
4. Do not publish or change any devotional content; only fix the
   routing / blank-page fault. Report back in `NOTES-FOR-MUSE.md` what you
   found and changed.
