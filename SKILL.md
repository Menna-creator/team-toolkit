---
name: team-toolkit
description: Four team commands for working smarter with Claude. Use this skill WHENEVER the user types or implies any, even loosely. /handoff-team (also /Handoff_team, "hand this off", "turn this into a reusable skill") — package the current workflow into a detailed SKILL.md plus support files a teammate drops into a Project for the same results. /handoff-ops (also /HandoffOps, "summary for ops or leadership") — a skimmable status summary of the real-world project, with tables, for operations and leadership. /better-prompt (also /BetterPrompt, "how should I have asked this") — after corrections finally got a good result, explain what made the difference and write a one-shot prompt that gets it next time. /downsize (also /downsize-model, "cut token cost") — recommend the lowest-cost model that can match the result, with a tuned example prompt. Also trigger when the user wants to hand off work, document a workflow, brief leadership, improve a prompt, or cut model or token cost, even without the slash command.
---

# Team Toolkit — work smarter with Claude

Four commands the Sell to Sean team uses to hand off work, brief leadership, sharpen prompts, and cut model cost. A user runs one by typing its command or asking for it in plain words. Route to the matching section, read the referenced file for the full method and template, then produce the deliverable.

## Commands

| Command | Also written | What it produces | Full method |
| --- | --- | --- | --- |
| `/handoff-team` | /Handoff_team | A detailed, reusable SKILL.md + any support files so a teammate reproduces this work | `references/handoff-team.md` |
| `/handoff-ops` | /HandoffOps, /HandoffOPs | A skimmable status brief (with tables) of the real work, for ops + leadership | `references/handoff-ops.md` |
| `/better-prompt` | /BetterPrompt | A one-shot prompt that gets the result they just earned through corrections, plus why it works | `references/better-prompt.md` |
| `/downsize` | /downsize-model, "Downsize model" | The lowest-cost model that can match the result, with a tuned example prompt | `references/downsize.md` |

Commands are case-insensitive and work with either a hyphen or an underscore.

## Before producing anything

- These commands work from what is in the current conversation or Project. `/handoff-team` and `/better-prompt` need the actual work visible in the thread. If it is not there, ask the user to paste it, upload it, or open the relevant Project before writing the deliverable — do not guess.
- Make the deliverable a downloadable file when you can create files; otherwise put it in the chat as a clean, copyable block or an artifact.
- Match the team's house style: skimmable, short, plain language. When the output will be shared or logged, show a draft for review before treating it as final.

## Offer the right command (lightly)

You may spot a good moment for one of these even when the user did not ask:
- A task took several rounds of correction before they were happy → offer `/better-prompt` in one line.
- A task looks repetitive, mechanical, or simple → offer `/downsize` in one line.

Keep it to a single soft offer. Do not nag, and do not interrupt an unfinished task.

## /handoff-team

Capture the repeatable workflow from this conversation or Project into a new, well-formed SKILL.md plus any templates or examples a teammate needs, so they get the same results with none of your context. Read `references/handoff-team.md` for the extraction checklist and the SKILL.md template, then save the files and tell the user how to share them.

## /handoff-ops

Write a one-page, skimmable status brief of the real-world project or work-in-progress (not the Claude Project) for operations and leadership to discuss — tables for status, blockers, and next steps. Read `references/handoff-ops.md` for the template.

## /better-prompt

After back-and-forth corrections finally produced the result the user wanted, explain in a few plain points what made the difference, then write a single reusable prompt that would get it on the first try. Read `references/better-prompt.md` for the method and output format.

## /downsize

Recommend the lowest-cost model likely to match the result for a task that is being repeated (or whenever asked), with a prompt tuned for that model and a quick way to check it holds up. Read `references/downsize.md` for the tiering and the one-pager format. This is informed guidance to test on a couple of real cases, not a measured guarantee.
