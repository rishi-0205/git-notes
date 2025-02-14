## Git Cherrypick

It is a powerful command that enables arbitrary git commits to be picked by reference and appended to the current working HEAD. Cherry picking is the act of picking a commit from a branch and applying it to another. This command can be useful for undoing changes. For example, say a commit is accidently made to the wrong branch. You can switch to the correct branch and cherry-pick the commit to where it should belong.

#### Usage

> git cherry-pick <commit>

This command copies the commit content and pastes on the new branch and creates new commit with new hash but the old message. The old commit still stays the way it was.

> git cherry-pick -e <commit>

This command lets you edit the commit msg.

> git cherry-pick -n <commit>

This command makes changed in the working directory but does not commit those changes.
