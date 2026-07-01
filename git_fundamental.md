# Day 1 Notes: Git Fundamentals

### 1. What is the difference between git add and git commit?
* `git add` selects changes and moves them into a temporary waiting area.
* `git commit` permanently saves those selected changes into your project history with a descriptive message.

### 2. What does the staging area do? Why doesn't Git just commit directly?
* The staging area acts as a rough draft layer where you prepare and organize your next save point.
* Git does not commit directly so you can group related changes together and leave out unfinished work.

### 3. What information does git log show you?
* `git log` displays a chronological list of all saved checkpoints in the repository.
* It shows the unique commit ID, the author's name and email, the date, and the commit message.

### 4. What is the .git/ folder and what happens if you delete it?
* The `.git/` folder is a hidden directory that stores the entire version history and configuration of your project.
* If you delete it, your project instantly loses all past history, branches, and tracking, turning back into a regular folder.

### 5. What is the difference between a working directory, staging area, and repository?
* **Working Directory:** The actual folder on your computer where you currently view and edit your files.
* **Staging Area:** The invisible preview zone where you pick and organize files before saving them.
* **Repository:** The permanent database that safely stores all your completed commits and project history.

