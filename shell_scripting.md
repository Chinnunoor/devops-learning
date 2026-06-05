# SHELL-SCRIPTING-LEARNING

## What is Shell Scripting?

Shell scripting means writing a group of terminal commands inside one file and running them together.

Normally, we type commands one by one in the terminal.

Shell script helps us save those commands in a file and run them with one command.

Simple meaning:

Shell scripting = automation using terminal commands

Example:

Instead of running these commands every day:

```bash
pwd
ls
date
```

You can put them inside one script and run the script.

---

## Why Do We Need Shell Scripting?

Shell scripting saves time.

It is useful when you do the same task again and again.

Without shell script:

You type commands manually  
You may forget steps  
You may make mistakes  
It takes more time  

With shell script:

Commands run automatically  
Same steps run every time  
Less manual work  
Faster work  
Good for DevOps and server tasks  

Simple meaning:

Shell scripting helps you automate repeated work.

---

## Where is Shell Scripting Used?

Shell scripting is used in:

DevOps  
Linux servers  
Application deployment  
Backup jobs  
Log checking  
File cleanup  
Monitoring  
Automation  
CI/CD pipelines  
GitHub Actions  
Cron jobs  

Simple meaning:

Shell scripting is mostly used to automate work on Linux servers.

---

# Shell Scripting Learning Roadmap

Learn shell scripting in levels.

## Level 0: Before Learning Shell Scripting

Before shell scripting, know basic Linux commands.

Basic commands:

`pwd` = show current location  
`ls` = list files and folders  
`cd` = move into a folder  
`mkdir` = create a folder  
`rm` = remove file or folder  
`touch` = create file  
`cat` = show file content  
`cp` = copy file  
`mv` = move or rename file  
`grep` = search text  
`find` = search files  
`chmod` = change permissions  

Simple meaning:

Linux commands are the building blocks of shell scripts.

---

## Level 1: Shell Script Basics

Topics:

What is shell  
What is bash  
Create a script file  
Shebang  
Echo  
Comments  
Run a script  
Permissions  

---

## Level 2: Variables and User Input

Topics:

Variables  
Read user input  
Command output in variable  
Environment variables  

---

## Level 3: Conditions

Topics:

if  
else  
elif  
Comparison operators  
File checks  
String checks  
Number checks  

---

## Level 4: Loops

Topics:

for loop  
while loop  
Loop through files  
Loop through arrays  

---

## Level 5: Functions

Topics:

Create function  
Call function  
Pass arguments  
Return status  

---

## Level 6: Script Arguments

Topics:

`$1`  
`$2`  
`$@`  
`$#`  
`$?`  

---

## Level 7: Real Automation

Topics:

Backup script  
Log checker  
File cleanup  
GitHub repo clone script  
Server health check  
Cron job  

---

# What is Shell?

Shell is a program that takes your command and gives it to the operating system.

Example:

You type:

```bash
ls
```

Shell understands this command and asks the system to list files.

Simple meaning:

Shell = bridge between you and the operating system

---

# What is Bash?

Bash is one type of shell.

Most Linux systems use Bash.

Full form:

```text
Bourne Again Shell
```

Simple meaning:

Bash = common shell used to write shell scripts

Check your shell:

```bash
echo $SHELL
```

Example output:

```bash
/bin/bash
```

On Mac, you may see:

```bash
/bin/zsh
```

That is okay. You can still write Bash scripts.

---

# Creating Your First Shell Script

Create a file:

```bash
touch hello.sh
```

Open it:

```bash
nano hello.sh
```

Add this:

```bash
#!/bin/bash

echo "Hello, Shell Scripting!"
```

Save and exit.

Simple meaning:

We created a script that prints a message.

---

# What is Shebang?

The first line is:

```bash
#!/bin/bash
```

This is called shebang.

It tells the system:

Run this script using Bash.

Simple meaning:

Shebang = tells which shell should run the script

---

# echo

`echo` is used to print text.

Command:

```bash
echo "Hello"
```

Output:

```bash
Hello
```

Simple meaning:

echo = print message

Example in script:

```bash
#!/bin/bash

echo "Starting script..."
echo "Task completed"
```

---

# Comments

Comments are notes inside a script.

They do not run.

Example:

```bash
#!/bin/bash

# This line prints a welcome message
echo "Welcome"
```

Simple meaning:

Comment = explanation for humans

Use comments to explain your script.

---

# How to Run a Shell Script

First give execute permission:

```bash
chmod +x hello.sh
```

Then run:

```bash
./hello.sh
```

