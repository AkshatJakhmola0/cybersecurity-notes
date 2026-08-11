# System Monitoring in Linux

## What is System Monitoring?

System monitoring in Linux refers to observing system resources, processes, users, and performance.

Linux provides tools for:

* CPU monitoring
* Memory monitoring
* Disk monitoring
* Process monitoring
* User activity monitoring
* System performance analysis

---

## Why is System Monitoring Important?

Without System Monitoring

* Performance problems may go unnoticed.
* High CPU usage can slow down systems.
* Memory exhaustion can crash applications.
* Disk space can become full.
* Suspicious processes may remain undetected.

With System Monitoring

* Performance problems can be identified.
* Resource usage can be analyzed.
* Suspicious processes can be investigated.
* System failures can be prevented.
* Security incidents can be detected.

---

## Real-World Example

When a Linux server becomes slow:

```text
Linux Server
      │
      ▼
Check CPU
      │
      ▼
Check Memory
      │
      ▼
Check Processes
      │
      ▼
Check Disk
      │
      ▼
Identify Problem
````

---

## Checking System Uptime

### uptime

Displays system uptime and load average.

```bash
uptime
```

Example:

```text
14:30:20 up 5 days, 3:20, 2 users, load average: 0.25, 0.30, 0.20
```

Displays:

* System uptime
* Logged-in users
* Load average

---

## Understanding Load Average

Example:

```text
load average: 0.25, 0.30, 0.20
```

The values represent:

```text
1 minute   5 minutes   15 minutes
```

A high load average may indicate heavy system activity.

---

## Viewing Running Processes

### ps

Displays running processes.

```bash
ps
```

View all processes:

```bash
ps aux
```

Example:

```text
USER       PID  %CPU  %MEM  COMMAND
root         1   0.0   0.1  systemd
user      1200   2.5   1.2  firefox
```

Displays:

* User
* PID
* CPU usage
* Memory usage
* Command

---

## Monitoring Processes in Real Time

### top

Displays processes and resource usage in real time.

```bash
top
```

Useful for:

* CPU monitoring
* Memory monitoring
* Process monitoring
* Identifying resource-intensive processes

---

### htop

Interactive alternative to `top`.

```bash
htop
```

Installation:

```bash
sudo apt install htop
```

Provides an easier-to-read process monitoring interface.

---

## Finding Processes

### pgrep

Searches for processes by name.

```bash
pgrep firefox
```

Example:

```text
1200
1250
```

Useful for finding process IDs quickly.

---

## Process ID (PID)

Every running Linux process has a unique Process ID.

Example:

```text
PID
1200
```

View PIDs:

```bash
ps aux
```

PIDs are useful when investigating or managing processes.

---

## Terminating Processes

### kill

Terminates a process using its PID.

```bash
kill 1200
```

The default signal is usually `SIGTERM`.

---

### kill -9

Forcefully terminates a process.

```bash
kill -9 1200
```

`SIGKILL` immediately terminates the process.

Use it carefully because the process cannot perform cleanup.

---

## Monitoring Memory

### free

Displays memory and swap usage.

```bash
free -h
```

Example:

```text
              total   used   free
Mem:           7.7G    3.2G   2.1G
Swap:          2.0G    0.2G   1.8G
```

Displays:

* Total memory
* Used memory
* Free memory
* Swap memory

---

## Monitoring Disk Space

### df

Displays filesystem disk usage.

```bash
df -h
```

Example:

```text
Filesystem      Size  Used Avail Use%
/dev/sda1        50G   20G   28G  42%
```

Displays:

* Disk size
* Used space
* Available space
* Usage percentage

---

## Checking Directory Size

### du

Displays disk usage of files and directories.

```bash
du -sh /var/log
```

Example:

```text
850M    /var/log
```

Useful for finding directories consuming large amounts of disk space.

---

## Monitoring Logged-in Users

### who

Displays currently logged-in users.

```bash
who
```

Example:

```text
user1   pts/0   2026-08-11 10:20
user2   pts/1   2026-08-11 11:15
```

---

### w

Displays logged-in users and their activity.

```bash
w
```

Provides:

* Logged-in users
* Login time
* Idle time
* Current activity
* System load

---

## Viewing Process Tree

### pstree

Displays processes in a tree structure.

```bash
pstree
```

Example:

```text
systemd
 ├─sshd
 │  └─bash
 └─cron
