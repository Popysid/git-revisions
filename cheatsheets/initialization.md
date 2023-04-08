# Initialization of a Git project

## New local project

### Initialization:
1. Open bash terminal
2. Print working directory `pwd`
3. Go to your **root** directory `cd ~`
4. Otherwise type `cd ..` to go up one folder until you reach it
5. Create a directory for your project `mkdir directory-name`
6. Initilize git project `git init`

### First commit: 
1. Create first file `touch filename.txt`
2. Update file `nano filename.txt`
3. Type some text in nano
4. Save with **^O** (Control + O)
5. Quit nano with **^X** (Control + X)
6. Add file to git `git add filename.txt`
7. Commit the changes `git commit -m "message git"`

---

## New remote project

### Create repository:
1. Go to [GitHub](https://github.com/)
2. Sign-in to your account
3. Click on **repositories**
4. Click on **New**
5. Enter a name
6. Select *public* or *private*
7. Click on **Create repository**
8. Copy SSH url
9. Paste it somewhere to retrieve it easily


---

## Link Git to Github

### SSH connection:

Refer to [this article](https://docs.github.com/fr/authentication/connecting-to-github-with-ssh) 

### Add remote origin to local repository:
1. Get back to bash terminal
2. Check existing remote `git remote -v`
3. If no return from this command, need to add origin
4. Add origin `git add remote origin git-ssh-origin-url` (replace *git-ssh-origin-url* by the SSH url you copied)
5. Check remote `git remote -v` (should prinnt your fetch and push remote origin url)
6. If returns something wrong set it again `git set-url origin git-ssh-origin-url`
7. If needs to remove origin `git remote remove origin`

---

## Push to remote origin

### First push:
1. Verify that your git status is clean `git status`
2. If any unstaged modifications `git add filename.txt` then `git commit -m "modification message"`
3. Or if you don't want to commit yet `git stash`
4. Verify that you last commit is in stage `git log` (lists your commits)
5. If happy with everything, push `git push -u origin branch-name` (for a first push branch-name should be *main* or *master*)

---

## Check your remote repository

### On Github:
1. Go to [GitHub](https://github.com)
2. Click on your repository name
3. check that the last commits you pushed are here

---

**Done!**