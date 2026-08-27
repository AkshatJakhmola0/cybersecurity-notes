# Lab Report – Users and Permissions

## Lab Title

Users and Permissions in Linux

---

## Aim

To understand how Linux manages users, groups, file ownership, permissions, privilege delegation, and special permissions.

---

## Tools Used

- Kali Linux
- Terminal
- Linux User Management Utilities

---

## Commands Performed

### User Enumeration

```bash
whoami
id
who
w
```

### User Information Files

```bash
cat /etc/passwd
sudo cat /etc/shadow
```

### User Management

```bash
sudo useradd testuser
sudo passwd testuser
sudo userdel testuser
```

### Group Management

```bash
sudo groupadd security
sudo usermod -aG security analyst
groups analyst
```

### Ownership Management

```bash
touch file.txt
sudo chown kali:kali file.txt
sudo chgrp security file.txt
```

### Permission Management

```bash
chmod u+x file.txt
chmod g+w file.txt
chmod o-r file.txt

chmod 777 file.txt
chmod 755 file.txt
chmod 644 file.txt
chmod 600 file.txt
```

### Directory Permissions

```bash
mkdir testdir
ls -ld testdir
```

### Sudo Privileges

```bash
sudo -l
```

### Umask

```bash
umask
umask 022
```

### SUID Enumeration

```bash
find / -perm -4000 2>/dev/null
```

### World Writable Files

```bash
find / -perm -002 2>/dev/null
```

---

## Results

### User Management

Successfully created and removed user accounts.

### Group Management

Successfully created security group and added analyst user.

### Ownership Management

File ownership and group ownership changed successfully.

### Permission Management

Permissions modified using symbolic and numeric methods.

### Privilege Verification

Confirmed sudo access for user kali.

### SUID Discovery

Identified multiple SUID-enabled binaries including:

```bash
sudo
passwd
su
mount
pkexec
```

### World Writable Files

Identified writable directories including:

```bash
/ tmp
/run/shm
/run/lock
```

---

## Security Relevance

Understanding Linux permissions is essential for:

- System administration
- Access control
- Privilege management
- Incident response
- Privilege escalation assessment
- Security hardening

Misconfigured permissions may expose systems to unauthorized access and privilege escalation attacks.

---
