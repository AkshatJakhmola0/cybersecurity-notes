# Lab Report

## Experiment Title

Study of the TASKKILL Command in Windows

---

## Objective

To learn how to use the TASKKILL command to terminate running processes using their Process ID (PID), Image Name, and forceful termination. The experiment also aims to understand the importance of process management in Windows administration and cybersecurity.

---

## Tools Used

- Windows 11
- Command Prompt
- Notepad

---

## Commands Executed

```cmd
taskkill /?

tasklist

taskkill /PID <PID>

taskkill /IM notepad.exe

taskkill /F /IM notepad.exe
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the built-in help using the `taskkill /?` command.
3. Launched the Notepad application.
4. Executed the `tasklist` command to identify the Process ID (PID) of Notepad.
5. Attempted to terminate the process using an incorrect PID and observed the error.
6. Identified the correct PID using `tasklist`.
7. Successfully terminated the process using `taskkill /PID <PID>`.
8. Opened Notepad again and terminated it using `taskkill /IM notepad.exe`.
9. Opened Notepad once more and forcefully terminated it using `taskkill /F /IM notepad.exe`.
10. Recorded the observations and captured screenshots.

---

## Results

Successfully displayed the TASKKILL help documentation, identified the running Notepad process, terminated it using its Process ID (PID), terminated it using its Image Name, and forcefully terminated it using the `/F` option. The experiment also demonstrated that Process IDs are dynamically assigned and must be verified before using the `/PID` option.

---

## Conclusion

The TASKKILL command is an essential Windows command-line utility for managing running processes. It enables users to terminate applications using either their Process ID or Image Name and supports forceful termination when required. The command is widely used by system administrators and cybersecurity professionals during troubleshooting, malware containment, incident response, and digital forensic investigations.

---

## Skills Gained

- Process Termination
- PID Identification
- Image Name Identification
- Forceful Process Termination
- Windows Process Management
- Windows Troubleshooting
- Incident Response Basics
- Malware Containment Fundamentals
