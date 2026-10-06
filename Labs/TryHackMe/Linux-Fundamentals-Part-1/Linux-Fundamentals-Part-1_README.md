# Linux Fundamentals Part 1

**Platform:** TryHackMe  
**Room:** Linux Fundamentals Part 1  
**Difficulty:** Easy  
**Status:** Completed ✅

This room was my first hands-on TryHackMe introduction to Linux. I used the browser-based Ubuntu machine to practice basic Linux commands, filesystem navigation, file searching, text searching, and shell operators.

🔗 **Official Room:** https://tryhackme.com/room/linuxfundamentalspart1

---

## 🎯 Objective

The main objective of this room was to become comfortable interacting with a Linux system through the terminal.

The room focused on:

- Understanding where Linux is commonly used
- Interacting with a Linux machine through the terminal
- Navigating the Linux filesystem
- Reading and locating files
- Searching file contents
- Using basic shell operators
- Building command-line confidence

---

## 🧪 Practical Environment

The room provided a deployable **Ubuntu Linux machine** directly in the browser.

I practiced the commands and concepts inside the provided lab environment rather than only reading the theory.

---

## 📚 What I Learned

### 1. Linux Fundamentals

Learned the role of Linux as an operating system and why Linux is widely used in:

- Servers
- Websites and web applications
- Embedded systems
- Networking infrastructure
- Security tooling
- Enterprise environments

I also learned the concept of Linux distributions, including Ubuntu and Debian.

---

### 2. Basic Terminal Commands

Practiced basic commands for interacting with a Linux terminal.

| Command | Purpose |
|---|---|
| `echo` | Output text |
| `whoami` | Display the current user |
| `ls` | List files and directories |
| `cd` | Change directory |
| `cat` | Display file contents |
| `pwd` | Display the current working directory |

Example:

```bash
whoami
pwd
ls
cd Documents
cat todo.txt
```

---

### 3. Linux Filesystem Navigation

Practiced navigating directories without relying on a graphical interface.

Important concepts:

- Current working directory
- Absolute paths
- Relative paths
- Home directory
- Files vs directories
- Moving between directories

Example:

```bash
pwd
ls
cd /home/tryhackme
ls
```

---

### 4. Searching for Files

Learned how `find` can be used to locate files efficiently.

Examples:

```bash
find -name passwords.txt
find -name "*.txt"
```

This is useful when working with large directory structures where manually checking every directory would be inefficient.

---

### 5. Searching File Contents with `grep`

Learned how `grep` can search inside files for specific text.

Example:

```bash
grep "THM" access.log
```

Also learned recursive searching:

```bash
grep -R "keyword" /etc/
```

This is particularly useful for:

- Log analysis
- Configuration analysis
- Finding specific values
- Security investigations
- Reconnaissance and troubleshooting

---

### 6. Shell Operators

Practiced basic shell operators used to control command execution and output.

| Operator | Purpose |
|---|---|
| `&` | Run a command in the background |
| `&&` | Run the next command only if the previous command succeeds |
| `>` | Redirect output and overwrite a file |
| `>>` | Redirect output and append to a file |

Examples:

```bash
command &
command1 && command2

echo "hello" > file.txt
echo "world" >> file.txt
```

### `>` vs `>>`

```text
>   → overwrite existing contents
>>  → append to existing contents
```

Understanding this difference is important when working with files and automation.

---

## 🔧 Important Commands — Quick Reference

```bash
# User
whoami

# Current location
pwd

# List directory contents
ls
ls -la

# Change directory
cd directory
cd ..
cd ~

# Read a file
cat file.txt

# Search for files
find -name "file.txt"
find -name "*.txt"

# Search inside files
grep "keyword" file.txt
grep -R "keyword" directory/

# Output / file redirection
echo "text" > file.txt
echo "text" >> file.txt
```

---

## 🔐 Cybersecurity Relevance

These Linux fundamentals are directly relevant to cybersecurity.

### Reconnaissance

Commands such as:

```bash
ls
find
grep
```

help locate files, directories, and useful information.

### Log Analysis

`grep` can quickly filter large log files for:

- IP addresses
- usernames
- error messages
- suspicious strings
- indicators of interest

### System Administration

Commands such as:

```bash
whoami
pwd
cd
ls
```

are fundamental when working on remote Linux systems.

### Security Tools

Many cybersecurity tools and environments are Linux-based, so being comfortable with the terminal is essential for further security learning.

---

## 🧠 Key Takeaways

- Linux is heavily used across modern computing and cybersecurity.
- The terminal is a primary way of interacting with Linux systems.
- `ls`, `cd`, `pwd`, and `cat` are essential filesystem commands.
- `find` helps locate files efficiently.
- `grep` helps search file contents.
- Shell operators can combine commands and redirect output.
- Strong Linux fundamentals make later cybersecurity labs much easier.

---

## 📝 What This Room Added to My Skills

Before this room, Linux commands were mainly something I knew conceptually.

After completing the room, I had practical experience with:

```text
Linux
  │
  ├── Terminal
  ├── Filesystem Navigation
  ├── File Reading
  ├── File Searching
  ├── Text Searching
  └── Shell Operators
```

This became one of the foundations for my later cybersecurity labs and tooling practice.

---

## 🔄 Next Step

Continue building Linux skills through:

- More advanced Linux commands
- SSH
- Permissions
- Users and groups
- Processes
- Networking commands
- Bash scripting
- Security-focused Linux administration

---

## ⚖️ Ethical Practice

All practical work in this room was performed inside the authorized TryHackMe training environment.

The techniques documented here are intended for:

- Education
- Authorized labs
- Defensive security
- Responsible cybersecurity practice

---

**Status: Completed ✅**
