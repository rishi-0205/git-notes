## Git Clone

Mainly used to point to an existing repo and make a clone or copy of that repo in a new directory location.

#### Basic usage

> git clone <remote-repo-url>

This command creates a new subdirectory in the current directory and then clones the repo

##### Clone to a specific folder

> git clone <remote-repo-url> <directory>

This command clones the remote repo in the current directory without creating a new subdirectory

##### Cloning a specific tag

> git clone --branch <tag> <repo>

This command is used to clone only specific tags.
Note: Git treats tags as branches, hence --branch flag

##### Shallow Clone

> git clone -depth=1 <repo>
> This command is used to create shallow clones.
> You can modify depth value to specify how many latest commits must be cloned

##### Cloning a specific branch

> git clone --branch <branch-name> <repo>

This command only clones a specific branch instead of the whole repo

##### Bare cloning

> git clone --bare

This command clones the repo with ommiting the working directory. This means that a repository will be set up with the history of the project that can be pushed and pulled from, but cannot be edited directly. In addition, no remote branches for the repo will be configured. Used to create hosted repository

##### Mirror cloning

> git clone --mirror

This command works same as bare cloning but in addition, it will clone all the extended refs of the remote repository, and maintain remote branch tracking configuration.

##### Cloning with a template

> git clone --template=<template_directory> <repo>

Clones the repo at ＜ repo location ＞ and applies the template from ＜ template directory ＞ to the newly created local branch.
