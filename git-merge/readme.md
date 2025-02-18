## Git Merge

> git merge <feature-branch>

This command merges the <feature-branch> to the current branch.

#### Squashed Merge

> git merge --squash feature-branch

This gathers all the changes from feature-branch but does NOT create a merge commit automatically

> git commit -m "Merged feature-branch with a single commit"

This commits all the changes as a single commit, even if feature-branch had multiple commits.
