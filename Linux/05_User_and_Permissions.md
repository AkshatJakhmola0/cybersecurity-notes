# Users and Permissions in Linux

## What are Users and Permissions?

Linux is a multi-user operating system, meaning multiple users can access the same system.

To protect files and system resources, Linux uses permissions and ownership controls.

These controls determine:

* Who can access files
* Who can modify files
* Who can execute programs
* Who can administer the system

---

## Why Are Permissions Important?

Without Permissions

Every user could:

* Read sensitive files
* Delete important data
* Modify system configurations
* Access confidential information

This would create major security risks.

With Permissions

Users only receive the access they need.

This helps:

* Protect sensitive data
* Prevent accidental damage
* Enforce security policies
* Reduce insider threats

---

## Real-World Example

Imagine a company server.

```text
System Administrator
        │
        ▼
   Full Access
        │
        ▼
 Regular Users
        │
        ▼
 Limited Access
```

Administrators can manage the system, while regular users can only access their own files.

---

## View Current User

### whoami

Displays the currently logged-in user.

```bash
whoami
```

Example Output:

```text
akshat
```

Useful during system administration and investigations.

---

## Display User Information

### id

Displays user ID (UID), group ID (GID), and group memberships.

```bash
id
```

Example Output:

```text
uid=1000(user) gid=1000(user) groups=1000(user)
```

---

## View Logged-in Users

### who

Displays currently logged-in users.

```bash
who
```

Example Output:

```text
user tty1 2025-07-22 10:00
```

Useful for monitoring system activity.

---

## User Accounts in Linux

User information is stored in:

```text
/etc/passwd
```

View file:

```bash
cat /etc/passwd
```

Each line represents one user account.

---

## View User Account Details

Example:

```text
akshat:x:1000:1000:Akshat:/home/akshat:/bin/bash
```

Meaning:

```text
Username
Password Placeholder
UID
GID
Description
Home Directory
Default Shell
```

---

## View Groups

Group information is stored in:

```text
/etc/group
```

View file:

```bash
cat /etc/group
```

Groups help manage permissions efficiently.

---

## Create a User

### useradd

Creates a new user account.

```bash
sudo useradd analyst
```

---

## Set User Password

### passwd

Assigns a password to a user.

```bash
sudo passwd analyst
```

---

## Delete a User

### userdel

Deletes a user account.

```bash
sudo userdel analyst
```

---

## Delete User and Home Directory

```bash
sudo userdel -r analyst
```

Removes user files as well.

---

## Create a Group

### groupadd

Creates a new group.

```bash
sudo groupadd SOC
```

---

## Add User to a Group

### usermod

```bash
sudo usermod -aG SOC analyst
```

Meaning:

* a = append
* G = group

---

## File Ownership

Every file has:

* Owner
* Group
* Permissions

View ownership:

```bash
ls -l
```

Example Output:

```text
-rw-r--r-- 1 akshat SOC 1200 report.txt
```

Meaning:

```text
Owner = akshat
Group = SOC
File = report.txt
```

---

## Change File Owner

### chown

Changes file ownership.

```bash
sudo chown analyst report.txt
```

---

## Change Owner and Group

```bash
sudo chown analyst:SOC report.txt
```

---

## Change Group Ownership

### chgrp

```bash
sudo chgrp SOC report.txt
```

Changes only the group.

---

## Linux Permission Types

Linux uses three permission types:

```text
r = Read
w = Write
x = Execute
```

---

## Permission Structure

Example:

```text
-rwxr-xr--
```

Breakdown:

```text
Owner  Group  Others
rwx    r-x    r--
```

Meaning:

Owner:

* Read
* Write
* Execute

Group:

* Read
* Execute

Others:

* Read

---

## View File Permissions

```bash
ls -l
```

Example:

```text
-rw-r--r-- 1 user user 100 notes.txt
```

---

## Change Permissions

### chmod

Changes file permissions.

```bash
chmod 755 script.sh
```

---

## Numeric Permission Values

```text
Read    = 4
Write   = 2
Execute = 1
```

Examples:

```text
7 = 4+2+1 = rwx
6 = 4+2   = rw-
5 = 4+1   = r-x
4 = 4     = r--
```

---

## Common Permission Values

### 777

```bash
chmod 777 file.txt
```

Permissions:

```text
rwxrwxrwx
```

Everyone has full access.

⚠ Not recommended.

---

### 755

```bash
chmod 755 script.sh
```

Permissions:

```text
rwxr-xr-x
```

Common for scripts and directories.

---

### 644

```bash
chmod 644 file.txt
```

Permissions:

```text
rw-r--r--
```

Common for files.

---

## Symbolic Permission Method

Add execute permission:

```bash
chmod +x script.sh
```

Remove write permission:

```bash
chmod -w file.txt
```

Add read permission:

```bash
chmod +r file.txt
```

---

## Sudo Privileges

### sudo

Allows a user to execute commands as administrator.

```bash
sudo apt update
```

Used extensively in Linux administration.

---

## View Sudo Users

```bash
getent group sudo
```

or

```bash
sudo cat /etc/sudoers
```

Displays users with elevated privileges.

---

## Why Users and Permissions Matter in Cybersecurity

Security professionals use user and permission management to:

* Prevent unauthorized access
* Protect sensitive data
* Enforce least privilege
* Investigate compromised accounts
* Detect privilege escalation
* Secure Linux systems

Poor permission management is one of the most common causes of security incidents.

---

## Interview Questions

### Q1. What command displays the current user?

```bash
whoami
```

---

### Q2. What command displays user and group information?

```bash
id
```

---

### Q3. What command changes file ownership?

```bash
chown
```

---

### Q4. What command changes permissions?

```bash
chmod
```

---

### Q5. What does permission 755 mean?

```text
Owner  = rwx
Group  = r-x
Others = r-x
```

---

### Q6. What does permission 644 mean?

```text
Owner  = rw-
Group  = r--
Others = r--
```

---

### Q7. What command adds execute permission?

```bash
chmod +x filename
```

---

### Q8. What is sudo?

sudo allows authorized users to execute commands with administrative privileges.

---

## Key Takeaways

✔ Linux supports multiple users.

✔ Every file has an owner and group.

✔ Permissions control access to files and directories.

✔ chmod changes permissions.

✔ chown changes ownership.

✔ sudo provides administrative access.

✔ Principle of Least Privilege is an important security concept.

✔ User and permission management is a critical cybersecurity skill.
