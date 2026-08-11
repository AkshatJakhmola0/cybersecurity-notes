# Linux Security Basics

## What is Linux Security?

Linux security refers to protecting Linux systems, users, files, processes, and network services from unauthorized access and malicious activity.

Linux provides security mechanisms for:

* User authentication
* File permissions
* Access control
* Process management
* Network security
* Software management
* Security monitoring

---

## Why is Linux Security Important?

Without Linux Security

* Unauthorized users may access systems.
* Sensitive files may be modified.
* Services may be exploited.
* Malware may damage systems.
* Attackers may gain persistent access.

With Linux Security

* Access can be controlled.
* Files can be protected.
* Services can be secured.
* Suspicious activity can be investigated.
* System compromise can be reduced.

---

## Linux Security Model

Linux security is based on several important concepts:

```text
User
 │
 ▼
Authentication
 │
 ▼
Authorization
 │
 ▼
File Permissions
 │
 ▼
Processes & Services
 │
 ▼
Network Security
````

---

## User Accounts

Linux systems use user accounts to control access.

### View Current User

```bash
whoami
```

Displays the username of the currently logged-in user.

---

### View User Information

```bash
id
```

Example:

```text
uid=1000(user) gid=1000(user) groups=1000(user)
```

Displays:

* User ID
* Group ID
* Group memberships

---

## Root User

The `root` user has administrative privileges.

Check current user:

```bash
whoami
```

Example:

```text
root
```

Root can:

* Modify system files
* Install software
* Manage users
* Start or stop services
* Change permissions

Using root privileges should be done carefully.

---

## sudo

`sudo` allows authorized users to execute commands with elevated privileges.

Example:

```bash
sudo apt update
```

Another example:

```bash
sudo systemctl restart ssh
```

Using `sudo` is generally safer than logging in directly as root.

---

## Managing Users

### useradd

Creates a new user.

```bash
sudo useradd username
```

---

### passwd

Changes a user's password.

```bash
sudo passwd username
```

---

### userdel

Deletes a user account.

```bash
sudo userdel username
```

---

## Managing Groups

### groupadd

Creates a new group.

```bash
sudo groupadd security
```

---

### usermod

Adds a user to a group.

```bash
sudo usermod -aG security username
```

Groups make it easier to manage access to files and resources.

---

## File Permissions

Linux uses permissions to control access to files and directories.

Example:

```text
-rwxr-xr--
```

Permissions are divided into:

```text
User    Group    Others
rwx     r-x      r--
```

---

## Permission Types

| Permission | Meaning | Value |
| ---------- | ------- | ----- |
| `r`        | Read    | 4     |
| `w`        | Write   | 2     |
| `x`        | Execute | 1     |

Example:

```text
rwx = 4 + 2 + 1 = 7
r-x = 4 + 0 + 1 = 5
r-- = 4 + 0 + 0 = 4
```

Therefore:

```text
754
```

means:

```text
Owner  = 7
Group  = 5
Others = 4
```

---

## Viewing File Permissions

### ls -l

```bash
ls -l
```

Example:

```text
-rwxr-xr-- 1 user security 1200 script.sh
```

Displays:

* File type
* Permissions
* Owner
* Group
* File size
* Filename

---

## Changing Permissions

### chmod

Changes file permissions.

Example:

```bash
chmod 755 script.sh
```

Another example:

```bash
chmod 600 secret.txt
```

`600` allows the owner to read and write while denying access to group and others.

---

## Changing File Ownership

### chown

Changes the owner of a file.

```bash
sudo chown user file.txt
```

Change owner and group:

```bash
sudo chown user:security file.txt
```

---

### chgrp

Changes the group ownership.

```bash
sudo chgrp security file.txt
```

---

## Special Permissions

Linux also provides special permission mechanisms.

### SUID

Allows a program to execute with the privileges of its file owner.

Example:

```text
-rwsr-xr-x
```

SUID should be monitored because misconfigured SUID files can create security risks.

---

### SGID

Allows programs or directories to use group ownership behavior.

Example:

```text
drwxr-sr-x
```

---

### Sticky Bit

Commonly used on shared directories.

Example:

```text
drwxrwxrwt
```

The `/tmp` directory commonly uses the sticky bit.

---

## Finding SUID Files

SUID files can be searched using:

```bash
find / -perm -4000 -type f 2>/dev/null
```

Useful during security assessments and investigations.

---

## Checking Running Services

### systemctl

Used to manage system services.

View service status:

```bash
systemctl status ssh
```

Start a service:

```bash
sudo systemctl start ssh
```

Stop a service:

```bash
sudo systemctl stop ssh
```

Enable a service at boot:

```bash
sudo systemctl enable ssh
```

---

## Checking Firewall

### ufw

UFW is a simple firewall management tool.

Check firewall status:

```bash
sudo ufw status
```

Enable firewall:

```bash
sudo ufw enable
```

Allow SSH:

```bash
sudo ufw allow 22
```

Firewalls help control network access to Linux systems.

---

## Secure SSH

SSH provides encrypted remote administration.

Example:

```bash
ssh user@192.168.1.100
```

Basic SSH security practices:

* Use strong authentication.
* Disable unnecessary accounts.
* Avoid direct root login.
* Use SSH keys where appropriate.
* Restrict unnecessary network access.
* Monitor SSH login activity.

---

## File Security

Sensitive files should have appropriate permissions.

Examples:

```bash
ls -l /etc/passwd
```

```bash
ls -l /etc/shadow
```

`/etc/shadow` contains password-related authentication information and should have restricted access.

---

## Checking Login Information

### last

Displays previous login sessions.

```bash
last
```

Useful for:

* Investigating user activity
* Detecting unexpected logins
* Security investigations

---

### who

Displays currently logged-in users.

```bash
who
```

---

## Checking Failed Logins

### lastb

Displays failed login attempts.

```bash
sudo lastb
```

Useful for detecting possible brute-force attacks.

---

## Security Updates

Keeping software updated is an important security practice.

On Debian/Ubuntu:

```bash
sudo apt update
```

Upgrade installed packages:

```bash
sudo apt upgrade
```

Security updates can fix known vulnerabilities.

---

## Checking Installed Packages

### dpkg

Lists installed Debian packages.

```bash
dpkg -l
```

Search for a specific package:

```bash
dpkg -l | grep ssh
```

Useful for identifying installed software.

---

## Linux Security for Cybersecurity

Linux security concepts are important for:

* SOC Analysts
* Penetration Testers
* Incident Responders
* Security Engineers
* System Administrators

Security professionals may investigate:

```text
User Accounts
      │
      ▼
