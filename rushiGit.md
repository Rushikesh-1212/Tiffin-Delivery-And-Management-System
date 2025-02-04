# Git

## basic workflow

```bash

# create a working directory
> mkdir app1
> cd app1

# initialize empty repo
> git init

# get status of repo
> git status

# get short status of repo
> git status -s

# symbols
# ??: untracked file (repository has not version created)
# A : the file is present in staging area and first version of it will be created in repository when committed
#  M: the changes are present in working directory (not yet moved to staging area)
# M : the file is modified and changes are present in the staging area
# UU:


# add the changes to the staging area
# > git add <file name>

# add all the changes from the current directory to the repository
> git add .

# commit a version in repository
# > git commit -m <message>
# when a commit is recorded by git, it will contain
# - commit id
# - author info
# - committer info
# - date time stamp
# - message
> git commit -m "first version of program"

# get the logs of commits
> git log

# get the logs with more options
# --oneline: use short info instead of long one
# --graph  : render a graph of commits
# --color  : use colors while rendering the commit graph
> git log --oneline --graph --color

# get the difference between the current version and previous version
> git diff

# remove the changes made to the file (which is present in working directory)
# checkout command accepts only one file, which means, if you want to loose the changes from multiple files, then you will have to execute the command multiple times
> git checkout <file name>


# unstage the changes (remove the changes from staging area)
> git reset

# remove the changes from both working directory as well as staging area
# note: please execute this command on your own risk
> git reset --hard

```

## branching

```bash

# branch is just a pointer to the last commit
# a new branch gets created under .git/refs/heads
# for first commit ,
# - a default branch gets created named main or master
# - the file .git/refs/heads/main contains the last commit id

# get the list of branches
> git branch

# create a new branch
# > git branch <branch name>
> git branch branch1

# switch to another branch
# > git checkout <branch name>
> git checkout branch1

# create and checkout the branch
# > git checkout -b <new branch name>
> git checkout -b branch2

# merge a branch
# - checkout the source branch branch
#   - in which you want to merge another branch
# > git merge <branch name>
> git checkout main
> git merge branch1

