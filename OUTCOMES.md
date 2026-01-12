# Exercise Outcomes Submission

**Student/Group Name**: Alberto García Cruz -  Grupo 8
**Level Completed**: intermediate
**Date**: 12/01/2026

---

## 📋 Exercise Summary

### Exercise: Merging, Conflict Resolution, and Tagging
**Status**: ✅ Completed

**What I did**:
I created two branches working on the same file to simulate a merge conflict. Since Git's auto-merge feature cannot resolve this automatically, the conflict must be handled manually by choosing the specific parts to keep from each branch. Once resolved, the final version is pushed to the repository.

In the second part, we used tags to create snapshots—essentially naming and describing a specific commit to mark it as a stable version. We also created a lightweight tag by adding the -test suffix for testing purposes.

**Commands Used**:
```bash
   git checkout intermediate
   git checkout -b feature/header
   git checkout intermediate
   git checkout -b feature/footer
   git checkout feature/header
   git add page.html
   git commit -m "Add header to page"
   git checkout feature/footer
   git add page.html
   git commit -m "Add footer to page"
   git checkout intermediate
   git merge feature/header
   git merge feature/footer
   git add page.html
   git commit -m "Merge footer with resolved conflicts
   git tag -a v1.0 -m "First stable version with merged features"
   git tag
   git show v1.0
   git push origin v1.0
   git tag v1.0-test
   git show v1.0
   git show v1.0-test

```

**Results/Output**:
```
$   git add page.html
   git commit -m "Add header to page"
[feature/header 587a730] Add header to page
 1 file changed, 26 insertions(+)
 create mode 100644 page.html
 $    git add page.html
   git commit -m "Add footer to page"
[feature/footer 58fd72d] Add footer to page
 1 file changed, 36 insertions(+)
 create mode 100644 page.html

 $ git merge feature/footer
Auto-merging page.html
CONFLICT (add/add): Merge conflict in page.html
Automatic merge failed; fix conflicts and then commit the result.

$ git commit -m "Merge footer with resolved conflicts"
[intermediate f2a6263] Merge footer with resolved conflicts

$ git show v1.0
tag v1.0
Tagger: Alberto García <albertogc2211@correo.ugr.es>
Date:   Mon Jan 12 19:19:50 2026 +0100

First stable version with merged features

commit f2a62637ffe21d3d9d558ce345d1f531a7c3fd81 (HEAD -> intermediate, tag: v1.0)
Merge: 587a730 58fd72d
Author: Alberto García <albertogc2211@correo.ugr.es>
Date:   Mon Jan 12 19:19:39 2026 +0100

    Merge footer with resolved conflicts

$ git show v1.0
   git show v1.0-test
tag v1.0
Tagger: Alberto García <albertogc2211@correo.ugr.es>
Date:   Mon Jan 12 19:19:50 2026 +0100

First stable version with merged features

commit f2a62637ffe21d3d9d558ce345d1f531a7c3fd81 (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: 587a730 58fd72d
Author: Alberto García <albertogc2211@correo.ugr.es>
Date:   Mon Jan 12 19:19:39 2026 +0100

    Merge footer with resolved conflicts

commit f2a62637ffe21d3d9d558ce345d1f531a7c3fd81 (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: 587a730 58fd72d
Author: Alberto García <albertogc2211@correo.ugr.es>
Date:   Mon Jan 12 19:19:39 2026 +0100

    Merge footer with resolved conflicts

```

## 🎯 Key Learnings

**Main concepts I learned**:
1. The Mechanics of Merge Conflicts: I learned that Git stops the merge process when it cannot automatically decide between two different changes to the same line/file, requiring human intervention.

2. Annotated vs. Lightweight Tags: I discovered that annotated tags are full objects in the Git database (including a message and author info), while lightweight tags are just pointers to a specific commit.

3. The Importance of the "Staging" Step after Resolution: After fixing a conflict, the file must be git add-ed to signal to Git that the conflict is resolved before the final merge commit can be made.

**Skills I improved**:

- Manual Conflict Resolution: Reading and editing conflict markers (<<<<<<<, =======, >>>>>>>) directly in the source code.
- Tag Management: Creating, listing, and pushing specific tags to a remote repository.
- History Visualization: Using git log --graph to understand how branches diverge and eventually converge through merges.

---

## 🚧 Challenges Faced

### Challenge 1: Manual Resolution Confusion
**Problem**: At first, it wasn't clear if I should delete the markers (<<<<<<<, etc.) or if Git would do it for me. I also wasn't sure if I should keep the content from both branches or just one.

**Solution**: I realized that I had to manually delete the marker lines and keep the content from both the header and footer to achieve the "full page" goal.

**Commands/Approach**:
```bash

git add page.html
git commit -m "Merge footer with resolved conflicts"

```

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [5] |Easy peasy |
| Branching & merging | [3] |It was my first time merging, but it was easy, at least from Visual Studio Code|
| Remote operations | [5] |No problem with it |
| Conflict resolution | [3] |At first it was hard, but at the end it was rewarding|
| History rewriting | [N/A] |N/A|
| Git hooks | [N/A] |N/A|
| Security practices | [N/A] |N/A|

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/Halberch/taller-master-ugr/tree/group-8-outcomes/intermediate`
- Key commits demonstrating your work:
f2a62637ffe21d3d9d558ce345d1f531a7c3fd81


## ✅ Completion Checklist

Before submitting, ensure you have:
- [X] Completed the exercise for your chosen level (including all parts)
- [X] Documented all commands used with their outputs
- [X] Described challenges and how you resolved them
- [X] Provided a thoughtful reflection on your learning
- [X] Self-assessed your confidence in each topic
- [X] Pushed your outcome branch to the remote repository
- [N/A] Created a Pull Request (if required by your instructor)


**Submission Date**: [12/01/2026]  
**Ready for Review**: ✅ Yes
