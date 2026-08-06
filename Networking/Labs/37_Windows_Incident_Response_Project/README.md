# Lab 37 – Windows Incident Response Mini Project

## Objective

To perform a basic Windows incident response investigation using native Command Prompt utilities and collect evidence related to user activity, network connections, running processes, services, startup programs, scheduled tasks, drivers, and privileged accounts.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrative privileges (recommended)

---

## Theory

Incident Response (IR) is the process of identifying, analyzing, containing, and investigating suspicious activities within a system. Security analysts frequently use native Windows commands to collect forensic evidence and perform rapid triage during investigations.

This project simulates a workstation investigation where suspicious activity has been reported. The goal is to gather system information and identify potential indicators of compromise (IOCs).

---

## Investigation Scenario

A Windows workstation has generated a security alert indicating possible suspicious activity. The analyst must collect evidence and determine whether abnormal user accounts, network connections, startup entries, scheduled tasks, services, or processes are present.

---

## Commands Used

```cmd
whoami

hostname

systeminfo

ipconfig /all

netstat -ano

tasklist

tasklist /svc

net user

net localgroup administrators

schtasks

driverquery

wmic startup get caption,command

openfiles /query
```

---

## Evidence Collection Areas

### User Identification

```cmd
whoami
```

Identifies the currently logged-in user.

---

### Host Identification

```cmd
hostname
```

Identifies the affected system.

---

### System Information

```cmd
systeminfo
```

Collects operating system and hardware details.

---

### Network Configuration

```cmd
ipconfig /all
```

Collects IP address, DNS, gateway, and adapter information.

---

### Active Network Connections

```cmd
netstat -ano
```

Displays listening ports and active connections.

---

### Running Processes

```cmd
tasklist
```

Lists currently running processes.

---

### Process-Service Mapping

```cmd
tasklist /svc
```

Maps Windows services to running processes.

---

### User Account Enumeration

```cmd
net user
```

Lists local user accounts.

---

### Administrator Enumeration

```cmd
net localgroup administrators
```

Lists users with administrative privileges.

---

### Scheduled Task Analysis

```cmd
schtasks
```

Displays configured scheduled tasks.

---

### Driver Enumeration

```cmd
driverquery
```

Lists installed device drivers.

---

### Startup Program Analysis

```cmd
wmic startup get caption,command
```

Alternative:

```cmd
reg query HKCU\Software\Microsoft\Windows\CurrentVersion\Run
```

Displays startup applications.

---

### Open File Analysis

```cmd
openfiles /query
```

Displays currently shared/open files.

---

## Investigation Workflow

1. Identify the active user.
2. Identify the affected workstation.
3. Collect operating system information.
4. Review network configuration.
5. Analyze active network connections.
6. Review running processes.
7. Map services to processes.
8. Enumerate local users.
9. Review administrative accounts.
10. Analyze scheduled tasks.
11. Review installed drivers.
12. Inspect startup applications.
13. Review open/shared files.
14. Document findings.
15. Produce an incident response report.

---

## Skills Gained

- Incident Response
- Windows Forensics
- System Enumeration
- Process Analysis
- Service Analysis
- Network Investigation
- User Enumeration
- Privilege Review
- Scheduled Task Analysis
- Startup Persistence Detection
- Driver Enumeration
- Security Auditing

---

## Cybersecurity Relevance

This project demonstrates practical skills used by:

- SOC Analysts
- Incident Responders
- Blue Team Analysts
- Digital Forensics Investigators
- System Administrators
- Threat Hunters

---

## Expected Outcome

Successfully perform a Windows incident response investigation, collect system evidence, analyze potential indicators of compromise, and document findings in a professional incident response report.
