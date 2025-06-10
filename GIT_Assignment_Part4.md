# Part 4
> Ensure you have completed all the previous 3 parts successfully before starting with this assignment. Also, Change the default branch of your repository to `default` instead of `main`.

## 4.1 Easy
1. Checkout the `develop` branch in your local and pull the latest changes. 
2. Create a folder `interview` at the root level in your project. Under that, Create a file `strengths.md`. 
3. Create two level 2 headings - `Technical` and `Non-Technical`. Do not add anything else to the file.
4. Create a branch off `develop`, give it a meaningful name, add, commit, push and raise a PR. Merge your changes into `develop` only.
5. At this point, ensure that your `main` branch is behind your `develop` branch.
6. Checkout `develop` branch in your local and take the latest pull.
7. Create 2 branches with names `technical` and `non-technical` off from `develop`.
8. Checkout the `technical` branch. Update the `strengths.md` file with atleast 3 bullet points under the `Technical` heading. add, commit, push and raise a PR to the `develop` branch. **DO NOT Merge your PR at the moment**
9. In your local, checkout the `non-technical` branch.
10. Update the `strengths.md` file with atleast 3 bullet points under the `Non-Technical` heading. Add and commit the changes, **but do not push them at the moment**.
11. On the GITHUB UI, merge the PR raised in step 8.
12. Push the changes of the `non-technical` branch, and raise a PR to the `develop` branch. You should see some merge conflicts on the UI. Do not resolve them on the GITHUB UI.
13. On local, try to rebase your `non-technical` branch onto `develop`.
14. Resolve merge conflicts in the vscode. Use a reasonable choice on what to keep.
15. add, commit and push again.
16. Go to your raised PR of step 12. The conflicts should not show up anymore. **[You might notice something interesting on the UI. *Hint: This is because of the rebase you did*]**.
17. Merge your PR. 

