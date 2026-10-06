# 🐚 Bash

> A complete record of my Bash learning journey, focused on Linux command-line usage, shell scripting, automation, system interaction, and cybersecurity workflows.

Bash is both a Unix shell and a scripting language. Learning Bash strengthened my Linux skills and taught me how to automate commands, manage files and processes, work with system information, and build repeatable security workflows.

---

## 🎯 Learning Objectives

My Bash learning focused on:

- Understanding the Bash shell
- Working efficiently from the Linux terminal
- Writing shell scripts
- Using variables and user input
- Working with conditions and loops
- Automating repetitive tasks
- Managing files and processes
- Using pipes and redirection
- Working with command-line tools
- Building cybersecurity-oriented automation workflows

---

# 1. 🐧 Bash & Shell Fundamentals

### What is Bash?

Bash stands for **Bourne Again SHell**.

It provides:

- A command-line interface
- Command execution
- Shell scripting
- Environment management
- Process control
- Automation capabilities

Basic workflow:

```text
User
 ↓
Bash Shell
 ↓
Command
 ↓
Operating System
 ↓
Output
```

---

# 2. ⌨️ Essential Linux Commands

Practiced common commands from Bash:

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
cat
less
head
tail
```

These commands are fundamental for navigating and managing a Linux environment.

---

# 3. 🔍 Searching & Text Processing

Studied commands such as:

```bash
find
grep
locate
sort
uniq
cut
wc
head
tail
```

Examples:

```bash
grep "error" logfile.txt
find /home -name "*.txt"
```

These tools are useful for:

- Log analysis
- Searching files
- Extracting information
- Processing security data

---

# 4. 🔀 Pipes

Pipes send the output of one command to another command.

Example:

```bash
cat logfile.txt | grep "error"
```

Concept:

```text
Command 1
   ↓
Output
   ↓
Pipe |
   ↓
Command 2
```

Pipes are one of the most powerful features of Unix-style command-line workflows.

---

# 5. 📤 Output Redirection

Studied:

```bash
>
>>
<
```

### `>`

Writes output to a file and replaces existing content.

```bash
ls > files.txt
```

### `>>`

Appends output.

```bash
date >> log.txt
```

### `<`

Uses a file as input.

```bash
command < input.txt
```

---

# 6. 🔗 Command Chaining

Studied operators:

```bash
;
&&
||
```

Examples:

```bash
command1 ; command2
```

```bash
command1 && command2
```

```bash
command1 || command2
```

This allows multiple operations to be combined into a single workflow.

---

# 7. 📝 Shell Scripts

A Bash script is a text file containing commands that Bash can execute.

Basic structure:

```bash
#!/bin/bash

echo "Hello, Cybersecurity!"
```

The first line is called the **shebang** and specifies the interpreter.

---

# 8. ▶️ Script Execution

A script can be executed using Bash:

```bash
bash script.sh
```

Or made executable:

```bash
chmod +x script.sh
./script.sh
```

Understanding executable permissions connects Bash scripting with Linux permission management.

---

# 9. 📦 Variables

Studied shell variables.

Example:

```bash
name="Rudra"
echo "$name"
```

Important concepts:

- Variable assignment
- Variable expansion
- Environment variables
- Local variables
- Special variables

---

# 10. ⌨️ User Input

Used:

```bash
read
```

Example:

```bash
read -p "Enter your name: " name
echo "Hello $name"
```

User input can be used to create interactive command-line utilities.

---

# 11. 🔢 Arrays

Studied Bash arrays.

Example:

```bash
ports=(22 53 80 443)

echo "${ports[0]}"
```

Arrays are useful when processing multiple values or targets in a controlled workflow.

---

# 12. 🔀 Conditional Statements

Studied:

```bash
if
elif
else
```

Example:

```bash
if [ "$status" = "open" ]; then
    echo "Service is available"
else
    echo "Service is unavailable"
fi
```

---

# 13. 🔁 Loops

Studied:

### For Loop

```bash
for item in "${items[@]}"; do
    echo "$item"
done
```

### While Loop

```bash
while condition; do
    # commands
