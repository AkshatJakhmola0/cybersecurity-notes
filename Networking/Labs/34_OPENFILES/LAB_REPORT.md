# LAB REPORT

## Experiment Title

Study of the OPENFILES Command in Windows Command Prompt

---

## Objective

To understand the working of the **OPENFILES** command and learn how to view open files, query shared file information, and enable local object tracking using Command Prompt.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

```cmd
openfiles /?

openfiles

openfiles /query

openfiles /local on

openfiles /query
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the OPENFILES help menu.
3. Executed the `openfiles` command to view open files.
4. Queried the list of currently opened shared files.
5. Enabled the **Maintain Objects List** feature using `openfiles /local on`.
6. Queried the open files again.
7. Observed that the configuration change requires a system restart before taking effect.
8. Verified that no shared open files were present during the experiment.

---

## Results

- Successfully displayed information about open files.
- Confirmed that local object tracking was disabled by default.
- Successfully enabled the **Maintain Objects List** feature.
- Observed that the feature becomes active only after restarting the system.
- No shared open files were found during the experiment.
- All commands executed successfully without errors.

---

## Conclusion

The **OPENFILES** command is a useful Windows administration utility for monitoring files opened through shared resources and enabling local file tracking. Although local object tracking requires a system restart before becoming active, the command provides administrators with valuable capabilities for file management, troubleshooting, and security monitoring. It is particularly useful in environments where monitoring access to shared files is important.

---

## Skills Gained

- Windows File Monitoring
- Shared Resource Management
- Windows Administration
- Command-Line Administration
- File Access Monitoring
- Security Auditing
- Digital Forensics
- Incident Response
