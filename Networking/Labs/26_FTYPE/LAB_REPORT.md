# LAB REPORT

## Experiment Title

Study of the FTYPE Command in Windows Command Prompt

---

## Objective

To understand the working of the **FTYPE** command and examine how Windows maps file types to the commands or applications used to open them.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

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

## Procedure

1. Opened Command Prompt.
2. Executed the `ftype` command to list all registered file types.
3. Viewed the help information using `ftype /?`.
4. Checked the command associated with the `exefile` file type.
5. Checked the `txtfilelegacy` file type.
6. Viewed the command associated with `htmlfile`.
7. Checked the `jpegfile` file type.
8. Viewed the command associated with `Python.File`.
9. Viewed the command associated with `batfile`.
10. Recorded and analyzed the outputs.

---

## Results

- Displayed all registered file types and their associated commands.
- `exefile` was configured as:

```text
"%1" %*
```

- `htmlfile` was associated with Internet Explorer.
- `Python.File` was associated with the Python Launcher (`py.exe`).
- `batfile` executed directly through Command Prompt.
- `txtfilelegacy` returned **"File type not found."**
- `jpegfile` also returned **"File type not found."**

---

## Conclusion

The **FTYPE** command successfully displayed the executable commands associated with different Windows file types. It demonstrated how Windows determines which application is used to open a particular file type. The experiment also showed that some file types may not have a registered FTYPE entry. Understanding these mappings is valuable for Windows administration, troubleshooting, malware analysis, and detecting file association hijacking.

---

## Skills Gained

- Windows Command-Line Administration
- File Type Analysis
- Windows File Associations
- System Configuration Auditing
- Malware Investigation
- Digital Forensics
- Incident Response
- Windows Troubleshooting
```
