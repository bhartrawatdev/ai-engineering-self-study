# CS102 — Main Project: Personal Dev Environment + End-to-End Git Workflow

This is the standalone spec for CS102's Main Project (also summarized in `CS102.md`). Use this file as your working checklist while building.

## Description

Two connected deliverables that together prove you can operate like an engineer, not just write code in isolation: a real dotfiles repo reflecting your actual setup, and a simulated but realistic collaboration workflow on GitHub (branches, a conflict, a merged PR).

## Part A — Dotfiles Repo

- [ ] Public GitHub repo containing your shell config (`.bashrc`/`.zshrc` or equivalent) and Git config (`.gitconfig`).
- [ ] Any editor settings you want version-controlled (VS Code `settings.json`, extension list, etc.) — optional but encouraged.
- [ ] A `.gitignore` that explicitly excludes secrets and `.env` files, with a comment explaining why they're excluded.
- [ ] A `README.md` explaining what's in the repo and how to apply it to a fresh machine.

## Part B — Simulated Collaboration Workflow

Using any small existing script (the CS101 Log Analyzer works well as the base):

- [ ] At least 3 feature branches, each for one distinct, focused change.
- [ ] At least one deliberate merge conflict, created intentionally and resolved by hand.
- [ ] At least one pull request opened and merged through the GitHub UI, with a real description explaining the change and why it was made.
- [ ] Clean, well-messaged commit history throughout — no "fix," "wip," "asdf," or similar filler commits.

## Suggested Approach

1. Set up the dotfiles repo first (Part A) — it's lower-stakes and gets your GitHub/SSH setup verified before you need it for Part B.
2. For Part B, plan your 3 branches *before* starting: pick 3 small, independent changes to the base script so you have a real reason for each branch to exist, rather than inventing busywork.
3. Deliberately engineer the conflict — e.g., have two branches both modify the same function's docstring or the same import line — so you get real practice resolving it rather than hoping one occurs naturally.

## Stretch Goals

- [ ] A shell script that automates applying your dotfiles to a fresh environment (symlinking configs into place) instead of requiring manual copy steps.
- [ ] Use `tmux` for the Part B workflow instead of a single terminal window.
- [ ] Redo at least one branch's integration using `rebase` instead of `merge`, and write a short note on how the resulting history differs.

## What "Done" Looks Like

- The dotfiles repo reflects your actual, current setup — not a fabricated example you'll never really use.
- You can run `git log --oneline --graph` on the Part B repo and narrate the story of what happened at each point without hesitation.
- SSH authentication to GitHub works from your primary machine.
- Both repo links are recorded here once complete:
  - Dotfiles repo: `<paste link once created>`
  - Collaboration-workflow repo: `<paste link once created>`
