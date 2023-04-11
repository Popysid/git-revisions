# Contributing to Git-Revisions project

## Documenting an issue:

- Fork the project on GitHub: 
    1. Click on **Fork** button
    2. Enter a rpository name (this will be th name of the project on your github account)
    3. (Optional) enter a description of the project (e.g: "My Git revisions project")
    4. Let the checkbox **copy the `name-of-default-branch` branch only** checked
    5. Click on **Create fork** button
- Clone the forked repository on your local machine:
    1. Click on **Code** button
    2. Choose your preffered clone method (Https, SSH or GitHub CLI)
    3. Click on the **copy** icon
    4. In your terminal type `git clone ` and paste here the copied url
- Pick up an issue on the initial project:
    1. Click on **Issues** button
    2. Click on the issue you want to pick up
    3. On the right click on **assign yourself** link
- Create an issue branch from **develop**:
    1. In your terminal `cd path-to-your-forked-project-folder`
    2. Type `git branch` and verify that you are on **develop** branch
    3. If not, type `git checkout develop`
    4. Create an issue branch `git checkout -b name-of-issue-branch` (e.g: if you pick up issue #5 about "Branches Managment" name your branch "issue5/branches-management")
- Create a file under the corresponding package (e.g: if it's a cheatsheet feature create a file named "branches-management.md" in the "cheatsheets" package)
- Document your cheatsheet
- Push your changes on your GitHub forked repository:
    1. Make sure you added your changes with `git status`
    2. If not, add your changes `git add .`
    3. Commit your changes `git commit -m "commit message"`
    4. Push your changes `git push origin name-of-your-issue-branch`
- Create a Pull Request from your issue branch to develop on your forked project:
    1. Click on **Pull Requests** button
    2. Click on **New pull request** button
    3. Choose **develop** branch as the **base** and your issue branch as the **compare**
    4. Click on **Create pull request** button
    5. Enter a title for your pull request
    6. (Optional) Enter a comment to explain your changes
    7. Click on **Create pull request** button 
- Create a Pull Request from your forked project to the initial project:
    1. Go on your forked project on [GitHub](https://github.com)
    2. Click on **Pull requests** button
    3. Click on **New pull request** button
    4. Choose *"Git-revisions"* as **base repository** and **develop** as the **base**
    5. Choose *"your-forked-project"* as **head repository** and **develop** as the **compare**
    6. Click on **Create pull request**
    7. Enter a title for your pull request (e.g: "issue #5: branches-management")
    8. (Optional) Enter a description of your changes
    9. Let the checkbox **Allow edits by maintainers** checked
    10. Click on **Create pull request**
- Wait for any comment from the maintainers (you should be noticed by GitHub if it happens)
- Address the comment:
    1. Make the wanted changes if it's relevant
    2. Or discuss the comment to defend your choices

 If your changes are validated by the maintainers, they will merge your pull request.

 **Thank you for contributing!**   
