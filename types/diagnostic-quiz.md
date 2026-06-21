# Type: Diagnostic Quiz / Mini-Audit

Use when the offer's paid mechanism is **diagnosis, correction, or accountability** — the prospect doesn't lack information, they lack an accurate read on their own situation, or lack the structure to act on what they already half-know. This type has scoring, branching, and tie-break logic. If there's nothing to diagnose (prospect has no existing attempt/situation to audit), this type is the wrong fit — route back to Step 3 in SKILL.md.

This file is the **shape** of the checklist. Populate every bracketed part with the specifics from Steps 1-3 before revealing to the user.

---

## The checklist shape (8 steps)

### 1. Lock the inputs
Write [3-6] exact questions, each one mapped to exactly one diagnosis category. No vague/open fields — every question should be answerable in one line and produce a flaggable signal.

Include one **specificity question** if the offer's value depends on the user feeling "they know my exact problem" — a question that captures location/trigger/timing detail, not just yes/no history. This question almost always flags (it's the trust-builder, not a true/false filter).

Consider one **severity multiplier** question (e.g. how long has this been going on) — this is not its own category, it feeds tie-break logic only.

✅ Pass bar: every question maps to exactly one category. No input scores two categories.

### 2. Assign category ownership
List categories (these come from the offer's actual diagnosis framework — what would the creator actually check if doing this live with a client?). Map each input to its one category explicitly.

✅ Pass bar: zero overlap.

### 3. Write scoring thresholds
For each category, define the specific answer pattern that counts as a flag. Avoid vague thresholds ("if they seem inconsistent") — use concrete cutoffs (specific numbers, specific phrases).

✅ Pass bar: thresholds specific enough that two different realistic answers can't both wrongly trigger the same flag.

### 4. Set tie-break logic
Define what happens when 2+ categories flag. There must be a single rule, not "show everything that flagged." Base the rule on what's actually most structurally important for this ICP (ask the creator if unclear — don't assume).

✅ Pass bar: one clear rule exists, with a stated reason tied to the ICP, not arbitrary ordering.

### 5. Write diagnosis copy per category
For each category: symptom → hidden reality → consequence. Reference the specificity question's actual answer pattern where possible — generic copy fails here even if the logic is correct.

✅ Pass bar: reads as written about this specific person's situation, not swappable into a different niche.

### 6. Write the corrective action per category
One action, narrow time scope (matches what's realistic for this ICP — often 7 days), **deliberately incomplete**. It should fix the symptom, not the pattern — the unsolved pattern is what the paid offer exists to solve.

**If the offer's positioning includes accountability as part of the paid value** (not just information/correction), the corrective action must include a built-in check-in mechanism — even a lightweight one (self-log, screenshot, or a scheduled DM prompt that ties into the creator's existing reply/triage system). Without this, an accountability-positioned offer's free asset will contradict its own pitch — check with the creator if this applies before finalizing.

✅ Pass bar: action alone is visibly incomplete; if accountability applies, the check-in is built in, not assumed.

### 7. Write the close
State or imply the gap that remains unsolved by the free asset — never with a direct pitch ("book a call"). The close should make the next problem obvious, not sell against it.

✅ Pass bar: no direct ask; gap is named or strongly implied.

### 8. Build, connect, QC
Build per the chosen tool (see Execution Layer below). Confirm any integration (capture → CRM/ESP, scheduled DM triggers) is tested with a real dummy run, not just configured. Then run the full pass in `references/qc.md` — do not skip this for "just a quiz."

---

## Execution layer

**Recommended tools (ranked):**

1. **Typeform** — best fit for most cases. Native Logic Jump handles branching/tie-break without code, clean diagnostic feel, free tier usually sufficient, easy embed or standalone link.
2. **Tally** — free, simpler logic engine, less polished feel, fine if budget is zero and branching needs are minimal.
3. **Google Forms + manual scoring** — works but unpolished, manual logic, last resort only.

**Full build-out — Typeform:**

1. New Typeform → start from blank, not a template (templates fight specific question wording).
2. Add each input question as a separate field — use Multiple Choice or Opinion Scale, not free text (free text can't feed Logic Jump cleanly).
3. Under each field's Logic settings, assign a hidden tag/value per answer option (e.g. `category_flag`) — this is the scoring mechanism without code.
4. Connect → Logic → build the tie-break conditional rules from Step 4 above.
5. Create one Ending screen per category outcome, plus a default "no major flag" ending. Paste in the diagnosis copy + corrective action for each.
6. Add an email/contact capture field before the final diagnosis reveal — gates the result, matches standard lead-capture funnels.
7. Connect → Integrations → connect to the creator's existing ESP/CRM/ManyChat (native integration list covers most common tools) so capture flows into existing nurture/triage automatically.
8. If a scheduled check-in DM applies (see Step 6 above), set this up in the connected automation tool (e.g. ManyChat scheduled message), not manually — test it fires correctly before calling it done.
9. Publish, grab the link, embed in existing funnel entry point (bio link, DM flow, etc.).

**Production flags for this type:** typically no video/voice required. Written assets needed: input questions, diagnosis copy per category, corrective action per category, close line. Design need is minimal — default platform styling is usually sufficient; brand color/logo upload is a quick optional polish step, not required.
