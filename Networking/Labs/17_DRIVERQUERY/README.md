# Lab 17 – DRIVERQUERY Command

## Objective

The objective of this lab is to understand the usage of the **DRIVERQUERY** command in Windows. This command is used to display information about installed device drivers, view detailed driver information, verify digitally signed drivers, and display driver information in different output formats. The lab also demonstrates the importance of device drivers in Windows administration and cybersecurity.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Administrative privileges (recommended)
- Basic understanding of Windows device drivers

---

## Theory

The **DRIVERQUERY** command is a built-in Windows command-line utility that displays information about all installed device drivers on a local or remote computer. It provides details such as driver names, driver types, start modes, current status, paths, manufacturers, and digital signatures.

System administrators use DRIVERQUERY to troubleshoot hardware issues, verify driver installations, and collect driver inventories. Cybersecurity professionals use it during incident response and forensic investigations to identify suspicious, outdated, or unsigned drivers that could indicate malicious activity.

---

## Syntax

```cmd
driverquery [options]
```

---

## Commands Used

```cmd
driverquery

driverquery /v

driverquery /fo csv

driverquery /si

driverquery /?
```

---

## Additional Reference Commands (Not Executed)

```cmd
driverquery /fo list

driverquery /fo table

driverquery /nh

driverquery /s ComputerName

driverquery /s ComputerName /u Username /p Password
```

---

## Steps Performed

1. Displayed the list of installed device drivers.
2. Displayed detailed information about each driver.
3. Displayed driver information in CSV format.
4. Displayed information about digitally signed drivers.
5. Displayed the built-in help menu for the DRIVERQUERY command.

---

## Expected Output

- List of installed device drivers.
- Detailed driver information.
- Driver information in CSV format.
- List of digitally signed drivers.
- DRIVERQUERY help documentation.

---

## Key Findings

- Successfully listed installed device drivers.
- Viewed detailed information including driver path, status, and start mode.
- Learned how to display driver information in CSV format.
- Verified digitally signed drivers installed on the system.
- Understood that Windows supports querying drivers on local as well as remote systems.
- Learned that digital signatures help verify the authenticity of device drivers.

---

## Cybersecurity Perspective

Device drivers operate in the Windows kernel and have high system privileges. Attackers may install malicious or vulnerable drivers to bypass security controls, hide malware, escalate privileges, or maintain persistence. During incident response and digital forensic investigations, security analysts use the DRIVERQUERY command to identify installed drivers, verify their digital signatures, and detect suspicious or unauthorized kernel drivers.

---

## Challenges

- The verbose (`/v`) output contains a large amount of information and may require filtering for easier analysis.
- Administrative privileges may be required to obtain complete driver information on some systems.
- Unsigned or unknown drivers should be investigated carefully before taking any action.

---

## Interview Questions

### 1. What is the DRIVERQUERY command?

It is a Windows command-line utility used to display information about installed device drivers.

---

### 2. Which command displays detailed driver information?

```cmd
driverquery /v
```

---

### 3. Which command displays signed drivers only?

```cmd
driverquery /si
```

---

### 4. Which command displays driver information in CSV format?

```cmd
driverquery /fo csv
```

---

### 5. Can DRIVERQUERY query remote computers?

Yes. It supports querying remote systems using the `/S`, `/U`, and `/P` parameters.

---

### 6. Why is DRIVERQUERY important in cybersecurity?

It helps security professionals identify installed drivers, verify digital signatures, detect suspicious or unsigned drivers, investigate kernel-level threats, and support digital forensic investigations.

---

## Skills Gained

- Windows Driver Enumeration
- Driver Analysis
- Digital Signature Verification
- Windows Troubleshooting
- System Administration
- Incident Response
- Digital Forensics
- Kernel Security Fundamentals

---

## Lab Summary

This lab demonstrated how to use the DRIVERQUERY command to enumerate installed device drivers, display detailed driver information, verify digitally signed drivers, and export driver details in different formats. Understanding DRIVERQUERY is valuable for Windows administration, hardware troubleshooting, cybersecurity operations, incident response, and forensic analysis.

---

## Evidence

Screenshots included:

- 01_driverquery_basic.png
- 02_driverquery_verbose.png
- 03_driverquery_csv.png
- 04_driverquery_signed.png
- 05_driverquery_help.png
