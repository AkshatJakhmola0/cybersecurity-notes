# LAB REPORT

## Experiment Title

Study of the TREE Command in Windows Command Prompt

---

## Objective

To understand the working of the **TREE** command and learn how to display the hierarchical structure of directories and files in Windows using Command Prompt.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

```cmd
tree

tree /?

tree C:\Users

tree C:\Users /F

tree C:\Windows

tree C:\Windows\System32

tree "%USERPROFILE%\Documents"

tree "%USERPROFILE%\Desktop"
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `tree` command to display the current directory structure.
3. Viewed the help information using `tree /?`.
4. Displayed the directory structure of `C:\Users`.
5. Used the `/F` option to display both folders and files.
6. Examined the structure of the `C:\Windows` directory.
7. Viewed the hierarchy of the `System32` directory.
8. Displayed the Documents and Desktop folder structures.
9. Recorded and analyzed the results.

---

## Results

- Successfully displayed the hierarchical directory structure.
- The default `tree` command listed only folders.
- The `/F` option displayed both folders and files.
- The `C:\Windows` and `System32` directories contained a large number of system folders.
- The Documents and Desktop outputs reflected the current user's directory structure.

---

## Conclusion

The **TREE** command provides a clear hierarchical view of directories and files in Windows. It is useful for understanding folder organization, documenting file systems, troubleshooting, and performing digital forensic investigations. The `/F` option offers a more detailed view by including files along with directories.

---

## Skills Gained

- Windows Command-Line Administration
- Directory Structure Analysis
- File System Navigation
- Windows System Exploration
- Digital Forensics
- Security Investigation
- System Documentation
- Troubleshooting
