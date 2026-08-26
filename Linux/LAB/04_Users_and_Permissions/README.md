# Lab 04 – Users and Permissions

## Objective

To understand how Linux manages users, groups, file ownership, and permissions. Learn how to create users, manage groups, assign ownership, and control access to files and directories.

---

## Prerequisites

- Kali Linux / Ubuntu
- Terminal Access
- Sudo Privileges

---

## Theory

Linux is a multi-user operating system where multiple users can access the same system. To maintain security, Linux uses users, groups, ownership, and permissions.

Every file and directory has:

- An Owner
- A Group
- Permission Settings

Permissions determine who can:

- Read a file
- Write to a file
- Execute a file

Proper permission management is critical for Linux administration and cybersecurity.

---

## Commands Used

```bash
whoami

id

groups

cat /etc/passwd

cat /etc/group

sudo useradd testuser

sudo passwd testuser

sudo groupadd analysts

sudo usermod -aG analysts testuser

ls -l

chmod 755 file.txt

chmod 644 file.txt

chmod +x script.sh

sudo chown testuser file.txt

sudo chgrp analysts file.txt

sudo userdel testuser
```

---

## User Enumeration

### Current User

```bash
whoami
```

Displays the currently logged-in user.

---

### User Information

```bash
id
```

Displays:

- User ID (UID)
- Group ID (GID)
- Group Memberships

---

### Group Membership

```bash
groups
```

Displays groups assigned to the current user.

---

## User Management

### Create User

```bash
sudo useradd testuser
```

Creates a new user account.

---

### Set Password

```bash
sudo passwd testuser
```

Assigns a password to the user.

---

### Delete User

```bash
sudo userdel testuser
```

Removes a user account.

---

## Group Management

### Create Group

```bash
sudo groupadd analysts
```

Creates a new group.

---

### Add User to Group

```bash
sudo usermod -aG analysts testuser
```

Adds a user to an existing group.

---

### View Local Groups

```bash
cat /etc/group
```

Displays configured groups.

---

## File Ownership

### View Ownership

```bash
ls -l
```

Displays file owner and group information.

---

### Change Owner

```bash
sudo chown testuser file.txt
```

Changes file ownership.

---

### Change Group

```bash
sudo chgrp analysts file.txt
```

Changes the group assigned to a file.

---

## File Permissions

### View Permissions

```bash
ls -l
```

Example:

```text
-rwxr-xr-x file.txt
```

---

### Numeric Permissions

```bash
chmod 755 file.txt
```

```text
Owner  = rwx = 7
Group  = r-x = 5
Others = r-x = 5
```

---

### Common Permission Values

```text
777 = rwxrwxrwx
755 = rwxr-xr-x
700 = rwx------
644 = rw-r--r--
600 = rw-------
```

---

### Make Script Executable

```bash
chmod +x script.sh
```

Adds execute permission to a file.

---

## Investigation Workflow

1. Identify the current user.
2. Review user and group information.
3. Enumerate local users.
4. Enumerate local groups.
5. Create a test user.
6. Create a test group.
7. Add the user to the group.
8. Review file ownership.
9. Modify file permissions.
10. Verify permission changes.

---

## Skills Gained

- Linux User Management
- Group Management
- File Ownership Management
- Permission Management
- Access Control
- Linux Administration
- Linux Security Fundamentals

---

## Cybersecurity Relevance

Understanding Linux permissions is essential for:

- SOC Analysts
- Security Engineers
- Linux Administrators
- Incident Responders
- Threat Hunters

Improper permissions can lead to privilege escalation, unauthorized access, and security incidents.

---
