---
description: Write a commit message
metadata:
  version: 0.1
---

# Write a Commit Message

You are tasked with writing a commit message for the uncommitted changes in the current repository. This should apply to all the current uncommitted changes, unless the user requests a smaller subset of the changes to be recorded.

Use the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format.

Do not include any attribution either to yourself or any contributing developers, including the user.

Write the commit message into a `.debug/commit-message.txt` file in the root of the repository, completely overwriting the previous contents if it already exists and not considering or referencing any of them since they belong to a totally separate previous commit. If the `.debug` directory does not exist, create it and add it to `.gitignore`.
