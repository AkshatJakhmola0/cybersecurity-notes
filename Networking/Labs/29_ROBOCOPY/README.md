
# Lab 29 – ROBOCOPY Command

## Objective

To understand the Windows **ROBOCOPY** command and learn how to copy files and directories using different options for backup, synchronization, and data migration.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of files and directories

---

## Theory

**ROBOCOPY (Robust File Copy)** is an advanced file-copy utility built into Windows. It is designed for reliable copying of files and directories, especially for backups and large data transfers.

Unlike `COPY` and `XCOPY`, ROBOCOPY automatically skips unchanged files, supports directory synchronization, retries failed copies, and preserves file attributes.

---

## Syntax

```cmd
robocopy Source Destination [Options]
```

Example:

```cmd
robocopy C:\Data D:\Backup /E
```

---

## Commands Used

```cmd
robocopy /?

mkdir C:\ROBOCOPY_Source

echo Test File > C:\ROBOCOPY_Source\test.txt

robocopy C:\ROBOCOPY_Source "%USERPROFILE%\Desktop\ROBOCOPY_Backup"

robocopy C:\ROBOCOPY_Source "%USERPROFILE%\Desktop\ROBOCOPY_Backup" /E

robocopy C:\ROBOCOPY_Source "%USERPROFILE%\Desktop\ROBOCOPY_Backup" /S

robocopy C:\ROBOCOPY_Source "%USERPROFILE%\Desktop\ROBOCOPY_Backup" /MIR
```

---

## Steps Performed

1. Displayed the ROBOCOPY help menu.
2. Created a test source directory.
3. Created a sample text file.
4. Copied the source directory to the destination.
5. Copied all directories using `/E`.
6. Copied non-empty directories using `/S`.
7. Mirrored the source and destination using `/MIR`.
8. Verified the copied file.

---

## Key Findings

- ROBOCOPY automatically created the destination directory.
- The initial copy successfully copied the test file.
- `/E` copied all directories, including empty ones.
- `/S` copied non-empty directories.
- `/MIR` synchronized the destination with the source.
- Existing unchanged files were skipped automatically.
- ROBOCOPY displayed detailed copy statistics after each operation.

---

## Cybersecurity Perspective

ROBOCOPY is useful for:

- Creating forensic backups.
- Collecting evidence from systems.
- Migrating user data.
- Synchronizing backup directories.
- Copying logs and investigation artifacts.

---

## Interview Questions

**Q1. What is ROBOCOPY used for?**  
Copies and synchronizes files and directories.

**Q2. What does `/E` do?**  
Copies all subdirectories, including empty ones.

**Q3. What does `/S` do?**  
Copies subdirectories except empty ones.

**Q4. What does `/MIR` do?**  
Mirrors the destination with the source, including deleting extra files in the destination.

**Q5. Why is ROBOCOPY preferred over XCOPY?**  
It is faster, more reliable, supports retries, synchronization, and skips unchanged files automatically.

---

## Skills Gained

- Windows Command-Line Administration
- File Synchronization
- Backup Operations
- Directory Management
- Windows Administration
- Digital Forensics
