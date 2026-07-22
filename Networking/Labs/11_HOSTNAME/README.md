# HOSTNAME Command

## Objective

The objective of this lab is to understand the **HOSTNAME** command in Windows and learn how to identify the name of the local computer. This command is useful for system administration, network troubleshooting, device identification, and cybersecurity investigations.

---

## Prerequisites

- Windows 10/11 Operating System
- Command Prompt (CMD)
- Basic understanding of computer networks
- Administrative privileges are **not required**

---

## Theory

The **HOSTNAME** command is a built-in Windows command-line utility that displays the name assigned to the current computer.

A hostname is a unique name used to identify a device on a network. Instead of remembering IP addresses, users and network services can identify systems using their hostnames. In Windows environments, hostnames are commonly used in DNS, Active Directory, file sharing, remote administration, and network troubleshooting.

The HOSTNAME command is read-only and does not modify any system settings.

---

## Syntax

```cmd
hostname
```

To display help information:

```cmd
hostname /?
```

---

## Commands Used

```cmd
hostname
hostname /?
```

---

## Additional / Reference Commands (Not Executed)

```cmd
echo %COMPUTERNAME%
systeminfo | findstr /B /C:"Host Name"
whoami
ipconfig /all
```

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `hostname` command to display the system hostname.
3. Executed the `hostname /?` command to view the built-in help information.
4. Recorded the output.
5. Captured screenshots for documentation.

---

## Expected Output

- Displays the hostname of the current computer.
- Shows a brief description and syntax when executed with the `/ ?` option.
- Does not make any changes to the system configuration.

---

## Cybersecurity Perspective

- Helps identify the local machine during incident response and forensic investigations.
- Useful for asset inventory and endpoint identification.
- Assists security analysts in correlating security logs with specific devices.
- Commonly used during penetration testing and network enumeration.
- Supports system administration and Active Directory troubleshooting.

---

## Challenges

- The command only displays the hostname and offers limited functionality.
- Hostnames can be manually changed by administrators, so they should not be used as the sole method of system identification.
- Hostnames alone do not provide network configuration details such as IP or MAC addresses.

---

## Interview Questions

### 1. What is the purpose of the HOSTNAME command?

**Answer:**  
It displays the name of the current computer.

---

### 2. Why is a hostname important?

**Answer:**  
It uniquely identifies a computer on a network and is used in DNS, Active Directory, and network communication.

---

### 3. Does the HOSTNAME command require administrator privileges?

**Answer:**  
No. It can be executed by any standard user.

---

### 4. Can the HOSTNAME command change the computer name?

**Answer:**  
No. It only displays the current hostname.

---

### 5. Where are hostnames commonly used?

**Answer:**  
DNS, Active Directory, network management, remote administration, file sharing, troubleshooting, and cybersecurity investigations.

---

## Skills Gained

- Learned to use the Windows HOSTNAME command.
- Identified the hostname of the local computer.
- Understood the role of hostnames in computer networks.
- Gained basic knowledge of device identification.
- Improved Windows command-line skills.
- Developed foundational knowledge useful for system administration and cybersecurity.

---

## Lab Summary

In this lab, the Windows **HOSTNAME** command was used to identify the local computer name. The experiment demonstrated how hostnames are used to uniquely identify systems on a network and highlighted their importance in Windows administration, DNS, Active Directory, troubleshooting, and cybersecurity. Although simple, the HOSTNAME command is a fundamental utility for network and system administrators.
