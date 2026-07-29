# Lab 22 – FIND Command

## Objective

The objective of this lab is to learn how to use the Windows **FIND** command to search for specific text within files. This lab demonstrates how to locate system information, identify keywords, perform case-insensitive searches, and display matching line numbers.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of text files
- Permission to execute system commands

---

# Theory

The **FIND** command is a built-in Windows command-line utility used to search for a specified string of text within one or more files. It is useful for filtering large files and locating specific information quickly.

Unlike **FINDSTR**, the FIND command performs simple text matching without supporting regular expressions. It is commonly used for searching configuration files, log files, and command outputs.

---

# Syntax

```cmd
find [options] "string" filename
```

Examples:

```cmd
find "Windows" systeminfo.txt

find /i "windows" systeminfo.txt

find /n "OS" systeminfo.txt
```

---

# Commands Used

```cmd
find /?

find "Windows" C:\Windows\System32\drivers\etc\hosts

systeminfo > systeminfo.txt

find "OS" systeminfo.txt

find "Version" systeminfo.txt

find "Memory" systeminfo.txt

find /i "windows" systeminfo.txt

find /n "OS" systeminfo.txt
```

---

# Steps Performed

### Step 1

Displayed the FIND command help menu.

```cmd
find /?
```

---

### Step 2

Searched the Hosts file for the word "Windows".

```cmd
find "Windows" C:\Windows\System32\drivers\etc\hosts
```

---

### Step 3

Saved the system information to a text file.

```cmd
systeminfo > systeminfo.txt
```

---

### Step 4

Searched for operating system information.

```cmd
find "OS" systeminfo.txt
```

---

### Step 5

Searched for version-related information.

```cmd
find "Version" systeminfo.txt
```

---

### Step 6

Displayed memory-related information.

```cmd
find "Memory" systeminfo.txt
```

---

### Step 7

Performed a case-insensitive search.

```cmd
find /i "windows" systeminfo.txt
```

---

### Step 8

Displayed matching lines along with their line numbers.

```cmd
find /n "OS" systeminfo.txt
```

---

# Expected Output

- FIND command help menu.
- Matching text from the Hosts file.
- System information saved to a text file.
- Operating system details.
- Windows and BIOS version information.
- Physical and virtual memory details.
- Case-insensitive search results.
- Matching lines with line numbers.

---

# Key Findings

- The FIND command searches for exact text within files.
- Search results include only the lines containing the specified text.
- The `/i` option ignores letter case during searching.
- The `/n` option displays the corresponding line numbers.
- System information can be filtered efficiently using FIND.
- FIND is useful for quickly locating important information in large text files.

---

# Cybersecurity Perspective

The FIND command is useful for cybersecurity professionals when analyzing command outputs, configuration files, and logs.

It can be used to:

- Search Windows configuration files.
- Filter log files during incident response.
- Identify operating system information.
- Locate specific keywords in forensic evidence.
- Verify configuration settings.
- Quickly extract relevant information from large text files.

Although FIND is a simple utility, it is valuable for basic log analysis and system auditing.

---

# Challenges

- FIND performs only exact text matching.
- It does not support regular expressions.
- Searches are case-sensitive unless the `/i` option is used.
- Large files may require multiple searches using different keywords.

---

# Interview Questions

### 1. What is the purpose of the FIND command?

**Answer:**

The FIND command searches for specific text strings within one or more files.

---

### 2. Which option performs a case-insensitive search?

**Answer:**

```cmd
/i
```

---

### 3. Which option displays line numbers?

**Answer:**

```cmd
/n
```

---

### 4. Can FIND search inside command output saved to a file?

**Answer:**

Yes. Command output can first be redirected to a text file and then searched using FIND.

---

### 5. What is one limitation of the FIND command?

**Answer:**

It supports only simple text matching and does not support regular expressions.

---

### 6. Why is FIND useful in cybersecurity?

**Answer:**

It helps analysts quickly search logs, configuration files, and command outputs for important keywords during investigations.

---

# Skills Gained

- Text Searching
- Windows Command Line
- Log Analysis
- System Information Filtering
- File Analysis
- Windows Administration
- Basic Incident Response
- Digital Forensics Fundamentals

---

# Lab Summary

In this lab, the **FIND** command was used to search text within files and command outputs. System information was redirected to a text file and searched for operating system details, version information, memory statistics, and Windows-related entries. The lab demonstrated how the FIND command simplifies information retrieval and supports system administration, troubleshooting, and cybersecurity investigations.
