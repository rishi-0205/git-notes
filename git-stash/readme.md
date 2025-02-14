## Git Stash

Temporarily saves your uncommitted changes without committing them, allowig you to switch branches or work on something else without losing progress, like a clipboard for your uncommitted changes, stash them away and bring them back later.

##### Stashing your work

> git stash

This stashes the changes made since last commit and reverts the branch to latest commit.
NOTE: This works only on the files which are being tracked by git.

> git stash save "saving-msg"

Adding a message to stash helps manage multiple stashes

##### Re-applying your stashed changes

> git stash pop

Popping your stash removes changes from the stash and reapplies them to your working copy

> git stash apply

This reapplies the changes and keep them in your stash as well

##### Stashing untracked files

> git stash -u

Adding -u flag stashes even untracked files

##### Stashing ignored files

> git stash -a

Adding -a flag stashes ignored files along with untracked files as well

#### Managing multiple stashes

> git stash list

This lists out all the stashes stored.

> git stash pop stash@{<stash-number>}

By default git stash pop reapply most recently added stash, but we can pass an identifier stash@{stash-number} as last arguement to choose from the available stashes

#### Viewing stash diffs

> git stash show

Shows summary of stash

> git stash show -p

Shows full diff of a stash

On both the above commands you add identifier as an arguement at the end to view specific stash.

#### Partial stashes

> git stash -p

This command opens an interactive session to select from the hunk to stash. It stashes and removes the selected changes from the working directory.

#### Creating a branch from your stash

> git stash branch <new-branch> <stash-identifier>

Created a new branch from the selected stash. It automatically restores and commits the tracked files but only restores the untracked files. It doesn't restore the ignored files at all.

#### Cleaning up your stash

> git stash drop <stash-identifier>

Deletes the specififed stash

> git stash clear

Deletes all the stashes
