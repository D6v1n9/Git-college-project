> Only proceed with this assignment once you're done with all previous assignments.

## Assignment 9 - Initial Setup
1. Find the PR you raised for `All assignments upto 7`. Change the PR title to `All assignments upto 7 except 6th`. Ensure the base and compareTo branches are correct and as per mentioned in Assignment 8 Setup Steps. Merge this PR using `squash and merge`.
2. Find the `assignment-8-task1` branch's PR you created for Assignment 8. Change the PR base to `develop`. Resolve conflicts, if any, using rebase. Then, merge the PR using `rebase and merge`.
3. Create a PR from `develop` to `main` titled `Assignment 8 Learnings`. **DO NOT** merge at the moment.
4. Checkout the `develop` branch in your local and pull in the latest changes.
5. Create a folder `coding_preparation` at the root.
6. Create a file `programs.md` under this folder. Add a level one heading `List of programs`.
7. Choose atleast 1 language - CPP, JAVA or PYTHON. This will decide the extension of our program file(s). Create a file named `checkPrime` with appropriate extension as per your choice of language. I'll call this file **`X`** from hereon.
8. Create a branch `dsa-prep`, add commit and push the changes, create a PR to `develop` from this branch. Merge the PR.

## Task 9.1 - Basic Revert
6. Create a branch `bad-developer` from `develop`.
7. Create a branch `good-developer` from `develop`.
8. Create a branch `documenter` from `develop`. 
9. Checkout the `good-developer` branch and update the file **`X`** with a O(sqrt(N)) time-complexity solution to check if a number is prime. Commit using msg "optimised code for checking prime". Create a PR to `develop` and merge this PR using `rebase and merge`.
10. Checkout the `bad-developer` branch and update the file **`X`** with a O(N) time-complexity solution to check if a number is prime.  Commit using msg "un-optimised code for checking prime". Create a PR to `develop`, resolve conflicts using rebase and accept the changes so that the un-optimised code overwrites whatever is present in the file **`X`**. Merge this PR using `rebase and merge`.
11. Checkout the `documenter` branch. We need to rebase this to `develop`. Once you do, under the file `programs.md`, add a bullet(unordered list) item `Program to check if a number is prime` - **`X`**.
12. Commit the changes. Push and raise a PR to `develop`. Merge the changes using `squash and merge`.
13. Checkout the `develop` branch and pull in the latest changes.
14. From the next line onwards, we'll log the entries in the file `terminalHistory.md`. Please ensure that the commands as well as their outputs are clearly visible in this file.
15. Create a branch `git-expert` from `develop`
16. We'll use `git revert` command. You can read more about this [here](https://www.w3schools.com/git/git_revert.asp), and [here](https://www.atlassian.com/git/tutorials/undoing-changes/git-revert). Also read about options/flags `-e, -n, --no-edit` etc.
17. Use the command `git log --oneline` to identify the commit hash for the commit made by the bad developer.
18. Use the command `git revert --no-edit <identified-hash>` to revert the identified commit.
19. Add an entry in the `README.md` under the progress tracker section as `Fixed error introduced by bad developer` and add timestamp as before. Commit and push the changes.
20. Copy everything on the terminal into the file `terminalHistory.md`. Commit and push the changes.
21. Raise a PR from `git-expert` to `develop`. Ideally, This PR should have **atleast** 3 commits - one for the revert you did, one for the progress tracker entry, and one for adding contents to the terminal history file. **DO NOT** Merge.