Simple meaning:

`chmod +x` = allow script to run  
`./hello.sh` = run this script from current folder  

---

# Why chmod +x is Needed?

Linux does not run every file automatically.

A script needs execute permission.

Command:

```bash
chmod +x script.sh
```

Simple meaning:

Give permission to run this file like a program.

---

# Variables

Variable stores a value.

Example:

```bash
name="Rasool"

echo "Hello $name"
```

Output:

```bash
Hello Rasool
```

Simple meaning:

Variable = container for value

Important:

Do not put spaces around `=`.

Correct:

```bash
name="Rasool"
```

Wrong:

```bash
name = "Rasool"
```

---

# Command Output in Variable

You can store command output in a variable.

Example:

```bash
today=$(date)

echo "Today is $today"
```

Simple meaning:

`$(command)` = run command and store result

Another example:

```bash
current_dir=$(pwd)

echo "You are in $current_dir"
```

---

# User Input

Use `read` to take input from user.

Example:

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Hello $name"
```

Simple meaning:

read = take input from user

---

# if Condition

`if` is used to make decisions.

Example:

```bash
#!/bin/bash

age=20

if [ "$age" -ge 18 ]; then
  echo "You are adult"
else
  echo "You are minor"
fi
```

Simple meaning:

if = check condition

---

# Number Comparisons

Use these for numbers:

```text
-eq = equal
-ne = not equal
-gt = greater than
-lt = less than
-ge = greater than or equal
-le = less than or equal
```

Example:

```bash
num=10

if [ "$num" -gt 5 ]; then
  echo "Number is greater than 5"
fi
```

---

# String Comparisons

Use these for text:

```text
=  equal
!= not equal
-z empty string
-n not empty string
```

Example:

```bash
name="Rasool"

if [ "$name" = "Rasool" ]; then
  echo "Name matched"
fi
```

Check empty:

```bash
name=""

if [ -z "$name" ]; then
  echo "Name is empty"
fi
```

---

# File Checks

Shell scripts can check files and folders.

Common checks:

```text
-f = file exists
-d = directory exists
-e = file or directory exists
-r = readable
-w = writable
-x = executable
```

Example:

```bash
file="app.log"

if [ -f "$file" ]; then
  echo "File exists"
else
  echo "File not found"
fi
```

Simple meaning:

File checks help scripts make safe decisions.

---

# for Loop

A loop repeats work.

Example:

```bash
for fruit in apple orange grapes
do
  echo "$fruit"
done
```

Output:

```bash
apple
orange
grapes
```

Simple meaning:

for loop = repeat for each item

---

# Loop Through Files

Example:

```bash
for file in *.txt
do
  echo "Found file: $file"
done
```

Simple meaning:

This checks every `.txt` file in the current folder.

---

# while Loop

`while` loop runs while a condition is true.

Example:

```bash
count=1

while [ "$count" -le 5 ]
do
  echo "Count is $count"
  count=$((count + 1))
done
```

Simple meaning:

while loop = repeat until condition becomes false

---

# Arrays

Array stores multiple values.

Example:

```bash
fruits=("apple" "orange" "grapes")

echo "${fruits[0]}"
```

Output:

```bash
apple
```

Simple meaning:

Array = list of values

Loop through array:

```bash
fruits=("apple" "orange" "grapes")

for fruit in "${fruits[@]}"
do
  echo "$fruit"
done
```

---

# Functions

Function is a reusable block of code.

Example:

```bash
greet() {
  echo "Hello Rasool"
}

greet
```

Simple meaning:

Function = reusable mini-script inside script

---

# Function with Argument

Example:

```bash
greet() {
  echo "Hello $1"
}

greet "Rasool"
```

Output:

```bash
Hello Rasool
```

Simple meaning:

`$1` means first value passed to the function.

---

# Script Arguments

You can pass values while running a script.

Example script:

```bash
#!/bin/bash

echo "First argument is $1"
echo "Second argument is $2"
```

Run:

```bash
./script.sh apple orange
```

Output:

```bash
First argument is apple
Second argument is orange
```

Simple meaning:

Arguments = values given to script while running

---

# Important Special Variables

```text
$1 = first argument
$2 = second argument
$@ = all arguments
$# = number of arguments
$? = previous command status
$$ = current script process ID
```

Example:

```bash
echo "Total arguments: $#"
echo "All arguments: $@"
```

---

# Exit Status

Every command gives a status.

```text
0 = success
non-zero = failure
```

Example:

```bash
ls

