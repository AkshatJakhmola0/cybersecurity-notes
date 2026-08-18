# Lab 01 – Linux Installation and Navigation

## Objective

To become familiar with the Linux operating system by learning basic navigation commands, identifying system information, and exploring the Linux file system using the terminal.

---

## Prerequisites

* Linux System (Ubuntu, Kali Linux, Debian, etc.)
* Terminal Access
* Basic understanding of operating systems

---

## Theory

Linux is an open-source operating system widely used in servers, cloud environments, cybersecurity, and software development.

Before performing advanced administrative or security tasks, it is important to understand how to navigate the Linux file system and gather basic system information.

System administrators, SOC analysts, penetration testers, and incident responders frequently use Linux command-line tools to interact with systems efficiently.

---

## Commands Used

```bash
pwd

ls

ls -l

ls -la

cd

cd ..

cd ~

whoami

hostname

uname -a
```

---

## Lab Tasks

### 1. Display Current Directory

```bash
pwd
```

Displays the present working directory.

---

### 2. List Directory Contents

```bash
ls
```

Displays files and folders in the current directory.

---

### 3. View Detailed File Information

```bash
ls -l
```

Displays permissions, ownership, size, and timestamps.

---

### 4. Display Hidden Files

```bash
ls -la
```

Displays all files including hidden files.

---

### 5. Change Directory

```bash
cd
```

Moves between directories.

Examples:

```bash
cd Documents
cd ..
cd ~
```

---

### 6. Identify Current User

```bash
whoami
```

Displays the currently logged-in user.

---

### 7. Identify Hostname

```bash
hostname
```

Displays the system hostname.

---

### 8. View Kernel and System Information

```bash
uname -a
```

Displays kernel version, architecture, hostname, and operating system information.

---

## Investigation Workflow

1. Open the terminal.
2. Determine the current working directory.
3. View directory contents.
4. Display hidden files.
5. Navigate between directories.
6. Identify the current user.
7. Identify the system hostname.
8. Collect kernel information.
9. Document observations.
10. Create a lab report.

---

## Skills Gained

* Linux Navigation
* Terminal Usage
* Directory Traversal
* User Identification
* Host Identification
* Linux Enumeration
* Basic System Reconnaissance

---

## Cybersecurity Relevance

Linux is widely used in cybersecurity operations.

These commands are commonly used by:

* SOC Analysts
* Incident Responders
* Threat Hunters
* System Administrators
* Penetration Testers
* Digital Forensics Investigators

Understanding Linux navigation is essential before learning process analysis, networking, log analysis, scripting, and security monitoring.

---

## Expected Outcome

Successfully navigate the Linux file system, identify the active user and host, collect system information, and gain familiarity with basic Linux terminal operations.
