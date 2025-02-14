## Git Log

Git log gives history of changes.

#### Usage

> git log

Basic command to display basic detail

> git log --oneline

Condenses each commit to a single line

> git log --decorate

Displays all the references that point to each commit

> git log --stat

Displays the number of insertions and deletions to each file altered by each commit.

> git log -p

Displays actual changes done to the file in each commit.

> git shortlog

Groups and displays each commit by author displaying only the first line of each commit message.

> git log --graph --oneline --decorate

Draws an ASCII graph representing the branch structure of the commit history. Usually used in conjunction with --oneline and --decorate to make it easier to see which commit belongs to which branch.