File Permissions
      │
      ▼
Running Processes
      │
      ▼
Services
      │
      ▼
Network Access
      │
      ▼
Logs
```

---

## Common SOC Security Commands

Check current user:

```bash
whoami
```

Check user information:

```bash
id
```

Check file permissions:

```bash
ls -l
```

Find SUID files:

```bash
find / -perm -4000 -type f 2>/dev/null
```

Check services:

```bash
systemctl status ssh
```

Check firewall:

```bash
sudo ufw status
```

Check login history:

```bash
last
```

Check failed logins:

```bash
sudo lastb
```

Check running processes:

```bash
ps aux
```

---

## Important Linux Security Commands

| Command     | Purpose                          |
| ----------- | -------------------------------- |
| `whoami`    | Current user                     |
| `id`        | User and group information       |
| `sudo`      | Execute commands with privileges |
| `ls -l`     | View permissions                 |
| `chmod`     | Change permissions               |
| `chown`     | Change ownership                 |
| `useradd`   | Create users                     |
| `usermod`   | Modify users                     |
| `passwd`    | Change passwords                 |
| `systemctl` | Manage services                  |
| `ufw`       | Manage firewall                  |
| `last`      | View login history               |
| `lastb`     | View failed logins               |
| `find`      | Search for files and SUID files  |

---

## Why Linux Security Matters in Cybersecurity

Cybersecurity professionals use Linux security concepts to:

* Control user access
* Protect sensitive files
* Investigate unauthorized access
* Detect suspicious accounts
* Identify risky permissions
* Monitor services
* Secure remote access
* Investigate brute-force attacks

Understanding Linux security is essential for **SOC Analysts, Incident Responders, Penetration Testers, and Security Engineers**.

---

## Interview Questions

### Q1. What is the root user?

The root user is the Linux superuser with extensive administrative privileges.

---

### Q2. What does sudo do?

`sudo` allows an authorized user to execute commands with elevated privileges.

---

### Q3. What does chmod do?

`chmod` changes the permissions of files and directories.

---

### Q4. What does chown do?

`chown` changes the owner and optionally the group of a file or directory.

---

### Q5. What do r, w, and x mean?

```text
r = Read
w = Write
x = Execute
```

---

### Q6. What does chmod 755 mean?

```text
Owner  = Read + Write + Execute
Group  = Read + Execute
Others = Read + Execute
```

---

### Q7. What is SUID?

SUID allows a program to execute with the privileges of its file owner.

---

### Q8. Which command checks currently logged-in users?

```bash
who
```

---

### Q9. Which command shows previous login sessions?

```bash
last
```

---

### Q10. Which command shows failed login attempts?

```bash
sudo lastb
```

---

### Q11. Which command manages Linux services?

```bash
systemctl
```

---

### Q12. Why is file permission important?

File permissions prevent unauthorized users from reading, modifying, or executing sensitive files.

---

## Key Takeaways

✔ Linux uses users and groups to control access.

✔ `root` is the Linux superuser.

✔ `sudo` provides controlled administrative privileges.

✔ `ls -l` displays file permissions.

✔ `chmod` changes permissions.

✔ `chown` changes file ownership.

✔ SUID, SGID, and Sticky Bit provide special permissions.

✔ `systemctl` manages services.

✔ `ufw` provides simple firewall management.

✔ `last` and `lastb` help investigate login activity.

✔ Regular security updates help protect against known vulnerabilities.

✔ Linux security knowledge is essential for cybersecurity professionals.

