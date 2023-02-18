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

Now create a new branch for the assignment

    git checkout -b assignment_x

If your workspace has current commits
-------------------------------------

    git fetch upstream
    git checkout -b [whatever your current workspace should be called]
    git checkout main
    git reset --hard upstream/main

Now you should be able to follow the instructions from the previous section.
