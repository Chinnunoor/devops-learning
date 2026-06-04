



# GIT-LEARNING

## What is Git?

Git is like a **time machine for code**.

When we write code, we make many changes. Sometimes the code works, sometimes it breaks. Git helps us save every important version of our project.

With Git, we can:

Track changes  
Go back to old versions  
Work safely with a team  
Keep project history  
Push code to GitHub  

Simple meaning:

Git helps developers track, save, and manage code changes.

---

## Why Do We Need Git?

Before Git, developers faced many problems.

The Past:

Lost changes  
Many file copies like `final`, `final2`, `final_updated`  
Team conflicts  
No proper backup  
No project history  

The Present with Git:

Track every change  
Restore any version  
Work with teams easily  
Keep backup on GitHub  
See full project history  

Simple meaning:

Git protects your code and helps you work professionally.

---

## Installing Git

Before using Git, install it on your computer.

Download Git from:

https://git-scm.com/downloads

After installation, open terminal and check:

```bash
git --version
```

Example output:

```bash
git version 2.49.0
```

---

## Initial Git Setup

After installing Git, set your name and email.

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

This name and email will be attached to every commit you create.

---

## Recommended Reading

The free official Git book is:

https://git-scm.com/book/en/v2

You do not need to read everything at once. Use it as a reference while practicing.

---

# Git Learning Roadmap

Learn Git in 3 levels.
## Level 0: Before Learning Git

Before learning Git, be comfortable with basic Linux/terminal commands.

These commands help you move around folders, create files, delete files, and manage your project from the terminal.

Basic commands to know:

`pwd` = show current location  
`ls` = list files and folders  
`cd` = move into a folder  
`mkdir` = create a new folder  
`rmdir` = remove an empty folder  
`rm` = remove a file  
`touch` = create a new file  
`clear` = clear the terminal screen  

Simple meaning:

Linux commands help you control your project folder from the terminal.

Why this is needed:

Git is mostly used from the terminal, so knowing these basic commands makes Git much easier to learn.

Example:

```bash
pwd
ls
mkdir git-practice
cd git-practice
touch
```


## Level 1: Beginner Git

git init  
git status  
git add  
git commit  
git log  
git push  

## Level 2: Daily Git Commands

branch  
merge  
pull  
push  
clone  
stash  
restore  

## Level 3: Professional Git

rebase  
cherry-pick  
reset  
pull request  
merge conflict  
force push  
company Git workflow  

---

# The Four Zones of Git

To understand Git clearly, first understand where your code moves.

```text
Working Directory → Staging Area → Local Repository → Remote Repository
```

Master these four zones, and Git becomes much easier.

---

## 1. Working Directory

This is where you write and change code.

Example:

You create or edit a file:

```bash
app.py
```

At this point, Git can see the file, but it is not saved in Git history yet.

Simple meaning:

Working Directory = your current workspace

---

## 2. Staging Area

The staging area is where you prepare changes before saving them.

Command:

```bash
git add app.py
```

Simple meaning:

Staging Area = ready area before commit

Memory:

git add = prepare

---

## 3. Local Repository

The local repository is where Git saves your changes permanently on your computer.

Command:

```bash
git commit -m "Added login feature"
```

Simple meaning:

Local Repository = saved Git history on your computer

Memory:

git commit = save

---

## 4. Remote Repository

The remote repository is where your code is stored online, like GitHub.

Command:

```bash
git push
```

Simple meaning:

Remote Repository = online backup and sharing place

Memory:

git push = send code to GitHub

---

# Creating Your First Git Repository

Before Git can track your project, you need to make your project a Git repository.

Command:

```bash
git init
```

Simple meaning:

Git, start tracking this project.

After running this command, Git creates a hidden folder called:

```bash
.git
```

This `.git` folder stores all Git information.

Important:

No `git init` means no Git tracking.

---

# git status

Command:

```bash
git status
```

Meaning:

Git, what is happening in my project right now?

It shows:

New files  
Modified files  
Deleted files  
Files ready to commit  
Files not tracked yet  

Example:

```bash
touch app.py
git status
```

Output:

```bash
Untracked files:
  app.py
```

Simple meaning:

Git can see `app.py`, but Git is not tracking it yet.

Memory:

When confused, run:

```bash
git status
```

---

# Untracked vs Tracked Files

## Untracked File

