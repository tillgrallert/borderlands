---
layout: post
title: "Git and GitHub"
date: 2015-06-10 10:24:34
---

# versioning systems

- git: versioning tool
- GitHub: is the online platform for sharing and collaborating using git
- subversion: private, some people still use it

## git

- git is open, approved by the W3C
- follow the instructions on GitHub to install git through the command line
- seems to be the most complicated thing for humanists
- one has to remember the order of steps over and over and over again
    + get them tattooed on our forearms

- git can be installed through the command line. `$sudo app-get install git`

1. **initiate** git on the highest level of your project!
    - `$git init` creates two things: `.git` (folder) and `.gitignore` (file)
    - make sure to add all file types you want to ignore (images, etc.) and **everything** that contains sensitive information
2. **add**: now, git needs to start tracking changes
    - `$git add .` 
    - every new file, folder, etc. needs to be added, which can be done by the specific path or using the above command again
3. **commit**: every new file, folder, etc. 
    - `$git commit -m "added something, made some changes, etc."`
    - start with the message "initial commit"
4. **add and commit**: add and commit can be done at the some step: `$git commit -am "added something to a specific file"`
4. check status of git: `$git status`
- one can always start over: **BUT NEVER ever DO so** `rm -r .git`

# GitHub

Everything is done in pushing and pulling.

## general commitments among collaborators to avoid conflicts

Always pull the moment you want to start working on something in order to make sure that you start with the most current version.
Always promise to push at the end of the session! And, of course, commit and push constantly

## push

`git remote add origin https://github.com/tillgrallert/borderlands.git`
`git push -u origin master`

- `origin` is the variable that will hence stand for the full address
- `master` addresses the master branch
- `-u` is short for "upstream"

## pull

## clone

`$git clone https://github.com/...`
- make sure to be in the right working directory

## branches

- if you work on a single branch, sequential edits will overwrite each other
- so use branches for each **contributor**
    + none of the code has to be reviewed among contributors
- many projects use **forking**, which means, you are not technically a member of a project. You sign out code and then make a pull-request that includes a "code review", i.e. an editorial decision

1. create a branch: checkout
    + `$git checkout -b [new branche's name]`
    + `-b` creates a new branch
    + `$git branch` will return all branches
    
2. push a branch back to GitHub
    + `$git push origin [name of the branch]`

## merges

## public / private repos

Write them an email explaining that you use github in class etc. and you will get a small number of private repositories