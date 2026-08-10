# Linux File System

## What is the Linux File System?

The Linux File System is the way Linux organizes and stores files and directories.

Unlike Windows, Linux does not use drive letters such as C:\ or D:.

Everything in Linux starts from a single root directory called:

```bash
/
```

All files, folders, devices, and storage locations exist under this root directory.

---

## Why Do We Need a File System?

Without a File System

The operating system would not know:

* Where files are stored
* How files are organized
* How applications access data
* How permissions are managed

Finding and managing data would become extremely difficult.

With a File System

Linux can:

* Organize files efficiently
* Control access permissions
* Manage storage devices
* Locate system resources quickly

---

## Real-World Example

Think of the Linux file system as a tree.

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── opt
├── root
├── tmp
├── usr
└── var
```

The root directory (/) is the top of the tree, and all other directories branch from it.

---

## Why is the Linux File System Important in Cybersecurity?

A cybersecurity professional frequently investigates files and directories to:

* Analyze logs
* Detect malware
* Review user activity
* Investigate incidents
* Find persistence mechanisms
* Audit system configurations

Understanding the Linux file system is essential during incident response and forensic investigations.

---

## Important Linux Directories

### Root Directory (/)

The top-level directory of the Linux file system.

```bash
/
```

Everything begins here.

---

### Binary Files (/bin)

Contains essential user commands.

Examples:

```bash
/bin/ls
/bin/cat
/bin/cp
```

These commands are required for normal system operation.

---

### Boot Files (/boot)

Contains files needed during system startup.

Examples:

* Linux kernel
* Bootloader files

---

### Device Files (/dev)

Contains representations of hardware devices.

Examples:

```bash
/dev/sda
/dev/null
/dev/tty
```

Linux treats devices as files.

---

### Configuration Files (/etc)

Stores system configuration files.

Examples:

```bash
/etc/passwd
/etc/shadow
/etc/hosts
```

Security analysts frequently investigate this directory.

---

### User Home Directories (/home)

Stores personal files for normal users.

Example:

```bash
/home/akshat
```

Each user typically has a separate home directory.

---

### Root User Home (/root)

Home directory of the root administrator account.

```bash
/root
```

Different from the root directory (/).

---

### Temporary Files (/tmp)

Stores temporary files created by applications.

Example:

```bash
/tmp
```

Files may be deleted automatically after reboot.

---

### User Programs (/usr)

Contains installed software, libraries, and utilities.

Examples:

```bash
/usr/bin
/usr/lib
/usr/share
```

Many application files reside here.

---

### Variable Data (/var)

Stores data that changes frequently.

Examples:

```bash
/var/log
/var/mail
/var/spool
```

This directory is extremely important during investigations.

---

## Important Security Directories

### Log Files

```bash
/var/log
```

Contains:

* Authentication logs
* System logs
* Service logs
* Security logs

---

### User Information

```bash
/etc/passwd
```

Contains user account information.

---

### Password Information

```bash
/etc/shadow
```

Contains password hashes.

Accessible only by privileged users.

---

## File Path Types

### Absolute Path

Starts from the root directory.

Example:

```bash
/home/user/Documents/report.txt
```

Absolute paths always begin with:

```bash
/
```

---

### Relative Path

Starts from the current directory.

Example:

```bash
Documents/report.txt
```

Relative paths do not start with /.

---

## Linux vs Windows File Structure

### Linux

```bash
/home/user/file.txt
```

### Windows

```text
C:\Users\User\file.txt
```

Linux uses:

```bash
/
```

Windows uses:

```text
\
```

---

## Interview Questions

### Q1. What is the root directory in Linux?

The root directory (/) is the top-level directory from which all other directories originate.

---

### Q2. Which directory stores user home folders?

```bash
/home
```

stores home directories for regular users.

---

### Q3. Where are Linux log files commonly stored?

```bash
/var/log
```

contains most system and security logs.

---

### Q4. What is the difference between / and /root?

* `/` is the root of the file system.
* `/root` is the home directory of the root user.

---

## Key Takeaways

✔ Linux uses a hierarchical file system structure.

✔ Everything starts from the root directory (/).

✔ Important directories include /etc, /home, /usr, and /var.

✔ Security analysts frequently investigate /etc and /var/log.

✔ Understanding the Linux file system is essential for administration, incident response, and cybersecurity.
