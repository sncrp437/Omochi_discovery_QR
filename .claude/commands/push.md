---
description: Commit all changes and push to current branch
allowed-tools: Bash
argument-hint: [commit message]
---

## Task

Commit all staged and unstaged changes, then push to the current git branch.

## Instructions

1. Run `git status` to see what changes exist
2. Run `git branch --show-current` to get the current branch name
3. Run `git diff --stat` to show a summary of changes
4. If there are changes to commit:
   - Stage all changes with `git add .`
   - Create a commit with the provided message (or generate one based on changes if no message provided)
   - Push to origin with the current branch name
5. Report the result to the user

## Commit Message

$ARGUMENTS

If no commit message is provided, generate a brief descriptive message based on the changed files.

## Commit Format

Always include the co-author line:
```
Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>
```

## Safety

- Never force push
- Never push to main/master without explicit user confirmation
- Show the user what will be committed before committing
