# LINUX-LEARNING

## What is Linux?

Linux is an **operating system**.

An operating system is the main software that helps you use a computer.

Examples of operating systems:

Windows  
macOS  
Linux  

Simple meaning:

Linux helps the computer run programs, manage files, manage users, and control hardware.

Linux is mostly used in:

Servers  
Cloud platforms  
DevOps  
Docker  
Kubernetes  
Cybersecurity  
Automation  
Production applications  

Simple meaning:

Linux is the main operating system used in real company servers.

---

## Why Do We Need Linux?

Most real-world applications run on Linux servers.

When you open a website or use an app, many times the backend is running on a Linux server.

As a developer, DevOps engineer, or cloud engineer, Linux helps you:

Use servers  
Run applications  
Check logs  
Manage files  
Install software  
Fix production issues  
Write automation scripts  
Work with Docker and Kubernetes  

Simple meaning:

Linux is important because servers use Linux, and DevOps work happens mostly on Linux.

---

## Linux vs Terminal

Linux is the operating system.

Terminal is the place where you type commands.

Simple meaning:

Linux = system  
Terminal = command window  

Example:

```bash
pwd
ls
cd Desktop
```

These commands are typed inside the terminal.

---

## Shell

Shell is the program that understands your commands.

When you type a command, the shell reads it and tells Linux what to do.

Common shells:

```text
bash
zsh
sh
```

Simple meaning:

Shell = command interpreter

Example:

```bash
echo "Hello Linux"
```

The shell understands this and prints the message.

---

## Linux Learning Roadmap

Learn Linux in levels.

```text
Level 0: Terminal Basics
Level 1: Basic Linux Commands
Level 2: File and Directory Management
Level 3: File Viewing
Level 4: Searching
Level 5: Permissions
Level 6: Users and Groups
Level 7: Processes
Level 8: Disk and System Info
Level 9: Package Management
Level 10: Networking Basics
Level 11: Logs and Services
Level 12: Shell Scripting Basics
Level 13: DevOps Linux Skills
```

Simple meaning:

First learn how to move around, then learn files, permissions, users, processes, networking, and scripting.

---

# Level 0: Terminal Basics

Before learning Linux deeply, be comfortable with the terminal.

Basic commands to know:

```text
pwd   = show current location
ls    = list files and folders
cd    = change directory
clear = clear terminal screen
whoami = show current user
```

Simple meaning:

Terminal commands help you control your computer using text.

---

## pwd

Command:

```bash
pwd
```

Meaning:

Show my current location.

Simple meaning:

pwd = where am I?

Example output:

```bash
/Users/noor/Desktop/linux-practice
```

Use this when you are confused about your current folder.

---

## ls

Command:

```bash
ls
```

Meaning:

List files and folders in the current location.

Simple meaning:

ls = what is inside this folder?

Example:

```bash
ls
```

Output:

```bash
Desktop Documents Downloads
```

Useful options:

```bash
ls -l
ls -a
ls -la
```

Meanings:

```text
ls -l  = show detailed list
ls -a  = show hidden files also
ls -la = show detailed list including hidden files
```

---

## cd

Command:

```bash
cd folder-name
```

Meaning:

Move into a folder.

Simple meaning:

cd = go to another folder

Example:

```bash
cd Desktop
```

Go back one folder:

```bash
cd ..
```

Go to home folder:

```bash
cd ~
```

Or simply:

```bash
cd
```

---

## clear

Command:

```bash
clear
```

Meaning:

Clear the terminal screen.

Simple meaning:

clear = clean the screen

It does not delete files. It only clears the view.

---

## whoami

Command:

```bash
whoami
```

Meaning:

Show the current logged-in user.

Simple meaning:

whoami = which user am I?

Example output:

```bash
noor
```

---

# Level 1: Basic Linux Commands

These are the first commands every beginner should know.

```text
pwd
ls
cd
mkdir
rmdir
rm
touch
echo
cat
clear
```

Simple meaning:

These commands help you create, move, view, and delete files and folders.

