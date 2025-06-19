## 4.2 Easy
1. Checkout the `develop` branch in your local and pull the latest changes. 
2. You should have a folder `interview` at the root level in your project. Under that, Create a file `companies.md`. 
3. Create two level 2 headings - `Technical` and `Non-Technical`. Do not add anything else to the file.
4. Create a branch off `develop`, give it a meaningful name, add, commit, push and raise a PR. Merge your changes into `develop` only.
5. At this point, ensure that your `main` branch is behind your `develop` branch.
6. Checkout `develop` branch in your local and take the latest pull.
7. Create 2 branches with names `technical-companies` and `non-technical-companies` off from `develop`.
8. Checkout the `technical-companies` branch. **_Remove the `Non-Technical` Heading_ from the companies.md file**. Update the `companies.md` file with atleast 3 bullet points **mentioning tech company names you'd love to be part of** under the `Technical` heading. add, commit, push and raise a PR to the `develop` branch. **DO NOT Merge your PR at the moment**
9. In your local, checkout the `non-technical-companies` branch. **_Remove the `Technical` Heading_ from the companies.md file**.
10. Update the `strengths.md` file with atleast 3 bullet points **mentioning non-tech company names you'd love to be part of** under the `Non-Technical` heading. Add and commit the changes, **but do not push them at the moment**.
11. On the GITHUB UI, merge the PR raised in step 8.
12. Push the changes of the `non-technical-companies` branch, and raise a PR to the `develop` branch. You should see some merge conflicts on the UI. Do not resolve them on the GITHUB UI.
13. On local, try to rebase your `non-technical-companies` branch onto `develop`.
14. Resolve merge conflicts in the vscode. Use a reasonable choice on what to keep.
15. add, commit and push again.
16. Go to your raised PR of step 12. The conflicts should not show up anymore. **[You might notice something interesting on the UI. *Hint: This is because of the rebase you did*]**.
17. Merge your PR. 
