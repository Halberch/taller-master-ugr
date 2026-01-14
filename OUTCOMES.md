# Exercise Outcomes Submission

**Student/Group Name**: Alberto García Cruz - Grupo 8
**Level Completed**: master-of-the-universe  
**Date**: 14/01/2026

---

## 📋 Exercise Summary

### Exercise: Branch Protection Rules and Security Best Practices (GPG Signing & Sensitive Data Management)
**Status**: ✅ Completed

**What I did**:
In this expert-level exercise, I implemented advanced security protocols to protect the repository's integrity. I configured Branch Protection Rules on GitHub to prevent unverified commits and direct pushes to the main branch. I successfully established a Chain of Trust by generating a GPG key pair and configuring Git to sign every commit, ensuring non-repudiation. Additionally, I performed a Security Audit using deep-inspection Git commands to scan for sensitive data and large blobs, and I enabled GitHub’s native security features, including Dependabot and Secret Scanning.

**Commands Used**:
```bash
   git checkout main
   git pull origin main
   echo "test" > direct-push.txt
   git add direct-push.txt
   git commit -m "Attempting direct push"
   git push origin main  # This should fail if protections are active!

   $ gpg --full-generate-key
   gpg --list-secret-keys --keyid-format=LONG
   git config --global user.signingkey ****

   git log -p | grep -i "password\|api_key\|secret\|token" | head -20
   git rev-list --objects --all | \
     git cat-file --batch-check='%(objecttype) %(objectname) %(objectsize) %(rest)' | \
     sed -n 's/^blob //p' | \
     sort --numeric-sort --key=2 | \
     tail -n 10




```

**Results/Output**:
```
$    git push origin main  # This should fail if protections are active!
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: error: GH006: Protected branch update failed for refs/heads/main.
remote: 
remote: - Commits must have verified signatures.
remote:   Found 1 violation:
remote:
remote:   a7d9562a05048abd8cfc8cd7f32258f3d419d245
remote:
remote: - Changes must be made through a pull request.
To https://github.com/Halberch/taller-master-ugr.git
 ! [remote rejected] main -> main (protected branch hook declined)
error: failed to push some refs to 'https://github.com/Halberch/taller-master-ugr.git'

$    git commit -S -m "feat: Add workflow documentation"
[feature/protected-workflow 154828f] feat: Add workflow documentation
 1 file changed, 1 insertion(+)
 create mode 100644 workflow.txt

```

**Screenshots**:
- [img/BranchProtectionRule.png: Config on GitHub]
- [img/GPGKeyGitHub.png: GPG Key added on GitHub]
- [img/PassEnCommit.png: Pass asked when trying a commit]
- [img/VerifiedCommits.png: Commits verified on GitHub]
- [img/GitHubSecurityFeaturesActivated.png: Security features activated on GitHub]
- [img/PullRequestGitHub.png: PullRequest on GitHub]


---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Asymmetric Cryptography in Git: How GPG keys provide a digital signature that proves commit authorship.
2. Branch Governance: Implementing "Guardrails" through protection rules to enforce code quality and security.
3. Using commands to audit the internal object database for leaked secrets or oversized files.

**Skills I improved**:
- Configuring a local environment to support cryptographically signed workflows.
- Activating automated security scanners (Dependabot, CodeQL) within the GitHub ecosystem.
- Understanding the process of secret rotation and history rewriting with git-filter-repo.

---

## 🚧 Challenges Faced

### Challenge 1: GPG Agent & Git Integration
**Problem**: Even after generating the key, Git failed to sign commits with the error gpg: signing failed: No secret key.

**Solution**: I had to ensure the email address in the GPG key exactly matched the email in my git config user.email and properly link the Key ID in the global configuration.


### Challenge 2: Protected Branch Rejection
**Problem**: I tried to fix a small typo in CODEOWNERS directly on main, but GitHub blocked the push.

**Solution**: I realized that "Master of the Universe" level rules apply to everyone. I had to create a new feature branch, commit with my signature, and merge via a Pull Request.

---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how easy it is to steal an identity in Git. Without GPG signing, anyone can commit using another person's email. Seeing the "Verified" badge for the first time gave me a new perspective.

**What I found most difficult**:
The GPG setup was the most technical part. Dealing with the GPG agent, managing passphrases, and exporting the public key to GitHub requires precision, as a single mismatch in the ID or email breaks the entire chain.

**What I found most useful**:
The ability to audit the repository for large blobs and secrets. In real-world projects, repos often become bloated over time. Knowing how to find the "heaviest" objects in the history is a crucial skill for repository maintenance.

**How I would apply this in real projects**:
I will never start a professional project without enabling Branch Protection and Dependabot. I will also encourage my teams to sign their commits to ensure the integrity of our software.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [5] |Fully mastered. |
| Branching & merging | [5] | Comfortable with complex flows.|
| Remote operations | [5] |Understand hooks and rejections.|
| Conflict resolution | [4] |Can handle most manual merges |
| History rewriting | [4] | Understand the risks of --force.|
| Git hooks | [5] | Confident in GPG and Protections.|
| Security practices | [4] |Aware of rotation and scanning. |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/Halberch/taller-master-ugr/tree/group-8-outcomes/master-of-the-universe`
- Key commits demonstrating your work:
  - 154828f: Verified commit adding security documentation.
  - b53e1da: Updated CODEOWNERS via Pull Request.

---

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

## 📝 Additional Comments

[Any additional thoughts, questions, or feedback about the exercises]

---

**Submission Date**: [14/01/2026]  
**Ready for Review**: ✅ Yes
