# Team Toolkit

Four Claude commands the Sell to Sean team uses to work faster — hand off work, brief leadership, sharpen prompts, and cut model cost.

## What's in it

| Command | What it does |
| --- | --- |
| `/handoff-team` | Turns the work in a chat or Project into a detailed, reusable skill a teammate can drop in and get the same result. |
| `/handoff-ops` | Writes a skimmable, table-driven status brief of the real project for ops and leadership. |
| `/better-prompt` | After you've corrected Claude into the result you wanted, explains what worked and writes you a reusable one-shot prompt. |
| `/downsize` | Recommends the cheapest model that can match the result, with a tuned prompt and a way to check it. |

Commands aren't case-sensitive, and a hyphen or an underscore both work (`/handoff-team`, `/Handoff_team`).

## Install it

Two ways:

- **As a skill** — download `team-toolkit.skill`, open it in Claude, and click **Save skill** to install it (if your account allows skill creation).
- **In a Project** — upload `SKILL.md` and the `references/` folder into a Claude Project's knowledge, so everyone in that Project can use the commands.

## Use it

Type a command (`/handoff-ops`) or just ask in plain words ("brief Sean on where this project stands"). Claude will also quietly offer `/better-prompt` or `/downsize` when it spots a good moment.

## Good to know

- The commands read from what's in the current chat or Project, so `/handoff-team` and `/better-prompt` need the actual work visible in the thread.
- `/downsize` is advice to test on a couple of real cases, not a measured token guarantee.

## Structure

```
team-toolkit/
├── SKILL.md              # the skill — routes the four commands
├── references/           # the method + template behind each command
│   ├── handoff-team.md
│   ├── handoff-ops.md
│   ├── better-prompt.md
│   └── downsize.md
└── team-toolkit.skill    # packaged, installable version
```

---

Internal to Sell to Sean. Edit the files and re-share to update.
