---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# **Git**

A Powerful Version Control System

---

# **What is Git?**

- A distributed version control system
- Tracks changes in source code
- Enables collaboration among developers
- Created by Linus Torvalds in 2005

---

# **Why Use Git?**

- Keeps a history of changes
- Allows collaboration without conflicts
- Enables branching and merging
- Helps in reverting changes safely
- Used by companies and open-source projects worldwide

---

# **Installing Git**

- Windows: [git-scm.com](https://git-scm.com/)
- macOS: `brew install git`
- Linux: `sudo apt install git` or `sudo dnf install git`

Verify installation:
```sh
git --version
```

---

# **Basic Git Commands**

- `git init` → Initialize a repository
- `git clone <repo-url>` → Clone a repository
- `git status` → Check repository status
- `git add <file>` → Stage changes
- `git commit -m "message"` → Commit changes

---

# **Configuring Git**

Set your name and email:
```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
Check configuration:
```sh
git config --list
```

---

# **Working with Repositories**

- **Untracked** → New files not yet staged
- **Staged** → Files added with `git add`
- **Committed** → Changes stored in history

Workflow:
1. Modify files
2. `git add` to stage changes
3. `git commit` to save changes

---

# **Branching in Git**

- Create a new branch:
```sh
git branch feature-branch
```
- Switch to a branch:
```sh
git checkout feature-branch
```
- Create and switch:
```sh
git checkout -b feature-branch
```
- Merge branches:
```sh
git merge feature-branch
```

---

# **Remote Repositories**

- Link a remote repository:
```sh
git remote add origin <repo-url>
```
- Push changes:
```sh
git push origin main
```
- Pull updates:
```sh
git pull origin main
```

---

# **Handling Conflicts**

- Occurs when multiple people change the same part of a file
- Git will prompt for manual resolution
- Use:
```sh
git status
git diff
git merge --abort
```
- Edit the file, then:
```sh
git add <file>
git commit -m "Resolved conflict"
```

---

# **Undoing Changes**

- Reset staged changes:
```sh
git reset HEAD <file>
```
- Undo last commit (keep changes):
```sh
git reset --soft HEAD~1
```
- Undo last commit (discard changes):
```sh
git reset --hard HEAD~1
```

---

# **Git Best Practices**

- Write meaningful commit messages
- Use `.gitignore` to exclude unnecessary files
- Regularly pull updates from the remote
- Use branches for new features
- Keep commits small and focused

---

# **Resources**

- [Git Official Website](https://git-scm.com/)
- [GitHub Documentation](https://docs.github.com/en/get-started)
- [Learn Git Branching](https://learngitbranching.js.org/)

---

# **Thank You!**

Happy Coding with Git! 🚀
