# LAB REPORT

## Experiment Title

Windows Administration Mini Project – System Audit Using Command Prompt

---

## Objective

To perform a comprehensive Windows system administration audit using built-in Command Prompt utilities and collect information related to the operating system, network configuration, user accounts, running processes, services, storage utilization, installed drivers, and power settings.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)
- Built-in Windows Administrative Utilities

---

## Commands Executed

```cmd
systeminfo

hostname

whoami

ipconfig /all

net user

tasklist

sc query

fsutil volume diskfree C:

driverquery

powercfg /getactivescheme
```

---

## Procedure

1. Opened Command Prompt with administrative privileges.
2. Collected detailed operating system and hardware information using `systeminfo`.
3. Identified the system hostname using `hostname`.
4. Verified the currently logged-in user using `whoami`.
5. Retrieved detailed network configuration using `ipconfig /all`.
6. Enumerated local user accounts using `net user`.
7. Reviewed active processes using `tasklist`.
8. Examined running Windows services using `sc query`.
9. Collected storage information using `fsutil volume diskfree C:`.
10. Listed installed device drivers using `driverquery`.
11. Verified the active power scheme using `powercfg /getactivescheme`.
12. Documented findings and analyzed the collected information.

---

## Results

### System Information

- Operating System: Microsoft Windows 11 Home Single Language
- System Model: Dell Vostro 3420
- 64-bit Windows operating system detected.

### User Information

- Current user account identified successfully.
- Local user accounts were enumerated.

### Network Information

- Active network configuration was displayed.
- IPv4 address, gateway, and DNS information were successfully collected.

### Process and Service Analysis

- Running processes were listed successfully.
- Active Windows services were identified and reviewed.

### Storage Analysis

- Total Disk Capacity: Approximately 258.7 GB
- Used Space: Approximately 250.6 GB
- Free Space: Approximately 4.5 GB

### Driver Information

- Installed device drivers were successfully enumerated.

### Power Configuration

- Active Power Plan: Balanced

---

## Findings

### Positive Findings

- System information was successfully collected.
- Network connectivity was properly configured.
- User accounts were accessible for auditing.
- Services and processes were running normally.
- Driver information was available for review.
- Power management configuration was functioning correctly.

### Security and Administrative Concern

- The primary storage volume had critically low free space.
- Less than 5 GB of free storage remained on the system drive.
- High disk utilization may impact:
  - Windows Updates
  - System Performance
  - Virtual Memory Operations
  - Application Installation
  - Log Storage

---

## Conclusion

The Windows Administration Audit was completed successfully using native Command Prompt utilities. The project demonstrated practical system administration techniques including operating system auditing, user account enumeration, network analysis, process monitoring, service inspection, storage assessment, driver enumeration, and power configuration verification.

The audit identified low available disk space as the most significant issue requiring attention. Regular system audits and proactive storage management are recommended to maintain system performance, stability, and security.

---

## Skills Gained

- Windows Administration
- System Auditing
- Network Enumeration
- User Account Management
- Process Monitoring
- Service Analysis
- Storage Assessment
- Driver Enumeration
- Power Management
- Security Auditing
- Incident Response Fundamentals
- Command-Line Administration
