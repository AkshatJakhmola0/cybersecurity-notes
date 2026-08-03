# Lab 31 – ICACLS Command

## Objective

To understand the Windows **ICACLS** command and learn how to view, grant, and remove NTFS file and folder permissions using Command Prompt.

---

## Prerequisites

- Windows 10/11
- Command Prompt (Run as Administrator)
- Basic understanding of NTFS permissions

---

## Theory

**ICACLS (Integrity Control Access Control Lists)** is a built-in Windows command-line utility used to display, modify, back up, and restore NTFS file and folder permissions.

It allows administrators to manage user access rights, making it an essential tool for Windows administration and cybersecurity.

---

## Syntax

```cmd
icacls <File_or_Folder> [Options]
```

Examples:

```cmd
icacls C:\Users

icacls C:\Data /grant Everyone:R
```

---

## Commands Used

```cmd
icacls /?

mkdir C:\ICACLS_Lab

echo Test File > C:\ICACLS_Lab\test.txt

icacls C:\ICACLS_Lab

icacls C:\ICACLS_Lab\test.txt

icacls C:\ICACLS_Lab /grant Everyone:R

icacls C:\ICACLS_Lab /remove Everyone
```

---

## Steps Performed

1. Displayed the ICACLS help menu.
2. Created a test folder.
3. Created a sample text file.
4. Viewed the folder permissions.
5. Viewed the file permissions.
6. Granted **Read** permission to the **Everyone** group.
7. Removed the permission from the **Everyone** group.
8. Verified the updated permissions.

---

## Key Findings

- ICACLS displays NTFS file and folder permissions.
- Permissions can be granted or removed for users and groups.
- NTFS permissions help control access to system resources.
- Permission changes take effect immediately after execution.
- ICACLS is widely used for access control and security management.

---

## Cybersecurity Perspective

ICACLS is useful for:

- Access Control Management
- Permission Auditing
- Digital Forensics
- Incident Response
- Windows Security Administration
- Hardening File Permissions

---

## Interview Questions

**Q1. What is ICACLS used for?**  
It is used to view and manage NTFS file and folder permissions.

**Q2. Which command displays file permissions?**

```cmd
icacls filename
```

**Q3. What does `/grant` do?**  
It grants permissions to a user or group.

**Q4. What does `/remove` do?**  
It removes permissions for a specified user or group.

**Q5. Why is ICACLS important in cybersecurity?**  
It helps manage access control, audit permissions, and secure sensitive files and directories.

---

## Skills Gained

- Windows Permission Management
- NTFS Access Control
- Windows Administration
- Command-Line Administration
- Security Auditing
- Digital Forensics
- Access Control Management
