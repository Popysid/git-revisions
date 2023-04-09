# Branches Management

It's important to know how to manage the different branches on Git and GitHub.

## Git local branches management

### Check you local branches:
To check your local branches type `git branch`

### Check local AND remote branches:
To check all branches type `git branch --all`

### Rename the master branch to main:
To rename the master branch to main typ `git branch -M main` (with a capital M)

### Create a local branch:
To create a local branch named *"new-branch"* type `git branch new-branch`

### Switch from main to new local branch:
Type `git checkout new-branch`

### Delete new local branch: (because you are not happy with this branch name)
1. Switch to main first `git checkout main`
2. Type `git branch -d new-branch` (with lowercase d)
3. If it doesn't work: it means you've already commited on this branch, typ `git branch -D new-branch` (with capital D)

### Create a new branch named *"feature/new-branch_1"* and checkout to it in one command line:
Type `git checkout -b feature/new-branch_1`

### Rename a local branch from *"feature/new-branch_1"* to *"feature/my-awesome-feature"*:
1. Make sure you are on the branch you want to rename `git branch` (the branch your are on has a * before its name)
2. If not on th right branch `git checkout feature/new-branch_1`
3. Type `git branch -m feature/my-awesome-feature` (with a lowercase m)

### Push your local branch to remote repository:
Type `git push origin feature/my-awesome-feature` 

---

## GitHub remote branches management