echo $?
```

Simple meaning:

`$?` tells whether previous command succeeded or failed.

---

# set -e

`set -e` stops the script if any command fails.

Example:

```bash
#!/bin/bash

set -e

mkdir test
cd test
echo "Success"
```

Simple meaning:

set -e = stop script on error

Useful in automation and GitHub Actions.

---

# set -x

`set -x` shows each command before running it.

Example:

```bash
#!/bin/bash

set -x

echo "Hello"
date
```

Simple meaning:

set -x = debug mode

Use this when you want to see what script is doing.

---

# Redirect Output

You can send output to a file.

Overwrite file:

```bash
echo "Hello" > output.txt
```

Append to file:

```bash
echo "World" >> output.txt
```

Simple meaning:

`>` = write fresh  
`>>` = add to existing file  

---

# Pipe

Pipe sends output of one command to another command.

Example:

```bash
cat app.log | grep "error"
```

Simple meaning:

Pipe = pass result to next command

Better:

```bash
grep "error" app.log
```

---

# grep

`grep` searches text.

Example:

```bash
grep "error" app.log
```

Simple meaning:

grep = find matching text

Ignore case:

```bash
grep -i "error" app.log
```

Show line number:

```bash
grep -n "error" app.log
```

---

# find

`find` searches files and folders.

Example:

```bash
find . -name "*.log"
```

Simple meaning:

Find all `.log` files from current folder.

Find by name:

```bash
find . -name "app.txt"
```

Find directories:

```bash
find . -type d
```

Find files:

```bash
find . -type f
```

---

# Real Script 1: Backup Script

Create:

```bash
nano backup.sh
```

Add:

```bash
#!/bin/bash

set -e

SOURCE_DIR="my-project"
BACKUP_DIR="backup"

mkdir -p "$BACKUP_DIR"

DATE=$(date +%Y-%m-%d-%H-%M-%S)

tar -czf "$BACKUP_DIR/project-backup-$DATE.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully"
```

Run:

```bash
chmod +x backup.sh
./backup.sh
```

Simple meaning:

This script compresses a folder and saves it as backup.

---

# Real Script 2: Log Error Checker

Create:

```bash
nano check-errors.sh
```

Add:

```bash
#!/bin/bash

LOG_FILE="app.log"

if [ ! -f "$LOG_FILE" ]; then
  echo "Log file not found"
  exit 1
fi

grep -i "error" "$LOG_FILE"
```

Simple meaning:

This script checks if a log file has errors.

---

# Real Script 3: File Cleanup Script

Create:

```bash
nano cleanup.sh
```

Add:

```bash
#!/bin/bash

TARGET_DIR="temp-files"