An untracked file is a file Git can see, but Git is not managing yet.

Example:

```bash
touch app.py
git status
```

Git shows:

```bash
Untracked files:
  app.py
```

Simple meaning:

Git sees the file, but it is not tracking it yet.

---

## Tracked File

A tracked file is a file Git is managing.

To track a file, run:

```bash
git add app.py
```

Simple meaning:

A file becomes tracked when you add it using `git add`.

---

# git add

Command:

```bash
git add app.py
```

Meaning:

Git, prepare this file for the next commit.

Example:

```bash
touch app.py
git status
git add app.py
git status
```

After `git add`, Git shows:

```bash
Changes to be committed
```

Simple meaning:

The file is ready to save.

Memory:

git add = prepare

---

# git commit

Command:

```bash
git commit -m "Added app file"
```

Meaning:

Git, save this version of my project.

Example:

```bash
git add app.py
git commit -m "Added app file"
```

Simple meaning:

Commit is a saved version of your project.

Memory:

git commit = save

---

# git log

Command:

```bash
git log
```

Meaning:

Show my project history.

For a short and clean view:

```bash
git log --oneline
```

Git log shows:

Commit ID  
Author  
Date  
Commit message  

Simple meaning:

git commit saves the version.  
git log shows the saved versions.

---

# git push

Command:

```bash
git push
```

Meaning:

Send committed code from your computer to GitHub.

Simple meaning:

git commit saves code locally.  
git push sends saved code online.

Memory:

git push = upload code to GitHub

---

# Level 1 Summary

If you understand this flow, you know the foundation of Git.

```text
Write code → Check status → Add → Commit → Log → Push
```

Commands:

```bash
git init
git status
git add .
git commit -m "message"
git log --oneline
git push
```

Simple meaning:

Create Git project  
Check changes  
Prepare files  
Save version  
View history  
Send to GitHub  

---

# Level 2: Daily Git Commands

These are commands developers use in real projects.

---

## Branch

A branch is a safe place to work on new changes.

Simple meaning:

Branch = separate workspace

Example:

```bash
git branch feature-login
```

Or:

```bash
git switch -c feature-login
```

Use branch when you want to work without disturbing the main code.

---

## Merge

Merge means joining branch changes into another branch.

Simple meaning:

Merge = combine work

Example:

```bash
git switch main
git merge feature-login
```

Use merge when your branch work is completed.

---

## Pull

Pull means bringing the latest code from GitHub to your computer.

Simple meaning:

Pull = download latest code

Command:

```bash
git pull
```

Use pull before starting work, so your local code is updated.

---

## Push

Push means sending your committed code to GitHub.

Simple meaning:

Push = upload your saved code

Command:

```bash
git push
```

Use push after commit.

---

## Clone

Clone means copying a GitHub project to your computer.

Simple meaning:

Clone = download full project

Command:

```bash
git clone <repository-url>
```

Use clone when the project already exists on GitHub.

---

## Stash

Stash means temporarily saving unfinished work.

Simple meaning:

Stash = keep unfinished work safely for later

Commands:

```bash
git stash
git stash list
git stash pop
```

Use stash when your work is not ready to commit, but you need to switch tasks.

---

## Restore

Restore means undoing unwanted file changes.

Simple meaning:

Restore = remove unwanted changes

Command:

```bash
git restore app.py
```

To unstage a file:

```bash
git restore --staged app.py
```

Use restore when you changed something by mistake.

---

# Level 2 Summary

Daily developer flow:

```bash
git pull
git switch -c feature/my-task
git status
git add .
git commit -m "completed my task"
git push
```

Simple meaning:

Get latest code  
Create branch  
Work safely  
Save changes  
Send branch to GitHub  

---

# Level 3: Professional Git

These commands are used more in teams and company projects.

---

## Rebase

Rebase means updating your branch with the latest code in a clean way.

Simple meaning:

Rebase = clean update

Command:

```bash
git rebase main
```

Use rebase when you want a clean commit history.

---

## Cherry-pick

Cherry-pick means taking one specific commit from another branch.

Simple meaning:

Cherry-pick = pick one needed change

Command:

```bash
git cherry-pick <commit-id>
```

Use cherry-pick when you need only one commit, not the full branch.

---

## Rebase vs Merge

Both bring changes from one branch to another.

