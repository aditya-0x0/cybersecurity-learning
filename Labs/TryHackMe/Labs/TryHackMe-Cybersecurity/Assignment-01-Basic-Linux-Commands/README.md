# Assignment 01 — Basic Linux Commands

**Course:** TuteDude Cybersecurity  
**Lab:** TryHackMe — `TuteDude-CyberSecurity`  
**Topic:** Basic Linux Commands  
**Status:** Evidence available; documentation based on the screenshots provided.

## Objective

Practice connecting to the course lab and using basic Linux commands to identify the current directory and logged-in user.

## Lab Environment

- Parrot Security running in VirtualBox
- Course-provided Linux target named `hacking`
- SSH access to the lab target

> The screenshots show a course lab target at `10.0.2.4` on port `8080` and a prompt asking the learner to connect with SSH. These details are recorded only as visible in the supplied evidence; use the current target details shown by your own lab when repeating the exercise.

## Steps Performed

### 1. Access the lab

The lab console displayed the target details and requested an SSH login. The supplied file set includes a screenshot of the lab console and SSH-login stage.

### 2. Check the current working directory

Command:

```bash
pwd
```

Observed output:

```text
/home/student
```

**What it does:** `pwd` prints the current working directory.

### 3. Identify the current user

Command:

```bash
whoami
```

Observed output:

```text
student
```

**What it does:** `whoami` prints the username of the current effective user.

## Evidence

- [`evidence/01-lab-and-terminal.png`](evidence/01-lab-and-terminal.png) — lab target console and terminal context.
- [`evidence/02-pwd-whoami.png`](evidence/02-pwd-whoami.png) — `pwd` and `whoami` commands with their outputs.
- [`evidence/03-ssh-login.png`](evidence/03-ssh-login.png) — SSH/login stage supplied with the assignment.

## Key Takeaways

- `pwd` is used to confirm the current working directory.
- `whoami` identifies the current user.
- SSH is commonly used to access a remote Linux machine securely.
- Before running commands in a lab, confirm that the target and environment are the ones provided for the exercise.

## Notes

This README documents only the commands and activity visible in the submitted evidence. Add further commands, outputs, and screenshots if the assignment required additional tasks that are not shown here.

---

**Learning workflow:** Understand the task → run the command → verify the output → document the evidence.
