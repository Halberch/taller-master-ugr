# Exercise Outcomes Submission

**Student/Group Name**: Alberto García Cruz / Grupo 8
**Level Completed**: master
**Date**: 14/01/2026

---

## 📋 Exercise Summary

### Exercise: Rewriting History (Rebase and Amend Commits)
**Status**: ✅ Completed

**What I did**:
This exercise is focused on rewriting history using amend and interactive rebase. So I learned how to modify the last commit without creating a new one by using git commit --amend and verified the changes by comparing commit SHAs before and after the amend. I also practiced cleaning up commit history with git rebase -i, applying operations such as pick and fixup. Additionally, I created a feature branch, made changes, and successfully rebased it onto the updated master branch to maintain a linear history. Finally, I learned why rewriting public or shared history is dangerous, and understood the difference between git push --force and git push --force-with-lease.

**Commands Used**:
```bash

   echo "version=1.0" > config.txt
   git add config.txt
   git commit -m "Add configuration file"
   echo "environment=production" >> config.txt
   git add config.txt
   git commit --amend -m "Add complete configuration file"
   git log --oneline -n 3
   echo "Feature A" > featureA.txt
   git add featureA.txt
   git commit -m "Add feature A"
   
   echo "Feature B" > featureB.txt
   git add featureB.txt
   git commit -m "Add feature B"
   
   echo "Fix typo in A" >> featureA.txt
   git add featureA.txt
   git commit -m "Fix typo"
   git rebase -i HEAD~3
   i
   Changed pick for fixup
   Press "ESC"
   :wq to save in VIM
   git log --oneline -n 5

   git checkout -b feature/awesome-feature
   echo "Awesome Feature" > awesome.txt
   git add awesome.txt
   git commit -m "Add awesome feature"

   git checkout master
   echo "Master update" > master-update.txt
   git add master-update.txt
   git commit -m "Update on master branch"

   git checkout feature/awesome-feature
   git rebase master
   git log --graph --oneline --all -n 10

```

**Results/Output**:
```
$ git log --graph --all --oneline
* 13ef3f8 (feature/awesome-feature) Add awesome feature
* 08cf187 (HEAD -> group-8-outcomes/master, master) Update on master branch
* b96d128 Add feature B
* 097c223 Add feature A
* 8bbee2f Add complete configuration file
```


## 🎯 Key Learnings

**Main concepts I learned**:
1. I learned that "amending" or "rebasing" doesn't actually change a commit; it creates a new one with a different SHA, effectively replacing the old one in the timeline.
2. I understood how rebase avoids the "diamond shape" in git graphs, making the history easier to read.
3. I learned how to merge minor corrections into main feature commits using interactive rebase to keep the log professional.

**Skills I improved**:
- Ability to use rebase -i to reorganize, squash, and reword commits.
- Efficiently switching between master and feature branches while maintaining a clean workflow.
- Understanding the difference between --force and --force-with-lease to prevent overwriting colleagues' work.
- Using VIM to rebase properly

---

## 🚧 Challenges Faced

### Challenge 1: The Interactive Rebase Editor (Vim)
**Problem**: When running git rebase -i, the terminal opened the Vim editor and it was my first time using it.

**Solution**: I learned to use i to enter insert mode, Esc to exit it, and :wq to save and quit.

**Commands/Approach**:
```bash
   Pressed i to enter insert mode
   Changed pick for fixup
   Press "ESC"
   :wq to save in VIM
```

---

### Challenge 2: SHA changes
**Problem**: At first, it was confusing why the commit hashes changed even if the code was almost the same

**Solution**: I verified that because the parent commit or the timestamp changed during the rebase/amend process, Git generates a brand new SHA-1 hash.

---

## 💭 Personal Reflection

**What surprised me**:
The most surprising discovery was the concept of commit immutability. Before this exercise, I thought git commit --amend or rebase simply "edited" an existing commit.

**What I found most difficult**:
The most challenging part was mastering the Interactive Rebase workflow, specifically when dealing with the editor. Understanding that the commits are listed in chronological order (oldest at the top) which is the opposite of git log

**What I found most useful**:
Being able to clean my local git log before pushing to remote.

**How I would apply this in real projects**:
I would clean my git log in order to create an easy to read log for my colleagues

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [5] |Very comfortable. |
| Branching & merging | [5] |Understand the flow well. |
| Remote operations | [4] |Comfortable with push/pull. |
| Conflict resolution | [4] |Can handle most manual merges. |
| History rewriting | [4] |rebase -i and amend understood. |
| Git hooks | [N/A] | |
| Security practices | [4] |Understand force-with-lease. |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/Halberch/taller-master-ugr/tree/group-8-outcomes/master`
- Key commits demonstrating your work:
* 13ef3f8 (feature/awesome-feature) Add awesome feature
* 08cf187 (HEAD -> group-8-outcomes/master, master) Update on master branch


## ✅ Completion Checklist

Before submitting, ensure you have:
- [X] Completed the exercise for your chosen level (including all parts)
- [X] Documented all commands used with their outputs
- [X] Described challenges and how you resolved them
- [X] Provided a thoughtful reflection on your learning
- [X] Self-assessed your confidence in each topic
- [X] Pushed your outcome branch to the remote repository
- [X] Created a Pull Request (if required by your instructor)

---


**Submission Date**: [14/01/2026]  
**Ready for Review**: ✅ Yes
