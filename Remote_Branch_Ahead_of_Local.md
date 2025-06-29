# 🔧 Git Push Rejected – Non-Fast-Forward Fix

## ❗️ Problem
When running:
```bash
git push origin assignment8-task-2
```
You got this error:
```scss
! [rejected] assignment8-task-2 -> assignment8-task-2 (non-fast-forward)
error: failed to push some refs...
```

## 🔍 Why It Happened
- Your local branch (`assignment8-task-2`) is behind the remote branch.
- The remote has new commits that your local branch doesn’t have.
- Git blocks the push to avoid losing those remote changes.

## ✅ Recommended Fix: Use Rebase (Avoid Merge Commits)
You want to reapply your local commits on top of the updated remote branch.

## ✅ Correct Steps
(When your branch is `assignment8-task-2` and remote is `origin`)

### ✅ Step 1: Rebase your local branch onto the remote version
```bash
git pull --rebase origin assignment8-task-2
```
🔹 You're on `assignment8-task-2`, so you're pulling and rebasing from the same branch on the remote (`origin`).

### ❌ Wrong Approach
If you run:
```bash
git rebase develop assignment8-task-2
```
This means:
- Rebase `assignment8-task-2` onto `develop`
- Both branches are local
- It does not fetch anything from GitHub
❌ Not what you want here

### ✅ Correct Goal
Rebase your local `assignment8-task-2` on top of the remote `assignment8-task-2`.

### ✅ Step 2: Resolve conflicts (if any)
For each conflict:
```bash
# After fixing the file
git add <filename>

# Continue the rebase
git rebase --continue
```
🔁 If you want to cancel the rebase at any time:
```bash
git rebase --abort
```

### ✅ Step 3: Push your updated branch
```bash
git push origin assignment8-task-2
```
✅ Now the push will succeed — your branch is updated with the remote.

## 🧠 Summary Table
| Step | What You Do | Command |
|------|-------------|---------|
| 1 | Rebase local with remote | `git pull --rebase origin assignment8-task-2` |
| 2 | Fix conflicts & continue | `git add .` + `git rebase --continue` |
| 3 | Push to GitHub | `git push origin assignment8-task-2` |