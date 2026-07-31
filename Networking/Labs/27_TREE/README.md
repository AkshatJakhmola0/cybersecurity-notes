
# Lab 27 – TREE Command

## Objective

To understand the Windows **TREE** command and learn how to display the hierarchical structure of directories and files using Command Prompt.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of Windows directories

---

## Theory

The **TREE** command displays the folder structure of a specified drive or directory in a tree-like format. By default, it displays only folders, while the `/F` option displays both folders and files.

The command is useful for visualizing directory structures, documenting file systems, troubleshooting, and digital forensic investigations.

---

## Syntax

```cmd
tree [Drive:][Path]
tree [Drive:][Path] /F
```

Example:

```cmd
tree C:\Users
```

---

## Commands Used

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

## Steps Performed

1. Displayed the directory tree of the current location.
2. Viewed the TREE command help menu.
3. Displayed the folder structure of `C:\Users`.
4. Displayed folders and files in `C:\Users` using `/F`.
5. Viewed the Windows directory structure.
6. Examined the `System32` directory.
7. Displayed the Documents folder structure.
8. Displayed the Desktop folder structure.

---

## Key Findings

- TREE displays directories in a hierarchical format.
- By default, only folders are displayed.
- The `/F` option includes files in the output.
- Large directories such as `System32` produce extensive output.
- The command is useful for understanding folder organization and file locations.

---

## Cybersecurity Perspective

The TREE command helps security professionals to:

- Understand directory structures during investigations.
- Identify suspicious folders.
- Document system layouts.
- Assist in malware analysis.
- Support digital forensic examinations.

---

## Interview Questions

**Q1. What is the purpose of the TREE command?**  
Displays the hierarchical structure of directories.

**Q2. Which option displays files as well as folders?**  
`/F`

**Q3. What is the default behavior of TREE?**  
It displays only directories.

**Q4. Why is TREE useful in cybersecurity?**  
It helps analyze and document directory structures during investigations.

**Q5. Which command displays the Windows directory structure?**

```cmd
tree C:\Windows
```

---

## Skills Gained

- Windows Command-Line Navigation
- Directory Structure Analysis
- File System Visualization
- Windows Administration
- Digital Forensics
- Security Investigation
