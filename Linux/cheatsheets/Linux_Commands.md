# Linux Commands Cheat Sheet

## Navigation Commands

| Command | Description |
|----------|-------------|
| pwd | Show current directory |
| ls | List files and folders |
| ls -l | Long listing format |
| ls -la | Show hidden files |
| cd directory | Change directory |
| cd .. | Move one level up |
| cd ~ | Go to home directory |

---

## File Management Commands

| Command | Description |
|----------|-------------|
| touch file.txt | Create a file |
| mkdir folder | Create directory |
| rm file.txt | Delete file |
| rm -r folder | Delete directory |
| cp file1 file2 | Copy file |
| mv old new | Move/Rename file |

---

## File Viewing Commands

| Command | Description |
|----------|-------------|
| cat file.txt | Display file content |
| less file.txt | View large files |
| head file.txt | Show first 10 lines |
| tail file.txt | Show last 10 lines |
| tail -f file.txt | Monitor file in real time |

---

## System Information Commands

| Command | Description |
|----------|-------------|
| uname | Show kernel name |
| uname -a | Detailed system information |
| hostname | Show system hostname |
| whoami | Show current user |
| id | Display user and group IDs |
| uptime | Show system uptime |
| date | Display current date and time |

---

## Search Commands

| Command | Description |
|----------|-------------|
| find / -name file.txt | Search files |
| which command | Locate executable |
| whereis command | Locate binary and manuals |
| grep keyword file.txt | Search text in file |

---

## SOC Analyst Usage

- System enumeration
- Evidence collection
- User identification
- File investigation
- Initial incident response

---

## Quick Examples

```bash
pwd
ls -la
whoami
uname -a
find / -name passwords.txt
```