done
```

Also practiced:

```bash
break
continue
```

Loops are essential for automation.

---

# 14. 🔧 Functions

Functions allow reusable Bash code.

Example:

```bash
check_file() {
    if [ -f "$1" ]; then
        echo "File exists"
    fi
}
```

Functions help keep larger scripts organized and reusable.

---

# 15. 📥 Command-Line Arguments

Bash provides positional parameters.

Common variables:

```text
$0   Script name
$1   First argument
$2   Second argument
$#   Number of arguments
$@   All arguments
```

Example:

```bash
#!/bin/bash

echo "Target: $1"
```

Usage:

```bash
./script.sh example.com
```

---

# 16. 🚦 Exit Status

Commands return an exit status.

Convention:

```text
0      Success
non-zero  Error / failure
```

The previous command's exit status can be accessed using:

```bash
$?
```

Example:

```bash
command

if [ $? -eq 0 ]; then
    echo "Success"
fi
```

---

# 17. ⚠️ Error Handling

Studied basic techniques for handling command failures.

Examples:

```bash
command || echo "Command failed"
```

And:

```bash
if command; then
    echo "Success"
else
    echo "Failed"
fi
```

For larger scripts, careful error handling makes automation more reliable.

---

# 18. 🌍 Environment Variables

Important environment variables include:

```bash
$PATH
$HOME
$USER
$SHELL
$PWD
```

View environment variables:

```bash
env
```

or:

```bash
printenv
```

Environment variables are important for configuration and command execution.

---

# 19. 🧮 Arithmetic

Bash supports arithmetic expressions.

Example:

```bash
a=10
b=5

result=$((a + b))

echo "$result"
```

Operators include:

```text
+
-
*
/
%
```

---

# 20. 🔎 Test Conditions

Used test expressions such as:

```bash
[ -f file ]
[ -d directory ]
[ -r file ]
[ -w file ]
[ -x file ]
```

Also studied string and numeric comparisons.

---

# 21. 📁 File & Directory Automation

Bash can automate:

- Creating directories
- Renaming files
- Copying files
- Moving files
- Removing files
- Searching files
- Processing large numbers of files

Example:

```bash
for file in *.log; do
    echo "Processing $file"
done
```

---

# 22. 🖥️ Process Management

Bash interacts with Linux processes.

Commands:

```bash
ps
top
htop
jobs
bg
fg
kill
pkill
```

Studied concepts:

- Foreground processes
- Background processes
- Process IDs
- Signals
- Job control

---

# 23. 🔐 Permissions

Bash scripts must follow Linux permission rules.

Example:

```bash
chmod +x script.sh
```

Studied:

```text
r = read
w = write
x = execute
```

This connects Bash scripting with Linux security and access control.

---

# 24. 🌐 Networking from Bash

Bash can combine Linux networking utilities into automation workflows.

Useful commands:

```bash
ping
ip
ss
curl
wget
nslookup
dig
traceroute
```

Example:

```bash
ping -c 4 example.com
```

Bash can therefore automate authorized network diagnostics and analysis.

---

# 25. 🔐 Bash for Cybersecurity

Bash is especially useful in cybersecurity because many security tools run from the command line.

Applications include:

### Reconnaissance Automation

Combining authorized tools and processing their output.

### Log Analysis

Searching logs for suspicious patterns.

### System Enumeration

Collecting system information during authorized assessments.

### File Analysis

Finding and processing files.

### Security Checks

Automating repetitive configuration checks.

### Tool Chaining

Using pipes and scripts to connect multiple command-line tools.

---

# 26. 🧰 Useful Command-Line Tools

Bash workflows commonly use tools such as:

```text
grep
awk
sed
cut
sort
uniq
find
xargs
curl
wget
jq
tr
head
tail
```

These tools are particularly useful for transforming and analyzing command output.

---

# 27. 🔎 Bash & Reconnaissance

Bash can automate parts of authorized reconnaissance workflows.

Example concept:

```text
Input
  ↓
Command
  ↓
Output
  ↓
Filter
  ↓
Process
  ↓
Report
```

The purpose is to reduce repetitive manual work.

Any scanning or reconnaissance must only target systems where explicit authorization exists.

---

# 28. 📊 Log Analysis

Bash is useful for quickly searching large text-based logs.

Example:

```bash
grep "Failed" auth.log
```

Combining tools:

```bash
grep "Failed" auth.log | sort | uniq -c
```

This can help identify repeated events or patterns during defensive analysis.

---

# 29. 🔄 Automation Workflow

A typical Bash automation workflow:

```text
Define Task
    ↓
