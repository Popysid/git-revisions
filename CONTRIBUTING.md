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
- Push your changes on your GitHub forked repository
- Create a Pull Request from your issue branch to develop
- If it can be merged without conflicts merged it
