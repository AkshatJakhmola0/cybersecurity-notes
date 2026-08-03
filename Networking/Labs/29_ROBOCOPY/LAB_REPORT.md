# LAB REPORT

## Experiment Title

Study of the ROBOCOPY Command in Windows Command Prompt

---

## Objective

To understand the working of the **ROBOCOPY** command and learn how to copy, synchronize, and mirror files and directories using different command-line options.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

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

## Procedure

1. Opened Command Prompt.
2. Displayed the help information for the ROBOCOPY command.
3. Created a test source directory.
4. Created a sample text file inside the source directory.
5. Performed a basic copy to the destination folder.
6. Used the `/E` option to copy all directories.
7. Used the `/S` option to copy non-empty directories.
8. Used the `/MIR` option to synchronize the destination with the source.
9. Verified that the file was successfully copied.

---

## Results

- Successfully created the source directory and sample file.
- ROBOCOPY automatically created the destination directory.
- The initial copy successfully copied the test file.
- `/E` copied all directories, including empty ones.
- `/S` copied only non-empty directories.
- `/MIR` synchronized the destination with the source.
- Subsequent executions skipped unchanged files automatically.
- No failed or mismatched files were reported during the experiment.

---

## Conclusion

The **ROBOCOPY** command is a reliable and efficient Windows utility for copying, synchronizing, and backing up files and directories. It automatically skips unchanged files, provides detailed copy statistics, and supports advanced options such as directory mirroring. These features make it an essential tool for Windows administration, data migration, backup operations, and digital forensic investigations.

---

## Skills Gained

- Windows Command-Line Administration
- File and Directory Synchronization
- Backup Operations
- Windows File Management
- System Administration
- Digital Forensics
- Security Investigation
- Data Migration
