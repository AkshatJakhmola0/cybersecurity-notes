# GETMAC Command

## Objective

The objective of this lab is to understand the **GETMAC** command in Windows and learn how to retrieve the **Media Access Control (MAC) addresses** of network adapters. This command helps identify network interfaces and is useful for network administration, troubleshooting, asset management, digital forensics, and cybersecurity.

---

## Prerequisites

- Windows 10/11 Operating System
- Command Prompt (CMD)
- Basic understanding of computer networks
- Administrative privileges are **not required**

---

## Theory

The **GETMAC** command is a built-in Windows command-line utility that displays the **Physical (MAC) Address** of network adapters installed on a computer.

A **MAC (Media Access Control) Address** is a unique 48-bit hardware identifier assigned to a network interface by the manufacturer. It is used for communication within a Local Area Network (LAN) and operates at the **Data Link Layer (Layer 2)** of the OSI Model.

The GETMAC command can display adapter information in different formats such as **Table**, **List**, and **CSV**. It also supports verbose output for displaying additional details about each network adapter and can retrieve MAC address information from remote systems when appropriate permissions are available.

---

## Syntax

```cmd
getmac
```

Verbose output:

```cmd
getmac /v
```

List format:

```cmd
getmac /fo list
```

CSV format:

```cmd
getmac /fo csv
```

Display help:

```cmd
getmac /?
```

---

## Commands Used

```cmd
getmac
getmac /v
getmac /fo list
getmac /fo csv
getmac /?
```

---

## Additional / Reference Commands (Not Executed)

```cmd
getmac /nh
getmac /fo table
getmac /s ComputerName
getmac /s ComputerName /u Domain\User /p Password
ipconfig /all
```

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `getmac` command to display the MAC addresses of all network adapters.
3. Executed the `getmac /v` command to display detailed information about each adapter.
4. Executed the `getmac /fo list` command to display the output in List format.
5. Executed the `getmac /fo csv` command to display the output in CSV format.
6. Executed the `getmac /?` command to view the available options and syntax.
7. Recorded the outputs and captured screenshots for documentation.

---

## Expected Output

- Displays the MAC addresses of installed network adapters.
- Identifies active and disconnected network interfaces.
- Displays detailed adapter information in verbose mode.
- Supports Table, List, and CSV output formats.
- Displays the available command-line options with the help command.

---

## Cybersecurity Perspective

- Identifies network devices during incident response.
- Assists in endpoint inventory and asset management.
- Helps detect unauthorized devices connected to a network.
- Useful for MAC address filtering and access control.
- Supports digital forensics by identifying hardware involved in network communication.
- Helps correlate devices during network investigations and penetration testing.

---

## Challenges

- Displays information only for Windows-recognized network adapters.
- Does not display IP address configuration.
- Remote system queries require appropriate permissions and network connectivity.
- MAC addresses can be spoofed and should not be relied upon as the only method of device identification.

---

## Interview Questions

### 1. What is the purpose of the GETMAC command?

**Answer:**  
It displays the MAC (Physical) addresses of network adapters installed on a Windows system.

---

### 2. What is a MAC Address?

**Answer:**  
A MAC Address is a unique hardware identifier assigned to a network interface card (NIC) for communication on a local network.

---

### 3. Which OSI layer uses the MAC Address?

**Answer:**  
The Data Link Layer (Layer 2).

---

### 4. What does the `/V` option do?

**Answer:**  
It displays detailed (verbose) information, including the connection name, adapter name, MAC address, and transport name.

---

### 5. Which output formats are supported by GETMAC?

**Answer:**  
Table, List, and CSV.

---

### 6. Can GETMAC retrieve information from a remote computer?

**Answer:**  
Yes. It supports remote systems using the `/S` option when appropriate permissions are available.

---

## Skills Gained

- Learned to use the Windows GETMAC command.
- Identified MAC addresses of network adapters.
- Distinguished between active and disconnected network interfaces.
- Displayed adapter information in Table, List, and CSV formats.
- Understood the importance of MAC addresses in networking.
- Improved Windows networking and troubleshooting skills.
- Developed practical knowledge useful for system administration, digital forensics, and cybersecurity.

---

## Lab Summary

In this lab, the Windows **GETMAC** command was used to examine the MAC addresses of installed network adapters. The experiment demonstrated how to retrieve physical addresses, view detailed adapter information, and display output in multiple formats. The lab highlighted the importance of MAC addresses in device identification, network management, troubleshooting, digital forensics, and cybersecurity investigations.
