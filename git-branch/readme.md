## Git Branch

A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

#### Common Options

> git branch

or

> git branch --list

List all the branches in your repository.

> git branch <branch-name>

Created a new branch called <branch>. This does not check out the new branch.

> git branch -d <branch>

Deletes the specific branch. This is "safe" operation, it prevents the deletion of branch if there are unmerged changes

> git branch -D <branch>

Force delete the specific branch, even if it has unmerged changes.

> git branch -m <branch>

Rename the current branch to <branch>
