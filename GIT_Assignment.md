## GIT Assignment Steps
> Ensure you are doing the assignment parts sequentially.

### Assignment Part 1 - Basic Setups
1. Go through the `GIT_Instructions.md` file shared on the group carefully.
2. Create a github account using your iet davv email id, if not already. Make sure to keep the username in the format "yourname-iet", for ex-"harshaltiwari-iet", "tanishqsoni-iet" . 
3. Create and add ssh keys using this account and add it to your vscode - [Generate and add SSH Keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
4. Setup Github on VSCode: [Setup Steps](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git)
5. Install GitLens extension in VSCode.


### Assignment Part 2 - Repository Creation and Git Basics
1. From the GITHub UI, Create a repository by the name `<YourFirstName>Profile`, for e.g. `RaseshProfile`. Make the repository private, and add a `.gitignore` file to it while doing this setup. DO NOT add README.md file while creating the repository.
2. Clone the Repository into your local system.
3. Create a branch named `develop` off the `main` branch.
4. Create a `README.md` file (follow the exact name).
5. Add the current timestamp to this `README.md` file at the top in the format - `Friday 6th June 2025 - 7:18PM`.
6. Add/Stage the file.
7. Commit the file and provide a meaningful message.
8. Push the file to remote.
9. Go to the GITHUB UI and create a Pull Request so as to merge this `develop` branch into `main` and add a description to the pull request in the UI - "In this PR, I am adding my intro to the repository via the Readme file".
10. Merge the `develop` branch into the `main` branch. Ensure both `develop` and `main` branches are exactly the same after this merge.

### Assignment Part 3 - Git Intermediate
#### PART 3.1
1. Checkout the `develop` branch in your local.
2. Below the timestamp, Create a level 2 heading in the existing `README.md` file with the text "Who am I". Write atleast 100 words about yourself in a paragraph. 
3. Create a custom branch with the name `intro-<YourBirthDate>-<YourFirstName>`. The `YourBirthDate` should be in the format DDMMYY (without any separators). For example, intro-180916-vinod.
4. Add, commit and push this custom branch to the repository.
5. Create a PR from `intro-<YourBirthDate>` to the `develop` branch.
6. Merge the custom branch into develop.
7. Delete your custom branch.

#### PART 3.2
1. Create a PR from develop to `main` from the GITHUB UI.
2. Merge the changes into the `main` branch.
3. Ensure both `develop` and `main` branches are exactly the same after this merge. Also, ensure that these 2 are the only branches in your repository.



> At the end, add your github username and github repository URL in the [web dev task tracker sheet](https://docs.google.com/spreadsheets/d/1dMv0wIbXa-F0j_KIqNLPR2Ojz66wR9ZBp352dMpFvJk/edit?usp=sharing) under the columns `GIT Username` and `GIT Repo URL` respectively.