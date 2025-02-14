## Git Rebase

Rebasing is the process of moving or combining a sequence of commits to a new base commit. From a content perspective, rebasing is changing the base of your branch from one commit to another making it appear as if you'd created your branch from a different commit. Internally, Git accomplishes this by creating new commits and applying them to the specified base. It's very important to understand that even though the branch looks the same, it's composed of entirely new commits.

#### Usage

> git rebase <base>

This command rebases the current branch onto <base>. When the command is run, git finds the common ancestor commit and detaches the branch from that part. Then git recommits all the commits individually on the new base.
This process also changes the commit hash as new commits are being made.

> git rebase --interactive <base>

Running git rebase with the -i flag begins an interactive rebasing session. Instead of blindly moving all of the commits to the new base, interactive rebasing gives you the opportunity to alter individual commits in the process. This lets you clean up history by removing, splitting, and altering an existing series of commits.

#### Advanced Usage

> git rebase --onto <new-base> <old-base> <branch>

git rebase --onto allows you to rebase a specific range of commits onto a different branch or commit.
Unlike regular git rebase <base>, which rebases the entire branch, --onto gives more control over what to rebase and where to place it.
