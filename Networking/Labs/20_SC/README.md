
# Lab 20 – SC (Service Controller)

## Objective

The objective of this lab is to learn how to use the Windows **SC (Service Controller)** command to manage and examine Windows services. This lab demonstrates how to view running and stopped services, inspect service configurations, identify service names, and understand their role in Windows system administration and cybersecurity.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrator privileges (recommended)
- Basic knowledge of Windows Services

---

# Theory

Windows Services are background processes that start automatically or manually to provide essential operating system and application functionality. Services can run without user interaction and are managed by the **Service Control Manager (SCM)**.

The **SC (Service Controller)** command-line utility communicates with the Service Control Manager to query, configure, start, stop, and manage Windows services.

Security professionals frequently use the SC command during:

- Incident Response
- Malware Analysis
- Digital Forensics
- System Auditing
- Windows Hardening
- Security Monitoring

Attackers also abuse Windows services for persistence and privilege escalation, making knowledge of this command important for cybersecurity professionals.

---

# Syntax

```cmd
sc [command] [service_name] [options]
```

Examples:

```cmd
sc query

sc query state= all

sc qc EventLog

sc GetDisplayName EventLog
```

---

# Commands Used

```cmd
sc

sc query

sc query state= all

sc qc EventLog

sc GetKeyName "Windows Event Log"

sc GetDisplayName EventLog

sc /?
```

---

# Steps Performed

### Step 1

Executed the SC command to view available Service Controller commands.

**Command**

```cmd
sc
```

---

### Step 2

Displayed all currently running Windows services.

**Command**

```cmd
sc query
```

---

### Step 3

Displayed both running and stopped Windows services.

**Command**

```cmd
sc query state= all
```

---

### Step 4

Viewed the configuration details of the Windows Event Log service.

**Command**

```cmd
sc qc EventLog
```

---

### Step 5

Retrieved the internal service name from the display name.

**Command**

```cmd
sc GetKeyName "Windows Event Log"
```

---

### Step 6

Retrieved the display name using the internal service name.

**Command**

```cmd
sc GetDisplayName EventLog
```

---

### Step 7

Displayed detailed help information for the SC command.

**Command**

```cmd
sc /?
```

---

# Expected Output

- List of available SC commands.
- Running Windows services.
- Running and stopped services.
- Service configuration details.
- Internal service names.
- Display names.
- Help documentation for SC.

---

# Key Findings

- SC communicates directly with the Windows Service Control Manager.
- Windows services have both a Service Name and a Display Name.
- Services can exist in different states such as Running and Stopped.
- Service configuration includes executable path, startup type, and dependencies.
- Windows relies on numerous background services for system functionality.
- Security analysts can use SC to investigate suspicious services.

---

# Cybersecurity Perspective

The SC command is one of the most valuable Windows administration tools for cybersecurity professionals.

It allows analysts to:

- Enumerate active services
- Identify disabled or stopped services
- Verify service configurations
- Detect suspicious services
- Investigate malware persistence
- Examine startup behavior
- Support incident response investigations
- Audit Windows systems

Many malware families create malicious Windows services to maintain persistence. During threat hunting and forensic investigations, analysts use the SC command to identify unknown or unauthorized services.

---

# Challenges

- Understanding the difference between Service Name and Display Name.
- Remembering the correct syntax for query options.
- Reading long outputs containing hundreds of services.
- Identifying legitimate versus suspicious services.

---

# Interview Questions

### 1. What is the purpose of the SC command?

**Answer:**
It is used to communicate with the Windows Service Control Manager for managing Windows services.

---

### 2. What is the difference between a Service Name and a Display Name?

**Answer:**
The Service Name is the internal identifier, while the Display Name is the user-friendly name shown in Windows.

---

### 3. Which command displays all running services?

**Answer**

```cmd
sc query
```

---

### 4. Which command displays all services including stopped ones?

**Answer**

```cmd
sc query state= all
```

---

### 5. Why is the SC command important in cybersecurity?

**Answer:**
It helps identify malicious services, persistence mechanisms, startup configurations, and suspicious background processes.

---

### 6. Which command displays the configuration of a service?

**Answer**

```cmd
sc qc <ServiceName>
```

Example

```cmd
sc qc EventLog
```

---

# Skills Gained

- Windows Service Management
- Service Enumeration
- Windows Administration
- Incident Response
- Threat Hunting
- Malware Persistence Analysis
- Service Configuration Analysis
- Windows Security Fundamentals

---

# Lab Summary

In this lab, the Windows **SC (Service Controller)** command was used to examine Windows services and their configurations. Running and stopped services were enumerated, service names were identified, and configuration details of the Windows Event Log service were reviewed. The lab demonstrated how the SC command assists administrators and cybersecurity professionals in auditing Windows systems, troubleshooting services, and detecting potential persistence mechanisms used by attackers.
