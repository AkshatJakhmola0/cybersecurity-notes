# Lab 19 – NET Command

## Objective

The objective of this lab is to learn how to use the **NET** command in Windows to obtain information about local user accounts, groups, shared resources, account policies, and workstation configuration. The lab demonstrates how the NET command assists in Windows administration, troubleshooting, security auditing, and cybersecurity investigations.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Basic understanding of Windows user accounts and networking

---

## Theory

The **NET** command is a built-in Windows command-line utility used for managing and displaying information related to network resources, user accounts, groups, shared folders, and system configuration. It consists of several subcommands, each designed to perform a specific administrative task.

System administrators use the NET command for managing users, configuring shared resources, checking account policies, and troubleshooting network-related issues. In cybersecurity, the NET command is frequently used during reconnaissance, incident response, digital forensics, and Active Directory investigations to enumerate system information without modifying the operating system.

---

## Syntax

```cmd
net [subcommand]
```

Common subcommands:

```cmd
net
net help
net user
net localgroup
net share
net accounts
net config workstation
```

---

## Commands Used

```cmd
net

net help

net user

net localgroup

net share

net accounts

net config workstation
```

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `net` command to display available NET subcommands.
3. Used `net help` to view detailed help information.
4. Executed `net user` to display local user accounts.
5. Used `net localgroup` to list local security groups.
6. Executed `net share` to display shared folders and resources.
7. Used `net accounts` to view local account and password policy settings.
8. Executed `net config workstation` to display workstation configuration details.
9. Recorded the outputs and captured screenshots.

---

## Expected Output

The commands should display:

- Available NET subcommands
- Help information
- Local user accounts
- Local groups
- Shared resources
- Account policy information
- Workstation configuration

---

## Key Findings

- Successfully explored the available NET command subcommands.
- Displayed all local user accounts on the system.
- Listed local security groups configured in Windows.
- Identified shared folders and administrative shares.
- Viewed password and account policy settings.
- Retrieved workstation configuration information.
- Understood how the NET command assists in Windows administration and security investigations.

---

## Cybersecurity Perspective

The **NET** command is one of the most valuable Windows administration and cybersecurity utilities. It enables security professionals to enumerate local users, security groups, shared resources, and password policies without making changes to the system. During penetration testing, incident response, and Active Directory assessments, NET commands help identify privileged accounts, administrative groups, network shares, and system configuration, making them essential for reconnaissance and security auditing.

---

## Challenges

- Understanding the purpose of different NET subcommands.
- Interpreting local group information.
- Identifying default administrative shares.
- Understanding account policy settings.
- Distinguishing workstation configuration from user account information.

---

## Interview Questions

### 1. What is the purpose of the NET command?

### 2. What information does the `net user` command display?

### 3. How is `net localgroup` useful in Windows administration?

### 4. What are administrative shares shown by `net share`?

### 5. Why is the `net accounts` command important for security?

### 6. How does the NET command assist during cybersecurity investigations?

---

## Skills Gained

- Windows User Enumeration
- Group Enumeration
- Network Share Enumeration
- Password Policy Analysis
- Windows Administration
- Security Auditing
- Incident Response Fundamentals
- Windows Command Line Proficiency

---

## Lab Summary

In this lab, the NET command was used to explore various Windows administrative functions, including user enumeration, local group inspection, shared resource identification, password policy analysis, and workstation configuration. The experiment demonstrated how NET provides valuable system information required for Windows administration, cybersecurity assessments, digital forensics, and enterprise security operations.
