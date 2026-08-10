# Basic Linux Commands

## What are Linux Commands?

Linux commands are instructions entered into the terminal to perform specific tasks.

Commands allow users to:

* Navigate directories
* View files
* Manage users
* Monitor systems
* Configure networks
* Perform administrative tasks

Most cybersecurity professionals spend significant time working in the Linux terminal.

---

## Why Are Linux Commands Important?

Without Commands

Users would rely entirely on graphical interfaces.

This can:

* Limit functionality
* Slow down administration
* Make automation difficult

With Commands

Users can:

* Work faster
* Automate tasks
* Manage remote servers
* Perform security investigations efficiently

---

## Real-World Example

When a cybersecurity analyst connects to a Linux server:

```text
Analyst
   │
   ▼
Linux Terminal
   │
   ▼
Commands
   │
   ▼
System Information
```

Commands provide direct control over the operating system.

---

## Current Working Directory

### pwd

Displays the current directory.

```bash
pwd
```

Example Output:

```bash
/home/akshat
```

Useful for identifying your current location in the file system.

---

## List Files and Directories

### ls

Displays files and folders.

```bash
ls
```

Example Output:

```bash
Documents
Downloads
Pictures
```

---

### ls -l

Displays detailed information.

```bash
ls -l
```

Example Output:

```bash
drwxr-xr-x 2 user user 4096 Jul 20 Documents
-rw-r--r-- 1 user user 1200 Jul 20 notes.txt
```

---

### ls -a

Displays hidden files.

```bash
ls -a
```

Example Output:

```bash
.
..
.bashrc
.profile
Documents
```

Hidden files start with a dot (.).

---

## Change Directory

### cd

Moves between directories.

```bash
cd Documents
```

---

### Go Back One Directory

```bash
cd ..
```

---

### Go to Home Directory

```bash
cd ~
```

or

```bash
cd
```

---

## Clear Terminal Screen

### clear

Clears the terminal display.

```bash
clear
```

Useful when the terminal becomes cluttered.

---

## Identify Current User

### whoami

Displays the logged-in user.

```bash
whoami
```

Example Output:

```bash
akshat
```

Frequently used during security investigations.

---

## View Hostname

### hostname

Displays the system hostname.

```bash
hostname
```

Example Output:

```bash
ubuntu-server
```

Useful for identifying systems on a network.

---

## View Date and Time

### date

Displays current system date and time.

```bash
date
```

Example Output:

```bash
Tue Jul 22 10:30:45 IST 2025
```

Useful during forensic investigations.

---

## System Information

### uname

Displays operating system information.

```bash
uname
```

Example Output:

```bash
Linux
```

---

### uname -a

Displays detailed system information.

```bash
uname -a
```

Example Output:

```bash
Linux ubuntu 6.8.0 x86_64 GNU/Linux
```

Useful for identifying kernel versions.

---

## Display Logged-in Users

### who

Displays users currently logged into the system.

```bash
who
```

Example Output:

```bash
akshat tty1 2025-07-22 09:00
```

Useful for monitoring user activity.

---

## Display User Information

### id

Displays user and group information.

```bash
id
```

Example Output:

```bash
uid=1000(user) gid=1000(user) groups=1000(user)
```

Frequently used for permission analysis.

---

## View Command History

### history

Displays previously executed commands.

```bash
history
```

Example Output:

```bash
1 pwd
2 ls
3 cd Documents
```

Very useful during investigations.

---

## Display Manual Pages

### man

Displays documentation for commands.

```bash
man ls
```

Provides detailed command information.

---

## Command Help

### --help

Displays quick help information.

```bash
ls --help
```

Useful when learning new commands.

---

## Why These Commands Matter in Cybersecurity

Security professionals use these commands to:

* Identify users
* Determine system information
* Investigate incidents
* Analyze user activity
* Review command history
* Navigate forensic evidence

These commands form the foundation of Linux administration and security analysis.

---

## Interview Questions

### Q1. What command displays the current directory?

```bash
pwd
```

---

### Q2. What command displays the current user?

```bash
whoami
```

---

### Q3. How do you view hidden files?

```bash
ls -a
```

---

### Q4. What command displays system information?

```bash
uname -a
```

---

### Q5. How do you view command documentation?

```bash
man <command>
```

Example:

```bash
man ls
```

---

## Key Takeaways

✔ Linux commands are used to interact with the operating system.

✔ pwd displays the current directory.

✔ ls displays files and directories.

✔ cd changes directories.

✔ whoami identifies the logged-in user.

✔ uname displays operating system information.

✔ history helps review previously executed commands.

✔ These commands are essential for Linux administration and cybersecurity.
