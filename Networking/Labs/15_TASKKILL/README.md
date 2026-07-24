# Lab 15 – TASKKILL Command

## Objective

The objective of this lab is to understand how to use the **TASKKILL** command to terminate running processes in Windows. The lab demonstrates terminating processes using their Process ID (PID), Image Name, and forceful termination. It also explains the importance of process termination in Windows administration, troubleshooting, malware containment, incident response, and digital forensics.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Basic understanding of Windows processes
- Notepad application (used for safe testing)

---

## Theory

The **TASKKILL** command is a built-in Windows command-line utility used to terminate one or more running processes on a local or remote computer. Processes can be terminated using their **Process ID (PID)** or **Image Name**. The command also supports forceful termination, filtering, and terminating process trees.

System administrators use TASKKILL to stop unresponsive applications and manage system resources. Cybersecurity professionals use it during incident response to isolate malicious processes, stop malware execution, terminate unauthorized applications, and contain security incidents.

---

## Syntax

```cmd
taskkill [options]
```

---

## Commands Used

```cmd
taskkill /?

tasklist

taskkill /PID <PID>

taskkill /IM notepad.exe

taskkill /F /IM notepad.exe
```

---

## Additional Reference Commands (Not Executed)

```cmd
taskkill /T /PID <PID>

taskkill /FI "IMAGENAME eq chrome.exe"

taskkill /FI "STATUS eq NOT RESPONDING"

taskkill /FI "MEMUSAGE gt 50000"

taskkill /F /T /IM application.exe
```

---

## Steps Performed

1. Displayed the built-in help for the TASKKILL command.
2. Opened Notepad.
3. Listed running processes using TASKLIST.
4. Identified the PID of the Notepad process.
5. Terminated Notepad using its PID.
6. Opened Notepad again.
7. Terminated Notepad using its Image Name.
8. Opened Notepad once more.
9. Forcefully terminated Notepad using the `/F` option.

---

## Expected Output

- TASKKILL help documentation.
- Successful termination of a process using PID.
- Successful termination using Image Name.
- Successful forceful termination.
- Confirmation messages after each successful operation.

---

## Key Findings

- Successfully terminated a running process using its Process ID (PID).
- Successfully terminated a process using its Image Name.
- Used the `/F` option to forcefully terminate a process.
- Learned that Process IDs change every time an application is restarted.
- Understood the difference between normal and forceful process termination.
- Explored the available command options through the built-in help.

---

## Cybersecurity Perspective

TASKKILL is an essential command during cybersecurity investigations and incident response. Security analysts use it to terminate malicious processes, stop ransomware execution, isolate infected applications, and contain active threats before performing further forensic analysis. It is also useful for stopping unauthorized software, troubleshooting compromised systems, and preventing malicious processes from consuming system resources.

---

## Challenges

- The first termination attempt using an incorrect PID failed because the process had a different PID.
- Identifying the correct PID required verifying the running processes using the TASKLIST command.
- Care must be taken to avoid terminating critical Windows system processes.

---

## Interview Questions

### 1. What is the purpose of the TASKKILL command?

It is used to terminate running processes in Windows.

---

### 2. What is the difference between `/PID` and `/IM`?

- `/PID` terminates a process using its Process ID.
- `/IM` terminates a process using its executable (Image) name.

---

### 3. What does the `/F` option do?

It forcefully terminates the specified process.

---

### 4. Why do Process IDs (PIDs) change?

Each time a process starts, Windows assigns it a new unique Process ID.

---

### 5. Which command is commonly used before TASKKILL?

```cmd
tasklist
```

It is used to identify the running process and its PID.

---

### 6. Why is TASKKILL important in cybersecurity?

It helps security professionals stop malicious processes, contain attacks, terminate malware, and perform incident response activities.

---

## Skills Gained

- Process Termination
- PID Identification
- Image Name Identification
- Forceful Process Termination
- Windows Process Management
- Windows Troubleshooting
- Incident Response Basics
- Malware Containment Fundamentals

---

## Lab Summary

This lab demonstrated how to terminate running Windows processes using the TASKKILL command. Processes were terminated using both their Process ID and Image Name, and forceful termination was also performed. The lab provides practical knowledge useful for Windows administration, cybersecurity operations, malware analysis, and incident response.
