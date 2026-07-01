GIT-CHEAT-SHEET(1)             Git Manual Suite             GIT-CHEAT-SHEET(1)

NAME
       git - the stupid content tracker

SYNOPSIS
       git [--version] [--help] [-C <path>] <command> [<args>]

DESCRIPTION
       Git is a fast, scalable, distributed revision control system with an
       unusually rich command set that provides both high-level operations
       and full access to internals.

STARTING A PROJECT
       init
           Create an empty Git repository or reinitialize an existing one.
           $ git init

       clone
           Clone a repository into a new directory.
           $ git clone <url>

DAY-TO-DAY WORK
       add
           Add file contents to the staging area (index).
           $ git add <file>
           $ git add .

       status
           Show the working tree status, highlighting staged and unstaged changes.
           $ git status

       diff
           Show changes between commits, commit and working tree, etc.
           $ git diff

       commit
           Record changes to the repository.
           $ git commit -m "Your commit message"

       rm
           Remove files from the working tree and from the index.
           $ git rm <file>

EXAMINING HISTORY
       log
           Show commit logs, history, and authors.
           $ git log --oneline --graph

       show
           Show various types of objects (commits, tags, etc.).
           $ git show <commit-hash>

BRANCHING AND MERGING
       branch
           List, create, or delete branches.
           $ git branch
           $ git branch <branch-name>

       checkout / switch
           Switch branches or restore working tree files.
           $ git switch <branch-name>
           $ git checkout -b <new-branch-name>

       merge
           Join two or more development histories together.
           $ git merge <branch-name>

       rebase
           Reapply commits on top of another base tip.
           $ git rebase <branch-name>

SHARING AND UPDATING
       remote
           Manage set of tracked repositories.
           $ git remote add origin <url>

       fetch
           Download objects and refs from another repository.
           $ git fetch origin

       pull
           Fetch from and integrate with another repository or a local branch.
           $ git pull origin <branch-name>

       push
           Update remote refs along with associated objects.
           $ git push origin <branch-name>

SEE ALSO
       git-config(1), git-add(1), git-commit(1), git-log(1)

Git Reference                    2026-07-01                 GIT-CHEAT-SHEET(1)