if [ -d "$TARGET_DIR" ]; then
  rm -rf "$TARGET_DIR"/*
  echo "Cleanup completed"
else
  echo "Directory not found"
fi
```

Simple meaning:

This script removes files inside a temporary folder.

Warning:

Be careful with `rm -rf`.

---

# Real Script 4: Server Health Check

Create:

```bash
nano health-check.sh
```

Add:

```bash
#!/bin/bash

echo "Disk usage:"
df -h

echo
echo "Memory usage:"
free -h

echo
echo "Running processes:"
ps aux | head
```

Simple meaning:

This script shows basic server health.

Note:

`free -h` works on Linux. On Mac, use:

```bash
vm_stat
```

---

# Real Script 5: GitHub Repo Backup Script

Example idea:

```bash
#!/bin/bash

REPOS=("repo-one" "repo-two" "repo-three")

for repo in "${REPOS[@]}"
do
  git clone "https://github.com/username/$repo.git"
done
```

Simple meaning:

This script clones multiple GitHub repositories automatically.

---

# Cron Job

Cron is used to run scripts automatically at a fixed time.

Open cron editor:

```bash
crontab -e
```

Example:

```bash
0 9 * * * /home/user/backup.sh
```

Simple meaning:

Run backup script every day at 9 AM.

Cron format:

```text
minute hour day month weekday
```

Example:

```text
0 9 * * *
```

Means:

Every day at 9:00 AM.

---

# Shell Script in GitHub Actions

GitHub Actions can run shell scripts.

Example:

```yaml
name: Run Shell Script

on:
  workflow_dispatch:

jobs:
  run-script:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repo
        uses: actions/checkout@v4

      - name: Run script
        run: |
          chmod +x scripts/myscript.sh
          ./scripts/myscript.sh
```

Simple meaning:

GitHub Actions can run your script automatically in the cloud.

---

# Common Beginner Mistakes

## Mistake 1: Spaces around equal sign

Wrong:

```bash
name = "Rasool"
```

Correct:

```bash
name="Rasool"
```

---

## Mistake 2: Forgetting chmod +x

If you see permission denied, run:

```bash
chmod +x script.sh
```

---

## Mistake 3: Wrong file path

Wrong path causes file not found.

Check current location:

```bash
pwd
ls
```

---

## Mistake 4: Not using quotes

Better:

```bash
rm "$file"
```

Risky:

```bash
rm $file
```

Simple meaning:

Quotes protect values with spaces.

---

## Mistake 5: Using rm -rf carelessly

This can delete important files.

Be careful.

Before deleting, print the target:

```bash
echo "$TARGET_DIR"
```

---

## Mistake 6: Forgetting fi or done

Every `if` must end with:

```bash
fi
```

Every loop must end with:

```bash
done
```

---

## Mistake 7: Not testing step by step

Do not write a big script and run directly.

Test small parts first.

---

# Best Shell Scripting Memory Trick

```text
echo = print
read = input
variable = store value
if = decision
for = repeat list
while = repeat condition
function = reusable code
$1 = first argument
$? = previous command result
chmod +x = make script runnable
./script.sh = run script
```

---

# Practice Roadmap

## Practice 1: First Script

```bash
mkdir shell-practice
cd shell-practice
touch hello.sh
nano hello.sh
```

Add:

```bash
#!/bin/bash

echo "Hello Shell"
```

Run:

```bash
chmod +x hello.sh
./hello.sh
```

Goal:

Understand how to create and run a script.

---

## Practice 2: Variables

```bash
#!/bin/bash

name="Rasool"
course="Shell Scripting"

echo "$name is learning $course"
```

Goal:

Understand variables.

---

## Practice 3: User Input

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Welcome $name"
```

Goal:

Understand `read`.

---

## Practice 4: if Condition

```bash
#!/bin/bash

echo "Enter a number:"
read num

if [ "$num" -gt 10 ]; then
  echo "Number is greater than 10"
else
  echo "Number is 10 or less"
fi
```

Goal:

Understand conditions.

---

## Practice 5: for Loop

```bash
#!/bin/bash

for item in apple orange grapes
do
  echo "$item"
done
```

Goal:

Understand loops.

---

## Practice 6: File Check

```bash
#!/bin/bash

file="notes.txt"

if [ -f "$file" ]; then
  echo "File exists"
else
  echo "File not found"
fi
```

Goal:

Understand file checks.

---

## Practice 7: Script Arguments

```bash
#!/bin/bash

echo "First argument: $1"
echo "Second argument: $2"
echo "Total arguments: $#"
```

Run:

```bash
./args.sh hello world
```

Goal:

Understand script arguments.

---

## Practice 8: Real Mini Project

Create a script that:

Creates a backup folder  
Copies all `.txt` files into backup folder  
Prints success message  

Example:

```bash
#!/bin/bash

mkdir -p backup

cp *.txt backup/

echo "All text files copied to backup folder"
```

Goal:

Understand simple automation.

---

# Final Shell Scripting Cheat Sheet

## Basic Script

```bash
#!/bin/bash

echo "Hello"
```

## Run Script

```bash
chmod +x script.sh
./script.sh
```

## Variables

```bash
name="Rasool"
echo "$name"
```

## User Input

```bash
read name
echo "$name"
```

## if Condition

```bash
if [ "$num" -gt 10 ]; then
  echo "Greater"
else
  echo "Smaller"
fi
```

## for Loop

```bash
for item in one two three
do
  echo "$item"
done
```

## while Loop

```bash
while [ "$count" -le 5 ]
do
  echo "$count"
  count=$((count + 1))
done
```

## Function

```bash
hello() {
  echo "Hello"
}

hello
```

## Arguments

```bash
echo "$1"
echo "$2"
echo "$@"
echo "$#"
```

## File Check

```bash
if [ -f "file.txt" ]; then
  echo "File exists"
fi
```

## Useful Commands in Scripts

```bash
pwd
ls
cd
mkdir
rm
cp
mv
cat
grep
find
date
tar
chmod
```

---

# Final Summary

Shell scripting is about automation.

The basic idea is:

```text
Write terminal commands → Save in a file → Run together → Automate work
```

Most important flow:

```bash
touch script.sh
nano script.sh
chmod +x script.sh
./script.sh
```

If you understand this flow clearly, shell scripting becomes much easier.

Simple final meaning:

Shell script is your shortcut for repeated terminal work.
