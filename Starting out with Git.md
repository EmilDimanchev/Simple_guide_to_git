# Starting out with Git

This is meant as a cheat sheet to help PhD students and other researchers get started with simple version control workflows.

It is specifically intended for working with Git through a shell (Command Line on Windows or bash/zsh/etc. on MacOS).

### Common commands

Initialize a repository in your current folder

`git init`

Get an overview of what’s going on

`git status`

### Committing 

1. Add a file to your “staging area”
For a certain file

`git add <filename>`

Or add everything

`git add .`

2. Commit what you have staged

`git commit -m “a short message to remind you what this is”`

### Branching

Make a new branch

`git branch <new branch name>` 

List all branches

`git branch` 

Moving into a branch

`git checkout <branch name>`

Renaming branches

`git branch -M <new name>`

### Keeping track of your commits

This will give you an overview of your commits with their respective “hashes” which are essentially reference codes

`git log --oneline` 

If you want to go back to a given commit, use the command below and copy paste the hash

`git checkout <hash of commit>`

You will now find yourself in what is called a “detached head”. If you want to work off of the commit you just checked out, turn it into a new branch:

First, make a new branch

`git checkout <a new branch name>`

Then, go into it

`git checkout <the name of the new branch>`

### Interacting to Github

Connect your local repository with a Github repository
`git remote add origin https://github.com/...`

Push (roughly speaking, “upload”) your files

`git push -u origin main`

### Get repositories from Github

`git clone <url> .`

### Mark files you do not want to be version controlled

Create git ignore file
`touch .gitignore` 

In it, type things you want ignored like folder or file names
