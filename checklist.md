# Checklist — Output Format

This file defines how the generated checklist should be *formatted* when shown to the user (Step 5 of `SKILL.md`), and the closing prompt that follows once all steps are confirmed (end of Step 6, per `iteration.md`).

This is a **template for structure**, not content — the actual steps and pass bars come from the selected file in `types/`, populated with the user's specifics from Steps 1-3.

---

## Format when first presenting the full checklist (overview only)

Before Step 6 begins, give the user a single compressed overview so they know what's coming — titles only, no detail, no pass bars yet. This is the only time the full list appears at once, and it's a preview, not the working version.

```
Here's the build checklist for your [type] — [N] steps:

1. [Step title]
2. [Step title]
3. [Step title]
...

We'll go one at a time — I'll walk you through each step, check your work against
the bar before moving on, so you actually end up knowing how to do this again next time.

Ready to start with Step 1?
```

## Format for each individual step during guided iteration

Each step, when revealed one at a time per `iteration.md`, should follow this shape:

```
**Step [N]: [Step title]**

[The instruction, populated with their specifics — not the generic type-file
language verbatim, but adapted to their actual offer/ICP/category from Steps 1-3]

✅ Pass bar: [the specific bar for this step, from the type file]

Go ahead — [specific prompt for what they should produce or answer].
```

After they respond and pass:

```
That clears the bar — [one-line specific reason why, referencing their actual content].

**Step [N+1]: [next step title]**
...
```

## Closing — after the final step is confirmed

Once the last step in the checklist passes, do **not** immediately jump to "you're done." First run the QC pass per `references/qc.md`, then close with a prompt to go build and return — do not assume the conversation continues seamlessly into a finished asset.

```
That's the full checklist confirmed. Before you call this done, run it through the
QC pass — go check it against references/qc.md, especially Part 2 (the technical
and build checks) since plenty of this only breaks once it's actually built and
connected, not while it's still ideas on a page.

Here's what to do now:

1. Go build this for real — set up the [tool from the Execution Layer], write
   the final copy in your brand voice, connect whatever needs connecting.
2. Don't rush this part. The checklist got the thinking right; the build still
   needs your actual attention.
3. Once it's built (or even partway through, if you get stuck), come back here
   and show me:
   - Screenshots of what you've built so far
   - The actual copy/logic as it exists in the tool, not just the draft we wrote
   - Anything that didn't work the way the checklist assumed it would

I'll check it against the pass bars again with the real thing in front of me,
not the plan — that's usually where the actual problems show up.
```

## Why this two-stage close matters

The checklist passing in conversation is not the same as the asset existing and working. Per `iteration.md`'s "user wants to go build offline" guidance — confirming steps as done based on described intent rather than real evidence defeats the purpose of QC. This closing format exists specifically to force a return-and-verify loop rather than letting the conversation end on "looks good in theory."
