# Lead Magnet Architect

A guided build companion for Claude — not a one-shot generator. Walks you through diagnosing, correcting, and building a lead magnet specific to your offer and audience.

Every idea is run through two filters before anything gets built:

1. **The $50 Test** — would a stranger pay $50 for this as a standalone asset?
2. **The Bigger-Problem Test** — does this small win expose the structural problem only your paid offer fixes?

## How it works

1. **Diagnose** — collect your offer, audience, and rough idea (if you have one)
2. **Breakdown** — run the idea against both filters and explain exactly where it fails
3. **Fix** — propose directions that pass both filters, tied to your offer's paid mechanism
4. **Route** — load the type-specific reference for the selected lead magnet format
5. **Checklist** — generate a build checklist populated with your actual inputs
6. **Iterate** — reveal one step at a time, check your work, correct, then advance
7. **QC** — re-apply both filters to the finished asset plus copy/logic/production checks

## Structure

```
lead-magnet-architect/
├── SKILL.md                    ← core skill definition and flow
├── checklist.md                ← checklist formatting and close sequence
├── iteration.md                ← step-by-step reveal and feedback mechanics
├── references/
│   └── qc.md                  ← quality control filters and final pass criteria
└── types/
    ├── diagnostic-quiz.md     ← quiz / mini-audit build reference
    ├── swipe-file.md          ← curated examples build reference
    ├── text-based.md          ← framework / worksheet build reference
    └── video-sequence.md      ← video series build reference
```

## Installation

Place this folder in your Claude skills directory (e.g. `~/.claude/skills/` for Claude Code, or upload into your Claude Project on claude.ai).

Triggers on: "lead magnet," "free offer," "freebie idea," "what should my lead magnet be," requests to evaluate an existing lead magnet idea, or any request to build a quiz/audit/swipe file/calculator/template pack intended to generate leads.

## Dependency

This skill requires [brand-voice](https://github.com/hangyibaite/brand-voice-skill) to be installed before writing any user-facing copy. It will prompt you to set that up if it's missing.
