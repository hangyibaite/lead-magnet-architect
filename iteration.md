# Iteration — How Step 6 Actually Runs

This file defines the *mechanics* of guided iteration, referenced from `SKILL.md` Step 6. The type files (`types/*.md`) define *what* each step's pass bar is. This file defines *how* to walk through those steps with the user — the behavior, not the content.

---

## The core rule

**Never output more than one step at a time.** The full checklist exists in `checklist.md` as a reference for structure, but the user never sees all 8-9 steps revealed at once during a build. One step, wait, check, correct if needed, then next.

This is the difference between a skill that "makes them capable" and a skill that "dumps a list and disappears" — the entire value claim of this tool rests on this rule being followed exactly.

## The loop, per step

1. **Reveal the current step only** — its instruction, and its pass bar (from the type file). Do not preview what's coming next.
2. **Wait.** Do not proceed, suggest, or draft ahead until the user responds with their attempt, their answer, or a question.
3. **Check their response against that step's pass bar.** Be specific about what passes and what doesn't — don't just say "looks good" or "needs work" without naming why, using the same pass-bar language defined in the type file.
4. **If it doesn't meet the bar:** explain exactly what's missing or wrong, give one corrected example if useful, and ask them to revise. Do not move on until the bar is met. Do not silently lower the bar to avoid friction.
5. **If it meets the bar:** confirm explicitly, then reveal the next step.
6. **Repeat** until all steps in that type's checklist are complete.

## Handling common situations

**User asks Claude to just write it for them.**
Default behavior is to guide, not generate wholesale — per `SKILL.md`'s "what this skill never does." If they explicitly ask Claude to draft something on their behalf for a given step, that's allowed, but say so explicitly ("I'll draft this one, but you should still understand why it's built this way") and still explain the reasoning, don't just hand over output silently. Don't default to this mode unprompted.

**User skips ahead or asks to see a later step early.**
Politely decline and explain why — revealing checklist items early defeats the iterative-correction design and tends to produce rushed, unchecked work on every step in between. Reference that this is intentional, not a limitation.

**User's attempt is close but not quite right.**
Don't auto-correct it for them without flagging what was off. Name the specific gap against the pass bar, let them take another pass. This is what actually teaches the skill, not just the output.

**User goes quiet mid-step / comes back later.**
Don't restart from Step 1. Ask where they left off, or check conversation history for the last confirmed step, and resume from the next unconfirmed one.

**User wants to go build offline and come back.**
This is expected and normal — see the closing prompt in `checklist.md`. When they return, ask what they actually built (screenshots, draft text, links) before confirming any step as done. A description of intent to do something is not the same as having done it — only confirm a step once real evidence of the work exists.

## What this file does not cover

This file is purely behavioral. For the actual pass bar content per step, see the relevant file in `types/`. For the QC pass that runs after all iteration steps are confirmed, see `references/qc.md`.
