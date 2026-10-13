# Assignment 02 — Linux Permissions

**Course:** TuteDude Cybersecurity  
**Lab:** TryHackMe — `TuteDude-CyberSecurity`  
**Topic:** Linux file permissions and access control  
**Status:** Documented from the submitted assignment evidence

## Objective

Understand how Linux file and directory permissions affect access, inspect hidden files, and read files in the provided training environment.

## Lab Environment

- Parrot Security OS running in VirtualBox
- Course-provided target accessed over SSH
- TryHackMe room: `TuteDude-CyberSecurity`

Only use these techniques in systems and labs where you have authorization.

## Tasks and What I Practiced

### 1. Connect to the training machine

The evidence shows an SSH connection from the Parrot Security terminal to the course target.

SSH is used to access a remote system through an encrypted connection. Use the host and credentials provided by the active lab rather than reusing old target details.

### 2. Read a file in the `loot` directory

Commands shown in the evidence:

```bash
cat readme.txt
ls -la
cat .hidden_file.txt
```

**What I learned:**
- `cat` displays file contents.
- `ls -la` lists files, including hidden entries whose names begin with a dot.
- A file may be present but not obvious in a normal directory listing.

The screenshot shows the `readme.txt` file and a hidden file named `.hidden_file.txt` in the lab's `loot` directory.

### 3. Inspect Linux permissions

The `ls -la` output displays permission strings such as `-rw-rw-r--` and `drwxr-x---`.

The first character indicates the file type; the remaining characters describe read (`r`), write (`w`), and execute (`x`) permissions for the owner, group, and others.

Examples:

- `-rw-rw-r--` — regular file; owner and group can read/write; others can read.
- `drwxr-x---` — directory; owner has read/write/execute, group has read/execute, and others have no permissions.

For directories, `x` means the ability to traverse/access entries within the directory; `r` allows listing names and `w` allows modifying directory entries, subject to the relevant permissions.

### 4. Read a restricted practice file

The screenshot shows navigation to `/home/student/practice` and reading `restricted_file.txt`.

Commands visible in the evidence:

```bash
cd /
ls
cd /home/student/practice
ls
cat restricted_file.txt
```

This exercise demonstrates that file access depends on the permissions configured in the lab. The supplied screenshot shows the file content being read successfully in the training environment.

### 5. Review a script-based file-reading task

The room prompt shown in the screenshot asks the learner to edit `read_secret.sh` so that it reads `secret.txt`. The provided evidence does not show the completed script or the final answer for this task, so it is recorded here as a task prompt rather than marked complete.

## Evidence

- [`evidence/01-linux-permissions-task.png`](evidence/01-linux-permissions-task.png) — terminal commands, hidden-file discovery, permission listing, and the room task prompt.
- [`evidence/02-ssh-lab-access.png`](evidence/02-ssh-lab-access.png) — SSH connection and lab target context.

## Key Takeaways

- Use `ls -la` to inspect hidden files and view permission strings.
- Linux permissions are separated into owner, group, and others.
- Read, write, and execute permissions have different meanings for files and directories.
- `cat` can display file contents when the current user has permission.
- Record only the steps and results actually shown by the evidence; verify remaining task answers before documenting them as completed.

## Commands Quick Reference

| Command | Purpose |
|---|---|
| `ssh user@host` | Connect to an authorized remote lab |
| `pwd` | Print the current working directory |
| `ls -la` | List files, including hidden files, with details |
| `cat filename` | Display a file's contents |
| `cd /path` | Change directory |

---

**Learning workflow:** Inspect → understand permissions → test in the lab → verify output → document evidence.
