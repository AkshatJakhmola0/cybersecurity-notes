# LAB REPORT

## Experiment Title

Advanced Text Searching Using the FINDSTR Command

---

## Objective

To learn how to use the Windows **FINDSTR** command to perform advanced text searches within files, including case-insensitive searches, exact phrase matching, multiple keyword searches, line numbering, and regular expression-based pattern matching.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)
- FINDSTR Command
- System Information File (`systeminfo.txt`)

---

## Commands Executed

```cmd
findstr /?

findstr "Windows" systeminfo.txt

findstr /i "windows" systeminfo.txt

findstr /n "OS" systeminfo.txt

findstr /b "OS" systeminfo.txt

findstr /c:"Microsoft Windows" systeminfo.txt

findstr "Memory Version" systeminfo.txt

findstr /r "^OS" systeminfo.txt
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the FINDSTR help menu.
3. Searched the `systeminfo.txt` file for the keyword **Windows**.
4. Performed a case-insensitive search using the `/i` option.
5. Displayed matching lines with line numbers using the `/n` option.
6. Searched for lines beginning with **OS** using the `/b` option.
7. Performed an exact phrase search using the `/c:` option.
8. Searched for multiple keywords in a single command.
9. Used a regular expression to locate lines starting with **OS**.

---

## Results

- Successfully displayed the FINDSTR help information.
- Retrieved Windows-related entries from the system information file.
- Performed successful case-insensitive searches.
- Displayed matching lines along with their line numbers.
- Filtered only the lines beginning with **OS**.
- Successfully searched for an exact phrase.
- Retrieved results containing multiple keywords.
- Used a regular expression to locate operating system information.

---

## Conclusion

The FINDSTR command successfully demonstrated advanced text searching capabilities within files. It provided efficient methods for filtering system information using keywords, exact phrases, line numbering, and regular expressions. The lab highlighted the usefulness of FINDSTR for log analysis, configuration review, troubleshooting, and cybersecurity investigations where accurate text searching is essential.

---

## Skills Gained

- Advanced Text Searching
- Windows Command Line
- Regular Expression Basics
- Log Analysis
- Configuration File Analysis
- Threat Hunting
- Digital Forensics
- Incident Response
