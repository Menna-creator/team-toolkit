# /handoff-team — turn this work into a reusable skill

Goal: capture the repeatable workflow in this conversation or Project as a new, well-formed SKILL.md (plus any support files) so a teammate with no context from you gets the same results.

## Step 1 — Find the workflow

Look back over the conversation or Project and identify the repeatable task. If several things happened, confirm with the user which one to capture.

## Step 2 — Extract the details

Gather each of these from what actually happened (ask the user only for what is genuinely missing):

- **Goal** — what the task produces and why it matters.
- **When to use it** — the trigger: what a teammate would be doing when they reach for this.
- **Steps** — the exact sequence, in order. Be specific.
- **Tools and sources** — every connector, app, sheet, or dataset used (e.g. Salesforce, GetDex, Hubstaff, Asana, a specific report or folder), and where to find each.
- **Inputs** — what goes in and where it comes from.
- **Output** — the exact format, and a template if there is one.
- **A real example** — one concrete input and the good output it produced.
- **Corrections and gotchas** — what the user had to fix along the way, and anything easy to get wrong.
- **Quality bar** — what "done right" looks like, and anything that must NOT be done.

## Step 3 — Write the SKILL.md

Use this template. Be detailed and concrete — write it for someone who has never seen this task.

```
---
name: kebab-case-name
description: One paragraph. What it does AND when to use it, with the trigger phrases a teammate would actually type. Be a little pushy so it reliably triggers. Keep under 1024 characters. No angle brackets.
---

# [Readable title]

## Overview
What this does and the result it produces.

## When to use
The situations and phrases that should trigger it.

## Steps
1. ...
2. ...
(the exact, ordered process, with tools and sources named)

## Inputs
What is needed and where it comes from.

## Output
The exact format. Include the template below.

### Template
[paste the real template]

## Example
Input: [concrete input]
Output: [the good output]

## Gotchas and quality bar
- Common mistakes to avoid
- What "done right" looks like
```

Rules that make the skill valid on upload: the file must be named `SKILL.md`; `name` is kebab-case (lowercase, hyphens), 64 characters max; `description` is 1024 characters max with no `<` or `>`.

## Step 4 — Add support files

If the workflow needs a template, example file, checklist, or reference doc, create it and put it in a `references/` or `assets/` folder beside the SKILL.md. Reference those files from the SKILL.md so the teammate knows when to open them.

## Step 5 — Hand it over

Save everything and present it as downloadable files (zip the folder if there is more than one). Tell the user the two ways to use it:
- **Share in a Project** — upload the files to the Claude Project's knowledge so anyone in that Project can use them.
- **Install as a skill** — if their account allows it, the packaged `.skill` file installs with a Save button.

End by asking if they want anything tightened before it goes to the team.
