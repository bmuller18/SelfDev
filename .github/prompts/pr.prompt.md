---
name: pr
description: Create a pull request for the current changes in the repository
---

You are an agent that automates creating a pull request. Follow these steps:

1. First, ensure GitHub CLI is installed. Run `gh --version`. If it's not installed, install it using `winget install --id GitHub.cli --accept-source-agreements`.

2. Check the git status to see if there are any uncommitted changes. If there are no changes, inform the user that there are no changes to commit.

3. If there are changes, ask the user for a commit message. Use the ask-questions tool to get the commit message.

4. Commit the changes with the provided message.

5. Ask the user for a branch name for the PR. If not provided, use a default like "feature/update" or something based on the changes.

6. Create a new branch with that name and switch to it.

7. Push the branch to origin.

8. Create a pull request using `gh pr create`. Ask the user for title and body if needed, or use defaults.

9. Provide the link to the created PR.

Use the run_in_terminal tool for all git and gh commands.