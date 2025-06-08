## Useful GIT resources

- [Generate and add SSH Keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- ```git clone <ssh-link-from-github-ui>```
- Setup Github on VSCode: [Setup Steps](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git)
- Install GitLens extension in VSCode.
- Use GITBash or Bash Terminals in VSCODE. Avoid using windows/powershell.

## Branch Naming Conventions
- the branch will have 3 sections: <full_name>-<change_type>-<short_description>
- separate multiple words with underscores within a section
- <firstname_lastname> - < frontend | backend | fullstack > - <short_description_separated_with_underscores> 
For example: ```rasesh_tongia-frontend-ui_for_company_profile```
- use lowercase characters only
- use meaningful branch names


## GIT Conventions
- DO NOT merge anything to the ```main``` branch
- DO NOT create branches off the ```main``` branch
- Always create your branch off the ```develop``` branch
- NEVER use ```git add .``` Add only intended files carefully.
- Although the gitignore will be setup, always ensure you are not pushing the node_modules folder, or any files with credentials/secret keys. Inform other team members asap if you notice any such files being pushed.
- Always use meaningful commit messages
- It is advisable to breakdown a feature into multiple commits on your feature branch. So for example, if in your feature branch, you are changing around 10 files, you can commit them in batches of 3-4 with separate meaningful commits before pushing them. This will help us debugging/backtracking task easier.
- Never force push into any public branch - main or develop.
- **We'll always use ```merge``` to integrate our feature branch changes into the ```main or develop``` branches. However, We'll use rebase on our feature branches to have linear history on them.**
- If the merge check fails on your pull request, due to conflicts with the base branch, always use ```rebase``` as described in the rebasing section below.

### Useful GIT Commands and recommendations
- Always use ```git stash -m "<name for the stash>"``` to save stashes with dedicated names.
- Prefer using ```git stash apply``` instead of ```git stash pop``` to preserve your stashed changes. POP deletes the changes from the stash and you might lose out on your changes if you end up discarding something in the work directory.
- 


## Creating a feature branch -  Example Workflow
- ```git checkout develop```
- ```git pull```
- If the git pull shows you some changes in package.json, its good to do a npm install again so that you have the latest versions of all the libraries as well as any new libraries/packages installed in your local.
- ```git checkout -b <your-feature-branch-name>```. This will create a branch off develop and will switch to that branch.
- Make changes in your feature branch
- ```git add <list-of-changed-files>``` Make sure you are only adding/staging the files that you have changed and not the files from others.
- ```git commit -m "<meaningful-commit-message>"```
- ```git push origin <your-feature-branch-name>```
- Visit the GITHUB UI and create a Pull Request(PR). Ensure the base/target branch is set properly. Usually the base branch would be ```develop``` and compare branch would be ```<your-feature-branch-name>```
- Add reviewers to your PR - atleast 2.
- If some reviewers add some comments or have requested changes, either reply appropriately, or do the requested changes, commit and push them, and then mark the conversation as resolved. 
- Once you've recieved 2 approvals and have no unresolved conversations, you should be able to merge your changes.


## Raising PRs, Merging Changes, and Rebase Help
If you are facing merge conflicts in the PR, please rebase your branch to develop, resolve conflicts and push the updated changes.
1. Switch to develop branch: ```git checkout develop```
2. Pull the latest changes from develop: ```git pull```
3. Rebase your branch onto develop. There are 2 ways:
    - In two steps: ```git checkout <your-branch-name>``` and ```git rebase develop```
    - In one command(via shorthand of above command): ```git rebase develop <your-branch-name>```
    - In both cases, you'll end up in switching to your branch. Also, you can use ```-i flag``` to interactively rebase your branch.
4.  resolve conflicts (if any)
5.  add/stage modified files (if any)
6.  ```git push origin <your-branch-name> --force-with-lease```
7. Ask reviewers to approve the new changes. 
8. Ideally, your PR should not have any merge conflicts now.
9. Merge the PR.

