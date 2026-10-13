# Assignment 03 — File System Commands

**Course:** TuteDude Cybersecurity  
**Lab:** TryHackMe — `TuteDude-CyberSecurity`  
**Topic:** Linux file-system navigation and file inspection  
**Evidence status:** Screenshots supplied; this README documents the visible work.

## Objective

Practice navigating a Linux file system, listing files, identifying hidden files, and reading file contents in the authorized course lab.

## Environment

- Parrot Security OS in VirtualBox
- SSH session to the course-provided Linux target
- TryHackMe room: `TuteDude-CyberSecurity`

## Commands Practiced

### 1. Print the current directory

```bash
pwd
```

The screenshot shows `/home/student` as the current working directory.

**Purpose:** `pwd` prints the full path of the current directory.

### 2. Identify the current user

```bash
whoami
```

The visible output is `student`.

**Purpose:** `whoami` prints the current effective username.

### 3. List files and directories

```bash
ls
```

The lab output shows entries including `loot`, `practice`, `read_secret.sh`, `run_secret`, and `secret.txt`.

**Purpose:** `ls` lists the contents of a directory.

### 4. Navigate into a directory

```bash
cd loot
ls
```

The terminal shows navigation into the `loot` directory and a listing that includes `readme.txt`.

**Purpose:** `cd` changes the current working directory.

### 5. Read a file

```bash
cat readme.txt
```

The screenshot shows the file being read successfully after using the correct filename. An earlier typo (`cat reatme.txt`) returned a “No such file or directory” error.

**Purpose:** `cat` prints file contents. The error is a useful reminder to verify filenames carefully.

### 6. Show hidden files and file details

```bash
ls -la
```

The output includes `.hidden_file.txt` as well as permission and ownership information.

**Purpose:** `-a` includes hidden entries (names beginning with `.`), while `-l` shows detailed information such as permissions, owner, size, and modification time.

### 7. Read a hidden file

```bash
cat .hidden_file.txt
```

The screenshot shows the hidden file being accessed successfully in the lab.

**Purpose:** A leading dot makes a filename hidden from a standard `ls` listing; it does not by itself provide access control.

## Additional Task Visible in the Room

The room page also shows a task asking the learner to inspect `/home/student/practice/restricted_file.txt` and to edit `read_secret.sh` so it reads `secret.txt`. The provided screenshots do **not** show a verified final result for those two prompts, so they are recorded as follow-up tasks rather than marked complete here.

## Evidence

- [`evidence/01-file-system-commands.png`](evidence/01-file-system-commands.png) — `pwd`, `whoami`, `ls`, and navigation into `loot`.
- [`evidence/02-reading-file-and-hidden-file.png`](evidence/02-reading-file-and-hidden-file.png) — reading `readme.txt`, using `ls -la`, and reading `.hidden_file.txt`.
- [`evidence/03-room-task-progress.png`](evidence/03-room-task-progress.png) — room page and the additional prompts visible in the supplied screenshot.
- [`evidence/04-ssh-lab-access.png`](evidence/04-ssh-lab-access.png) — SSH/lab terminal context.

## Key Takeaways

- Use `pwd` to confirm where you are.
- Use `ls` to list directory contents and `ls -la` to include hidden files and detailed metadata.
- Use `cd` to navigate between directories.
- Use `cat` to inspect readable text files.
- Hidden filenames begin with a dot, but hidden does not mean protected.
- When a command fails, check the spelling and the current directory before retrying.
- Only document a task as complete when its result is visible or otherwise verified.

## Quick Reference

| Command | Purpose |
|---|---|
| `pwd` | Print the current directory |
| `whoami` | Show the current user |
| `ls` | List directory contents |
| `ls -la` | Show detailed listing, including hidden entries |
| `cd path` | Change directory |
| `cat filename` | Print a text file's contents |

---

**Workflow:** Navigate → inspect → read → verify → document.
