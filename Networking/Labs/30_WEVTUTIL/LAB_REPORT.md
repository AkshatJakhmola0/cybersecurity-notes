# LAB REPORT

## Experiment Title

Study of the WEVTUTIL Command in Windows Command Prompt

---

## Objective

To understand the working of the **WEVTUTIL** command and learn how to view, query, and analyze Windows Event Logs using Command Prompt.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

```cmd
wevtutil /?

wevtutil el

wevtutil gl System

wevtutil qe System /c:10

wevtutil qe Application /c:10

wevtutil qe Security /c:5

wevtutil gli System
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the WEVTUTIL help menu.
3. Listed all available Windows Event Logs.
4. Viewed the configuration of the System log.
5. Queried the latest 10 events from the System log.
6. Queried the latest 10 events from the Application log.
7. Queried the latest 5 events from the Security log.
8. Displayed general information about the System log.
9. Analyzed the output of each command.

---

## Results

- Successfully listed all available Windows Event Logs.
- Retrieved configuration details of the System log.
- Displayed recent events from the System and Application logs.
- Retrieved Security log events (Administrator privileges may be required).
- Displayed general information about the System log.
- Verified that WEVTUTIL can efficiently manage and query Windows Event Logs.

---

## Conclusion

The **WEVTUTIL** command is a powerful Windows utility for managing and analyzing Event Logs. It allows administrators and security professionals to view log configurations, retrieve event records, and monitor system, application, and security activities. These capabilities make WEVTUTIL an essential tool for Windows administration, troubleshooting, incident response, and digital forensic investigations.

---

## Skills Gained

- Windows Event Log Analysis
- Windows Administration
- Command-Line Management
- Security Monitoring
- Incident Response
- Digital Forensics
- Windows Troubleshooting
- Event Log Investigation