Merge keeps full history.  
Rebase makes history clean and straight.  

Simple meaning:

Merge = safe and easy  
Rebase = clean history  

For beginners, use merge first.

---

## Reset

Reset means going back to a previous Git state.

Simple meaning:

Reset = go back

Commands:

```bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```

Meanings:

```text
soft  = undo commit, keep changes staged
mixed = undo commit, keep changes unstaged
hard  = undo commit and delete changes
```

Warning:

Be careful with `git reset --hard` because it can delete your changes.

---

## Pull Request

A Pull Request is a request to add your branch code into the main branch.

Simple meaning:

Pull Request = please review and merge my code

In companies, developers usually do not push directly to main.

They follow this:

Create branch  
Make changes  
Push branch  
Open Pull Request  
Team reviews  
Merge into main  

---

## Merge Conflict

A merge conflict happens when Git cannot decide which change to keep.

Simple meaning:

Merge Conflict = two people changed the same part of the same file

How to fix:

Open the conflicted file  
Choose the correct code  
Remove conflict marks  
Save the file  
Add and commit again  

Commands:

```bash
git add .
git commit -m "fixed merge conflict"
```

---

## Force Push

Force push means replacing remote history with your local history.

Command:

```bash
git push --force
```

Simple meaning:

Force Push = overwrite GitHub history

Warning:

Use this carefully. In company projects, use it only when your team says it is okay.

Safer command:

```bash
git push --force-with-lease
```

---

# Real Company Git Workflow

Most companies follow this Git flow:

```text
Pull latest code
Create new branch
Make code changes
Add and commit changes
Push branch
Create Pull Request
Team reviews code
Merge into main
```

Commands:

```bash
git pull
git switch -c feature/my-task
git status
git add .
git commit -m "completed my task"
git push origin feature/my-task
```

Then create a Pull Request in GitHub, GitLab, or Bitbucket.

---

# Practice Roadmap

## Practice 1: First Git Project

```bash
mkdir git-practice
cd git-practice
git init
touch app.py
git status
git add app.py
git commit -m "created app file"
git log --oneline
```

Goal:

Understand init, status, add, commit, and log.

---

## Practice 2: Modify and Save Again

```bash
echo "print('Hello Git')" > app.py
git status
git add app.py
git commit -m "added hello message"
git log --oneline
```

Goal:

Understand how Git tracks file changes.

---

## Practice 3: Create a Branch

```bash
git switch -c feature-login
touch login.py
git add login.py
git commit -m "added login file"
```

Goal:

Understand branch as a safe workspace.

---

## Practice 4: Merge Branch

```bash
git switch main
git merge feature-login
```

Goal:

Understand how to bring branch changes into main.

---

## Practice 5: Use Stash

```bash
echo "temporary work" > temp.txt
git status
git stash
git status
git stash pop
```

Goal:

Understand temporary saving.

---

# Common Beginner Mistakes

## Mistake 1: Forgetting git status

Always check what is happening before running Git commands.

```bash
git status
```

---

## Mistake 2: Committing without adding

Wrong flow:

```bash
git commit -m "message"
```

Correct flow:

```bash
git add .
git commit -m "message"
```

---

## Mistake 3: Pulling while having unfinished work

Before pull, check:

```bash
git status
```

If you have unfinished work, either commit it or stash it.

---

## Mistake 4: Using reset --hard without understanding

`git reset --hard` can delete your work.

Use it carefully.

---

## Mistake 5: Force pushing in team projects

Do not use force push in company projects unless your team says it is okay.

---

# Final Git Cheat Sheet

## Most Important Commands

```bash
git init
git status
git add .
git commit -m "message"
git log --oneline
git push
git pull
git clone <url>
git branch
git switch -c branch-name
git merge branch-name
git stash
git stash pop
git restore file-name
```

---

# Best Memory Trick

```text
git status = check
git add = prepare
git commit = save
git log = history
git push = upload
git pull = download
git clone = copy project
git branch = safe workspace
git merge = combine work
git stash = temporary save
git restore = undo changes
```

---

# Final Summary

Git is not just about commands.

Git is about safely managing your project.

The basic idea is:

```text
Change code → Prepare code → Save code → Share code
```

In Git commands:

```bash
git status
git add .
git commit -m "message"
git push
```

If you understand this flow clearly, Git becomes much easier.




            
            

            

