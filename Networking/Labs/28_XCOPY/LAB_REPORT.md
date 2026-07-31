# LAB REPORT

## Experiment Title

Study of the XCOPY Command in Windows Command Prompt

---

## Objective

To understand the working of the **XCOPY** command and learn how to copy files and directories using different command-line options in Windows.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

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

## Procedure

1. Opened Command Prompt.
2. Displayed the help information for the XCOPY command.
3. Created a test directory named `XCOPY_Lab`.
4. Created a sample text file inside the directory.
5. Copied the directory using the default XCOPY command.
6. Used the `/S` option to copy subdirectories.
7. Used the `/E` option to copy all directories, including empty ones.
8. Used the `/Y` option to overwrite existing files without confirmation.
9. Verified that the destination contained the copied file.

---

## Results

- Successfully created the test directory and sample file.
- The default XCOPY command copied the file successfully.
- The `/S` option copied directories and subdirectories.
- The `/E` option copied the complete directory structure.
- The `/Y` option copied files without displaying an overwrite confirmation.
- The copied file was successfully verified at the destination.

---

## Conclusion

The **XCOPY** command is a powerful Windows utility for copying files and directories. It supports recursive copying, complete directory backups, and automatic overwriting of existing files through command-line options. The command is widely used for backup, file migration, and system administration tasks.

---

## Skills Gained

- Windows Command-Line Administration
- File and Directory Management
- Data Backup Operations
- Recursive Directory Copying
- Windows System Administration
- Digital Forensics
- Security Investigation
- Command-Line Automation
