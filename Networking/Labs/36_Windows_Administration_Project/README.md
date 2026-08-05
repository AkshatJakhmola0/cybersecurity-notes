# Lab 36 – Windows Administration Mini Project

## Objective

To perform a Windows system administration audit using built-in Command Prompt utilities and collect important information about the operating system, users, network configuration, processes, services, storage, drivers, and power settings.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrative privileges (recommended)

---

## Theory

Windows administrators frequently perform system audits to understand the current state of a computer. These audits help identify system configuration, network settings, active users, running processes, installed drivers, storage usage, and power configurations.

This project demonstrates how built-in Windows commands can be used to collect and document system information without installing third-party tools.

---

## Commands Used

```cmd
systeminfo

hostname

whoami

ipconfig /all

net user

tasklist

sc query

fsutil volume diskfree C:

driverquery

powercfg /getactivescheme
```

---

## Information Collected

### System Information

```cmd
systeminfo
```

Collects operating system and hardware information.

---

### Computer Name

```cmd
hostname
```

Displays the system hostname.

---

### Current User

```cmd
whoami
```

Displays the currently logged-in user.

---

### Network Configuration

```cmd
ipconfig /all
```

Displays detailed network settings.

---

### Local User Accounts

```cmd
net user
```

Lists local user accounts on the system.

---

### Running Processes

```cmd
tasklist
```

Displays currently running processes.

---

### Running Services

```cmd
sc query
```

Displays active Windows services.

---

### Storage Information

```cmd
fsutil volume diskfree C:
```

Displays disk size and free space information.

---

### Installed Drivers

```cmd
driverquery
```

Lists installed device drivers.

---

### Active Power Plan

```cmd
powercfg /getactivescheme
```

Displays the currently active power plan.

---

## Project Workflow

1. Gather operating system information.
2. Identify the current user and computer name.
3. Review network configuration.
4. Enumerate local user accounts.
5. Analyze running processes.
6. Review active Windows services.
7. Check storage utilization.
8. Review installed drivers.
9. Verify active power configuration.
10. Document findings and recommendations.

---

## Skills Gained

- Windows Administration
- System Auditing
- Network Enumeration
- User Account Management
- Process Monitoring
- Service Analysis
- Storage Monitoring
- Driver Enumeration
- Power Management
- Command-Line Administration

---

## Cybersecurity Relevance

This project demonstrates skills commonly used in:

- Security Operations Centers (SOC)
- System Administration
- Incident Response
- Digital Forensics
- Vulnerability Assessments
- Endpoint Auditing
- Blue Team Operations

---

## Outcome

Successfully performed a Windows administrative audit and documented critical system information including operating system details, user accounts, network settings, storage status, running services, installed drivers, and power configuration.
