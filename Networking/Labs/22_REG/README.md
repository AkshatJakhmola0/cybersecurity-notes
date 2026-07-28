# Lab 21 – REG (Windows Registry)

## Objective

The objective of this lab is to understand the Windows **REG** command and learn how to view and analyze Registry keys from the Command Prompt. This lab focuses on querying important Registry locations related to the operating system, desktop settings, installed applications, environment variables, startup programs, and system information.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrator privileges (recommended)
- Basic knowledge of the Windows Registry

---

# Theory

The **Windows Registry** is a hierarchical database that stores configuration settings for the Windows operating system, hardware devices, installed software, user preferences, and system services.

The **REG** command is a built-in Windows utility that allows administrators to query, modify, import, export, and manage Registry entries directly from the Command Prompt.

Registry analysis is an essential skill for system administrators and cybersecurity professionals because many Windows settings, startup programs, and malware persistence mechanisms are stored in the Registry.

---

# Syntax

```cmd
reg <operation> [options]
```

Examples:

```cmd
reg query "HKLM\SOFTWARE"

reg add "HKCU\Test"

reg delete "HKCU\Test"
```

---

# Commands Used

```cmd
reg

reg /?

reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion"

reg query "HKCU\Control Panel\Desktop"

reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall"

reg query "HKCU\Environment"

reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Run"

reg query "HKLM\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName"
```

---

# Steps Performed

### Step 1

Executed the `reg` command to view available Registry operations.

```cmd
reg
```

---

### Step 2

Displayed the REG help menu.

```cmd
reg /?
```

---

### Step 3

Queried the Windows operating system information stored in the Registry.

```cmd
reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion"
```

---

### Step 4

Viewed desktop-related Registry settings.

```cmd
reg query "HKCU\Control Panel\Desktop"
```

---

### Step 5

Listed installed applications registered in Windows.

```cmd
reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall"
```

---

### Step 6

Displayed the current user's environment variables.

```cmd
reg query "HKCU\Environment"
```

---

### Step 7

Viewed applications configured to start automatically when the user logs in.

```cmd
reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Run"
```

---

### Step 8

Displayed the active computer name stored in the Registry.

```cmd
reg query "HKLM\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName"
```

---

# Expected Output

- List of REG operations.
- REG help information.
- Windows version details.
- Desktop configuration values.
- Installed application Registry keys.
- User environment variables.
- Startup program entries.
- Active computer name.

---

# Key Findings

- The Windows Registry stores both system-wide and user-specific configuration settings.
- Registry data is organized into hierarchical keys and values.
- Installed applications are recorded under the Uninstall Registry key.
- Startup applications can be identified through the Run Registry key.
- Environment variables are stored in dedicated Registry locations.
- The REG command provides quick access to important Windows configuration data.

---

# Cybersecurity Perspective

The Windows Registry plays a significant role in cybersecurity investigations.

Security analysts use Registry queries to:

- Detect malware persistence mechanisms.
- Identify suspicious startup programs.
- Audit installed software.
- Verify operating system information.
- Examine user-specific configuration changes.
- Support digital forensic investigations.
- Detect unauthorized Registry modifications.
- Assist during incident response activities.

Many malware families create or modify Registry keys to maintain persistence after system reboots, making Registry analysis an essential investigative skill.

---

# Challenges

- Understanding the Registry hierarchy.
- Identifying the correct Registry path.
- Reading lengthy Registry outputs.
- Distinguishing legitimate Registry entries from suspicious ones.

---

# Interview Questions

### 1. What is the Windows Registry?

**Answer:**

The Windows Registry is a hierarchical database that stores operating system, software, hardware, and user configuration settings.

---

### 2. What is the purpose of the REG command?

**Answer:**

It is used to view and manage Windows Registry keys and values from the Command Prompt.

---

### 3. Which Registry key stores installed applications?

**Answer:**

```cmd
HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall
```

---

### 4. Which Registry key contains startup programs?

**Answer:**

```cmd
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
```

---

### 5. Why is Registry analysis important in cybersecurity?

**Answer:**

It helps identify persistence mechanisms, startup applications, malware modifications, and system configuration changes.

---

### 6. Which command displays Registry help?

**Answer:**

```cmd
reg /?
```

---

# Skills Gained

- Windows Registry Navigation
- Registry Enumeration
- Windows Administration
- Startup Program Analysis
- System Configuration Analysis
- Digital Forensics
- Threat Hunting
- Incident Response Fundamentals

---

# Lab Summary

In this lab, the **REG** command was used to examine important areas of the Windows Registry. Operating system information, desktop settings, installed applications, environment variables, startup programs, and computer configuration were successfully queried. The lab demonstrated how Registry analysis supports Windows administration and helps cybersecurity professionals investigate system configurations, identify persistence mechanisms, and perform forensic analysis.

| 08_computername.png | Active computer name |
