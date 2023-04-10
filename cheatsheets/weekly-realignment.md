# Weekly Realignement

The good practice is to realign your work with the remote develop branch on weekly bases so that your local feature branch is not diverging too much with the work pushed and merged by your team. There are different startegies to realign with develop. We will see the different options.

## Realign on develop with simple merge: (Fast-forward)

You’ll notice the phrase *"fast-forward"* in that merge. **Fast-forward** is the default option for `git merge`command line.

With **Fast-forward**, when possible resolve the merge as a fast-forward (only update the branch pointer to match the merged branch; do not create a merge commit). When not possible (when the merged-in history is not a descendant of the current history), create a merge commit.

See [Documentation about fast-forward merge](https://git-scm.com/docs/git-merge)

### Pull the changes from remote develop:
1. Check your Git status on the branch you are `git status`
2. If Git status is not clean `git add filename.txt` or `git add .` if many files
3. Commit your changes `git commit -m "commit message"`
4. Checkout to develop `git checkout develop`
5. Pull from remote develop branch `git pull origin develop`

### Fix Git conflicts if any:
(**TODO:** Place explanation on how to fix Git conflicts here)

### Merge changes from develop to your local feature branch:
1. If no conflicts or conflicts are solved `git checkout branch-name-to-realign-with-develop`
2. Merge the changes from develop `git merge develop`
3. Again, fix conflicts if any
4. Your branch is realigned with remote develop. You're good to go!

---

## Realign on develop with non-fast-forward merge:

**TODO:** Place process for non-fast-forward merging startegy here

---

## Realign on develop with rebase:

**TODO:** Place process for rebasing startegy here

