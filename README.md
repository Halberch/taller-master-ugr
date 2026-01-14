# taller-master-ugr
A Git Training Repository for Master Students at UGR

This repository is designed to help master students develop professional Git skills through hands-on exercises organized by difficulty level.

## 📚 Training Structure

This repository contains exercises across **four difficulty levels**, each in its own branch. You must complete all exercises in each branch before progressing to the next level. After finishing a level, create an outcome branch to document and submit your work for evaluation.

### 🌱 Newbie Level
**Branch**: `newbie`  
**Exercise**: 1  
**Topics**:
- Basic Git commands (init, clone, add, commit, status, log)
- Creating and switching branches
- Basic remote operations (push, pull)

**You MUST start here**: We consider you new to Git or need a refresher on the basics.

```bash
git checkout newbie
```

### 🔧 Intermediate Level
**Branch**: `intermediate`  
**Exercise**: 1  
**Topics**:
- Merging branches and resolving conflicts
- Using tags for releases

**Continue here**: You're now comfortable with basic Git but need to deepen your understanding of collaboration workflows.

```bash
git checkout intermediate
```

### 🎯 Master Level
**Branch**: `master`  
**Exercise**: 1  
**Topics**:
- Rewriting history (rebase, amend commits, interactive rebase)

**Now is time for a level up. Continue here**: You want to master advanced Git techniques used in professional environments.

```bash
git checkout master
```

### 🌟 Master of the Universe Level
**Branch**: `master-of-the-universe`  
**Exercise**: 1  
**Topics**:
- Branch protection rules and secure workflows
- Security best practices (GPG signing, managing sensitive data)
- Verified commits and security auditing

**Now is time for a level up. Continue here**: You want to master advanced Git techniques used in professional environments.

```bash
git checkout master-of-the-universe
```

## 🚀 Getting Started

1. **Clone the repository**:
   ```bash
   git clone git@github.com:miguel-oltra/taller-master-ugr.git
   cd taller-master-ugr
   ```

2. **Choose your level**: Checkout the branch for your skill level
   ```bash
   git checkout <branch-name>
   ```

3. **Read the exercises**: Each branch has a README.md with detailed exercises

4. **Complete the exercises**: Follow the instructions and practice!

## 📖 Additional Resources