---

## mkdir

Command:

```bash
mkdir folder-name
```

Meaning:

Create a new folder.

Simple meaning:

mkdir = make directory

Example:

```bash
mkdir linux-practice
```

This creates a folder named `linux-practice`.

---

## rmdir

Command:

```bash
rmdir folder-name
```

Meaning:

Remove an empty folder.

Simple meaning:

rmdir = remove empty directory

Example:

```bash
rmdir old-folder
```

Important:

`rmdir` works only if the folder is empty.

---

## touch

Command:

```bash
touch file-name
```

Meaning:

Create a new empty file.

Simple meaning:

touch = create empty file

Example:

```bash
touch notes.txt
```

This creates a file named `notes.txt`.

---

## echo

Command:

```bash
echo "Hello Linux"
```

Meaning:

Print text on the terminal.

Simple meaning:

echo = display message

Example:

```bash
echo "Hello Linux"
```

Output:

```bash
Hello Linux
```

Write text into a file:

```bash
echo "This is my first file" > notes.txt
```

Append text to a file:

```bash
echo "Second line" >> notes.txt
```

Memory:

```text
>  = overwrite file
>> = add to end of file
```

---

## rm

Command:

```bash
rm file-name
```

Meaning:

Remove a file.

Simple meaning:

rm = delete file

Example:

```bash
rm notes.txt
```

Remove a folder with files inside:

```bash
rm -r folder-name
```

Warning:

Be careful with `rm`. Deleted files may not come back easily.

---

# Level 2: File and Directory Management

These commands help you manage files and folders.

```text
cp = copy
mv = move or rename
rm = remove
mkdir = create folder
touch = create file
```

---

## cp

Command:

```bash
cp source destination
```

Meaning:

Copy a file.

Simple meaning:

cp = duplicate file

Example:

```bash
cp notes.txt backup.txt
```

This copies `notes.txt` into `backup.txt`.

Copy folder:

```bash
cp -r folder1 folder2
```

`-r` means recursive. It copies everything inside the folder.

---

## mv

Command:

```bash
mv old-name new-name
```

Meaning:

Move or rename a file/folder.

Simple meaning:

mv = move or rename

Rename example:

```bash
mv old.txt new.txt
```

Move example:

```bash
mv notes.txt Documents/
```

---

## File Paths

A path tells where a file or folder is located.

There are two types:

```text
Absolute path
Relative path
```

---

## Absolute Path

Absolute path starts from the root location.

Example:

```bash
/Users/noor/Desktop/file.txt
```

Simple meaning:

Absolute path = full address

---

## Relative Path

Relative path starts from your current location.

Example:

```bash
Desktop/file.txt
```

Simple meaning:

Relative path = nearby address from current folder

---

## Important Symbols

```text
.  = current folder
.. = parent folder
~  = home folder
/  = root folder
```

Examples:

```bash
cd .
cd ..
cd ~
cd /
```

---

# Level 3: File Viewing

These commands help you read file content.

```text
cat
less
head
tail
```

---

## cat

Command:

```bash
cat file-name
```

Meaning:

Show the full file content.

Simple meaning:

cat = print file content

Example:

```bash
cat notes.txt
```

Use `cat` for small files.

---

## less

Command:

```bash
less file-name
```

Meaning:

View a file page by page.

Simple meaning:

less = read large file slowly

Example:

```bash
less app.log
```

Controls:

```text
Space = next page
b     = previous page
q     = quit
/word = search inside file
```

Use `less` for large files.

---

## head

Command:

```bash
head file-name
```

Meaning:

Show first 10 lines of a file.

Simple meaning:

head = top lines

Example:

```bash
head app.log
```

Show first 20 lines:

```bash
head -20 app.log
```

---

## tail

Command:

```bash
tail file-name
```

Meaning:

Show last 10 lines of a file.

Simple meaning:

tail = bottom lines

Example:

```bash
tail app.log
```

Watch live logs:

```bash
tail -f app.log
```

Simple meaning:

