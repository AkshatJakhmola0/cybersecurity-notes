# Lab 35 – SHUTDOWN Command

## Objective

To understand the Windows **SHUTDOWN** command and learn how to schedule system shutdowns, restart the computer, log off users, cancel scheduled operations, and access remote shutdown management options.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrator privileges (recommended)

---

## Theory

**SHUTDOWN** is a built-in Windows command-line utility used to shut down, restart, log off, or manage local and remote systems. It allows administrators to automate power operations and safely control system availability.

The command is widely used in Windows administration, maintenance tasks, scripting, and enterprise environments.

---

## Syntax

```cmd
shutdown [options]
```

Examples:

```cmd
shutdown /s /t 60

shutdown /r /t 60

shutdown /a
```

---

## Commands Used

```cmd
shutdown /?

shutdown /a

shutdown /l

shutdown /s /t 60

shutdown /a

shutdown /r /t 60

shutdown /a

shutdown /i
```

---

## Steps Performed

1. Displayed the SHUTDOWN help menu.
2. Attempted to abort a shutdown operation.
3. Tested the logoff command.
4. Scheduled a system shutdown with a timer.
5. Cancelled the scheduled shutdown.
6. Scheduled a system restart with a timer.
7. Cancelled the scheduled restart.
8. Opened the Remote Shutdown graphical interface.

---

## Key Findings

- SHUTDOWN can perform shutdown, restart, and logoff operations.
- Shutdown and restart operations can be scheduled using timers.
- Scheduled operations can be cancelled using `/a`.
- The `/i` option opens the Remote Shutdown Dialog.
- The command is useful for local and remote system administration.

---

## Cybersecurity Perspective

SHUTDOWN is useful for:

- Windows Administration
- Remote System Management
- Incident Response
- Maintenance Automation
- Enterprise Administration
- System Recovery Operations

---

## Interview Questions

**Q1. What is the purpose of the SHUTDOWN command?**  
It is used to shut down, restart, log off, or manage local and remote Windows systems.

**Q2. Which command schedules a shutdown after 60 seconds?**

```cmd
shutdown /s /t 60
```

**Q3. Which command schedules a restart?**

```cmd
shutdown /r /t 60
```

**Q4. How do you cancel a scheduled shutdown or restart?**

```cmd
shutdown /a
```

**Q5. Which command opens the Remote Shutdown Dialog?**

```cmd
shutdown /i
```

---

## Skills Gained

- Windows Administration
- System Management
- Remote Administration
- Command-Line Operations
- Incident Response
- Enterprise System Control
- IT Support Operations
