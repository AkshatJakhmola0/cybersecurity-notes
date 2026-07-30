# LAB REPORT

## Experiment Title

Understanding File Extension Associations Using the ASSOC Command

---

## Objective

To study the Windows **ASSOC** command and understand how file extensions are associated with file types in Windows. The experiment also demonstrates how to view file associations for different file extensions without modifying the system configuration.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)
- ASSOC Command

---

## Commands Executed

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

## Procedure

1. Opened Command Prompt.
2. Executed the `assoc` command to display all registered file extension associations.
3. Displayed the help information using `assoc /?`.
4. Checked the association of `.txt` files.
5. Checked the association of `.exe` files.
6. Checked the association of `.pdf` files.
7. Checked the association of `.html` files.
8. Checked the association of `.jpg` files.
9. Checked the association of `.py` files.
10. Compared the returned file types for different extensions.

---

## Results

- Successfully displayed all file extension associations configured on the system.
- Displayed the syntax and usage of the ASSOC command.
- The `.txt` extension was associated with `txtfilelegacy`.
- The `.exe` extension was associated with `exefile`.
- The `.html` extension was associated with `htmlfile`.
- The `.jpg` extension was associated with `jpegfile`.
- The `.py` extension was associated with `Python.File`.
- The `.pdf` extension returned **"File association not found for extension .pdf"**, indicating no ASSOC entry was available for that extension.

---

## Conclusion

The ASSOC command successfully displayed file extension-to-file-type mappings in Windows. It helped identify how the operating system recognizes different file formats and demonstrated that some extensions may not have an ASSOC entry. Understanding file associations is important for Windows administration, troubleshooting, malware analysis, and detecting file association hijacking during cybersecurity investigations.

---

## Skills Gained

- Windows Command-Line Administration
- File Association Analysis
- Windows File Type Identification
- System Configuration Auditing
- Cybersecurity Investigation
- Malware Persistence Awareness
- Windows Troubleshooting
- Incident Response Fundamentals
