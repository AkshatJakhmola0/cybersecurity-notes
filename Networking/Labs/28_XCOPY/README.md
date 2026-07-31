# Lab 28 – XCOPY Command

## Objective

To understand the Windows **XCOPY** command and learn how to copy files and directories using different command-line options.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of files and directories

---

## Theory

**XCOPY** is a command-line utility used to copy files, folders, and complete directory structures. It provides more functionality than the basic `COPY` command and supports recursive copying, empty directories, and overwrite options.

It is commonly used for backups, file migration, and system administration.

---

## Syntax

```cmd
xcopy Source Destination [Options]
```

Example:

```cmd
xcopy C:\Data D:\Backup /E
```

---

## Commands Used

```cmd
xcopy /?

mkdir C:\XCOPY_Lab

echo Test File > C:\XCOPY_Lab\test.txt

xcopy C:\XCOPY_Lab "%USERPROFILE%\Desktop\XCOPY_Backup"

xcopy C:\XCOPY_Lab "%USERPROFILE%\Desktop\XCOPY_Backup" /S

xcopy C:\XCOPY_Lab "%USERPROFILE%\Desktop\XCOPY_Backup" /E

xcopy C:\XCOPY_Lab "%USERPROFILE%\Desktop\XCOPY_Backup" /Y
```

---

## Steps Performed

1. Viewed the XCOPY help menu.
2. Created a test folder.
3. Created a sample text file.
4. Copied the folder using the default XCOPY command.
5. Copied using the `/S` option.
6. Copied using the `/E` option.
7. Copied using the `/Y` option.
8. Verified the copied file.

---

## Key Findings

- XCOPY copies files and directories.
- `/S` copies subdirectories except empty ones.
- `/E` copies all directories including empty ones.
- `/Y` suppresses overwrite confirmation.
- Windows may ask whether the destination is a file or directory if it does not already exist.

---

## Cybersecurity Perspective

XCOPY is useful for:

- Creating backups.
- Collecting forensic evidence.
- Copying log files.
- Migrating data securely.
- Preparing incident response data.

---

## Interview Questions

**Q1. What is XCOPY used for?**  
Copies files and directories.

**Q2. What does `/S` do?**  
Copies subdirectories except empty ones.

**Q3. What does `/E` do?**  
Copies all directories including empty ones.

**Q4. What does `/Y` do?**  
Suppresses overwrite confirmation.

**Q5. Why is XCOPY useful in cybersecurity?**  
It helps back up and collect evidence while preserving directory structures.

---

## Skills Gained

- Windows CMD
- File Management
- Directory Copying
- Backup Operations
- Digital Forensics
- Windows Administration


