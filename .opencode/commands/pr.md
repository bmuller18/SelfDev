---
description: "Commit, push and create a pull request"
agent: build
---

Create a pull request following this workflow:

1. Run `git status` to see all changed files
2. Run `git diff` to review the changes
3. Run `git log --oneline -5` to see recent commits for style

Ask the user:
- PR title (or use conventional commit format from the last commit)
- PR description/body (optional, can be auto-generated from commits)
- Target branch (default: main or master)

Steps to execute:
1. If there are unstaged changes, ask the user which files to include
2. Stage the files with `git add`
3. Create commit with message following conventional commits: `type(scope): description`
4. Push the branch with `git push -u origin HEAD` (creates branch if not exists)
5. Create PR with `gh pr create --title "TITLE" --body "BODY" --base TARGET_BRANCH`

If `gh` CLI is not installed, inform the user and provide manual instructions:
```bash
git push -u origin HEAD
gh pr create --title "PR Title" --body "Description"
```

Verify the PR was created successfully and provide the URL.
