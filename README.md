# Viral Repurpose

A skill for repurposing proven viral transcripts. Hand it a transcript and a new topic. It preserves the original's structure, rhythm, and beats while swapping only what has to change.

---

## What this is for

You found a reel that hit. Same niche, similar audience, proven beats. You want to make a version for YOUR topic without losing what made the original work.

This skill does the careful swap operation. Keeps every word that can stay. Changes only what must change for your use case.

---

## What's in this folder

```
viral-repurpose/
├── SKILL.md                              Main workflow (8 steps, run in order)
├── references/
│   ├── short-form.md                     Rules for under-90s content (rhythm + pacing)
│   ├── long-form.md                      Rules for over-90s content (argument flow)
│   ├── patterns.md                       Library of 15 reusable structural shells
│   ├── troubleshooting.md                11 common failure modes + fixes
│   └── question-batches.md               When and what to ask you
└── assets/
    └── structural-plan-template.md       Format for the planning step
```

---

## Installation

Drop the entire `viral-repurpose/` folder into your user skills directory. Claude will pick it up automatically the next time you paste a transcript.

---

## How to trigger it

The skill auto-triggers when you paste a transcript. You don't need to invoke it by name.

### Fastest path — paste + direction together

Paste the transcript. In the same message, give Claude:
- The concept, tool, or service replacing the original's topic
- The audience (broad top-of-funnel or specific niche)
- The CTA format

Example:
```
[paste the transcript]

Repurpose for [your topic]. Audience is [broad TOF / specific niche].
CTA is comment "[keyword]" for the [deliverable].
```

Claude will format the transcript, output a structural plan, then deliver the script.

### Slower path — paste alone

If you just paste a transcript with no direction, Claude formats it and asks 2-3 batched questions before writing. Answer them and Claude writes.

### Mid-iteration

If Claude already delivered a draft and you want changes, just describe what to change. Claude won't re-ask the direction questions.

---

## What you'll get back, every time

In order:

1. **Cleaned transcript with timestamps** — output as a separate block at the top
2. **Structural plan** — 3-6 lines covering what's preserved, what's swapped, what needs your input
3. **The script itself** — with timestamps matching the original's rhythm

For any joke, punchline, or specific line that needs paraphrasing, Claude outputs 3-5 options labeled by angle (sharper / softer / more meta / more relatable / etc.) and waits for you to pick before locking it in.

---

## How to get the best results

**Tell Claude what to preserve word-for-word.** If a line in the original is iconic and must not change, say so up front. Claude defaults to preserving but explicit calls help.

**Flag your real proof.** If the original has specific numbers, case studies, or named clients, tell Claude what equivalent proof YOU have (or don't). Claude will never invent numbers.

**Pick options with one-word tone descriptors.** "Go with #3 — sharper" beats "I like option 3 because of the rhythm." Saves rounds.

**For long-form, expect more setup.** Over 90 seconds, Claude maps the argument structure first. It may ask about your thesis and what shift you want in the audience before writing.

**Match the original's vibe in your direction.** If the original is chaotic and deadpan, you don't need to spell it out — Claude preserves it. But if you want to TILT the vibe (more polished, less profane), say so early.

---

## Common gotchas

**Don't paste a transcript and ask for the script in two separate messages.** Paste both together. Claude needs to see the transcript and direction in the same context.

**Don't argue with the formatted version.** The cleaned + timestamped transcript is the foundation. Point out errors, but don't ask Claude to skip the formatting step.

**Don't expect proof you didn't supply.** If the original has "$10k in 30 days" and you haven't said you've done that, Claude swaps it for a process claim and flags the swap. That's the design.

**Don't lock in a paraphrase before seeing options.** Even with a strong idea, let Claude offer 3-5. You might find something better.

**Don't ask Claude to "just make it shorter."** Tell it WHICH section to compress (build, explanation, examples) and which to leave alone (hook, payoff, CTA).

---

## Troubleshooting

If a script feels off, the answer is usually in `references/troubleshooting.md`. Skim the symptoms. One will match.

Most common symptoms and fixes:

| Symptom                              | Fix                                                    |
|--------------------------------------|--------------------------------------------------------|
| Script feels too long                | Compress the build, never the hook/payoff/CTA          |
| Script feels preachy                 | Restore the self-aware meta beats Claude stripped      |
| Rhythm feels off                     | Rule-of-X got collapsed — restore the count            |
| Pivot is too abrupt                  | Restore the bridge sentence or connector ("so", "but") |
| Jokes feel out of place              | Claude paraphrased without offering options — redo     |
| CTA feels disconnected               | Add one bridge sentence between payoff and CTA         |
| Hook doesn't earn its spot           | Hook and payoff must agree — fix one to match other    |
| Reads as a different person          | Voice markers got stripped — restore fillers + caps    |
| Specifics feel off                   | Truth-check every number and named entity              |

Full diagnostic + fix for each symptom lives in `references/troubleshooting.md`.

---

## When NOT to use this skill

- Writing a script from scratch with no transcript reference — this skill is for repurposing, not generating
- Rewriting your own existing script — use a copy-editing or humanizer skill instead
- Translating between languages — use a translation workflow
- Generating B-roll directions, on-screen text, or captions — use a media-specific skill

---

## The non-negotiables (what the skill will never do)

1. Skip formatting and timestamping the transcript
2. Write a script before outputting the structural plan
3. Lock in a paraphrased joke without offering 3-5 options
4. Invent numbers, case studies, or named results you didn't supply
5. Kill iconic closer lines without you explicitly asking
6. Rewrite a sentence that could have stayed verbatim

If you ever see Claude do one of these, point it out. It's a bug, not a feature.
