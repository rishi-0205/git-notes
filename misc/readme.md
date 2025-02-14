## MISCELLANEOUS TOPICS

###### What is a Repository?

A repository(repo) in git is a storage location where all your project files, history, and version control information are kept.
The structure of git repo looks like this:
my-project/ # Your project folder (Repository)
│
├── .git/ # Hidden folder (Git database)
│ ├── objects/ # Stores commits, files, tags as SHA-1 hashes
│ ├── refs/ # References to commits (branches, tags)
│ ├── HEAD # Points to the current branch
│ ├── config # Configuration settings
│ ├── index # Staging area (index)
│ └── logs/ # History of branch changes
│
├── file1.txt # Project files
├── file2.py
└── README.md

###### What is a Branch in git?

A branch in git is parallel version of your repository that allows you to work on different features, bug fixes, or experiment without affecting the main project.
It can be thought of as a copy of the codebase where you can make changes without disrupting the main branch.

###### What is a remote in git?

A remote in git is a reference to a repository hosted on a server(such as github, gitlab or bitbucket). It allows multiple developers to collaborate on the same project by pushing and pulling changes between the local and remote repositories.

###### What are the difference between local and remote branches?

Local branches exist only on your computer. They can be created, modified and deleted without affecting others. They need to be pushed to remote repositories to be shared.
Remote branches exist on a remote repository(Github, Gitlab,Bitbucket). They represent branches that have been pushed by you or others. You cannot directly modify a remote branch - you must pull, merge, or push changes to update it.

###### What happens when local and remote are not in sync?

When your local branch and remote branch are out of sync, git will alert you when you try to push or pull changes.
This happens in two main senarios:

1. Local is ahead of remote:
   When you made new commits locally but haven't pushed them yet, git warns that your branch is ahead of origin/main. This is normal situtaion where git will allow you to push
   Local: A --- B --- C (main)
   Remote: A --- B (origin/main)
   You need to push commit "C" to sync.
2. Local branch is behind remote:
   When someone else has pushed new commits to the remote branch, your local branch does not have those changes. Git will warn you and will not let you push your changes. You need to pull from remote and merge them to your local branch, only then you will be allowed to push on remote branch.
   Local: A --- B (main)
   Remote: A --- B --- C (origin/main)
   You need to pull commit "C" before pushing.
3. You made local commits (C,D) and someone else pushed new commits (X,Y) to the same branch. Now your local and remote histories do not match, so git will block you from pushing. There are two options to resolve this, first is to merge the remote with local which is a safer option but keeps extra merge commits. Second is to rebase, give you a cleaner history.
   Local: A --- B --- C --- D (main)
   Remote: A --- B --- X --- Y (origin/main)
   You and someone else made different commits.

###### What happens when you delete a local branch? What happens when you delete a remote branch?

A local branch exists only on your computer and is not shared with others until you push it. Deleting a local branch does not affect the remote repository. When the branch it deleted, it is removed from your local system. The commit history remains intact unless they were unmerged and have no references.
A remote exists on Github, Gitlab, or other remote repositories. Deleting a remote branch removes it for everyone with access to the repo. It does not delete the branch from other people's local repositories - they must manually delete it if needed. When the remote branch is deleted, no collaborators can pull it anymore. If someone has the branch locally, they can keep working on it, but they need to push to a new branch name if they want to restore it.

###### What do these mean? Pull requests and Merge requests

Both pull requests and merge requests serve the same purpose: they allow developers to propose code changes and request reviews before merging them into the main branch.
A Pull Request(PR) is a request to merge changes from one branch into another in a remote repository(Github and Bitbucket).
A Merge Request(MR) is same as a Pull Request but is used in Gitlab instead of Github.

###### What is a fast-forward merge?

A fast-forward merge occers when the target branch has no new commits since the feature branch was created, allowing git to move the branch pointer forward without creating a new merge commit.

###### What is a squashed merge?

A squashed merge is a type of merge where all the commits from a feature branch are combined into a single commit before merging into the main branch. This gives a clean commit history on the main branch.

###### What is a HEAD in Git?

HEAD is a pointer(or reference) to the current commit you are working on in Git. It typically points to the latest commit on the currently checked-out branch.
