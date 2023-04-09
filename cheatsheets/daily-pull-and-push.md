# Daily Pull and Push

## Most common Git command lines

During development of a project, here are the most common Git command lines:

- **Pull from remote feature branch:** (At the beginning of the work day and before any push)
1. Checkout to your feature branch if not already on `git checkout branch-name`
2. Check if your Git status is clean before pulling `git status`
3. There are some changes that are not ready to commit `git stash`
4. Pull the latest changes from your team `git pull origin branch-name`
5. Retrieve your changes `git stash pop`
6. Add your changes `git add filename.txt` or `git add .`if many files
7. Commit your changes `git commit -m "commit message`
8. Ready to work on feature branch

---

- **Push on remote feature branch:** (At the end of the work day or after a substancial piece of code)
1. Check that your Git status is clean `git status`
2. If not clean `git add filename.txt` or `git add .` if many files
3. Commit your changes `git commit -m "commit message"`
4. Push to remote feature branch `git push origin branch-name`
5. You're all done
