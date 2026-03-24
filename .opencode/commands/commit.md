---
description: "Create a git commit with your changes"
agent: build
---

Create a git commit with the current changes following these steps:

1. Run `git status` to see all changed files
2. Run `git diff` to review the staged and unstaged changes
3. Run `git log --oneline -5` to see recent commit messages for style consistency

Analyze the changes and create a commit that:
- Has a clear, concise commit message (max 72 chars for subject line)
- Follows conventional commits format if applicable: `type(scope): description`
- Explains WHY the change was made, not just what changed
- Is atomic (one logical change per commit)

If there are no changes to commit, inform the user that there are no changes to commit.

Ask the user for confirmation before executing the commit. If they want to modify the message, allow them to do so.
