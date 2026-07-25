# Lab 16 – SCHTASKS Command

## Objective

The objective of this lab is to understand how to use the **SCHTASKS** command to manage scheduled tasks in Windows. The lab demonstrates how to view existing scheduled tasks, create a new task, run it manually, and delete it. It also explains the importance of scheduled tasks in Windows administration and cybersecurity.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Administrative privileges (recommended)
- Basic understanding of Windows Task Scheduler

---

## Theory

The **SCHTASKS** command is a built-in Windows command-line utility used to create, query, modify, run, end, and delete scheduled tasks on both local and remote computers. Scheduled tasks allow Windows or users to automate programs, scripts, and maintenance activities at specified times or events.

System administrators use SCHTASKS to automate system maintenance, software updates, backups, and administrative tasks. Cybersecurity professionals use it to identify persistence mechanisms, investigate suspicious scheduled tasks, detect malware, and remove unauthorized tasks during incident response.

---

## Syntax

```cmd
schtasks [options]
```

---

## Commands Used

```cmd
schtasks /?

schtasks /query

schtasks /create /tn "Notepad Lab" /tr "notepad.exe" /sc once /st 23:59

schtasks /run /tn "Notepad Lab"

schtasks /delete /tn "Notepad Lab" /f
```

---

## Additional Reference Commands (Not Executed)

```cmd
schtasks /change /?

schtasks /end /tn "TaskName"

schtasks /query /fo LIST

schtasks /query /fo TABLE

schtasks /query /v

schtasks /showsid /tn "TaskName"
```

---

## Steps Performed

1. Displayed the built-in help for the SCHTASKS command.
2. Listed all scheduled tasks on the system.
3. Created a scheduled task named **Notepad Lab**.
4. Executed the scheduled task manually.
5. Verified that the scheduled task launched the application.
6. Deleted the scheduled task after testing.

---

## Expected Output

- SCHTASKS help documentation.
- List of scheduled tasks available on the system.
- Successful creation of a scheduled task.
- Successful execution of the scheduled task.
- Successful deletion of the scheduled task.

---

## Key Findings

- Successfully viewed all scheduled tasks on the system.
- Created a new scheduled task using the command line.
- Executed the scheduled task manually.
- Successfully removed the scheduled task after testing.
- Learned how Windows Task Scheduler automates applications and administrative tasks.
- Understood the lifecycle of creating, executing, and deleting scheduled tasks.

---

## Cybersecurity Perspective

Scheduled tasks are frequently abused by attackers to establish persistence on compromised systems. Malware often creates scheduled tasks that execute malicious programs automatically during startup or at scheduled intervals. Security analysts use SCHTASKS to inspect scheduled tasks, detect unauthorized persistence mechanisms, remove malicious tasks, and perform forensic investigations.

---

## Challenges

- Creating scheduled tasks requires specifying a valid future execution time.
- Administrative privileges may be required for certain operations.
- Care should be taken when modifying or deleting existing system tasks.

---

## Interview Questions

### 1. What is the purpose of the SCHTASKS command?

It is used to create, query, modify, run, and delete scheduled tasks in Windows.

---

### 2. Which command displays all scheduled tasks?

```cmd
schtasks /query
```

---

### 3. Which command creates a scheduled task?

```cmd
schtasks /create
```

---

### 4. Which command runs a scheduled task immediately?

```cmd
schtasks /run /tn "TaskName"
```

---

### 5. Which command deletes a scheduled task?

```cmd
schtasks /delete /tn "TaskName" /f
```

---

### 6. Why is SCHTASKS important in cybersecurity?

Attackers commonly use scheduled tasks for persistence. Security professionals use SCHTASKS to identify, investigate, and remove malicious scheduled tasks during incident response and threat hunting.

---

## Skills Gained

- Windows Task Scheduler Management
- Scheduled Task Enumeration
- Task Creation
- Task Execution
- Task Deletion
- Windows Automation
- Persistence Detection
- Incident Response Fundamentals

---

## Lab Summary

This lab demonstrated how to manage Windows scheduled tasks using the SCHTASKS command. The experiment included viewing existing tasks, creating a new scheduled task, executing it manually, and deleting it after testing. The knowledge gained is valuable for Windows system administration, automation, cybersecurity operations, threat hunting, and digital forensic investigations.

---

## Evidence

Screenshots included:

- 01_schtasks_help.png
- 02_schtasks_query.png
- 03_schtasks_create.png
- 04_schtasks_run.png
- 05_schtasks_delete.png
