# QC — Lead Magnet Quality Control

Run this on the **finished asset**, not the concept. A concept can pass the filters and still fail QC once real copy and logic exist. Run every check below before calling anything done.

---

## Part 1 — The Two Filters (generalized, re-run on the finished asset)

### The $50 Test
Would a stranger, with zero relationship to the creator, hesitate to pay $50 for this exact finished asset, standalone?

- If yes → not done. Identify what's generic or thin and fix it before moving on.
- Common failure: the asset *describes* value instead of *delivering* it. Information everyone already has, formatted nicely, still fails this test.
- This test applies to the finished copy/logic, not the idea. An idea can pass in concept and fail once written generically.

### The Bigger-Problem Test
Does using this asset — with zero extra explanation from the creator — cause the user to bump into the structural problem only the paid offer fixes?

- If the user can fully resolve their situation using only the free asset, it fails. The free asset should make the *next* problem visible, not solve every problem.
- If the free asset accidentally contradicts the paid offer's core mechanism (e.g. hands over a full plan when the paid offer's value is accountability, not planning), it fails — even if it passes the $50 Test.
- Re-check this specifically against the offer's actual paid mechanism, not the general topic. The bigger-problem connection has to be mechanism-specific, not topic-adjacent.

---

## Part 2 — Full QC Pass

### Copy quality
- [ ] No generic language — every sentence should read as written for the specific ICP, not swappable into a different niche
- [ ] Matches the creator's established voice/tone (check against Writing Style Guide if one exists)
- [ ] No more than 2 examples per concept, no concept repeated more than twice (if the asset teaches anything)
- [ ] Specificity check: could a different prospect in a different situation read this and feel equally "seen"? If yes, it's too generic — tighten it.
- [ ] No hidden pitch disguised as content — the close exposes the gap, it doesn't sell

### Logic / build check (for anything with scoring, branching, or automation)
- [ ] Every input question maps to exactly one category — no overlap
- [ ] Scoring thresholds tested against at least 2 different realistic answer sets per category — confirm no two distinct real answers wrongly trigger the same flag
- [ ] Tie-break rule exists and is singular (not "show all flagged categories")
- [ ] Edge case handled: what happens if nothing flags / the user "passes" everything?
- [ ] All conditional logic (Logic Jump, branching, routing) fires correctly when tested end-to-end, not just spot-checked

### Technical / delivery check
- [ ] All links work (test by clicking, not assuming)
- [ ] Capture mechanism (email/DM gate) fires before or after reveal as designed — confirm placement matches the funnel decision made during build
- [ ] Any integration (e.g. Typeform → ManyChat) confirmed connected and tested with a real dummy submission, not just configured
- [ ] Any scheduled/triggered follow-up (e.g. day-3 DM check-in) confirmed to actually fire on schedule — test with a real run, don't assume the automation works because it's configured
- [ ] Mobile rendering checked if the asset is web-based — most leads will open this on a phone

### Production check
- [ ] If video/audio was required, confirm it was actually recorded and is the right length/format specified during the build step
- [ ] If design assets were required, confirm brand consistency (colors, logo, fonts) — not default template styling left untouched

---

## How to use this file

Run Part 1 first. If either filter fails, stop — fix the asset before doing a technical QC pass on something that may get rewritten anyway. Once both filters pass, run Part 2 in full. Anything unchecked is not done, regardless of how good the rest of the asset looks.
