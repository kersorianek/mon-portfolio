---
layout: post
title: Git Commands I Actually Use
subtitle: A quick cheat sheet from daily work
thumbnail-img: /assets/img/git.png
tags: [Git]

comments: true
---

## Git Vocabulary You Should Know

- **Staged**: Added with `git add`, ready to commit  
- **Committed**: Saved snapshot with `git commit`  
- **Snapshot**: A commit (basically a saved state)  
- **Untracked Files**: Not yet staged or added  
- **Track a File**: Add to Git so it shows in `git status`  
- **Index**: Where staged files live before committing  
- **Detached HEAD**: When you check out a past commit and aren’t on a branch anymore  

---

## Commands I Actually Use (A Lot)

### 1. Add + Commit Quickly (For Tracked Files)
```bash
git commit -a -m "message"
```
Shortcut to `git add` + `git commit`, but **only works on already tracked files**, not new ones.

---

### 2. Check File Status
```bash
git status         # full details  
git status -s      # short format
```
- `??` → new file  
- `A`  → added to stage  
- `MM` → modified twice: staged, then changed again  
- `AM` → added, then modified before committing  

---

### 3. Who Changed What
```bash
git blame filename
```
Shows line-by-line changes and who made them. Super handy when hunting down bugs or typos.

---

### 4. See What’s Changed
- Before staging:
```bash
git diff
```
- After staging:
```bash
git diff --cached
```

---

### 5. Oops—Wrong Branch (Not Staged Yet)

#### A. Just reset the changes:
```bash
git checkout current_branch filename
```

#### B. Want to keep changes, but move to new branch:
```bash
git stash
git checkout -b new_branch
git stash apply
```

---

### 6. Unstage But Keep Your Changes
```bash
git restore --staged filename
```
Use `git diff --cached` first to see what’s been staged.

---

### 7. Ignore Files Forever
Add a `.gitignore` file to your directory. Example:
```
client_data.json
!important_file.txt  # use ! to *not* ignore this one
```

---

### 8. Fix Typos or Edit After Commit
```bash
git reset --soft HEAD^
# make edits
git commit -a -m "fixed stuff"
```

---

### 9. Merge Conflicts

- No time to fix → **reset everything**:
```bash
git reset --hard
```

- Already committed something bad:
```bash
git reset --hard ORIG_HEAD
```

---

### 10. Clean Up Merged Branches
```bash
git branch -d branch_name
```

---

### 11. Rebasing with Team Changes
```bash
git rebase
# fix conflicts if any
git rebase --continue
```
Use this when your feature branch is behind `master/main`, and you want a clean history.

---
