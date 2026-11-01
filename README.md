# skills

Agent skills I use every day.

## grill-me-humanly

Grills you on a plan or design, one question at a time, until you and the agent
agree on every decision. Each question is asked in plain language, with no
jargon, and every option comes with a concrete scenario (what you do, what the
system does, what breaks) or a small code snippet.

Use it before building something: say "grill me humanly" or run
`/grill-me-humanly`, then describe the plan.

<details>
<summary>Example: the same question, two ways</summary>

The question: *should my private skills folder become the public GitHub repo?*

**How a plain grilling might ask it:**

> Should the public repo preserve the existing git history, or start fresh?

**How grill-me-humanly asked it** (from a real session, shortened):

> Git keeps every old version of every file. If a project goes public, anyone
> can open its history and read those old versions, even files you've since
> deleted.
>
> **A) A brand-new, separate public project** ⭐ *recommended*
> - **What you do:** create `you/agent-skills` with only this skill, a README and a license.
> - **What the system does:** the history starts empty, so visitors see one clean snapshot.
> - **What breaks:** you now have two copies that can drift apart.
>
> **B) Upload your existing folder as-is and make it public**
> - **What you do:** one command, `gh repo create --public --source ~/.agents/skills --push`.
> - **What breaks:** anyone who clicks "History" can read every old snapshot, including
>   your employer's server address in an old config file. Deleting files later doesn't help.
>
> **C) Keep the existing folder but wipe its history first**
> - **What breaks:** every new personal skill needs a decision about whether it stays out
>   of the public version, and one forgotten exclusion leaks it.

</details>

## Install

**Claude Code, Codex, Cursor and other coding agents**

```bash
npx skills add k-droscova/skills
```

**claude.ai or ChatGPT**

1. Download [grill-me-humanly.zip](https://github.com/k-droscova/skills/releases/download/latest/grill-me-humanly.zip).
2. Upload it:
   - **claude.ai:** Settings → Skills → upload.
   - **ChatGPT:** Plugins → Skills → Create → Upload from your computer.
     (Only on plans that include skills.)

**By hand**

Copy `skills/grill-me-humanly/` into your agent's skills folder, for example
`~/.claude/skills/grill-me-humanly/` for Claude Code.

## Credits

grill-me-humanly is based on
[grill-me](https://github.com/mattpocock/skills) by
[Matt Pocock](https://github.com/mattpocock), used under the MIT License. I added
two rules: ask every question in plain language, and back every option with a
concrete scenario or code snippet.

## License

MIT. Each skill folder has its own `LICENSE.txt` with the copyright notices
that apply to it.
