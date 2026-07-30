# Lab 26 – FTYPE Command

## Objective

To understand the Windows **FTYPE** command and learn how it maps file types to the commands or applications used to open them. This lab also demonstrates the relationship between **ASSOC** and **FTYPE**.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of Windows file extensions

---

## Theory

The **FTYPE** command displays or modifies the command associated with a Windows file type.

Windows determines how a file opens in two steps:

- **ASSOC** → Maps a file extension to a file type.
- **FTYPE** → Maps the file type to the command that opens it.

Example:

```text
.txt → txtfilelegacy  (ASSOC)

txtfilelegacy → notepad.exe "%1"  (FTYPE)
```

This mapping is important for Windows administration and cybersecurity because attackers may hijack file associations to execute malicious programs.

---

## Syntax

```cmd
ftype
ftype FileType
```

Example:

```cmd
ftype exefile
```

---

## Commands Used

```cmd
ftype
ftype /?
ftype exefile
ftype txtfilelegacy
ftype htmlfile
ftype jpegfile
ftype Python.File
ftype batfile
```

---

## Steps Performed

1. Displayed all registered file types.
2. Viewed the FTYPE help page.
3. Checked the command for executable files.
4. Checked the command for text file type.
5. Viewed the HTML file association.
6. Checked the JPEG file type.
7. Viewed the Python file association.
8. Viewed the Batch file association.

---

## Key Findings

- FTYPE displays commands associated with Windows file types.
- `exefile` executes using `"%1" %*`.
- `htmlfile` opens using Internet Explorer.
- `Python.File` is associated with `py.exe`.
- `batfile` executes directly from CMD.
- `txtfilelegacy` and `jpegfile` had no registered FTYPE command.

---

## Cybersecurity Perspective

The FTYPE command helps security professionals to:

- Detect file association hijacking.
- Verify executable mappings.
- Investigate malware persistence.
- Audit Windows configuration.
- Support digital forensic investigations.

---

## Interview Questions

**Q1. What does the FTYPE command do?**  
Displays or modifies commands associated with Windows file types.

**Q2. What is the difference between ASSOC and FTYPE?**  
ASSOC maps extensions to file types, while FTYPE maps file types to executable commands.

**Q3. Why is FTYPE useful in cybersecurity?**  
It helps detect malicious changes to file execution behavior.

**Q4. Which command displays the executable file type?**

```cmd
ftype exefile
```

**Q5. Why might "File type not found" appear?**  
Because no command is registered for that file type.

---

## Skills Gained

- Windows CMD
- File Type Analysis
- Windows File Associations
- Security Auditing
- Malware Investigation
- Digital Forensics
