## Git Diff

This command is used to compare changes between different versions of the files in your git repository.
It helps to see what has changed in your working directory, what is staged but not yet committed and differences between commits, branches or tags

#### Basic Usage of git diff

##### View unstaged changes

> git diff

Shows all the changes in the working directory that has not been staged.

##### View staged (but not commited) changes

> git diff --staged

or

> git diff -- cached

Shows difference between the staging area and the last commit

#### Comparing different states

##### Compare working directory vs. last commit

> git diff HEAD

Shows changes in both unstaged and staged files

##### Compare two commits

> git diff <commit1> <commit2>

Shows differences between two commits

##### Compare a branch with another

> git diff <branch1> <branch2>

Shows differences between two branches

##### Compare a file across two commits

> git diff <commit1> <commit2> -- <file>

Shows changes only for <file> between two commits
