# Observations – Windows Incident Response Mini Project

## 1. User Identification (`whoami`)

* Successfully identified the currently logged-in user.
* Verified the security context under which the investigation was performed.
* Useful for accountability and activity tracing.

---

## 2. Host Identification (`hostname`)

* Successfully identified the workstation hostname.
* Hostname serves as a unique identifier within the network.
* Important for incident tracking and asset management.

---

## 3. System Information (`systeminfo`)

* Collected detailed operating system information.
* Retrieved OS version, architecture, hardware details, and installation information.
* Useful for vulnerability assessment and incident investigation.

---

## 4. Network Configuration (`ipconfig /all`)

* Displayed detailed network adapter information.
* Retrieved IP address, subnet mask, gateway, DNS servers, and adapter details.
* Confirmed active network connectivity.
* Useful for identifying network exposure and communication paths.

---

## 5. Active Network Connections (`netstat -ano`)

* Displayed active TCP and UDP network connections.
* Identified listening ports and active communication sessions.
* Displayed Process IDs (PIDs) associated with network activity.
* Useful for identifying suspicious or unauthorized communications.

---

## 6. Running Processes (`tasklist`)

* Enumerated active processes running on the system.
* Displayed process names, PIDs, and memory usage information.
* Useful for identifying abnormal or unauthorized applications.
* Provides visibility into current system activity.

---

## 7. Process-Service Mapping (`tasklist /svc`)

* Displayed services associated with running processes.
* Allowed correlation between services and host processes.
* Useful during malware and persistence investigations.
* Helps identify suspicious service activity.

---

## 8. User Account Enumeration (`net user`)

* Listed all local user accounts configured on the system.
* Included built-in and manually created accounts.
* Useful for identifying unauthorized or inactive accounts.
* Supports user account auditing activities.

---

## 9. Administrator Group Review (`net localgroup administrators`)

* Displayed users and groups with administrative privileges.
* Useful for reviewing privileged account assignments.
* Helps detect privilege escalation or unauthorized access.
* Important for security assessments.

---

## 10. Scheduled Task Analysis (`schtasks`)

* Enumerated scheduled tasks configured on the system.
* Displayed automated tasks and execution schedules.
* Useful for identifying persistence mechanisms.
* Helps detect unauthorized automated execution.

---

## 11. Driver Enumeration (`driverquery`)

* Listed installed device drivers and related information.
* Provided visibility into kernel-level components.
* Useful for detecting unauthorized or suspicious drivers.
* Supports system integrity verification.

---

## 12. Startup Program Analysis (`wmic startup get caption,command`)

* Displayed applications configured to start automatically.
* Identified persistence locations used by software.
* Useful for detecting unwanted startup entries.
* Commonly reviewed during malware investigations.

---

## 13. Open File Analysis (`openfiles /query`)

* Reviewed currently open and shared files.
* Provided visibility into active file usage.
* Useful for identifying remote access and file activity.
* Supports forensic evidence collection.

---

## 14. Overall Analysis

* Successfully collected system evidence using native Windows commands.
* Reviewed users, processes, services, network activity, startup entries, scheduled tasks, and drivers.
* Investigated common Indicators of Compromise (IOCs).
* Demonstrated a basic Windows incident response and forensic triage workflow.
* Provided practical experience in evidence collection and security analysis.
