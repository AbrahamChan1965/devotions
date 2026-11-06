# Notes for Muse — Proper 28 (Year A) is handled by Claude

**From:** Claude (working with Abraham in the Poimen's Pulpit Service OS project)
**Date:** 2026-11-05
**Status:** Proper 28 is being built and published by Claude. **You do not need to execute anything for Proper 28.** Please do not rebuild, regenerate, or overwrite any of it.

## What Claude has already done

1. Created the branch `proper-28` from `main` (commit `397cba6`).
2. Added the Chinese devotionals for Proper 28 (Sunday 2026-11-15), reading week Mon 11-09 – Sat 11-14:
   - `year-a/proper-28/index.html` — week page, title 「他把家業交給你」, 本週金句 「交出家業的主人，把自己也交了出去。」
   - `year-a/proper-28/{mon,tue,wed,thu,fri,sat}/index.html` — six daily pages (third draft, six-direction exegesis).
3. Updated on the branch only:
   - `index.html` — home page now features Proper 28; Proper 28 added to the archive list.
   - `today/index.html` — router entry `{m:"2026-11-09", p:"/year-a/proper-28/"}` added.
   - `rss.xml` — one new item for Proper 28.
4. Readings used (RCL Year A, Proper 28): Judges 4:1-7 + Psalm 123 (Track 1, main line); 1 Thessalonians 5:1-11; Matthew 25:14-30. Track 2 (Zephaniah 1:7, 12-18; Psalm 90) appears only as a cross-reference line. Saturday: Parashat Toldot (Gen 25:19–28:9), Haftarah Malachi 1:1–2:7 — verified for Shabbat 2026-11-14.

## Still to come (Claude will do these)

- English pages are now on the branch too (`en/year-a/proper-28/`, `en/index.html`, `en/today/index.html`), awaiting Abraham's review.
- One merge of `proper-28` into `main` (Chinese and English together), done by Claude when Abraham approves. Branch previews on Cloudflare do not build, so there is no preview URL — that is expected.
- The Proper 28 sermon and song pages are on hold by Abraham's decision. Do not publish them.

## Please do not

- Do not edit, regenerate, or force-push anything under `year-a/proper-28/` or `en/year-a/proper-28/`.
- Do not merge `proper-28` into `main` yourself, and do not delete the branch.
- Do not change the Proper 28 entries in `index.html`, `today/index.html`, `en/today/index.html`, or `rss.xml`.
- Do not add a separate scheduled push for Proper 28 — the publishing time is handled from Claude's side.

## Please do

When you come into this repository to work, **report the above to Abraham in your work group**: tell him that Claude has already built Proper 28 on the branch `proper-28` (Chinese done, English pending his approval), that publishing is scheduled from Claude's side, and that you have left Proper 28 untouched. If you need to work on anything else in this repo, branch from `main` and stay clear of the files listed above.
