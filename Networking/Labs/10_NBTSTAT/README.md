
# NBTSTAT Command

## Objective

The objective of this experiment is to learn and understand the Windows **NBTSTAT (NetBIOS over TCP/IP Statistics)** command. This lab demonstrates how to view local NetBIOS names, inspect the NetBIOS name cache, examine name resolution statistics, and view active NetBIOS sessions. It also helps in understanding how NetBIOS is used in Windows networking and its importance in network troubleshooting and cybersecurity.

---

## Prerequisites

- Windows 10/11 Operating System
- Command Prompt (CMD)
- Administrator privileges (recommended)
- Active network connection
- Basic knowledge of TCP/IP and NetBIOS

---

## Theory

**NBTSTAT (NetBIOS over TCP/IP Statistics)** is a built-in Windows command-line utility used to display NetBIOS protocol statistics, local and remote NetBIOS names, name cache information, and active NetBIOS sessions.

NetBIOS (Network Basic Input/Output System) enables applications on different computers to communicate over a local network. Although modern Windows networks mainly use DNS, NetBIOS is still found in many enterprise environments for compatibility and legacy support.

Cybersecurity professionals use the `nbtstat` command to collect information during network enumeration, incident response, and troubleshooting.

---

## Syntax

```cmd
nbtstat [option]
```

Example:

```cmd
nbtstat -n
```

---

## Commands Used

### 1. Display Help Information

```cmd
nbtstat
```

Displays the syntax, options, and usage information for the `nbtstat` command.

---

### 2. Display Local NetBIOS Names

```cmd
nbtstat -n
```

Displays the NetBIOS names registered on the local computer.

---

### 3. Display NetBIOS Name Cache

```cmd
nbtstat -c
```

Displays the NetBIOS name cache containing recently resolved remote NetBIOS names.

---

### 4. Display Name Resolution Statistics

```cmd
nbtstat -r
```

Displays statistics showing how many NetBIOS names were resolved by broadcast and by WINS.

---

### 5. Display NetBIOS Sessions

```cmd
nbtstat -s
```

Displays the current NetBIOS sessions and their status.

---

## Additional Commands for Learning (Not Executed)

```cmd
nbtstat -a <hostname>
```

Displays the NetBIOS name table of a remote computer using its hostname.

```cmd
nbtstat -A <IP_Address>
```

Displays the NetBIOS name table of a remote computer using its IP address.

```cmd
nbtstat -R
```

Purges and reloads the NetBIOS name cache.

```cmd
nbtstat -RR
```

Releases and refreshes NetBIOS names registered with a WINS server.

```cmd
nbtstat -S
```

Displays NetBIOS sessions with IP addresses instead of hostnames.

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `nbtstat` command to display help information.
3. Displayed the local NetBIOS name table using `nbtstat -n`.
4. Viewed the NetBIOS name cache using `nbtstat -c`.
5. Examined NetBIOS name resolution statistics using `nbtstat -r`.
6. Displayed active NetBIOS sessions using `nbtstat -s`.
7. Recorded observations and captured screenshots for each command.

---

## Expected Output

- Help information for the NBTSTAT utility.
- Local NetBIOS names registered on the computer.
- Cached NetBIOS name entries.
- Name resolution statistics.
- Active NetBIOS session information.

---

## Cybersecurity Perspective

The `nbtstat` command is useful during security assessments and incident response because it helps identify NetBIOS names, cached network information, and active sessions.

Common cybersecurity uses include:

- Network enumeration
- Host identification
- Investigating legacy Windows networks
- Troubleshooting name resolution issues
- Identifying active NetBIOS sessions
- Collecting information during incident response
- Supporting internal penetration testing

---

## Challenges

- Some modern networks disable NetBIOS, resulting in limited or no output.
- Name cache entries depend on previous network communication.
- Active sessions may not exist on standalone systems.
- Remote NetBIOS queries may fail if NetBIOS over TCP/IP is disabled.

---

## Interview Questions

### Q1. What is NBTSTAT?

**Answer:** NBTSTAT is a Windows command-line utility used to display NetBIOS over TCP/IP statistics, name tables, name cache, and active NetBIOS sessions.

---

### Q2. Which command displays the local NetBIOS name table?

**Answer:**

```cmd
nbtstat -n
```

---

### Q3. Which command displays the NetBIOS name cache?

**Answer:**

```cmd
nbtstat -c
```

---

### Q4. Which command displays NetBIOS name resolution statistics?

**Answer:**

```cmd
nbtstat -r
```

---

### Q5. Which command displays active NetBIOS sessions?

**Answer:**

```cmd
nbtstat -s
```

---

### Q6. Which command clears and reloads the NetBIOS name cache?

**Answer:**

```cmd
nbtstat -R
```

---

## Skills Gained

- Learned to use the Windows `nbtstat` utility.
- Viewed local NetBIOS names.
- Examined the NetBIOS name cache.
- Analyzed NetBIOS name resolution statistics.
- Viewed active NetBIOS sessions.
- Improved Windows networking troubleshooting skills.
- Gained practical knowledge useful for cybersecurity and system administration.

---

## Lab Summary

In this lab, the Windows **NBTSTAT** utility was used to explore NetBIOS over TCP/IP information. Local NetBIOS names, cached name entries, name resolution statistics, and active NetBIOS sessions were examined. The experiment demonstrated how NBTSTAT assists in network troubleshooting, legacy Windows network management, and cybersecurity investigations.
