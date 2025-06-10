# Part 5
## 5.1 Stash and Reset
1. Checkout the `develop` branch in your local and pull the latest changes.
2. In the README.md file, below your 100 word introduction, create a level 3 heading titled "Progress Tracker". We'll create an ordered list of changes here.
3. Next, Create a file `analysis.md` under the `interview` folder.
4. Edit that file and create the following level 3 headings

    - **Rank of items(most useful first) for placements**
        
        - Create an ordered list in markdown format, where you list down all the things you think are useful for placements. Do not use any AI tool. Share your perspective about what you think is useful. You can describe your points too. 

    - **Things you'd like to finish before placements/graduating from IET**

        - Do not write the name of any TV show. 
        - List down things, from a tech standpoint on what you'd like to learn before you leave.
5. Next, Create another file `review.md` under the `interview` folder.
    - **Feedback**
        - Leave this section empty for now.

    - **Three things that people closest to you think you're good at**
        - I'd like you to share anything that others find you are good at - should be non-technical. 

6. Stash the file `analysis.md` file with the message `stash containing analysis file`.
7. Stash the file `review.md` file with the message `stash containing review file`.
8. Create a branch for the progress tracker (give a meaningful name), add, commit(provide a meaningful message).
9. Oh, but wait, we forgot to add anything to the tracker we just created. Now, let's try to bring the contents from commit to stage area again. Use `git reset --soft HEAD^`. [Read](https://www.geeksforgeeks.org/practical-uses-of-git-reset-soft/) about what this command does in detail. It will be highly useful going forward.
10. Create an ordered list item under the *Progress Tracker* heading with  the following text,  `Initialised-the-tracker - <YourFullName> - <Current-Timestamp>`. For example, **Initialised-the-tracker - Adam Jim - Sunday 8th June 2025 3:45 PM**
11. add(Stage), Commit, Push, create a PR and merge the changes to the README.md file into the `develop` branch.
12. Checkout `develop` branch, pull the latest changes.

## 5.2 Conflicts - Easy
1. Create 2 branches off the `develop` branch - named `analysis` and `review`
2. Checkout the `analysis` branch, and take out the corresponding stash. Now, in the readme.md, add an ordered list item to the Progress Tracker with text `AddedSelfReflection-<Timestamp>`.
3. Add, commit and raise a PR. **Do not merge this PR**
4. Checkout the `review` branch, and take out the corresponding stash. Now, in the readme.md, add an ordered list item to the Progress Tracker with text `AddedPeerReview-<Timestamp>`. 
5. Add, commit and raise a PR, and merge to `develop`.
6. On the Github UI, go to the PR raised for the `analysis` branch (whatever you did in step 3 above).
7. You should see some merge conflicts.
8. On your local, use rebase to resolve this.
9. Smartly resolve the conflicts, and merge this PR.
