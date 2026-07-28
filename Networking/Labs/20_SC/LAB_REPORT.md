# LAB REPORT

## Experiment Title

Windows Service Management using the SC (Service Controller) Command

---

## Objective

To understand the functionality of the Windows **SC (Service Controller)** command and learn how to query services, inspect service configurations, identify service names, and analyze Windows services from a cybersecurity perspective.

---

## Tools Used

- Windows 10 Command Prompt (CMD)
- SC (Service Controller)
- Administrator Command Prompt

---

## Commands Executed

```cmd
sc

sc query

sc query state= all

sc qc EventLog

sc GetKeyName "Windows Event Log"

sc GetDisplayName EventLog

sc /?
```

---

## Procedure

### Step 1

Opened **Command Prompt** with Administrator privileges.

---

### Step 2

Executed the `sc` command to display all available Service Controller commands.

---

### Step 3

Ran the following command to view all currently running Windows services.

```cmd
sc query
```

---

### Step 4

Executed the following command to display both running and stopped services.

```cmd
sc query state= all
```

---

### Step 5

Queried the configuration of the Windows Event Log service.

```cmd
sc qc EventLog
```

---

### Step 6

Retrieved the internal Service Name using the Display Name.

```cmd
sc GetKeyName "Windows Event Log"
```

---

### Step 7

Retrieved the Display Name using the Service Name.

```cmd
sc GetDisplayName EventLog
```

---

### Step 8

Displayed the SC help menu to understand available commands and syntax.

```cmd
sc /?
```

---

## Results

- Successfully viewed the list of available SC commands.
- Enumerated all active Windows services.
- Displayed both running and stopped services.
- Retrieved configuration details of the Windows Event Log service.
- Identified the relationship between Service Names and Display Names.
- Learned the syntax and options available for the SC command.
- Observed that Windows uses numerous background services for system operations.

---

## Conclusion

The **SC (Service Controller)** command is an essential Windows administrative tool for managing and investigating Windows services. During this lab, various SC commands were used to enumerate services, inspect service configurations, and understand how Windows identifies services using Service Names and Display Names. The exercise demonstrated the importance of Windows services in system functionality and highlighted how service analysis supports troubleshooting and cybersecurity investigations.

---

## Skills Gained

- Windows Service Enumeration
- Windows Service Management
- Service Configuration Analysis
- Windows Administration
- Command-Line Proficiency
- Security Auditing
- Threat Hunting Fundamentals
- Incident Response Basics