`tail -f` shows new lines as they are added.

Use this often for checking application logs.

---

# Level 4: Searching

Searching is very important in Linux.

Important commands:

```text
grep
find
which
whereis
```

---

## grep

Command:

```bash
grep "word" file-name
```

Meaning:

Search for text inside a file.

Simple meaning:

grep = search inside file

Example:

```bash
grep "ERROR" app.log
```

This shows lines containing `ERROR`.

Ignore case:

```bash
grep -i "error" app.log
```

Show line numbers:

```bash
grep -n "ERROR" app.log
```

Search inside all files:

```bash
grep -r "ERROR" .
```

Simple meaning:

```text
-i = ignore capital/small letters
-n = show line number
-r = search inside folders also
```

---

## find

Command:

```bash
find location -name "file-name"
```

Meaning:

Search for files and folders.

Simple meaning:

find = search file by name

Example:

```bash
find . -name "notes.txt"
```

Find all `.txt` files:

```bash
find . -name "*.txt"
```

Find folders:

```bash
find . -type d -name "logs"
```

Find files:

```bash
find . -type f -name "*.log"
```

---

## which

Command:

```bash
which command-name
```

Meaning:

Show where a command is installed.

Simple meaning:

which = command location

Example:

```bash
which java
```

Example output:

```bash
/usr/bin/java
```

---

# Level 5: Permissions

Linux permissions control who can read, write, or run a file.

There are 3 permission types:

```text
r = read
w = write
x = execute
```

Simple meaning:

```text
read    = open/view file
write   = edit file
execute = run file
```

---

## Permission Example

Command:

```bash
ls -l
```

Example output:

```bash
-rwxr-xr--  1 noor staff  100 Jun 5 script.sh
```

Understand this:

```text
- rwx r-x r--
```

Breakdown:

```text
-   = file
rwx = owner permissions
r-x = group permissions
r-- = others permissions
```

Simple meaning:

Owner can read, write, execute.  
Group can read and execute.  
Others can only read.  

---

## File Types in ls -l

First character tells file type:

```text
- = normal file
d = directory
l = link
```

Example:

```bash
-rw-r--r-- file.txt
drwxr-xr-x folder
lrwxr-xr-x shortcut
```

---

## chmod

Command:

```bash
chmod permission file-name
```

Meaning:

Change file permissions.

Simple meaning:

chmod = change access

Example:

```bash
chmod +x script.sh
```

This gives execute permission.

Run script:

```bash
./script.sh
```

---

## Numeric Permissions

Permissions also have numbers:

```text
r = 4
w = 2
x = 1
```

Examples:

```text
7 = 4+2+1 = read + write + execute
6 = 4+2   = read + write
5 = 4+1   = read + execute
4 = 4     = read only
```

Common permissions:

```bash
chmod 755 script.sh
chmod 644 file.txt
chmod 700 private-folder
```

Meanings:

```text
755 = owner full access, others read/execute
644 = owner read/write, others read only
700 = only owner has full access
```

---

## chown

Command:

```bash
chown user file-name
```

Meaning:

Change file owner.

Simple meaning:

chown = change owner

Example:

```bash
sudo chown noor file.txt
```

Change owner and group:

```bash
sudo chown noor:staff file.txt
```

---

# Level 6: Users and Groups

Linux can have many users.

Each user can belong to groups.

Simple meaning:

User = person/account  
Group = team of users  

---

## user commands

Show current user:

```bash
whoami
```

Show user ID and group info:

```bash
id
```

Show logged-in users:

```bash
who
```

---

## sudo

Command:

```bash
sudo command
```

Meaning:

Run command with admin/root permission.

Simple meaning:

sudo = run as admin

Example:

```bash
sudo apt update
```

Use sudo when a command needs higher permission.

Warning:

Do not use sudo blindly. It gives powerful access.

---

## su

Command:

```bash
su username
```

Meaning:

Switch to another user.

Simple meaning:

su = switch user

Example:

```bash
su root
```

---

# Level 7: Processes

A process is a running program.

