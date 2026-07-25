# Lab Report

## Experiment Title

Study of the SCHTASKS Command in Windows

---

## Objective

To learn how to use the SCHTASKS command to view, create, execute, and delete scheduled tasks in Windows. The experiment also aims to understand the role of scheduled tasks in system administration, automation, and cybersecurity.

---

## Tools Used

- Windows 11
- Command Prompt
- Task Scheduler
- Notepad

---

## Commands Executed

```cmd
schtasks /?

schtasks /query

schtasks /create /tn "Notepad Lab" /tr "notepad.exe" /sc once /st 23:59

schtasks /run /tn "Notepad Lab"

schtasks /delete /tn "Notepad Lab" /f
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the built-in help using the `schtasks /?` command.
3. Listed all scheduled tasks using `schtasks /query`.
4. Created a scheduled task named **Notepad Lab** to launch Notepad.
5. Executed the scheduled task manually using the `/run` option.
6. Verified that Notepad launched successfully.
7. Deleted the scheduled task using the `/delete` option with the `/f` parameter.
8. Recorded observations and captured screenshots.

---

## Results

Successfully displayed the SCHTASKS help documentation, viewed existing scheduled tasks, created a new scheduled task, executed it manually, and deleted it after testing. The experiment demonstrated how Windows Task Scheduler can automate applications and administrative tasks through the command line.

---

## Conclusion

The SCHTASKS command is a powerful Windows command-line utility for managing scheduled tasks. It enables administrators to automate routine operations and allows security professionals to investigate, manage, and remove scheduled tasks that may be used for persistence by malicious software. Understanding SCHTASKS is valuable for Windows administration, system automation, incident response, threat hunting, and digital forensic investigations.

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
