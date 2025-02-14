## Git Commit

The git commit command captures a snapshot of the project's currently staged changes.

#### Command Options

> git commit

Commit the staged snapshot. This will open a text editor prompting you for a commit message.

> git commit -a

Commit a snapshot of all changes in the working directory. This only includes modifications to tracked files (those that have been added with git add at some point in their history).

> git commit -m "Commit Message"

A shortcut command that immediately creates a commit with a passed commit message.

> git commit -am "Commit Message"

Combination of -a and -m

> git commit --amend

Passing this option will modify the last commit. Instead of creating a new commit, staged changes will be added to the previous commit.
