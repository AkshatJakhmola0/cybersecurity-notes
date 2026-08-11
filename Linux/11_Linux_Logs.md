# Linux Logs

## What are Linux Logs?

Linux logs are records of system, application, authentication, and security-related events.

Logs help administrators and security professionals:

* Troubleshoot problems
* Monitor system activity
* Investigate security incidents
* Detect suspicious behavior
* Track user activity
* Analyze system events

---

## Why are Linux Logs Important?

Without Logs

* Security events may be difficult to investigate.
* Failed login attempts may go unnoticed.
* System errors may be difficult to troubleshoot.
* Attack activity may leave little evidence.

With Logs

* Events can be investigated.
* User activity can be tracked.
* Failed authentication can be identified.
* Suspicious behavior can be detected.
* Security incidents can be reconstructed.

---

## Linux Logging Structure

Linux commonly stores traditional log files in:

```bash
/var/log
````

View the directory:

```bash
ls -lah /var/log
```

Example:

```text
auth.log
syslog
kern.log
dmesg
apt
```

The exact files can vary between Linux distributions.

---

## Common Linux Log Files

| Log File            | Purpose                         |
| ------------------- | ------------------------------- |
| `/var/log/syslog`   | General system activity         |
| `/var/log/auth.log` | Authentication and login events |
| `/var/log/kern.log` | Kernel messages                 |
| `/var/log/dmesg`    | Kernel and hardware messages    |
| `/var/log/boot.log` | Boot-related messages           |
| `/var/log/cron`     | Cron job activity               |
| `/var/log/apt/`     | Package management activity     |

Some distributions use different log locations or rely heavily on `systemd-journald`.

---

## Viewing Logs

### cat

Displays the contents of a log file.

```bash
cat /var/log/syslog
```

Useful for viewing smaller files.

---

### less

Allows logs to be viewed page by page.

```bash
less /var/log/syslog
```

Useful when working with large log files.

---

### tail

Displays the last lines of a file.

```bash
tail /var/log/syslog
```

Display the last 50 lines:

```bash
tail -n 50 /var/log/syslog
```

---

### head

Displays the first lines of a file.

```bash
head /var/log/syslog
```

---

## Monitoring Logs in Real Time

### tail -f

Continuously displays new log entries.

```bash
tail -f /var/log/syslog
```

Useful for:

* Monitoring applications
* Troubleshooting
* Incident response
* Watching security events

Stop with:

```text
Ctrl + C
```

---

## Authentication Logs

Authentication logs contain information about login and authentication events.

On Debian/Ubuntu:

```bash
/var/log/auth.log
```

View the log:

```bash
sudo less /var/log/auth.log
```

Useful for investigating:

* Successful logins
* Failed logins
* SSH activity
* sudo usage
* Authentication failures

---

## Searching Logs with grep

### grep

Searches for specific text.

Find failed login attempts:

```bash
sudo grep "Failed password" /var/log/auth.log
```

Find successful SSH logins:

```bash
sudo grep "Accepted" /var/log/auth.log
```

Search for SSH activity:

```bash
sudo grep "sshd" /var/log/auth.log
```

---

## Counting Failed Login Attempts

Count failed SSH password attempts:

```bash
sudo grep -c "Failed password" /var/log/auth.log
```

This can help identify possible brute-force activity.

---

## Finding Login Attempts from an IP

Example:

```bash
sudo grep "192.168.1.50" /var/log/auth.log
```

Useful for investigating activity associated with a specific IP address.

---

## System Logs

### syslog

On systems using traditional syslog logging:

```bash
sudo less /var/log/syslog
```

May contain:

* Service events
* System events
* Application messages
* Network events
* Errors

---

## Kernel Logs

### dmesg

Displays kernel messages.

```bash
dmesg
```

Useful for investigating:

* Hardware problems
* Device events
* Kernel errors
* Driver issues

View recent messages:

```bash
dmesg | tail
```

---

## systemd Journal

Modern Linux distributions commonly use `systemd-journald`.

### journalctl

Used to view systemd logs.

```bash
journalctl
```

View recent logs:

```bash
journalctl -n 50
```

Follow logs in real time:

```bash
journalctl -f
```

---

## Viewing Logs for a Service

Use `journalctl` with a service name.

Example:

```bash
journalctl -u ssh
```

View recent SSH logs:

```bash
journalctl -u ssh -n 50
```

Useful for investigating service-related problems.

---

## Viewing Logs by Time

Show logs from today:

```bash
journalctl --since today
```

Show logs from the last hour:

```bash
journalctl --since "1 hour ago"
```

Useful during incident investigations.

---

## Viewing Errors

Display error-level messages:

```bash
journalctl -p err
```

Useful for identifying system errors.

---

## Checking Boot Logs

View messages from the current boot:

```bash
journalctl -b
```

Useful for investigating startup problems.

---

## Log Rotation

Linux systems generate large amounts of log data.

**Log rotation** prevents logs from consuming excessive disk space.

Common tool:

```bash
logrotate
```

Configuration is commonly found in:

```bash
/etc/logrotate.conf
```

and:

```bash
/etc/logrotate.d/
```

---

## Finding Large Log Files

Check disk usage:

```bash
du -sh /var/log/*
```

Useful when a system is running out of disk space.

---

## Log Analysis with grep

Search for errors:

```bash
grep -i "error" /var/log/syslog
```

Search for warnings:

```bash
grep -i "warning" /var/log/syslog
```

Search for SSH events:

```bash
grep -i "ssh" /var/log/auth.log
```

The `-i` option makes the search case-insensitive.

---

## Combining Commands

Linux commands can be combined using pipes.

Example:

```bash
grep "Failed password" /var/log/auth.log | tail
```

This searches for failed passwords and displays the latest results.

Count failed attempts:

```bash
grep -c "Failed password" /var/log/auth.log
```

---

## Linux Logs and Cybersecurity

Logs are extremely important during security investigations.

Example:

```text
Suspicious Login
      │
      ▼
Check Authentication Logs
      │
      ▼
Identify Source IP
      │
      ▼
Check Username
      │
      ▼
Check Login Time
      │
      ▼
Investigate Activity
```

Logs can help identify:

* Brute-force attacks
* Unauthorized logins
* Suspicious sudo usage
* Malware activity
* Service failures
* Privilege escalation attempts

---

## Common SOC Investigation Commands

View authentication logs:

```bash
sudo less /var/log/auth.log
```

Find failed passwords:

```bash
sudo grep "Failed password" /var/log/auth.log
```

Find successful SSH logins:

```bash
sudo grep "Accepted" /var/log/auth.log
```

Monitor logs:

```bash
tail -f /var/log/syslog
```

View systemd logs:

```bash
journalctl
```

View SSH logs:

```bash
journalctl -u ssh
```

View recent logs:

```bash
journalctl -n 50
```

View errors:

```bash
journalctl -p err
```

View current boot logs:

```bash
journalctl -b
```

---

## Important Linux Log Commands

| Command      | Purpose                  |
| ------------ | ------------------------ |
| `cat`        | Display file contents    |
| `less`       | View files page by page  |
| `head`       | Show beginning of a file |
| `tail`       | Show end of a file       |
| `tail -f`    | Monitor new log entries  |
| `grep`       | Search log content       |
| `dmesg`      | View kernel messages     |
| `journalctl` | View systemd logs        |
| `logrotate`  | Manage log rotation      |
| `du`         | Check log disk usage     |

---

## Why Linux Logs Matter in Cybersecurity

Cybersecurity professionals use Linux logs to:

* Investigate security incidents
* Detect brute-force attacks
* Analyze authentication activity
* Identify suspicious IP addresses
* Investigate privilege escalation
* Monitor system services
* Reconstruct attacker activity
* Support digital forensics

Log analysis is a fundamental skill for **SOC Analysts, Incident Responders, Threat Hunters, and Security Engineers**.

---

## Interview Questions

### Q1. Where are Linux logs commonly stored?

```text
/var/log
```

---

### Q2. Which log contains authentication events on Ubuntu?

```text
/var/log/auth.log
```

---

### Q3. Which command searches text inside logs?

```bash
grep
```

---

### Q4. How can you monitor a log file in real time?

```bash
tail -f /var/log/syslog
```

---

### Q5. What is journalctl?

`journalctl` is used to view and analyze logs collected by `systemd-journald`.

---

### Q6. How can you view SSH service logs?

```bash
journalctl -u ssh
```

---

### Q7. How can you find failed SSH login attempts?

```bash
grep "Failed password" /var/log/auth.log
```

---

### Q8. What does dmesg display?

`dmesg` displays messages from the Linux kernel, including hardware and device-related events.

---

### Q9. What is log rotation?

Log rotation manages old log files to prevent logs from consuming excessive disk space.

---

### Q10. Why are logs important in cybersecurity?

Logs provide evidence of system and user activity and help security professionals detect and investigate security incidents.

---

## Key Takeaways

✔ Linux logs are commonly stored in `/var/log`.

✔ `auth.log` contains authentication-related events on Debian/Ubuntu systems.

✔ `syslog` contains general system activity on systems using traditional syslog.

✔ `grep` searches for specific events in logs.

✔ `tail -f` monitors logs in real time.

✔ `dmesg` displays kernel messages.

✔ `journalctl` is used to analyze systemd logs.

✔ `logrotate` manages log files and prevents excessive disk usage.

✔ Logs are essential for incident investigation and digital forensics.

✔ Log analysis is an important skill for SOC Analysts and Incident Responders.
