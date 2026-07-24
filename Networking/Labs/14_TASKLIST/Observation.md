# Lab 14 – TASKLIST Command

## Objective

The objective of this lab is to understand how to use the **TASKLIST** command to view running processes in Windows. The lab demonstrates how to display basic process information, verbose details, associated services, loaded DLL modules, and built-in command help. It also explains the importance of process enumeration in Windows system administration, incident response, malware analysis, and digital forensics.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Basic understanding of Windows processes

---

## Theory

The **TASKLIST** command is a built-in Windows command-line utility used to display all currently running processes on a local or remote computer. It provides valuable information such as Process ID (PID), memory usage, services hosted by each process, and loaded Dynamic Link Libraries (DLLs).

System administrators use TASKLIST for monitoring system performance and troubleshooting applications, while cybersecurity professionals use it during incident response, malware analysis, threat hunting, and digital forensic investigations to identify suspicious or malicious processes.

---

## Syntax

```cmd
tasklist [options]
```

---

## Commands Used

```cmd
tasklist
tasklist /v
tasklist /svc
tasklist /m
tasklist /?
```

---

## Additional Reference Commands (Not Executed)

```cmd
tasklist /FI "IMAGENAME eq chrome.exe"
tasklist /FI "PID gt 5000"
tasklist /FI "STATUS eq RUNNING"
tasklist /FO LIST
tasklist /FO CSV
tasklist /FO TABLE
tasklist /NH
tasklist /APPS
```

---

## Steps Performed

1. Displayed all running processes.
2. Viewed detailed process information.
3. Displayed Windows services associated with processes.
4. Displayed DLL modules loaded by running processes.
5. Viewed the built-in help documentation.

---

## Expected Output

- List of running processes.
- Process IDs (PID).
- Memory usage.
- Verbose process details.
- Windows services mapped to processes.
- DLL modules loaded by processes.
- TASKLIST help information.

---

## Key Findings

- Successfully listed all active processes running on the system.
- Identified Process IDs (PID) and memory consumption.
- Observed services hosted by Windows processes.
- Examined DLL modules loaded into various processes.
- Learned multiple filtering and formatting options.
- Understood how TASKLIST assists in Windows troubleshooting and cybersecurity investigations.

---

## Cybersecurity Perspective

TASKLIST is one of the most frequently used commands during security investigations. It allows analysts to identify suspicious processes, detect malicious applications, verify legitimate Windows services, inspect DLL usage, and collect evidence during incident response. It is also valuable for malware analysis, live forensics, SOC operations, and endpoint monitoring.

---

## Challenges

- Large number of running processes made analysis time-consuming.
- Some processes loaded hundreds of DLL modules.
- Differentiating between legitimate Windows processes and third-party applications required careful observation.

---

## Interview Questions

### 1. What is TASKLIST used for?

It displays all currently running processes on a Windows computer.

---

### 2. What is a PID?

PID (Process ID) is a unique number assigned to every running process.

---

### 3. Which command displays services associated with processes?

```cmd
tasklist /svc
```

---

### 4. Which command displays loaded DLL modules?

```cmd
tasklist /m
```

---

### 5. What does the `/V` option do?

It displays verbose information such as user name, CPU time, status, and window title.

---

### 6. Why is TASKLIST important in cybersecurity?

It helps identify suspicious processes, investigate malware, perform incident response, and conduct digital forensic analysis.

---

## Skills Gained

- Process Enumeration
- Windows Process Management
- PID Identification
- Service Enumeration
- DLL Inspection
- Windows Troubleshooting
- Malware Investigation Basics
- Incident Response Fundamentals

---

## Lab Summary

This lab demonstrated the use of the TASKLIST command to monitor running processes, inspect services and DLL modules, and understand process management in Windows. The knowledge gained is valuable for Windows administration, cybersecurity investigations, malware analysis, and digital forensics.
