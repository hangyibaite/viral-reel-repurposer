---
name: viral-repurpose
description: Use this skill whenever the user pastes a transcript of a proven viral or outlier piece of content. Triggers on requests like "rescript this", "repurpose this", "remix this reel", "rewrite this for my niche", "swap the topic to X", or simply a pasted transcript with or without explicit instructions. Also triggers when the user pastes raw transcript text and asks to make it about something else, or pastes a transcript without instructions (in which case format it and ask for direction). The job is to preserve the original's exact phrasing, structure, rhythm, and beats wherever possible, while swapping only what HAS to change. Always use this skill before rewriting any pasted transcript, even if the request seems straightforward.
---

# Viral Repurpose

You will use this skill whenever the user pastes a transcript and wants it repurposed. The original earned its results through its structure, rhythm, and specific phrasing. Preserve everything that can stay. Swap only what must change.

The biggest failure is rewriting too much. A good repurpose is a careful swap operation, not a rewrite.

---

## Run this workflow IN ORDER

### Step 1 — Format and timestamp the transcript FIRST

Do this every time. No exceptions. Even when the user gave full direction in the same message.

Clean the text:
- Separate run-together words ("yourown" → "your own", "I'mgonna" → "I'm gonna")
- Fix obvious transcription typos
- Preserve grammatical quirks that read as voice ("I am like officially about to..." → keep "like")
- Preserve fillers and contractions exactly ("okay", "gonna", "kinda", "I don't know", "or something")

Add timestamps in `[HH:MM:SS.mmm]` format. Estimate pacing:
- Short-form (under 90s total): 200-250 wpm
- Long-form (over 90s total): 150-180 wpm

Break lines at natural pauses, conjunctions, breath breaks, and emphasis changes. One beat per line.

Output the cleaned transcript as the first block of your response.

Do not skip this step. It is the foundation for everything else.

---

### Step 2 — Determine content type and load the matching reference

Count the estimated total runtime from your timestamps:
- Under 90 seconds → load `references/short-form.md`
- Over 90 seconds → load `references/long-form.md`

Apply that reference's rules to the rest of this workflow. The two types need different priorities (rhythm for short-form, argument flow for long-form).

---

### Step 3 — Ask the user how they want to repurpose this

Check if the user has supplied all of these:
- The concept, tool, or service replacing the original's central topic
- The audience (broad top-of-funnel, or a specific ICP)
- The CTA format (DM keyword, comment keyword, link in bio, caption pointer)
- Any specific lines they want preserved or cut

If yes to all → skip this step. Go to Step 4.

If anything is unclear → load `references/question-batches.md`. Ask the right batch. Max 3 questions in one turn. Batch them together.

Wait for the user's answer before going to Step 4. Do not write the script without this information.

---

### Step 4 — Map the structural bones

Load `references/patterns.md`.

Read the formatted transcript. Label every section by its function. Common functions:
- Hook
- Rehook
- Self-aware meta beat
- Headline drop
- Identity reframe
- Rule-of-X enumeration
- Step-by-step block
- Payoff / closer
- CTA

For each labeled section, decide which bucket it goes in:
- **Preserve verbatim** — iconic, voice-coded, or structurally critical
- **Preserve cadence, swap content** — the rhythm matters more than the words
- **Paraphrase with options** — joke, absurd specificity, pop reference, audience-specific punchline
- **Cut entirely** — doesn't fit the new topic at all

---

### Step 5 — Output the structural plan BEFORE writing

Write 3-6 lines stating:
- What you are preserving (name the iconic beats)
- What you are swapping (the topic-specific stuff)
- Which lines need paraphrase options
- Any open questions still standing

Do not write the script in this step. Output the plan only. Then write the script in the next message OR continue in the same message after the plan.

---

### Step 6 — Write the repurposed script

Obey these rules while writing:

- Preserve every word that can stay. Default to keeping. Justify each deletion.
- Match the original's timestamps within ±2 seconds per line when content length is similar.
- Preserve fillers ("okay", "I don't know", "or something")
- Preserve emphasis markers (CAPS, em-dashes, italics, ALL-CAPS)
- Preserve rule-of-X structures even when content changes
- Match runtime within ±20 seconds of original unless the user specified otherwise
- For short-form, prioritize rhythm. See `references/short-form.md`.
- For long-form, prioritize argument flow. See `references/long-form.md`.

---

### Step 7 — Handle jokes and specifics with OPTIONS, never lock-ins

If a line falls into any of these categories:
- An embedded joke
- An absurd specificity line ("What should I make with this food in my fridge?")
- A pop culture reference
- An audience-specific punchline
- A self-roast referencing topic-specific content
- A user-flagged line needing alternatives

Do this:

1. Identify what the line is doing structurally (briefly state the function)
2. Output 3-5 distinct options
3. Label each option's angle (sharper / softer / more meta / more relatable / more absurd / more deadpan / etc.)
4. Stop. Wait for the user to pick before locking it into the script.

Never deliver a final script with a paraphrased joke or specific committed. Always present alternatives first.

---

### Step 8 — Truth-check specifics

If the original contains numbers, case studies, dollar amounts, named clients, or specific results — and the user has not supplied equivalent proof:

- Replace with a process claim ("I run this every time I...")
- Replace with a principle claim ("this is the thing I trust before I lock anything in")
- Replace with something the user has genuinely done at a general level
- Flag the swap to the user and offer to slot in real numbers if they have them

Never fabricate proof. Never invent a number. Never name a client the user hasn't named.

---

## Anti-patterns — stop and fix these immediately

If you catch yourself doing any of these, stop and pull back:

- Writing entirely new sentences from scratch → you stopped repurposing and started drafting. Pull back to the original wording.
- Breaking the original's rule-of-X rhythm → match the structure exactly.
- Locking in a paraphrase without options → output 3-5 options instead.
- Inventing a specific number, result, or named entity → use a process claim.
- Skipping the structural plan → output the plan, then resume.
- Skipping formatting and timestamping → go back to Step 1.
- Killing an iconic closer ("Peace out", "Thank me later", "It's not that deep") without the user asking → restore it.
- Burying the headline → put the equivalent hard verdict line back in the same time slot as the original.

---

## When something feels wrong with the output

Load `references/troubleshooting.md`. Find the symptom. Apply the fix.

---

## Hard rules — never break

1. Format and timestamp the transcript BEFORE doing anything else.
2. Ask clarifying questions BEFORE writing if any direction is incomplete.
3. Output the structural plan BEFORE writing the script.
4. Output 3-5 options BEFORE committing to any paraphrased joke or specific line.
5. Preserve every word that could have stayed.
6. Never invent numbers, case studies, or named results.
7. Never kill iconic closer lines unless the user explicitly asks.
8. Never lock in a final script that violates any of rules 1-7.

---

## Quality check before delivering the script

Run this checklist. Fix anything that fails:

- [ ] Was the cleaned + timestamped transcript output first?
- [ ] Was the structural plan output before the script?
- [ ] Is the hook preserved or near-verbatim?
- [ ] Are iconic closers preserved?
- [ ] Does the rhythm match — repetitions, parallelisms, rule-of-X structures intact?
- [ ] Were jokes and specifics offered as 3-5 options rather than locked in?
- [ ] Are the timestamps realistic for the new content's length?
- [ ] Is the CTA in the user's preferred format?
- [ ] Are all proof points honest (no invented numbers or results)?
- [ ] Was every preservable word preserved?

If any answer is no, fix before delivering.
