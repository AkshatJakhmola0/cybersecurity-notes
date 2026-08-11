# Linux for SOC Analysts

## What is Linux for SOC Analysts?

Linux is widely used in cybersecurity and SOC environments for investigating systems, analyzing logs, monitoring processes, and examining network activity.

SOC Analysts use Linux to:

* Investigate security alerts
* Analyze authentication activity
* Monitor processes
* Investigate network connections
* Search logs
* Identify suspicious files
* Collect investigation evidence

---

## Why Linux is Important in SOC

Linux provides powerful command-line tools that allow analysts to quickly investigate suspicious activity.

A typical investigation may follow:

```text
Security Alert
      │
      ▼
Identify User
      │
      ▼
Check Login Activity
      │
      ▼
Analyze Logs
      │
      ▼
Check Processes
      │
      ▼
Check Network Connections
      │
      ▼
Check Files & Services
      │
      ▼
Document Findings
````

---

## Basic SOC Investigation Commands

### Identify the User

```bash
whoami
```

```bash
id
```

```bash
who
```

Useful for identifying the current user and active sessions.

---

### Check Login Activity

View previous logins:

```bash
last
```

View failed login attempts:

```bash
sudo lastb
```

Useful for identifying suspicious or unexpected login activity.

---

### Investigate Authentication Logs

On Debian/Ubuntu systems:

```bash
sudo grep "Failed password" /var/log/auth.log
```

Find successful SSH logins:

```bash
sudo grep "Accepted" /var/log/auth.log
```

These commands can help identify possible brute-force attacks or unauthorized access.

---

## Investigating Processes

View running processes:

```bash
ps aux
```

Monitor processes in real time:

```bash
top
```

Find a specific process:

```bash
pgrep process_name
```

SOC Analysts should look for:

* Unknown processes
* Suspicious process names
* Unexpected users
* High CPU usage
* Unusual parent-child relationships

---

## Investigating Network Activity

View active connections:

```bash
ss -tunap
```

View network interfaces:

```bash
ip addr
```

View routing information:

```bash
ip route
```

Investigate DNS:

```bash
dig example.com
```

Look for:

* Unknown remote connections
* Unexpected listening ports
* Suspicious destinations
* Unusual network activity

---

## Investigating Files

List files with permissions:

```bash
ls -l
```

Find recently modified files:

```bash
find /tmp -type f -mtime -1
```

Find executable files:

```bash
find /tmp -type f -perm /111
```

These commands can help identify potentially suspicious files.

---

## Investigating Services

View running services:

```bash
systemctl --type=service --state=running
```

Check a specific service:

```bash
systemctl status ssh
```

Unexpected services may require further investigation.

---

## Checking Scheduled Tasks

Cron jobs can be used for legitimate automation or persistence.

View current user's cron jobs:

```bash
crontab -l
```

During an investigation, look for:

* Unknown commands
* Suspicious scripts
* Unexpected execution times
* Commands running from unusual locations

---

## Investigating System Logs

View systemd logs:

```bash
journalctl
```

View recent logs:

```bash
journalctl -n 50
```

View errors:

```bash
journalctl -p err
```

Monitor logs in real time:

```bash
tail -f /var/log/auth.log
```

---

## Example SOC Investigation

Suppose a server generates an alert for a suspicious SSH login.

### Step 1 — Check Login History

```bash
last
```

### Step 2 — Check Failed Logins

```bash
sudo lastb
```

### Step 3 — Analyze Authentication Logs

```bash
sudo grep "Failed password" /var/log/auth.log
```

### Step 4 — Check Running Processes

```bash
ps aux
```

### Step 5 — Check Network Connections

```bash
ss -tunap
```

### Step 6 — Check Scheduled Tasks

```bash
crontab -l
```

### Step 7 — Check Suspicious Files

```bash
find /tmp -type f -mtime -1
```

The analyst then correlates the findings and determines whether the activity is legitimate or suspicious.

---

## Linux SOC Investigation Workflow

```text
Alert
 │
 ├── User
 │    └── whoami / id / who
 │
 ├── Authentication
 │    └── last / lastb / auth.log
 │
 ├── Processes
 │    └── ps / top
 │
 ├── Network
 │    └── ss / ip / dig
 │
 ├── Files
 │    └── ls / find
 │
 └── Persistence
      └── systemctl / crontab
```

---

## Common SOC Commands

| Command      | Purpose              |
| ------------ | -------------------- |
| `whoami`     | Current user         |
| `who`        | Logged-in users      |
| `last`       | Login history        |
| `lastb`      | Failed logins        |
| `ps aux`     | Running processes    |
| `top`        | Process monitoring   |
| `ss -tunap`  | Network connections  |
| `ip addr`    | IP configuration     |
| `grep`       | Search logs          |
| `journalctl` | System logs          |
| `find`       | Search files         |
| `systemctl`  | Manage services      |
| `crontab -l` | View scheduled tasks |

---

## Why Linux Matters in SOC

Linux skills help SOC Analysts:

* Investigate alerts
* Detect suspicious logins
* Analyze processes
* Investigate network activity
* Search security logs
* Identify suspicious files
* Detect persistence mechanisms
* Support incident response

Linux command-line knowledge is an important skill for **SOC Analysts, Incident Responders, and Threat Hunters**.

---

## Interview Questions

### Q1. Why is Linux important for SOC Analysts?

Linux provides powerful tools for log analysis, process monitoring, network investigation, and incident response.

---

### Q2. Which command shows running processes?

```bash
ps aux
```

---

### Q3. Which command shows active network connections?

```bash
ss -tunap
```

---

### Q4. How can you find failed SSH logins?

```bash
sudo grep "Failed password" /var/log/auth.log
```

---

### Q5. Which command shows login history?

```bash
last
```

---

### Q6. Which command shows failed login attempts?

```bash
sudo lastb
```

---

### Q7. Which command is used to view systemd logs?

```bash
journalctl
```

---

### Q8. How can you check scheduled cron jobs?

```bash
crontab -l
```

---

### Q9. Why should SOC Analysts monitor processes?

To identify unknown, unauthorized, or potentially malicious programs running on a system.

---

### Q10. What should an analyst check after detecting a suspicious login?

The analyst should investigate the user, source IP, authentication logs, running processes, network connections, files, services, and possible persistence mechanisms.

---

## Key Takeaways

✔ Linux is an important platform for SOC investigations.

✔ Authentication logs help investigate suspicious logins.

✔ `ps` and `top` help investigate processes.

✔ `ss` helps investigate network connections.

✔ `grep` and `journalctl` help analyze logs.

✔ `find` helps locate suspicious files.

✔ `systemctl` helps investigate services.

✔ `crontab` helps identify scheduled tasks.

✔ SOC investigations require correlating multiple sources of evidence.

✔ Linux command-line skills are essential for effective SOC analysis.