Examples:

Browser running  
Java app running  
Database running  
Server running  

Simple meaning:

Process = program currently running

---

## ps

Command:

```bash
ps
```

Meaning:

Show running processes for current terminal.

More useful command:

```bash
ps -ef
```

Search for a process:

```bash
ps -ef | grep java
```

Simple meaning:

Show all running Java processes.

---

## top

Command:

```bash
top
```

Meaning:

Show live running processes and system usage.

Simple meaning:

top = live task manager

Quit:

```text
q
```

---

## kill

Command:

```bash
kill PID
```

Meaning:

Stop a running process.

Simple meaning:

kill = stop process

Example:

```bash
kill 1234
```

Force kill:

```bash
kill -9 1234
```

Warning:

Use `kill -9` carefully. It forcefully stops the process.

---

# Level 8: Disk and System Info

These commands help you check system space and usage.

---

## df

Command:

```bash
df -h
```

Meaning:

Show disk space.

Simple meaning:

df = disk free

`-h` means human-readable.

Example:

```bash
df -h
```

Use this when checking if server disk is full.

---

## du

Command:

```bash
du -sh folder-name
```

Meaning:

Show folder size.

Simple meaning:

du = disk usage

Example:

```bash
du -sh logs
```

Show sizes of all items:

```bash
du -sh *
```

---

## uname

Command:

```bash
uname -a
```

Meaning:

Show system/kernel information.

Simple meaning:

uname = system info

---

## free

Command:

```bash
free -h
```

Meaning:

Show memory/RAM usage.

Simple meaning:

free = memory info

Note:

On macOS, `free` may not be available by default.

---

# Level 9: Package Management

Package manager is used to install software.

Different Linux systems use different package managers.

```text
Ubuntu/Debian = apt
Red Hat/CentOS = yum or dnf
macOS = brew
```

Simple meaning:

Package manager = software installer

---

## apt

Used in Ubuntu/Debian.

Update package list:

```bash
sudo apt update
```

Install software:

```bash
sudo apt install package-name
```

Example:

```bash
sudo apt install git
```

Remove software:

```bash
sudo apt remove package-name
```

---

## yum / dnf

Used in Red Hat/CentOS/Fedora.

Install software:

```bash
sudo yum install package-name
```

Or:

```bash
sudo dnf install package-name
```

Example:

```bash
sudo dnf install git
```

---

## brew

Used mostly on macOS.

Install software:

```bash
brew install package-name
```

Example:

```bash
brew install git
```

---

# Level 10: Networking Basics

Networking commands help you check internet, servers, ports, and connections.

Important commands:

```text
ping
curl
wget
ssh
scp
netstat
ss
```

---

## ping

Command:

```bash
ping google.com
```

Meaning:

Check if a server is reachable.

Simple meaning:

ping = are you alive?

Stop ping:

```text
CTRL + C
```

---

## curl

Command:

```bash
curl website-url
```

Meaning:

Send request to a URL and show response.

Simple meaning:

curl = test URL/API from terminal

Example:

```bash
curl https://example.com
```

Check only headers:

```bash
curl -I https://example.com
```

---

## wget

Command:

```bash
wget file-url
```

Meaning:

Download file from internet.

Simple meaning:

wget = download file

Example:

```bash
wget https://example.com/file.zip
```

---

## ssh

Command:

```bash
ssh username@server-ip
```

Meaning:

Connect to a remote server securely.

Simple meaning:

ssh = login to server

Example:

```bash
ssh ubuntu@12.34.56.78
```

---

## scp

Command:

```bash
scp file username@server-ip:/path
```

Meaning:

Copy file to remote server.

Simple meaning:

scp = secure copy

Example:

```bash
scp app.log ubuntu@12.34.56.78:/home/ubuntu/
```

---

# Level 11: Logs and Services

In real servers, you often check logs and services.

Simple meaning:

Logs = records of what happened  
Service = background application  

---

## logs

Common log location:

```bash
/var/log
```

Go to logs:

