# /better-prompt — turn a hard-won result into a one-shot prompt

Goal: when the user finally got the output they wanted after a few rounds of correction, teach them what made the difference and hand them a single prompt that would get it on the first try next time.

## Method

1. **Trace the thread.** Find the original ask, every correction or refinement the user made, and the final output they accepted.
2. **Diagnose the gap.** Name what the first prompt was missing that the corrections added. It is almost always one or more of: missing context or background, an unstated constraint, the desired format or structure, the tone or voice, a concrete example, the scope, or the audience.
3. **Explain it plainly.** Write 3–5 short points — "what made the difference" — in everyday language. No jargon.
4. **Write the reusable prompt.** A single copy-paste block that bakes in every correction. Spell out: who Claude should act as and any context, the task, the inputs, the constraints, the output format, the tone, and an example if one helped. Write it so the user only needs to swap in the new specifics each time.
5. **Note the model** (optional). If a particular tier fits, say so in one line (see `downsize.md`).

## Output format

Deliver inline:

```
What made the difference
- [point]
- [point]
- [point]

Your reusable prompt
----------------------------------------
[the full prompt, ready to copy, with [brackets] where they swap in specifics]
----------------------------------------
```

Offer to save it as a reusable snippet (a short markdown file) or add it to their Project so the team can reuse it.

## Example

Input: the user first asked "write a follow-up email to the vendor," then corrected it three times — make it shorter, keep it friendly not formal, and ask for a specific delivery date.

Output:

```
What made the difference
- You told it who it was writing to and the relationship (friendly, ongoing vendor).
- You set a length ("3–4 sentences") so it stopped over-writing.
- You named the one thing the email had to get: a committed delivery date.

Your reusable prompt
----------------------------------------
Write a short follow-up email (3–4 sentences) to [vendor], who we work with regularly —
warm and friendly, not formal. Goal: get a committed delivery date for [item]. End with a
clear question that asks for that date. Sign off as [name].
----------------------------------------
```
