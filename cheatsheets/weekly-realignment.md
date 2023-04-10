# Weekly Realignement

A good practice is to realign your work with the remote develop branch on weekly bases so that your local feature branch is not diverging too much with the work pushed and merged by your team. There are different startegies to realign with develop. We will see the different options.
- with [fast-forward](#ff)
- with [non-fast-forward](#nff)
- with [rebase](#rb)

**Disclamer!** This document is a cheatsheet made by a student for revisions purpose. It's my understanding of the good practices. It is not an official documentation to follow blindly. If you're working in a company, follow your company guidelines. If you are studying as well, listen to your teacher/mentor/coach advices.

---

## <a name="ff"></a>Realign on develop with simple merge: (Fast-forward)

You’ll notice the phrase *"fast-forward"* in that merge. **Fast-forward** is the default option for `git merge`command line.

With **Fast-forward**, when possible resolve the merge as a fast-forward (only update the branch pointer to match the merged branch; do not create a merge commit). When not possible (when the merged-in history is not a descendant of the current history), create a merge commit.

The result in your **git history** will be that your commits would have a linear representation. Just as if you made your commits sequentially in the source branch and in the destination branch, even if they were made in parallel.

See [Documentation about fast-forward merge](https://git-scm.com/docs/git-merge)

### Pull the changes from remote develop:
1. Check your Git status on the branch you are `git status`
2. If Git status is not clean `git add filename.txt` or `git add .` if many files
3. Commit your changes `git commit -m "commit message"`
4. Checkout to develop `git checkout develop`
5. Pull from remote develop branch `git pull origin develop`

### <a name="conflicts"></a>Fix Git conflicts if any:
(**TODO:** Place explanation on how to fix Git conflicts here)

### Merge changes from develop to your local feature branch:
1. If no conflicts or conflicts are solved `git checkout branch-name-to-realign-with-develop`
2. Merge the changes from develop `git merge develop`
3. Again, fix conflicts if any
4. Your branch is realigned with remote develop. You're good to go!

---

## <a name="nff"></a>Realign on develop with non-fast-forward merge:

You’ll notice the phrase *"non-fast-forward"* in that merge. **Non-fast-forward** is an option for `git merge`command line, that can be added as a flag in the command like this: `git merge --no-ff source-branch-name` when you're in the destination branch.

With **Non-fast-forward**, Git creates a merge commit in all cases, even when the merge could instead be resolved as a fast-forward.

The result in your **git history** will be that your commits would have a parallel representation. It will keep track of the history of your commits and the graph representation will show the branches created for before this merge.

- See [Documentation about non-fast-forward merge](https://git-scm.com/docs/git-merge)
- See [Discussion about whe to use it on SoF](https://stackoverflow.com/questions/18126297/when-to-use-the-no-ff-merge-option-in-git)

### Pull the changes from remote develop:
1. Check your Git status on the branch you are `git status`
2. If Git status is not clean `git add filename.txt` or `git add .` if many files
3. Commit your changes `git commit -m "commit message"`
4. Checkout to develop `git checkout develop`
5. Pull from remote develop branch `git pull origin develop`

### Fix Git conflicts if any:
See [Paragraph about fixing conflicts](#conflicts)

### Merge changes from develop to your local feature branch:
1. If no conflicts or conflicts are solved `git checkout branch-name-to-realign-with-develop`
2. Merge the changes from develop `git merge --no-ff develop`
3. Again, fix conflicts if any
4. Your branch is realigned with remote develop. You're good to go!

---

## <a name="rb"></a>Realign on develop with rebase:

**TODO:** Place process for rebasing startegy here

