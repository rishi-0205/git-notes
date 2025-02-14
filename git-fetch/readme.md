## Git Fetch

The git fetch command downloads commits, files, and refs from a remote repository into your local repo, but it doesn’t force you to actually merge the changes into your repository.

#### Git fetch commands and options

> git fetch <remote>

Fetch all of the branches from the repository. This also downloads all of the required commits and files from the other repository

> git fetch <remote> <branch>

Same as the above command, but only fetch the specified branch

> git fetch --all

Fetches all the registered remotes and their branches

> git fetch --dry-run

The --dry-run option will perform a demo run of the command. It will output examples of actions it will take during the fetch but not apply them.
