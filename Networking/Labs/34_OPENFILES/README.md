# Lab 34 – OPENFILES Command

## Objective

To understand the Windows **OPENFILES** command and learn how to view open files, query shared file information, and enable local object tracking using Command Prompt.

---

## Prerequisites

- Windows 10/11
- Command Prompt (Run as Administrator)

---

## Theory

**OPENFILES** is a built-in Windows command-line utility used to view and manage files that are currently opened over shared resources. It can also track locally opened files when the **Maintain Objects List** feature is enabled.

This command is primarily used by system administrators for file management, troubleshooting, and monitoring shared resources.

---

## Syntax

```cmd
openfiles [options]
```

Examples:

```cmd
openfiles

openfiles /query

openfiles /local on
```

---

## Commands Used

```cmd
openfiles /?

openfiles

openfiles /query

openfiles /local on

openfiles /query
```

---

## Steps Performed

1. Displayed the OPENFILES help menu.
2. Checked the list of open files.
3. Queried currently opened files.
4. Enabled the **Maintain Objects List** feature.
5. Queried open files again.
6. Observed that a system restart is required before local file tracking becomes active.

---

## Key Findings

- OPENFILES displays information about shared open files.
- Local file tracking is disabled by default.
- The `/local on` command successfully enables local object tracking.
- A system restart is required before the change takes effect.
- No shared open files were present during the experiment.

---

## Cybersecurity Perspective

OPENFILES is useful for:

- File Access Monitoring
- Shared Resource Management
- Windows Administration
- Incident Response
- Digital Forensics
- Security Auditing

---

## Interview Questions

**Q1. What is OPENFILES used for?**  
It is used to view and manage files that are opened over shared resources.

**Q2. Why does `openfiles /query` sometimes show a warning?**  
Because local object tracking is disabled by default and must be enabled using `openfiles /local on`.

**Q3. Which command enables local object tracking?**

```cmd
openfiles /local on
```

**Q4. Is a restart required after enabling local object tracking?**  
Yes. The change takes effect only after restarting the computer.

**Q5. Why is OPENFILES useful in cybersecurity?**  
It helps administrators identify open files, monitor shared resources, and support forensic investigations.

---

## Skills Gained

- Windows File Management
- Shared Resource Monitoring
- Windows Administration
- Command-Line Administration
- Security Monitoring
- Digital Forensics
- Incident Response
