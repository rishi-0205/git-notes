## Git Checkout

In Git terms, a "checkout" is the act of switching between different versions of a target entity. The git checkout command operates upon three distinct entities: files, commits, and branches.

#### Checking out branches

##### B/W existing branches

> git checkout <branch>

This command checks out the specified branch

##### New branches

> git checkout -b <new-branch>

This command creates a new branch named <new-branch> and simultaneously checkout that branch

> git checkout -b <new-branch> <existing-branch>

By default git checkout -b will base the new-branch off the current HEAD. An optional additional branch parameter can be passed to git checkout. In the above example, ＜ existing-branch ＞ is passed which then bases new-branch off of existing-branch instead of the current HEAD.
