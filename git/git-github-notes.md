# Git Notes 
###### CS50 Lecture of Bryan Yu
---

## Table of Contents
1. [Introduction](#introduction)
2. [Commands](#commands)
    - [Git clone](#git-clone)
    - [Git add](#git-add)
    - [Git commit](#git-commit)
    - [Git status](#git-status)
    - [Git push](#git-push)
    - [Git pull](#git-pull)
    - [Git log](#git-log)
    - [Git reset](#git-reset)
    - [Git branch](#git-branch)
    - [Git fetch](#git-fetch)
    - [Git merge](#git-merge)


## Introduction
A Git is a **version-control tool**. A command line tool that enables to track changes to code. It allows us to synchronize code between different people. 

**Github**. A website that stores git repositories ([GitHub](https://github.com))

## Commands

### Git clone
Take an online repository from internet and download to local computer

Syntax
```git
git clone <url>
```

Sample
```git
git clone https://github.com/rodrigo-sambayon/programming-notes.git
```

### Git add
Add a file to track 

Syntax
```git
git add <filename>
```

Sample
```git
git add foo.py
```

### Git commit
Tell git to take snapshot of the current state of the repository and keep track of many changes made to the files added using `git add`. Commit message `-m` is the description of the changes made over time.

`git commit -am` allows us to commit all changes.

Syntax
```git
git commit -m "message"
git commit -am "message"
```

Sample
```git
git commit -m "Initial commit"
git commit -am "Add new heading"
```

### Git status
Tells us what's currently happening in my repository.

Syntax
```git
git status
```

### Git push
Push the changes to github so that the online version of the repository has same contents as the local version of the repository.

Syntax
```git
git push
```

### Git pull
Pick the changes in the online repository to update the local version of the repository. 

Syntax
```git
git pull
```

### Git log
Kepp track of all changes made in the repository. For each `commit`, it tells what is the commit hash, who made the commit, the date of the commit and commit message.

Syntax
```git
git log
```

### Git reset
Take the current state of the repo and revert back to an older state. `<commit>` refers to the commit hash.
`origin/master` reset the repository to the original version in Github.

Syntax
```git
git reset --hard <commit>
git reset --hard orgin/master
```
Sample
```git
git reset --hard f0531eff4c71d490dd4035265ccbab7c4cbc6b5c
```

### Git branch
Allows to work on different parts on the repository at the same time such as working on a new feature. `HEAD` specifies what branch your are currently on. Then, branches can be merge after.

Syntax (*display list of branches*)
```git
git branch 
```

Syntax (*creating new branch and pointing the HEAD to it*)
```git
git checkout -b <branch_name>
```

Syntax (*switching out to existing branches*)
```git
git checkout <branch_name>
```

### Git fetch
Allows you to retrieve updates from a remote repository without applying them to your local working directory. When you run `git fetch`, Git contacts the remote repository, checks for any new commits or changes (such as branches, tags, or updates), and downloads them to your local machine. However, it **doesn’t merge** those changes into your current working branch.

Syntax
```git
git fetch origin
```

### Git merge
Take changes on one branch and merge to current branch where the head is pointing to.

Syntax (*Head is in master branch*)
```git
git merge <other_branch_name> 
```


### Github Fork
Making your own copy of other repository  such as `bootstrap` into your accoount. Make changes to it and merge your change via `pull requests` and the admin of that repo can examine/review your pull request.

### Github Pages
Take static websites and deploy to internet for free.

#### Steps
1. Create a new repository name `<your_username>.github.io`.
2. Create the repo.
3. Clone it.
4. Write HTML/css/js.
5. Git add, commit, push.
6. Access your pages via `https://<your_username>.github.io`.