```bash
cd /var/log
ls
```

View logs:

```bash
tail -f app.log
```

Search errors:

```bash
grep "ERROR" app.log
```

---

## systemctl

Command:

```bash
systemctl status service-name
```

Meaning:

Check service status.

Simple meaning:

systemctl = manage services

Examples:

```bash
sudo systemctl status nginx
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
```

Meanings:

```text
status  = check service
start   = start service
stop    = stop service
restart = restart service
```

---

## journalctl

Command:

```bash
journalctl -u service-name
```

Meaning:

View logs for a service.

Simple meaning:

journalctl = service logs

Example:

```bash
journalctl -u nginx
```

Live logs:

```bash
journalctl -u nginx -f
```

---

# Level 12: Shell Scripting Basics

A shell script is a file that contains Linux commands.

Simple meaning:

Shell script = commands saved in a file

It helps automate repeated work.

---

## Create a shell script

Create file:

```bash
touch hello.sh
```

Open file and add:

```bash
#!/bin/bash

echo "Hello from shell script"
```

Give execute permission:

```bash
chmod +x hello.sh
```

Run script:

```bash
./hello.sh
```

---

## Variables

Example:

```bash
name="Noor"
echo "Hello $name"
```

Simple meaning:

Variable = store value

---

## if condition

Example:

```bash
age=20

if [ $age -ge 18 ]; then
  echo "Adult"
else
  echo "Minor"
fi
```

Simple meaning:

if = make decision

---

## for loop

Example:

```bash
for fruit in apple banana orange; do
  echo "$fruit"
done
```

Simple meaning:

for loop = repeat work

---

# Level 13: DevOps Linux Skills

For DevOps, focus on these Linux skills:

```text
File navigation
Permissions
Users and groups
Logs
Processes
Services
Networking
Shell scripting
Package installation
SSH
Disk usage
Environment variables
Cron jobs
```

Simple meaning:

DevOps engineers use Linux to manage servers, debug issues, automate tasks, and deploy applications.

---

## Environment Variables

Environment variables store system values.

Command:

```bash
echo $PATH
```

Simple meaning:

Environment variable = value available to the system

Create variable:

```bash
export APP_ENV=dev
```

Use it:

```bash
echo $APP_ENV
```

---

## Cron Jobs

Cron jobs run commands automatically on schedule.

Simple meaning:

cron = scheduled task

Edit cron:

```bash
crontab -e
```

Example:

```bash
0 9 * * * /home/noor/backup.sh
```

Meaning:

Run `backup.sh` every day at 9 AM.

Cron format:

```text
minute hour day month day-of-week command
```

---

# Practice Roadmap

## Practice 1: Basic Navigation

```bash
pwd
ls
mkdir linux-practice
cd linux-practice
pwd
```

Goal:

Understand current location and moving into folders.

---

## Practice 2: Create Files and Folders

```bash
touch notes.txt
echo "Hello Linux" > notes.txt
cat notes.txt
mkdir backup
```

Goal:

Understand file creation and writing text.

---

## Practice 3: Copy, Move, and Delete

```bash
cp notes.txt backup.txt
mv backup.txt backup/
ls backup
rm notes.txt
```

Goal:

Understand file management.

---

## Practice 4: View Files

```bash
echo "line 1" > app.log
echo "line 2" >> app.log
echo "ERROR found" >> app.log
cat app.log
head app.log
tail app.log
```

Goal:

Understand file viewing commands.

---

## Practice 5: Search Text

```bash
grep "ERROR" app.log
grep -n "ERROR" app.log
find . -name "*.log"
```

Goal:

Understand searching inside files and finding files.

---

## Practice 6: Permissions

```bash
touch script.sh
echo '#!/bin/bash' > script.sh
echo 'echo "Hello"' >> script.sh
ls -l script.sh
chmod +x script.sh
ls -l script.sh
./script.sh
```

Goal:

Understand execute permission.

---

## Practice 7: Processes

```bash
ps
ps -ef | grep bash
top
```

Goal:

Understand running processes.

