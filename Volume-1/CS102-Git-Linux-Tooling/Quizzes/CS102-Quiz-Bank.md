# CS102 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Linux & Command Line Fundamentals

1. What's the difference between an absolute path and a relative path? Give an example of each.
2. Why is checking `pwd` before running a destructive command (like `rm -rf`) a good habit?
3. What do the three permission groups in `ls -l` output (e.g. `rwxr-xr--`) represent?
4. What's the difference between `head`, `tail`, and `tail -f`?

## Week 2 — Text Processing & Shell Power Tools

5. What does the `|` (pipe) operator actually do, conceptually?
6. When would you reach for `grep` vs. `sed` vs. `awk`? Give one example task for each.
7. Write (on paper, no need to run it) a piped command that finds all lines containing "ERROR" in a file and counts how many there are.
8. What's the difference between `>` and `>>` in redirection?

## Week 3 — Git Fundamentals

9. Describe the three-tree model (working directory, staging area, repository) in your own words.
10. Why does `git add` exist as a separate step from `git commit`?
11. What makes a commit message good vs. bad? Give one example of each.
12. What should always go in a `.gitignore`, and why?

## Week 4 — Git Collaboration & GitHub Workflow

13. What's the actual difference between `git merge` and `git rebase`? When would you pick one over the other?
14. What does Git mean when it reports a merge conflict — is it an error, or expected behavior?
15. What's the difference between `git reset --hard` and `git revert`? Which one is safer, and why?
16. What is a pull request, conceptually — what problem does it solve that pushing directly to `main` doesn't?

## Week 5 — Dev Environment & Productivity Tooling

17. Conceptually, how does SSH public/private key authentication work? Why is it more secure than password auth?
18. What's a dotfiles repo, and why is it worth maintaining even for a solo learner?
19. Why should secrets (API keys, tokens) live in environment variables or `.env` files instead of hardcoded in a script?
20. What's the difference between a `tmux` session and just having multiple terminal tabs open?

## Full-Course Gut Check

21. From a completely fresh terminal (no prior config), walk through — out loud, without notes — the exact steps to: set up SSH auth with GitHub, clone a repo, create a feature branch, make a change, commit it, push it, and open a pull request. If you can do this without hesitation, CS102 is done.
