# Lab 25 – ASSOC Command

## Objective

The objective of this lab is to understand how the Windows **ASSOC** command displays file extension associations. This lab demonstrates how Windows maps file extensions such as `.txt`, `.exe`, `.html`, `.jpg`, and `.py` to their corresponding file types.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of file extensions
- No administrator privileges required for viewing associations

---

# Theory

The **ASSOC** command is a built-in Windows command-line utility used to display or modify file extension associations.

A file association links a file extension to a file type. For example:

```cmd
.txt=txtfilelegacy
```

This means that files with the `.txt` extension are associated with the file type `txtfilelegacy`.

The ASSOC command does not directly show the application used to open a file. It only displays the file type associated with the extension. The **FTYPE** command can then be used to view the command linked to that file type.

---

# Syntax

```cmd
assoc
```

```cmd
assoc .extension
```

Example:

```cmd
assoc .txt
```

---

# Commands Used

```cmd
assoc

assoc /?

assoc .txt

assoc .exe

assoc .pdf

assoc .html

assoc .jpg

assoc .py
```

---

# Steps Performed

### Step 1

Displayed all file extension associations configured on the system.

```cmd
assoc
```

---

### Step 2

Displayed the ASSOC help information.

```cmd
assoc /?
```

---

### Step 3

Checked the file type associated with text files.

```cmd
assoc .txt
```

The `.txt` extension was associated with:

```text
txtfilelegacy
```

---

### Step 4

Checked the file type associated with executable files.

```cmd
assoc .exe
```

The `.exe` extension was associated with:

```text
exefile
```

---

### Step 5

Checked the file type associated with PDF files.

```cmd
assoc .pdf
```

The system returned:

```text
File association not found for extension .pdf
```

---

### Step 6

Checked the file type associated with HTML files.

```cmd
assoc .html
```

The `.html` extension was associated with:

```text
htmlfile
```

---

### Step 7

Checked the file type associated with JPEG image files.

```cmd
assoc .jpg
```

The `.jpg` extension was associated with:

```text
jpegfile
```

---

### Step 8

Checked the file type associated with Python files.

```cmd
assoc .py
```

The `.py` extension was associated with:

```text
Python.File
```

---

# Expected Output

- A complete list of configured file extension associations.
- Help information for the ASSOC command.
- File type associated with `.txt`.
- File type associated with `.exe`.
- File type associated with `.html`.
- File type associated with `.jpg`.
- File type associated with `.py`.
- A message indicating that no association was found for `.pdf`.

---

# Key Findings

- The ASSOC command displays file extension-to-file-type mappings.
- The `.txt` extension was associated with `txtfilelegacy`.
- The `.exe` extension was associated with `exefile`.
- The `.html` extension was associated with `htmlfile`.
- The `.jpg` extension was associated with `jpegfile`.
- The `.py` extension was associated with `Python.File`.
- No command-line association was found for the `.pdf` extension.
- ASSOC and FTYPE can be used together to understand file handling in Windows.

---

# Cybersecurity Perspective

File associations are important in cybersecurity because attackers may attempt to modify them to redirect legitimate files to malicious programs.

Security professionals can use ASSOC to:

- Identify unexpected file extension mappings.
- Detect possible file association hijacking.
- Investigate suspicious executable behavior.
- Verify script and document file associations.
- Audit system configuration.
- Support malware analysis and incident response.
- Identify extensions associated with interpreters such as Python.

Unexpected changes to extensions such as `.exe`, `.bat`, `.cmd`, `.vbs`, or `.js` may indicate malicious activity or system misconfiguration.

---

# Challenges

- The ASSOC command may produce a very long output.
- Some file extensions may not have an ASSOC entry.
- ASSOC shows only the file type and not the actual opening program.
- Modifying critical associations can cause applications or files to stop working correctly.
- Some modern Windows associations are managed through application-specific settings.

---

# Interview Questions

### 1. What is the purpose of the ASSOC command?

**Answer:**

The ASSOC command displays or modifies file extension associations in Windows.

---

### 2. What does the following output mean?

```text
.exe=exefile
```

**Answer:**

It means that the `.exe` extension is associated with the Windows file type named `exefile`.

---

### 3. What is the difference between ASSOC and FTYPE?

**Answer:**

ASSOC maps a file extension to a file type, while FTYPE displays the command used to open that file type.

---

### 4. Why might ASSOC return “File association not found”?

**Answer:**

It means that no file type mapping is currently registered through the ASSOC command for that extension.

---

### 5. Why are file associations important in cybersecurity?

**Answer:**

Attackers may modify file associations to make legitimate files launch malicious programs or scripts.

---

### 6. Which command checks the association of Python files?

**Answer:**

```cmd
assoc .py
```

---

# Skills Gained

- File Association Enumeration
- Windows Command-Line Administration
- File Extension Analysis
- System Configuration Auditing
- Malware Persistence Awareness
- Incident Response Fundamentals
- Windows Troubleshooting
- Security Investigation Basics

---

# Lab Summary

In this lab, the **ASSOC** command was used to examine file extension associations on a Windows system. The complete association list was displayed, and individual extensions including `.txt`, `.exe`, `.pdf`, `.html`, `.jpg`, and `.py` were checked.

The results showed that text, executable, HTML, image, and Python files were linked to specific Windows file types. The PDF extension did not have an ASSOC entry. This lab demonstrated how Windows maps file extensions to file types and highlighted the importance of monitoring file associations during security investigations.
