## Git Reset

The git reset command is a complex and versatile tool for undoing changes. It has three primary forms of invocation. These forms correspond to command line arguments --soft, --mixed, --hard. The three arguments each correspond to Git's three internal state management mechanism's, The Commit Tree (HEAD), The Staging Index, and The Working Directory.

#### Usage

> git reset --soft <commit>

Moves the head pointer to <commit>, puts all the commits made after <commit> to the staging area and working directory is also unaffected

> git reset --mixed <commit>

Moves the head pointer to <commit> as well as unstages any changes or commits made after <commit>. Working directory remains untouched

> git reset --hard <commit>

Moves the head pointer to <commit>, all changes are unstaged and working directory is reset to the state of <commit>
