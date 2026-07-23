# SYSTEMINFO Command

## Objective

The objective of this lab is to understand the **SYSTEMINFO** command in Windows and learn how to retrieve detailed information about the operating system, hardware, processor, memory, BIOS, network configuration, and security settings. This command is widely used for system administration, troubleshooting, digital forensics, and cybersecurity.

---

## Prerequisites

- Windows 10/11 Operating System
- Command Prompt (CMD)
- Basic knowledge of Windows operating systems
- Administrative privileges are **not required**

---

## Theory

The **SYSTEMINFO** command is a built-in Windows command-line utility that displays comprehensive information about the local or a remote computer.

It provides details such as the operating system version, computer name, BIOS version, processor, installed memory, boot time, network adapters, domain or workgroup membership, installed hotfixes, virtualization features, and security configuration.

System administrators use this command to collect system information for troubleshooting and inventory management. Cybersecurity professionals use it during system enumeration, incident response, digital forensics, vulnerability assessments, and penetration testing to quickly understand the target system.

The SYSTEMINFO command also supports displaying information from remote computers when appropriate permissions are available.

---

## Syntax

```cmd
systeminfo
```

Display the output one page at a time:

```cmd
systeminfo | more
```

Filter specific information:

```cmd
systeminfo | findstr /B /C:"Host Name"
```

Display help:

```cmd
systeminfo /?
```

---

## Commands Used

```cmd
systeminfo
systeminfo | more
systeminfo | findstr /B /C:"Host Name"
systeminfo /?
```

---

## Additional / Reference Commands (Not Executed)

```cmd
systeminfo /fo table
systeminfo /fo list
systeminfo /fo csv
systeminfo /nh
systeminfo /s ComputerName
systeminfo /s ComputerName /u Domain\User /p Password
wmic computersystem get model
hostname
```

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `systeminfo` command to display complete system information.
3. Executed the `systeminfo | more` command to display the output page by page.
4. Executed the `systeminfo | findstr /B /C:"Host Name"` command to display only the hostname.
5. Executed the `systeminfo /?` command to view the available options and syntax.
6. Recorded the outputs and captured screenshots for documentation.

---

## Expected Output

- Displays detailed operating system information.
- Displays BIOS, processor, and memory details.
- Displays hostname and workgroup/domain information.
- Displays installed network adapters and IP configuration.
- Displays installed hotfixes and virtualization information.
- Supports filtering, paging, and multiple output formats.

---

## Cybersecurity Perspective

- Performs initial system enumeration during penetration testing.
- Assists SOC analysts during incident response.
- Helps identify operating system versions for vulnerability assessment.
- Displays hardware and network information useful for digital forensics.
- Assists in asset inventory and endpoint identification.
- Helps verify virtualization-based security and installed security features.
- Provides valuable information for malware analysis and forensic investigations.

---

## Challenges

- Produces a large amount of output that may require filtering.
- Some information may not be available depending on system configuration.
- Remote queries require appropriate permissions and network connectivity.
- Sensitive system information should be handled securely when sharing reports.

---

## Interview Questions

### 1. What is the purpose of the SYSTEMINFO command?

**Answer:**  
It displays detailed information about the Windows operating system, hardware, memory, processor, BIOS, network configuration, and installed updates.

---

### 2. Can SYSTEMINFO retrieve information from a remote computer?

**Answer:**  
Yes. It supports remote systems using the `/S` option when appropriate permissions are available.

---

### 3. What does the `systeminfo | more` command do?

**Answer:**  
It displays the output one page at a time, making long outputs easier to read.

---

### 4. What is the purpose of the `findstr` command with SYSTEMINFO?

**Answer:**  
It filters specific information from the command output, such as displaying only the hostname.

---

### 5. Which output formats are supported by SYSTEMINFO?

**Answer:**  
Table, List, and CSV.

---

### 6. Why is the SYSTEMINFO command important in cybersecurity?

**Answer:**  
It provides comprehensive system information used for system enumeration, vulnerability assessment, incident response, digital forensics, asset management, and security investigations.

---

## Skills Gained

- Learned to use the Windows SYSTEMINFO command.
- Retrieved operating system and hardware information.
- Identified processor, BIOS, and memory details.
- Examined network configuration and installed hotfixes.
- Used filtering and paging techniques to analyze command output.
- Improved Windows administration and troubleshooting skills.
- Developed practical knowledge useful for cybersecurity, digital forensics, and incident response.

---

## Lab Summary

In this lab, the Windows **SYSTEMINFO** command was used to collect detailed information about the operating system, hardware, memory, processor, BIOS, network configuration, and security settings. The experiment also demonstrated output paging with the `more` command and filtering using `findstr`. The SYSTEMINFO utility is an essential tool for Windows administration, troubleshooting, asset management, digital forensics, incident response, and cybersecurity investigations.

