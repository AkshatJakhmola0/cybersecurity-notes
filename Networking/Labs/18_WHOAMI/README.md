# Lab 18 – WHOAMI Command

## Objective

The objective of this lab is to learn how to use the **WHOAMI** command in Windows to identify the currently logged-in user, view the Security Identifier (SID), examine group memberships, inspect user privileges, and understand the security context of the current session. This command is widely used in Windows administration, Active Directory environments, digital forensics, and cybersecurity investigations.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Basic understanding of Windows user accounts and permissions

---

## Theory

The **WHOAMI** command is a built-in Windows command-line utility that displays information about the current logged-in user. It helps administrators and security professionals identify the user account, associated Security Identifier (SID), group memberships, privileges, and security token information.

WHOAMI is commonly used during troubleshooting, system administration, penetration testing, privilege escalation analysis, and incident response. It provides valuable information about the security context under which a user or process is running.

---

## Syntax

```cmd
whoami [options]
```

Common options:

```cmd
whoami
whoami /all
whoami /user
whoami /groups
whoami /priv
whoami /user /fo list
whoami /?
```

---

## Commands Used

```cmd
whoami

whoami /all

whoami /user

whoami /groups

whoami /priv

whoami /user /fo list

whoami /?
```

---

## Steps Performed

1. Opened Command Prompt.
2. Executed the `whoami` command to display the current user.
3. Used `whoami /all` to display complete security information.
4. Executed `whoami /user` to display the current user's SID.
5. Used `whoami /groups` to view group memberships.
6. Executed `whoami /priv` to display user privileges.
7. Used `whoami /user /fo list` to display SID information in list format.
8. Executed `whoami /?` to view the help menu and available options.
9. Recorded the outputs and captured screenshots.

---

## Expected Output

The command should display:

- Current logged-in username
- User Security Identifier (SID)
- User group memberships
- User privileges
- Security token information
- Available WHOAMI command options

---

## Key Findings

- Successfully identified the currently logged-in Windows user.
- Retrieved the Security Identifier (SID) associated with the user account.
- Displayed all security groups assigned to the current user.
- Identified enabled and disabled user privileges.
- Learned different output formats supported by the WHOAMI command.
- Understood how Windows determines the security context of a logged-in user.

---

## Cybersecurity Perspective

The **WHOAMI** command is one of the first commands executed during security assessments, penetration testing, and incident response. It helps determine the identity of the current user, administrative rights, assigned privileges, and group memberships. Security analysts use this information to assess access levels, investigate privilege escalation opportunities, validate user permissions, and understand the security context of compromised or investigated systems.

---

## Challenges

- Understanding the purpose of Security Identifiers (SIDs).
- Differentiating between user groups and user privileges.
- Interpreting enabled and disabled privilege states.
- Understanding the relationship between user accounts and Windows security tokens.

---

## Interview Questions

### 1. What is the purpose of the WHOAMI command?

### 2. What information does the `/all` option display?

### 3. What is a Security Identifier (SID)?

### 4. How is `whoami /groups` different from `whoami /priv`?

### 5. Why is the WHOAMI command important in cybersecurity?

### 6. How can WHOAMI help during privilege escalation assessment?

---

## Skills Gained

- User Enumeration
- Windows Security Basics
- SID Identification
- Privilege Analysis
- Group Membership Analysis
- Windows Administration
- Security Assessment
- Incident Response Fundamentals

---

## Lab Summary

In this lab, the WHOAMI command was used to identify the current Windows user, examine security identifiers, group memberships, privileges, and available command options. The experiment demonstrated how Windows represents user identities and permissions through security tokens and SIDs. Understanding the WHOAMI command is essential for Windows administration, cybersecurity operations, digital forensics, and Active Directory environments.

---

## Evidence

- `01_whoami.png`
- `02_whoami_all.png`
- `03_whoami_user.png`
- `04_whoami_groups.png`
- `05_whoami_priv.png`
- `06_whoami_sid.png`
- `07_whoami_help.png`
