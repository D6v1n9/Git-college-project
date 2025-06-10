# Part 6
> Ensure that you've completed the previous 5 assignments before starting with this.

## Common Instructions

1. Checkout the `develop` branch in your local and pull the latest changes.
2. Did you notice something interesting? If not, run `git branch -r` in your local. This command will list all the remote branches. You may notice there's a branch, created by some idiot, with a poorly given name. Let's call this branch X. *If you do not see this branch, the idiot spared you from this assignment since you've still not completed assignment 5 **correctly**. Please do it at the earliest*
4. Checkout the branch `X`.
5. Go and view the file `review.md`.
6. Below the `Feedback` section, create a new level 3 heading named `Feedback for Rasesh`. Add your detailed feedback for me here.

> For people who have grasped a lot of git concepts and are comfortable using AI tools to solve assignments while also comprehending what every command is doing, i'd like you to try **6.1 Renaming the Branches (Without Hints)**.
If you are still in the process of learning, try out **6.1 Renaming the Branches (With Hints)**

## 6.1 Renaming the Branches (Without Hints) - To challenge yourself
6. Push your changes to this branch X.
7. Since the name is bad, rename the branch to something meaningful - (referred as Y from now on) and push the newly created branch to remote.
8. Delete the poorly named branch from local as well as remote. **Execute commands only if you know what you are doing**
9. Add entry to the progress tracker for branch Y.
10. Raise a PR for Y. **Do not merge**

## 6.1 Renaming the Branches (With Hints) - For people who are still learning and want step by step instructions.
6. Add, commit and push to this branch `X`. **DO NOT Create a PR**
7. Checkout the branch `develop` again.
8. Rename the branch `X` to something that is meaningful in your local. `git branch -m X <MeaningfulBranchName>`.
9. Switch to the newly renamed branch, and push the renamed branch to remote.
10. Let's delete the old branch. `git push origin --delete X`
11. Before raising a PR for our newly created branch, remember that we again forgot to add to the progress tracker.
12. Create an entry in the `README.md` file, under the "progress" section as you've been doing for assignment 5.
13. Add, commit and push to this branch.
14. Create a PR from this new branch to develop. Add me as a reviewer. **DO NOT merge it**
15. In your local, execute `git branch`. If you still see the branch `X`, delete it from your local by using `git branch -d X`, or if it throws errors saying it has unmerged changes,
16. `git branch -D X`.
