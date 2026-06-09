# Troubleshooting

When the output of a repurpose feels wrong, find the symptom below. Apply the fix. Do not deliver until the symptom is gone.

---

## Symptom: The script feels too long

**Diagnosis:** You padded the build to fit a runtime, or you added beats the original didn't have.

**Fix:**
1. Compare your script's beat count to the original's beat count. They should match.
2. If you added beats, remove them.
3. If beats are present but lines are longer than the original's, compress sentence-by-sentence until each beat matches the original's line length.
4. Compress the build/explanation sections first. Never compress the hook, the payoff line, or the CTA.

---

## Symptom: The script feels preachy

**Diagnosis:** You stripped self-aware meta beats. The original earned its sermon by interrupting itself.

**Fix:**
1. Re-read the original. Find every moment where the speaker self-deprecates, mocks themselves, or acknowledges they're doing The Cringe Thing™.
2. Each of those moments has a structural function. Put them back in the same time slots.
3. If you cut one because it felt "off-topic", you misjudged. Restore it.

---

## Symptom: The rhythm feels off

**Diagnosis:** You broke a rule-of-X pattern, or you collapsed a parallelism.

**Fix:**
1. Find every list, repetition, or parallel structure in the original.
2. Count the items in each.
3. Your version must have the same count and the same pattern.
4. If the original was "X. Y. Z." (three items), yours cannot be "X, then Y and Z." (collapsed). Restore the three discrete items.

---

## Symptom: The jokes feel out of place

**Diagnosis:** You swapped a joke without matching its structural function. Or you locked in a paraphrase instead of offering options.

**Fix:**
1. For each joke in the original, identify its function (self-roast / absurd specificity / audience pre-empt / etc.).
2. If your version's joke serves a different function, swap it for one that matches.
3. If you committed a paraphrase without offering options, undo it. Output 3-5 options. Wait for the user pick.

---

## Symptom: The pivot is too abrupt

**Diagnosis:** You cut a bridge or a transition the original used to ease the audience from one section to the next.

**Fix:**
1. Find the transition between your two sections in the original.
2. Identify the connector ("and", "so", "but", "which means", "now").
3. Restore it.
4. If the original used a full transition sentence ("Wait, I should probably explain..."), restore that too.

---

## Symptom: The audience can't tell what topic this is about

**Diagnosis:** You held the topic reveal too late, or you obscured the topic with too many preserved beats from the original.

**Fix:**
1. Identify when the audience needs to know the topic clearly (usually by 15-20 seconds in short-form, 30-45 seconds in long-form).
2. Make sure ONE line in that range plainly states the topic.
3. If preserving the original kept the topic vague past that point, swap one earlier line to clarify.

---

## Symptom: The CTA feels disconnected

**Diagnosis:** The CTA matches the user's format but doesn't flow from the payoff.

**Fix:**
1. The CTA should feel like the natural next step after the payoff line.
2. Add a bridge sentence between payoff and CTA if needed (one sentence max).
3. The bridge should answer "okay, so what do I do now?"

---

## Symptom: The hook isn't earning its spot

**Diagnosis:** You preserved the original's hook but the new topic doesn't deliver on what the hook promised.

**Fix:**
1. Re-read your hook. Ask: what does this hook promise the viewer?
2. Re-read your payoff. Does it deliver on that promise?
3. If no, either rewrite the hook to match the new payoff, OR rewrite the payoff to match the hook.
4. Hook and payoff are paired. They must agree.

---

## Symptom: The script reads as a different person than the original

**Diagnosis:** You stripped voice markers — fillers, contractions, cussing patterns, emphasis markers.

**Fix:**
1. Compare your version to the original side-by-side.
2. Mark every filler ("okay", "I don't know", "gonna", "kinda", "or something") in the original.
3. Each one should appear in roughly the same place in your version.
4. Same for cussing, CAPS, em-dashes, brackets.
5. Restore the markers. They are the voice.

---

## Symptom: The "feel" is right but the specifics are off

**Diagnosis:** You preserved structure but didn't truth-check the specifics for the new topic.

**Fix:**
1. Find every number, named entity, case study, dollar amount, or specific result in your version.
2. For each one, verify the user has actually supplied this proof or done this thing.
3. If yes, keep it.
4. If no, swap for a process claim or principle claim. Flag the swap to the user.

---

## Symptom: The user said preserve but you still changed things

**Diagnosis:** Mode mismatch. The user wanted minimal-change repurpose; you delivered medium-change.

**Fix:**
1. Re-read the user's instructions.
2. For every change you made, ask: did the user explicitly authorize this change, OR was it forced by the topic swap?
3. If neither, revert.
4. The default is to keep. Justify every change.

---

## Symptom: You skipped a step in the workflow

**Diagnosis:** You jumped from formatted transcript straight to script, or skipped questions, or skipped the structural plan.

**Fix:**
1. Go back to the workflow step you skipped.
2. Output the missing artifact (clarifying questions OR structural plan).
3. Then resume from that point.
4. Do not deliver the script until every workflow step has been completed in order.

---

## Symptom: The structural plan and the script don't match

**Diagnosis:** You drifted while writing.

**Fix:**
1. Compare your structural plan to your final script.
2. Where they diverge, decide which is correct.
3. If the plan was right, fix the script.
4. If the script revealed something the plan got wrong, update the plan and re-output it for the user.

---

## Symptom: The user keeps asking you to change the same thing

**Diagnosis:** You're paraphrasing without matching the user's actual preference, or you're missing context about their voice.

**Fix:**
1. Re-read the user's last 3 messages for patterns in what they keep changing.
2. Identify the pattern (e.g., "they keep removing business-coded language" or "they keep preserving more of the original than you assumed").
3. Apply the pattern to the rest of the script.
4. If you can't identify the pattern, ask the user directly what they're optimizing for.
