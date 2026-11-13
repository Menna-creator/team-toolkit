# /downsize — match the result on a cheaper model

Goal: for a task that is being repeated (or whenever the user asks), find the lowest-cost model likely to produce the same result, give a prompt tuned for it, and a quick way to check it holds up.

Be honest: you cannot measure token usage live, so this is a recommendation to test on a couple of real cases, not a guarantee.

## The model tiers

- **Haiku** — fastest and cheapest. Mechanical, structured, repetitive work: extracting data, tagging, formatting, pulling a straight report, simple summaries, find-and-replace.
- **Sonnet** — the default. Judgment, interpretation, multi-step work, and careful writing: analysis, reports that need explaining, drafting, most day-to-day tasks.
- **Opus** — the heaviest. Deep, multi-source reasoning, complex research, and high-stakes problem solving. Costs the most, so reserve it.

## How to pick

1. **Is the task mechanical or structured?** (extract, tag, format, pull, simple summarize) → try **Haiku**.
2. **Does it need judgment, interpretation, multi-step reasoning, or careful writing?** → **Sonnet**.
3. **Only if it is genuinely hard** — many sources, high stakes, deep reasoning → **Opus**.
4. **Split the work.** Do the thinking once on Sonnet, then run the repetitive bulk pass on Haiku.

Cheaper models do best with more explicit instructions, so when you tune the prompt for a lower tier, spell out the steps, give the exact output format, and include an example.

## Steps

1. Read the task that was done (or that the user describes).
2. Name the model they are using now, if known, and the lowest tier likely to match.
3. Write a prompt tuned for the cheaper model — explicit steps, exact format, an example.
4. Tell them how to check: run the cheaper setup on 2–3 real cases and compare to a known-good output. If it matches, switch. If not, step back up a tier.

## Output format

For a simple case, answer inline. For a task they will repeat, produce a short one-pager (markdown or a branded file) with this shape:

```
# Downsize: [task name]

Was using:   [model, if known]
Try instead: [recommended model]
Why:         [one line on complexity level]

## Tuned prompt for [recommended model]
[the prompt, with explicit steps, exact output format, and an example]

## How to check it holds up
Run this on 2–3 real cases and compare to your known-good result. Match → switch. Miss → step back up.
```
