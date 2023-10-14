---
layout: post
title:  "Submitting Assignments"
categories: intro
---


Submitting Assignments
======================

To start the assignment, make sure you are on `main`, and that it is up to date.

    git checkout main
    git fetch upstream
    git diff main...upstream/main

If not up to date, `git pull upstream main`

If this fails, you'll need to setup your upstream
-------------------------------------------------

- Move into the directory in which you cloned your fork
- Type `git remote -v`
- There should be one that is denoted origin - that should be linked to your fork
- We now want to set one called upstream, so when the assignments get updated, you can update your own copy of the repository
- Run `git remote add upstream git@github.com:kevinzluo/CompAssignmentsF23.git`
- now run `git pull upstream main`


Create a new branch for your new assignment
-------------------------------------------

Now create a new branch for the assignment

    git checkout -b assignment_x

If your workspace has current commits
-------------------------------------

    git fetch upstream
    git checkout -b [whatever your current workspace should be called]
    git checkout main
    git reset --hard upstream/main

Stage, Commit, Push
-------------------
- To stage active edits, run `git add -A`
- To commit, run `git commit -m "some commit message here don't actually type this out if you do I will laugh at you"`
- Finally, to push, run `git push`. Sometimes it will say there is no remote branch tracking the current one, at which point just run the command it tells you to run.
- Now, go to github and hopefully it will prompt you to create a PR. 