Collect Input
    ↓
Execute Commands
    ↓
Check Exit Status
    ↓
Process Output
    ↓
Generate Result
    ↓
Log Activity
```

---

# 30. 🛡️ Bash Security Practices

Important scripting practices:

- Quote variables where appropriate
- Validate user input
- Avoid blindly executing untrusted input
- Use absolute paths when appropriate
- Check command exit status
- Handle errors
- Avoid unnecessary privileges
- Keep scripts readable
- Avoid exposing secrets
- Use least privilege
- Test scripts in safe environments

A particularly important principle is to avoid constructing shell commands from untrusted input without proper validation and safe handling.

---

# 31. 🧪 Practical Applications

Bash can be used to build:

- System information scripts
- Log analyzers
- File integrity checks
- Backup scripts
- Network diagnostic scripts
- Security configuration checks
- Automation utilities
- Reconnaissance workflows for authorized targets
- Tool wrappers

---

# 32. 🧠 Bash in My Cybersecurity Workflow

Bash fits into my learning path:

```text
Linux
   ↓
Bash
   ↓
Command-Line Automation
   ↓
Security Tools
   ↓
Labs
   ↓
Reconnaissance & Analysis
   ↓
Cybersecurity Projects
```

Linux provides the environment.

Bash provides the automation layer.

Cybersecurity tools provide specialized capabilities.

Together they create efficient command-line workflows.

---

# 33. 📚 Important Bash Concepts

The key concepts I learned include:

- Shell fundamentals
- Commands
- Pipes
- Redirection
- Variables
- Environment variables
- User input
- Arrays
- Conditions
- Loops
- Functions
- Arguments
- Exit status
- File operations
- Process management
- Networking commands
- Automation
- Error handling

---

# 34. 🛠️ Bash Command Reference

| Category | Commands / Concepts |
|---|---|
| Navigation | `pwd`, `ls`, `cd` |
| Files | `touch`, `cp`, `mv`, `rm` |
| Search | `find`, `grep`, `locate` |
| Text processing | `awk`, `sed`, `cut`, `sort`, `uniq` |
| Viewing | `cat`, `less`, `head`, `tail` |
| Networking | `ping`, `ip`, `ss`, `curl`, `wget` |
| DNS | `nslookup`, `dig` |
| Processes | `ps`, `top`, `htop`, `kill` |
| Permissions | `chmod`, `chown` |
| Scripting | `if`, `for`, `while`, `case`, functions |
| Shell control | pipes, redirection, command chaining |

---

# 35. ⚖️ Ethical Use

Bash scripts documented and developed during my cybersecurity learning are intended for:

- Education
- Personal systems
- Authorized security testing
- CTFs
- Intentionally vulnerable labs
- Defensive security
- System administration
- Automation

I do not use scripts to access, scan, compromise, or interfere with systems without authorization.

---

# 📊 Completion Status

| Area | Status |
|---|---|
| Bash Fundamentals | ✅ Completed |
| Linux CLI | ✅ Completed |
| File Management | ✅ Completed |
| Pipes & Redirection | ✅ Completed |
| Variables | ✅ Completed |
| User Input | ✅ Completed |
| Arrays | ✅ Completed |
| Conditions | ✅ Completed |
| Loops | ✅ Completed |
| Functions | ✅ Completed |
| Command-Line Arguments | ✅ Completed |
| Exit Status | ✅ Completed |
| Error Handling | ✅ Completed |
| Environment Variables | ✅ Completed |
| Process Management | ✅ Completed |
| Networking Commands | ✅ Completed |
| Automation | ✅ Completed |
| Cybersecurity Applications | ✅ Completed |

---

## 🎯 Next Step

Bash is complete as a Linux scripting and automation foundation.

The next goal is to apply Bash through:

- Linux automation
- Security scripts
- Log analysis
- Tool chaining
- Authorized reconnaissance workflows
- System administration
- Cybersecurity projects

---

## ✅ Status

**Bash — Completed ✅**

Bash is now part of my Linux, scripting, automation, and cybersecurity toolkit.

---

### 🐚 Learn → Script → Automate → Analyze → Secure
