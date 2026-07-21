# Netsh Command

## Objective

The objective of this experiment is to learn and understand the Windows **Netsh (Network Shell)** command-line utility. This lab demonstrates how to view network interface information, wireless network profiles, Wi-Fi connection details, and Windows Firewall configuration using Netsh. It also helps in understanding how Netsh is used for network administration, troubleshooting, and cybersecurity tasks.

---

## Prerequisites

- Windows 10/11 Operating System
- Command Prompt (CMD)
- Administrator privileges (recommended)
- Active network connection
- Basic knowledge of networking concepts

---

## Theory

**Netsh (Network Shell)** is a built-in Windows command-line utility used to configure, monitor, and troubleshoot networking components. It allows administrators to manage network interfaces, wireless settings, IP configurations, firewall settings, routing, and other network services directly from the command line.

Netsh is commonly used by:

- Network Administrators
- System Administrators
- Cybersecurity Professionals
- Penetration Testers
- SOC Analysts

Unlike GUI-based configuration tools, Netsh provides quick access to network settings and is useful for scripting and automation.

---

## Syntax

```cmd
netsh [context] [command]
```

Example:

```cmd
netsh wlan show profiles
```

---

## Commands Used

### 1. Open Netsh Shell

```cmd
netsh
```

Displays the Netsh interactive command shell.

---

### 2. Display Network Interfaces

```cmd
netsh interface show interface
```

Shows all available network interfaces along with their administrative state, operational status, and interface type.

---

### 3. Display Saved Wi-Fi Profiles

```cmd
netsh wlan show profiles
```

Displays all wireless network (Wi-Fi) profiles saved on the computer.

---

### 4. Display Connected Wi-Fi Information

```cmd
netsh wlan show interfaces
```

Displays detailed information about the currently connected wireless network, including SSID, BSSID, signal strength, radio type, channel, authentication method, and MAC address.

---

### 5. Display Windows Firewall Configuration

```cmd
netsh advfirewall show allprofiles
```

Displays the configuration of Windows Defender Firewall for the Domain, Private, and Public network profiles.

---

## Additional Commands for Learning (Not Executed)

```cmd
netsh interface ip show config
```

Displays IP configuration for network interfaces.

```cmd
netsh wlan show drivers
```

Displays information about the installed wireless adapter and supported features.

```cmd
netsh wlan export profile key=clear
```

Exports saved Wi-Fi profiles along with their passwords.

```cmd
netsh advfirewall firewall show rule name=all
```

Displays all configured Windows Firewall rules.

```cmd
netsh winsock reset
```

Resets the Windows Winsock catalog.

```cmd
netsh int ip reset
```

Resets the TCP/IP stack to its default configuration.

---

## Steps Performed

1. Opened Command Prompt.
2. Entered the Netsh interactive shell.
3. Displayed all available network interfaces.
4. Listed all saved Wi-Fi profiles.
5. Displayed detailed information about the currently connected Wi-Fi network.
6. Viewed Windows Firewall settings for all network profiles.
7. Recorded observations and captured screenshots for each command.

---

## Expected Output

- Netsh interactive shell opens successfully.
- Available network interfaces are displayed.
- Saved Wi-Fi profiles are listed.
- Details of the connected wireless network are displayed.
- Firewall configuration for Domain, Private, and Public profiles is displayed.

---

## Cybersecurity Perspective

Netsh is an essential Windows networking tool frequently used by cybersecurity professionals for system auditing, network troubleshooting, and security analysis.

Common cybersecurity uses include:

- Auditing active network interfaces
- Identifying saved Wi-Fi networks
- Verifying wireless security settings
- Checking Windows Firewall status
- Troubleshooting connectivity issues
- Resetting damaged network configurations
- Collecting system information during incident response
- Network reconnaissance during internal assessments

---

## Challenges

- Some commands require Administrator privileges.
- Wi-Fi-specific commands only work if a wireless adapter is present.
- Firewall information may vary depending on the system configuration.
- Certain commands may not return output if the corresponding service is disabled.

---

## Interview Questions

### Q1. What is Netsh?

**Answer:** Netsh (Network Shell) is a Windows command-line utility used to configure, monitor, and troubleshoot networking components.

---

### Q2. Which command displays saved Wi-Fi profiles?

**Answer:**

```cmd
netsh wlan show profiles
```

---

### Q3. Which command displays the currently connected Wi-Fi details?

**Answer:**

```cmd
netsh wlan show interfaces
```

---

### Q4. Which command displays Windows Firewall configuration?

**Answer:**

```cmd
netsh advfirewall show allprofiles
```

---

### Q5. Which command resets the TCP/IP stack?

**Answer:**

```cmd
netsh int ip reset
```

---

### Q6. Which command resets the Winsock catalog?

**Answer:**

```cmd
netsh winsock reset
```

---

## Skills Gained

- Learned to use the Windows Netsh utility.
- Viewed network interface information.
- Identified saved Wi-Fi profiles.
- Examined connected wireless network details.
- Reviewed Windows Firewall configuration.
- Improved Windows networking and troubleshooting skills.
- Gained practical knowledge useful for cybersecurity and system administration.

---

## Lab Summary

In this lab, the Windows **Netsh** utility was used to explore different networking components. Network interfaces, saved Wi-Fi profiles, connected wireless network details, and firewall configurations were successfully examined. The experiment demonstrated how Netsh serves as a powerful command-line tool for network management, troubleshooting, and cybersecurity tasks.
