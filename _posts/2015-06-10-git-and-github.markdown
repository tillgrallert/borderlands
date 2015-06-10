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

$sudo app-get install git

1. **initiate** git on the highest level of your project!
    - `$git init` creates two things: `.git` (folder) and `.gitignore` (file)
    - make sure to add all file types you want to ignore (images, etc.) and **everything** that contains sensitive information
2. **add**: now, git needs to start tracking changes
    - `$git add .` 
3. **commit**: every new file, folder, etc. 
4. check status of git: `$git status`