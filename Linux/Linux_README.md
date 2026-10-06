# 🐧 Linux

> A complete record of my Linux learning journey for cybersecurity.

Linux was one of the first major foundations I studied after starting my cybersecurity journey.

I learned Linux not only as an operating system, but also as an environment for cybersecurity, system administration, networking, automation, and security testing.

---

## 📚 Topics Covered

### 1. Linux Fundamentals

- What is Linux?
- Linux vs Windows
- Linux distributions
- Kernel and Shell
- CLI vs GUI
- Linux directory structure
- Absolute and relative paths
- Root user and normal users
- Environment variables

---

### 2. Linux File System

Understanding the Linux filesystem and important directories:

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── tmp
├── usr
└── var
```

Important concepts:

- Files and directories
- Hidden files
- Absolute paths
- Relative paths
- System directories

---

### 3. File & Directory Management

Commands practiced:

```bash
pwd
ls
cd
mkdir
rmdir
touch
cp
mv
rm
find
locate
file
stat
```

Learned how to:

- Navigate directories
- Create files and directories
- Copy files
- Move and rename files
- Delete files and directories
- Search for files
- Identify file types
- Inspect file information

---

### 4. Viewing & Processing Files

Commands:

```bash
cat
less
more
head
tail
wc
sort
uniq
cut
grep
```

Also learned:

- Standard input
- Standard output
- Standard error
- Pipes
- Redirection
- Command chaining

Examples:

```bash
command > output.txt
command >> output.txt
command < input.txt
command1 | command2
```

---

### 5. Text Editors

Worked with Linux text editors, including:

- Nano
- Vim / Vi

Learned basic file editing directly from the terminal.

---

### 6. Linux File Permissions

Understanding:

```text
r = read
w = write
x = execute
```

Permission structure:

```text
Owner | Group | Others
 rwx  |  rwx  |  rwx
```

Commands:

```bash
ls -l
chmod
chown
chgrp
```

Also learned:

- Permission notation
- Numeric permissions
- Ownership
- User and group permissions
- Executable files

Example:

```bash
chmod 755 script.sh
```

---

### 7. Users & Groups

Learned:

- Linux users
- Groups
- Root privileges
- User identification
- File ownership
- Privilege management

Useful commands:

```bash
whoami
id
who
groups
su
sudo
passwd
```

---

### 8. Processes & System Management

Learned how Linux manages running processes.

Commands/tools:

```bash
ps
top
htop
kill
pkill
jobs
bg
fg
```

Concepts:

- Processes
- Process IDs
- Background processes
- Foreground processes
- Signals
- Process termination

---

### 9. Package Management

Learned how software/packages are installed and managed in Linux.

For Debian-based systems:

```bash
apt update
apt upgrade
apt install
apt remove
```

Also learned the basic concept of:

- Repositories
- Packages
- Package managers
- Software dependencies

---

### 10. Networking in Linux

Practiced basic Linux networking commands:

```bash
ip
ping
ss
netstat
curl
wget
nslookup
dig
```

Learned about:

- IP addresses
- Network interfaces
- Connectivity testing
- Ports
- DNS queries
- Network connections
- Downloading resources from the terminal

---

### 11. Services & Servers

Learned the fundamentals of Linux servers and services.

Topics:

- What is a server?
- Client-server architecture
- Running services
- Network services
- Basic server setup
- Hosting resources from Linux

Also practiced setting up a basic server environment.

---

### 12. Bash Shell

Learned Bash as a command-line shell and scripting environment.

Topics:

- Shebang
- Variables
- User input
- Command substitution
- Arrays
- Conditional statements
- Loops
- Functions
- Exit status
- Basic automation

Example:

```bash
#!/bin/bash

name="Rudra"

echo "Hello $name"
```

---

### 13. Bash Scripting

Practiced writing scripts for automation and command execution.

Concepts:

```bash
if
elif
else
for
while
case
```

Also learned how to:

- Create executable scripts
- Pass arguments
- Work with variables
- Use conditions
- Automate repetitive tasks

---

## 🔐 Linux for Cybersecurity

Linux became an important foundation for my cybersecurity learning.

I learned how Linux can be used for:

- Security testing
- Network analysis
- Reconnaissance
- Automation
- Web security testing
- System administration
- Running security tools
- Working with servers
- Managing permissions
- Analyzing processes and files

I also became familiar with security-focused Linux environments such as Kali Linux.

---

## 🛠️ Important Commands Reference

| Category | Commands |
|---|---|
| Navigation | `pwd`, `ls`, `cd` |
| Files | `touch`, `cp`, `mv`, `rm` |
| Directories | `mkdir`, `rmdir` |
| Search | `find`, `locate`, `grep` |
| File viewing | `cat`, `less`, `head`, `tail` |
| Permissions | `chmod`, `chown`, `chgrp` |
| Users | `whoami`, `id`, `who`, `groups` |
| Processes | `ps`, `top`, `htop`, `kill` |
| Networking | `ip`, `ping`, `ss`, `netstat` |
| DNS | `nslookup`, `dig` |
| Download | `curl`, `wget` |
| Packages | `apt` |
| Editors | `nano`, `vim` |
| Scripting | `bash` |

---

## 🧪 Practical Learning

During my Linux learning, I practiced:

- Navigating the Linux filesystem
- Managing files and directories
- Working with permissions
- Managing users and groups
- Running and managing processes
- Using networking commands
- Working with Linux servers
- Writing Bash scripts
- Automating tasks from the terminal
- Using Linux as a cybersecurity environment

---

## 🧠 Key Takeaways

The main things I learned from Linux:

1. How the Linux filesystem works
2. How to efficiently work from the terminal
3. How Linux permissions and ownership work
4. How users, groups, and privileges work
5. How to manage processes and services
6. How Linux networking works at a basic level
7. How to automate tasks using Bash
8. How Linux is used in cybersecurity

---

## ✅ Status

**Linux Fundamentals — Completed ✅**

Linux is now one of the foundational skills I use throughout my cybersecurity learning journey.

---

### 🔐 Learn → Practice → Understand → Document