---

## Practice 8: Disk Usage

```bash
df -h
du -sh *
```

Goal:

Understand disk space and folder size.

---

## Practice 9: Networking

```bash
ping google.com
curl -I https://example.com
```

Goal:

Understand basic network testing.

---

## Practice 10: Shell Script

```bash
touch hello.sh
echo '#!/bin/bash' > hello.sh
echo 'echo "Learning Linux"' >> hello.sh
chmod +x hello.sh
./hello.sh
```

Goal:

Understand simple shell scripting.

---

# Common Beginner Mistakes

## Mistake 1: Running a folder as a command

Wrong:

```bash
/Users/noor/Desktop/
```

This may show permission denied.

Correct:

```bash
cd /Users/noor/Desktop/
```

Simple meaning:

Use `cd` to go into a folder.

---

## Mistake 2: Using rm carelessly

Wrong:

```bash
rm -rf important-folder
```

This can delete everything inside.

Correct:

Check first:

```bash
ls important-folder
```

Then delete only if you are sure.

---

## Mistake 3: Forgetting chmod +x

If script does not run, check permission.

```bash
ls -l script.sh
chmod +x script.sh
./script.sh
```

---

## Mistake 4: Confusing > and >>

```bash
>  = overwrite
>> = append
```

Example:

```bash
echo "line 1" > file.txt
echo "line 2" >> file.txt
```

---

## Mistake 5: Not knowing current location

When confused, run:

```bash
pwd
ls
```

Simple meaning:

First check where you are and what is inside.

---

## Mistake 6: Searching with wrong path

If this does not work:

```bash
find folder -name "file.txt"
```

Try current folder:

```bash
find . -name "file.txt"
```

---

# Final Linux Cheat Sheet

## Navigation

```bash
pwd
ls
ls -la
cd folder
cd ..
cd ~
clear
```

## Files and Folders

```bash
mkdir folder
touch file.txt
cp file.txt copy.txt
cp -r folder1 folder2
mv old.txt new.txt
rm file.txt
rm -r folder
```

## File Viewing

```bash
cat file.txt
less file.txt
head file.txt
tail file.txt
tail -f app.log
```

## Searching

```bash
grep "word" file.txt
grep -i "word" file.txt
grep -n "word" file.txt
grep -r "word" .
find . -name "*.txt"
```

## Permissions

```bash
ls -l
chmod +x script.sh
chmod 755 script.sh
chmod 644 file.txt
chown user file.txt
```

## Users

```bash
whoami
id
who
sudo command
su username
```

## Processes

```bash
ps
ps -ef
ps -ef | grep java
top
kill PID
kill -9 PID
```

## Disk and System

```bash
df -h
du -sh *
uname -a
free -h
```

## Networking

```bash
ping google.com
curl https://example.com
curl -I https://example.com
wget file-url
ssh username@server-ip
scp file username@server-ip:/path
```

## Services and Logs

```bash
systemctl status service-name
systemctl start service-name
systemctl stop service-name
systemctl restart service-name
journalctl -u service-name
journalctl -u service-name -f
```

## Shell Script

```bash
#!/bin/bash

echo "Hello Linux"
```

Run:

```bash
chmod +x script.sh
./script.sh
```

---

# Best Memory Trick

```text
pwd = where am I?
ls = what is here?
cd = go there
mkdir = create folder
touch = create file
cat = read file
cp = copy
mv = move/rename
rm = delete
grep = search inside file
find = find file
chmod = change permission
sudo = run as admin
ps = show process
kill = stop process
df = disk space
du = folder size
ssh = connect to server
```

---

# Final Summary

Linux is not just about commands.

Linux is about controlling servers and systems.

The basic idea is:

```text
Move around → Manage files → Read logs → Check permissions → Manage processes → Automate tasks
```

Most important beginner flow:

```bash
pwd
ls
cd folder
cat file.txt
grep "ERROR" app.log
chmod +x script.sh
./script.sh
```

If you understand this flow clearly, Linux becomes much easier.