- **Git Documentation**: https://git-scm.com/doc
- **Interactive Git Tutorial**: https://learngitbranching.js.org/
- **GitHub Skills**: https://skills.github.com/
- **SSH Setup**: [Configure SSH credentials](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
- **GPG Setup**: [Managing commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification)

## 💡 Learning Path

We recommend following this progression:

```
Newbie → Intermediate → Master → Master of the Universe
```

However, feel free to jump to any level that matches your current knowledge.

## 🎓 Training Topics Covered

- **Git Key Features**: Local and remote operations, commits, working tree, staging area
- **Branching**: Creation, merging, strategies
- **History Management**: Viewing logs, rewriting history
- **Hooks**: Pre-commit, post-commit, pre-push automation
- **Security**: SSH keys, GPG keys, verified commits
- **Collaboration Workflows**: GitHub Flow, Git Flow, Forking workflow
- **Digital Trends**: GitOps, Infrastructure as Code, CI/CD, DevSecOps

## 📊 Exercise Overview

| Level | Exercise | Time Estimate | Key Skills |
|-------|----------|---------------|------------|
| Newbie | 1 | 1-2 hours | Foundation & basics |
| Intermediate | 1 | 2-3 hours | Collaboration & conflict resolution |
| Master | 1 | 3-4 hours | Advanced techniques & automation |
| Master of the Universe | 1 | 2-3 hours | Security & governance |

## 📤 Submitting Your Work

After completing your exercises, you must submit your work for evaluation by creating an outcome branch.

### Branch Naming Convention

Create a branch following this pattern:
```
group-[X]-outcomes/[level]
```

**Examples**:
- `group-A-outcomes/newbie`
- `group-B-outcomes/intermediate`
- `group-C-outcomes/master`
- `group-D-outcomes/master-of-the-universe`

### Submission Steps

1. **Complete all exercises** in your chosen level branch

2. **Create your outcome branch** from the exercise branch:
   ```bash
   # Example for Group A completing newbie level
   git checkout newbie
   git checkout -b group-A-outcomes/newbie
   ```

3. **Copy and complete the outcome template**:
   ```bash
   cp OUTCOME_TEMPLATE.md OUTCOMES.md
   # Edit OUTCOMES.md with your information
   ```

4. **Document your work** in `OUTCOMES.md`:
   - Summary of each exercise completed
   - Commands used with their outputs
   - Screenshots or logs demonstrating your work
   - Challenges faced and how you solved them
   - Personal reflection on what you learned

5. **Commit your outcome documentation**:
   ```bash
   git add OUTCOMES.md
   git commit -m "docs: Add outcomes for [level] level exercises"
   ```

6. **Push your outcome branch** to the remote:
   ```bash
   git push origin group-A-outcomes/newbie
   ```

7. **Create a Pull Request** (if required by your instructor):
   - Go to the repository on GitHub
   - Create a PR from your outcome branch to `main`
   - Add a clear title: "Outcomes: Group A - Newbie Level"
   - Add any additional comments or questions

### Required Documentation

Your `OUTCOMES.md` file must include:

✅ **Exercise Summaries**: Brief description of what you accomplished  
✅ **Commands & Outputs**: All key commands with their results  
✅ **Evidence**: Screenshots, logs, or commit hashes  
✅ **Challenges**: Problems faced and solutions found  
✅ **Reflection**: What you learned and how you'll apply it  
✅ **Self-Assessment**: Your confidence rating for each topic  

### Evaluation Criteria

Your work will be assessed based on:

1. **Completion of Exercises** (20%) - Did you finish all exercises?
2. **Understanding of Concepts** (25%) - Do you understand the "why" behind commands?
3. **Practical Application** (25%) - Did you use commands correctly and efficiently?
4. **Problem-Solving Skills** (20%) - How well did you handle challenges?
5. **Security Practices** (10%) - For Master of the Universe level only

See `EVALUATION_CRITERIA.md` for detailed rubric.

### Tips for Success

💡 **Be thorough**: Document everything, even small wins  
💡 **Be honest**: Share real challenges, not just successes  
💡 **Be reflective**: Show what you learned, not just what you did  
💡 **Be clear**: Use proper formatting and organization  
💡 **Be professional**: Treat this like a work portfolio  

### Need Help?

- Check the `OUTCOME_TEMPLATE.md` for guidance
- Review `EVALUATION_CRITERIA.md` to understand expectations
- Ask your instructor if you have questions
- Collaborate with your group members

---
## 🤖 Using GenAI Tools to Accelerate Your Learning

### Recommended Approach

#### ✅ Good Uses of AI

- **Explaining concepts**: Ask AI to explain what a command does and why
- **Debugging errors**: Share error messages to understand what went wrong
- **Exploring alternatives**: "What's the difference between rebase and merge?"
- **Reviewing your work**: Ask AI to review your git log and suggest improvements
- **Learning best practices**: "What's a good commit message format?"
- **Understanding documentation**: Have AI explain complex Git documentation

#### ❌ Avoid These Pitfalls

- Copying commands without understanding them
- Having AI complete entire exercises without your participation
- Submitting AI-generated reflections as your own thoughts
- Using AI to skip the learning process entirely

---

## 🤝 Contributing

This is a training repository. Students should:
- Create feature branches for their work
- Practice proper commit messages
- Use Pull Requests for collaboration exercises
- Submit outcomes using the standardized process above

## 📝 License

This repository is for educational purposes as part of the UGR Master's program.

## 👨‍🏫 Instructor

Created for Git Technology training at Universidad de Granada (UGR).

---

**Ready to begin?** Choose your level and checkout the corresponding branch to start learning! 🚀

