## Git Pull

The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.

#### Git Command Options

> git pull <remote>

Fetch the specified remote's copy of the current branch and immediately merge in into the local copy. Its same as git fetch <remote> followed by git merge origin/<current-branch>

> git pull --no-commit <remote>

Fetches and merges but does not commit the change.

> git pull --rebase <remote>

This one used git rebase instead of git merge

> git pull --verbose

Gives verbose output during a pull which displays content being downloaded and the merge details
