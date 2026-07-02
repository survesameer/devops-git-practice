Based on your Git practice history, here are concise interview-friendly notes for each **Git Branch** command.

| Command                                        | Syntax                          | Description (1–2 lines)                                                                                                   |
| ---------------------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **List all local branches**                    | `git branch`                    | Displays all local branches in the repository. The current branch is marked with `*`.                                     |
| **Create a new branch**                        | `git branch <branch-name>`      | Creates a new branch but does **not** switch to it. Used when you want to prepare a branch for future work.               |
| **Create and switch to a new branch**          | `git checkout -b <branch-name>` | Creates a new branch and immediately switches to it. This is the most commonly used command while starting a new feature. |
| **Switch to an existing branch (Old Method)**  | `git checkout <branch-name>`    | Moves your working directory to the specified branch. Your files change to match that branch's latest commit.             |
| **Switch to an existing branch (Recommended)** | `git switch <branch-name>`      | A newer and simpler command introduced to switch branches. Recommended over `git checkout` for branch switching.          |
| **Delete a local branch**                      | `git branch -d <branch-name>`   | Deletes a local branch only if it has already been merged. Helps keep the repository clean.                               |
| **Force delete a local branch**                | `git branch -D <branch-name>`   | Deletes a branch even if it contains unmerged commits. Use carefully, as unmerged work may be lost.                       |

---

# Commands from Your Practice

### 1. Check Existing Branches

```bash
git branch
```

**Purpose:** Shows all local branches and identifies the currently active branch.

**Example Output**

```text
* main
  feature-1
  feature-2
```

---

### 2. Create and Switch to a New Branch

```bash
git checkout -b feature-1
```

**Purpose:**

* Creates a new branch named `feature-1`
* Switches to it immediately

**Equivalent Commands**

```bash
git branch feature-1
git checkout feature-1
```

---

### 3. Create Branch Only

```bash
git branch main
```

**Purpose:**
Creates a branch if it doesn't already exist.

**Note:** In your repository, `main` already exists, so Git would return:

```text
fatal: a branch named 'main' already exists
```

---

### 4. Switch to Main Branch

```bash
git checkout main
```

**Purpose:**
Switches from the current branch to the `main` branch.

---

### 5. Switch Back to Feature Branch

```bash
git checkout feature-1
```

**Purpose:**
Moves back to continue development on `feature-1`.

---

### 6. Create Another Branch

```bash
git checkout -b feature-2
```

**Purpose:**
Creates another feature branch from the current branch and switches to it.

---

### 7. Switch Using New Command

```bash
git switch main
```

**Purpose:**
Switches to the `main` branch using Git's newer command.

**Recommended for Git 2.23+**

---

### 8. Delete a Branch

```bash
git branch -d feature-2
```

**Purpose:**
Deletes the `feature-2` branch after it has been merged.

If not merged, Git shows:

```text
error: The branch 'feature-2' is not fully merged.
```

---

### 9. Incorrect Command

```bash
git granch
```

**Purpose:**
This is a typo.

Git returns:

```text
git: 'granch' is not a git command.
```

---

# Typical Branch Workflow Used in Industry

```bash
git branch                     # Check existing branches

git checkout -b feature-login  # Create new feature branch

# Make code changes

git add .
git commit -m "Added login module"

git switch main                # Move back to main

git merge feature-login        # Merge feature branch

git branch -d feature-login    # Delete merged branch
```

---

# Interview Questions

**Q1. Difference between `git branch` and `git checkout -b`?**

| git branch                       | git checkout -b                    |
| -------------------------------- | ---------------------------------- |
| Creates a branch only            | Creates and switches to the branch |
| Current branch remains unchanged | Current branch changes immediately |

---

**Q2. Difference between `git checkout` and `git switch`?**

| git checkout                                                          | git switch                                              |
| --------------------------------------------------------------------- | ------------------------------------------------------- |
| Older command with multiple purposes (switch branches, restore files) | Newer command dedicated only to switching branches      |
| More flexible but can be confusing                                    | Simpler and recommended for day-to-day branch switching |

---

**Q3. When should you create a new branch?**

Create a new branch whenever you start a new feature, bug fix, enhancement, or experiment. This keeps the `main` branch stable and allows multiple developers to work independently without affecting each other's code.

