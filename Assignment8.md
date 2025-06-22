
> If you have been given a go ahead to proceed with this assignment, please first create a PR from `develop` to `main`. **Do NOT merge** this at this time. Give this PR the title `All assignments upto 7`. 

## Assignment 8 - Initial Setup
1. Checkout the `develop` branch.
2. Create and checkout branch `history` from `develop`. Create a file `terminalHistory.md` at the root. Push these changes, and merge to `develop`.
3. Pull the latest changes of `develop` branch. Create and checkout a branch `learnings` from `develop`. Check out this branch.
4. Let us call everything you have done for this assignment upto now as `Checkpoint #0`.
5. Create a file `quotes.md`under the `interview` folder. Under that file, create a level 2 heading `Best Quotes I have read in my life`. Recall atleast 3 quotes that have had a significant impact on you, or touched you and add it under this section. These could be on life, motivation, friendships, love, family, anything. **Commit** these changes to `learnings` branch.
6. Add an entry in the `README.md` file under the progress tracker for this task similar to how you have done previously. **Commit** these changes too.
7. Let us call everything you have done for this assignment upto now as `Checkpoint #1`.
8. Create a folder `myLearnings` under the `interview` folder. Create a file `myProjects.md` under this folder. Create a bullet list of tech-projects that you have worked on during your time in IET. The bullets should be in the format `Project Title - <Tenure>`. For example, `I am doing these just for Viva - <August 2015 - June 2019>` or `Waste Everyone's Time by Mentoring Poorly - <July 2024 - Ongoing>` etc. **Commit** these changes, again.
9. Add an entry in the `README.md` file under the progress tracker for this task similar to how you have done previously. **Commit** these changes too.
10. Let us call everything you have done for this assignment upto now as `Checkpoint #2`.
11. Create a file `shortcomings.md` under the root folder. List down atleast 3 of your weaknesses as unordered list. Describe each of them. **Commit** these changes too.
12. Add an entry in the `README.md` file under the progress tracker for this task similar to how you have done previously. **Commit** these changes too.
13. Let us call everything you have done for this assignment upto now as `Checkpoint #3`.
14. Now, create a new branch `backup` off `learnings`. Switch to the `backup` branch. In the `README.md` file, **at the top**, add a heading level one as `This is my backup branch`. Commit and push the changes to the `backup` branch. Raise a PR from `backup` to `develop`. **Do NOT merge**. Next, read about `git reset` and its options from any source you like. Some references: [here](https://www.geeksforgeeks.org/git/whats-the-difference-between-git-reset-mixed-soft-and-hard/), [here](https://www.gitkraken.com/learn/git/git-reset), [here](https://www.w3schools.com/git/git_reset.asp). You'll need these for the following tasks of this assignment.

> In none of the below tasks, you should be editing anything in the `backup` branch, in your local or remote.

## Task 8.1
> Ensure you are on the `learnings` branch. Also, clear your terminal before beginning this Task.
1. Create a branch named `assignment8-task-1` from `learnings`. Checkout to this newly created branch.
2. In the `terminalHistory.md` file, add a level 2 heading as `Task 8.1 Commands`. We will write the entire terminal history to this file after completing the steps below.
3. Let's say, the task is to completely remove the commits you did after the point marked as `Checkpoint #2` above.
4. Execute the command `git log --oneline`. Identify the commit we'd need to achieve this task.
5. Execute the appropriate git command to reset you branch to this identified commit.
6. Copy paste the terminal contents to the file `terminalHistory.md` under the `Task 8.1 Commands` as a [code block](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks). 
7.  Commit and push the changes. Create a PR from `assignment8-task-1` to `learnings`. Give this PR, the title `No negative thoughts`. **Do NOT merge**

## Task 8.2 
> Ensure you are on the `learnings` branch. Also, clear your terminal before beginning this Task.
1. Create a branch named `assignment8-task-2` from `learnings`. Checkout to this newly created branch.
2. In the `terminalHistory.md` file, add a level 2 heading as `Task 8.2 Commands`. We will write the entire terminal history to this file after completing the steps below.
3. This time, the task is to combine all the commits between `Checkpoint #1` to `Checkpoint #3` under one commit.
4. Execute the command `git log --oneline`. Identify the relevant commit ID.
5. Execute the appropriate git command to reset you branch to this identified commit. Club all the changes under a new commit message `locally squashed changes`. Push the changes.
6. Copy paste the terminal contents to the file `terminalHistory.md` under the `Task 8.2 Commands` as a [code block](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks). 
7.  Commit and push the changes. Create a PR from `assignment8-task-2` to `learnings`. Give this PR, the title `Learned how to clean up the mess`. **Do NOT merge**
