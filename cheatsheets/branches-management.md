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

### Delete a remote branch from local machine:
If you have accidentally pushed an unwanted branch, type `git push origin --delete feature/my-awesome-feature`

---

## GitHub remote branches management

### Create a remote branch:
1. Go in your repository
2. Click on **Code** button if **Branches** button is not on screen
3. Click on **Branches** button
4. Click on **New branch** button
5. Enter a branch name
6. Select the source branch you want
7. Click on **Create branch** button

### Create a remote branch from an issue:
1. Click on **Issues** button
2. Click on the issue you want to create a branch from
3. Assign the issue to yourself by clicking **assign yourself** link (in Assignees section on the right)
4. Click on **Create a branch** (in Development section on the right)
5. Enter a branch name (edit the suggestion)
6. Select the destination repository
7. Click on **Change branch source** link
8. Select a branch source (ideally develop)
9. Click on **Create branch** button

### Switch branch:
1. Click on the button with the branch icon with the name of the branch you are on
2. In the drop down menu select the branch you want to switch on
3. If you don't se the name of the branch uou want to switch on, click **View all branches** link

### Rename a remote branch:
1. Click on **Code** button if **Branches** button is not on screen
2. Click on **Branches** button
3. Click on the edit icon on the right of the name of the branch you want to rename
4. Edit the name of the branch
5. Click on **Rename branch**

**Important!** This will affect the link with your local branch that is tracking the remote one. If you want to check type `git branch --all` on your terminal. You'll see that it has not change the name of the branch in your branches list. You need to `git fetch`. Then you'll see that you have fetched the renamed branch but if you type `git branch --all` again, you'll have in the remote barcnhes list the old name and the new name. Type `git fetch --prune origin`. Now yif you `git branch --all`again, the old name has disapeared, but your local branch still have the old name and is not tracking the new remote branch name. try and do a push to from it to check: 
- do a change on the file (e.g. just a comment), type `git add filename.txt` then `git commit -m "commit message"` then `git push`
- As the old local branch name tracks the old remote branch name, instead of pushing on the new name it has recreated the old one and now you have 2 branches. that is not what we want.
- So we are going to delete this old name branch on Github:

### Delete a remote branch:
Click on the trash icon on right of the name of your unwanted branch (that's it!)

### Rename also your local branch and track the new remote branch name:
1. Make sure you're on the right branch `git branch` (the granch should have the * before its name)
2. Type `git branch -m new-branch-name` (with lowercase m)
3. Check the new branch name `git branch`
4. Set the upstream origin of your local branch renamed `git branch -u origin/new-branch-name`
5. You'll see a message saying: "branch '*new-branch-name*' set up to track '*origin/new-branch-name*'."

Now try again pushing some changes upstream with `git push`, and you'll see that the remote tracked branch has been correctly setup.
Clean your local branches list with `git fetch --prune origin` again to remove locally the remote branch that you have deleted on GitHub.