```

Useful for understanding parent-child process relationships.

---

## Monitoring System Resources

### vmstat

Displays system resource statistics.

```bash
vmstat
```

Useful for monitoring:

* CPU
* Memory
* Processes
* Swap
* I/O

---

## Monitoring Disk I/O

### iostat

Displays CPU and disk I/O statistics.

```bash
iostat
```

Installation:

```bash
sudo apt install sysstat
```

Useful for:

* Disk performance analysis
* I/O troubleshooting
* Identifying bottlenecks

---

## Checking Open Files and Connections

### lsof

Lists open files and the processes using them.

```bash
lsof
```

Check which process is using a port:

```bash
sudo lsof -i :80
```

Useful for:

* Identifying processes using ports
* Investigating network connections
* Troubleshooting applications
* Security investigations

---

## Network Interface Statistics

### ip -s link

Displays network interface statistics.

```bash
ip -s link
```

Shows:

* Received packets
* Transmitted packets
* Errors
* Dropped packets

---

## System Monitoring for Cybersecurity

System monitoring is important because unusual resource usage may indicate malicious activity.

Example:

```text
High CPU Usage
      │
      ▼
Identify Process
      │
      ▼
Check Process Owner
      │
      ▼
Check Command
      │
      ▼
Check Network Connections
      │
      ▼
Investigate
```

Possible suspicious activity:

* Unknown processes
* Unexpected CPU usage
* Unauthorized services
* Suspicious network connections
* Unusual user activity
* Possible cryptomining

---

## Common SOC Investigation Commands

View processes:

```bash
ps aux
```

Monitor processes:

```bash
top
```

Check memory:

```bash
free -h
```

Check disk:

```bash
df -h
```

Check directory size:

```bash
du -sh /var/log
```

Check logged-in users:

```bash
who
```

Check process tree:

```bash
pstree
```

Check open connections:

```bash
lsof
```

Check system load:

```bash
uptime
```

---

## Important System Monitoring Commands

| Command  | Purpose                        |
| -------- | ------------------------------ |
| `uptime` | System uptime and load         |
| `ps`     | Running processes              |
| `top`    | Real-time process monitoring   |
| `htop`   | Interactive process monitoring |
| `free`   | Memory usage                   |
| `df`     | Disk space                     |
| `du`     | File/directory usage           |
| `who`    | Logged-in users                |
| `w`      | User activity                  |
| `pstree` | Process hierarchy              |
| `kill`   | Terminate processes            |
| `vmstat` | System resource statistics     |
| `iostat` | Disk I/O statistics            |
| `lsof`   | Open files and connections     |

---

## Why System Monitoring Matters in Cybersecurity

Cybersecurity professionals use Linux monitoring tools to:

* Detect suspicious processes
* Identify resource abuse
* Investigate compromised systems
* Monitor user activity
* Identify unauthorized services
* Investigate malware behavior
* Detect possible cryptomining
* Troubleshoot security incidents

System monitoring is important for **SOC Analysts, Incident Responders, and Security Engineers**.

---

## Interview Questions

### Q1. Which command displays running processes?

```bash
ps aux
```

---

### Q2. Which command monitors processes in real time?

```bash
top
```

---

### Q3. What is the difference between top and htop?

`top` is a standard process monitoring tool, while `htop` provides an interactive and more user-friendly interface.

---

### Q4. Which command displays memory usage?

```bash
free -h
```

---

### Q5. Which command displays disk space?

```bash
df -h
```

---

### Q6. Which command displays directory usage?

```bash
du -sh
```

---

### Q7. What is a PID?

PID stands for **Process ID**. It is a unique number assigned to a running process.

---

### Q8. Which command terminates a process?

```bash
kill PID
```

---

### Q9. What does `kill -9` do?

It sends the `SIGKILL` signal and forcefully terminates a process.

---

### Q10. Which command shows logged-in users?

```bash
who
```

---

### Q11. Which command displays system uptime and load?

```bash
uptime
```

---

### Q12. Which command can identify a process using a port?

```bash
lsof -i :80
```

---

## Key Takeaways

✔ `uptime` displays system uptime and load average.

✔ `ps` displays running processes.

✔ `top` and `htop` monitor processes.

✔ `free -h` displays memory usage.

✔ `df -h` displays disk space.

✔ `du` displays file and directory usage.

✔ `who` and `w` show logged-in users.

✔ `pstree` displays process relationships.

✔ `kill` terminates processes.

✔ `lsof` identifies processes using files and ports.

✔ System monitoring is essential for SOC Analysts, Incident Responders, and Security Engineers.

