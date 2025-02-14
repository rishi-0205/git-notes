## Git Tag

Tags are ref's that point to specific points in Git history. Tagging is generally used to capture a point in history that is used for a marked version release (i.e. v1.0.1).
A tag is like a branch that doesn’t change. Unlike branches, tags, after being created, have no further history of commits. For more info on branches visit the git branch page.

#### Creating a tag

> git tag <tagname>

This will create a new tag on latest commit on current branch.
These are lightweight tags, storing only a name pointing to a commit.

> git tag -a <tagname> -m <message in quotes>

This created an annotated tag with a message related to the tag.
These store additional metadata like author, date, message, checksum

> git show <tag>

This command can be used to see details of the tag.

> git tag -a <tag> <commit>

This command is used to add tag to previous commits.

> git push origin <tag>

This command pushes tag to remote repo.

> git checkout <tag>

This command is used checkout tags

> git tag -d <tagname>

This command deletes the tag <tagname>

NOTE: Tags are very similar to branches. They both are pointers to commits, both can be revisited and both can be pushed to remote. But branches are used for development purposes and tags used to mark version/releases. You cannot checkout tags with an attached head. Branches move with new commit, tags dont.
