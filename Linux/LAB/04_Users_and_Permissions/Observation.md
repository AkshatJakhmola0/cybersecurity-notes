# Lab Observations – Users and Permissions

## Objective

To understand Linux user management, group management, file ownership, permissions, sudo privileges, umask settings, and privilege escalation related files.

---

## User Identification

### whoami

Output:

```bash
kali
```

Observation:
Displays the currently logged-in user.

---

### id

Output:

```bash
uid=1000(kali) gid=1000(kali)
```

Observation:
Shows User ID (UID), Group ID (GID), and all groups the user belongs to.

---

### who

Output:

```bash
kali seat0
```

Observation:
Displays currently logged-in users.

---

### w

Observation:
Shows logged-in users along with system uptime, load average, and running processes.

---

## User Information Files

### /etc/passwd

Observation:
Contains user account information such as username, UID, GID, home directory, and login shell.

Example:

```bash
kali:x:1000:1000::/home/kali:/usr/bin/zsh
```

---

### /etc/shadow

Observation:
Contains encrypted password hashes and password aging information.

Access requires root privileges.

---

## User Management

### Creating User

```bash
sudo useradd testuser
```

Observation:
Successfully created a new user account.

---

### Setting Password

```bash
sudo passwd testuser
```

Observation:
Password assigned successfully.

---

### Deleting User

```bash
sudo userdel testuser
```

Observation:
User account removed successfully.

---

## Group Management

### Create Group

```bash
sudo groupadd security
```

Observation:
New group named security was created.

---

### Add User to Group

```bash
sudo usermod -aG security analyst
```

Observation:
User analyst became a member of security group.

---

### Verify Membership

```bash
groups analyst
```

Output:

```bash
analyst : analyst security
```

Observation:
User belongs to both analyst and security groups.

---

## File Ownership

### chown

Initial attempt failed because file did not exist.

After creating file:

```bash
touch file.txt
sudo chown kali:kali file.txt
```

Observation:
Ownership changed successfully.

---

### chgrp

```bash
sudo chgrp security file.txt
```

Observation:
Group ownership changed successfully.

---

## File Permissions

### Symbolic Mode

Commands executed:

```bash
chmod u+x file.txt
chmod g+w file.txt
chmod o-r file.txt
```

Observation:
Permissions modified successfully using symbolic notation.

---

### Numeric Mode

Commands executed:

```bash
chmod 777 file.txt
chmod 755 file.txt
chmod 644 file.txt
chmod 600 file.txt
```

Observation:
Permissions changed successfully using octal values.

---

## Directory Permissions

### Create Directory

```bash
mkdir testdir
```

Output:

```bash
drwxrwxr-x
```

Observation:
Directory received default permissions based on current umask.

---

## Sudo Privileges

### sudo -l

Observation:
User kali can execute all commands as root.

```bash
(ALL : ALL) ALL
```

---

## Umask

### Current Value

```bash
umask
```

Output:

```bash
002
```

Observation:
New files and directories inherit permissions based on this mask.

---

### Change Umask

```bash
umask 022
```

Observation:
Future files will be more restrictive.

---

## SUID Files

### Command

```bash
find / -perm -4000 2>/dev/null
```

Observation:
Several binaries such as sudo, passwd, su, and mount have SUID permissions.

These programs run with owner privileges (root).

---

## World Writable Files

### Command

```bash
find / -perm -002 2>/dev/null
```

Observation:
Numerous world-writable locations were identified, including:

```bash
/tmp
/run/shm
/run/lock
```

These locations require monitoring because improper permissions may lead to privilege escalation opportunities.

---
