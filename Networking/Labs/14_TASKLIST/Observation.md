# Lab 14 – TASKLIST Observations

---

## 1. Display Running Processes

- Executed the `tasklist` command to display all running processes.
- Observed the Image Name, PID, Session Name, Session Number, and Memory Usage of each process.
- Identified Windows system processes such as `svchost.exe`, `winlogon.exe`, `lsass.exe`, and `services.exe`.
- Observed user applications including Chrome, OneDrive, WhatsApp, and other installed software.
- Learned that TASKLIST provides a quick overview of all active processes running on the system.

---

## 2. Display Detailed Process Information

- Executed the `tasklist /v` command.
- Observed additional details including Status, User Name, CPU Time, and Window Title.
- Verified that active desktop applications displayed the Running status.
- Learned that verbose information is useful for monitoring system activity and troubleshooting applications.

---

## 3. Display Services Associated with Processes

- Executed the `tasklist /svc` command.
- Observed Windows services mapped to each process.
- Identified important services such as WinDefend, WlanSvc, Dnscache, Dhcp, RpcSs, EventLog, and CryptSvc.
- Verified that user applications displayed **N/A** because they are not Windows services.
- Learned that this command is useful for service management and incident response.

---

## 4. Display Loaded DLL Modules

- Executed the `tasklist /m` command.
- Observed DLL modules loaded by running processes.
- Identified common Windows DLLs including `kernel32.dll`, `ntdll.dll`, `user32.dll`, `advapi32.dll`, and `combase.dll`.
- Observed that different applications loaded different DLLs depending on their functionality.
- Learned that DLL inspection helps detect injected or suspicious modules during malware analysis.

---

## 5. Display TASKLIST Help Information

- Executed the `tasklist /?` command.
- Reviewed the syntax, parameters, filters, and examples provided by the built-in help.
- Learned about options such as `/V`, `/SVC`, `/M`, `/FI`, `/FO`, `/NH`, and `/APPS`.
- Understood how filters can be used to search for specific processes.
- Learned that built-in documentation is useful for understanding advanced command usage.
