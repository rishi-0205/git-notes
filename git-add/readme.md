## Git Add

This command is used to promote pending changes to the staging area.

#### The Staging Area

The staging area(also known as index or cache) is an intermediate zone where git keeps track of the changes before commiting them.
It acts like a pre-commit buffer, you add changes to it, review them and then commit when ready.

#### Command Options

> git add <file or files>

Stage all the changes to the <file> or <files> for the next commit

> git add <directory>

Stage all the changes in <directory> for the next commit

> git add -p

Begins an interactive staging session that lets you choose portions of a file to add to the next commit. This will present you with a chunk of changes and prompt you for a command.

y - stage the chunk
n - ignore the chunk
s - split it into smaller chunks
e - manually edit the chunk
q - exit
a - stage all the remaining chunks
d - dont stage this or any remaining chunk
j - jump to the next chunk(without staging or rejecting)
J - jump to the next chunk without showing it
g - go to a specific chunk
/ - search for a hunk containing specific text
? - show a help menu with all options
