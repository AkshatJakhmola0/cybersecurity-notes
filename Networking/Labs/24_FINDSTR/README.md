# Lab 23 – FINDSTR Command

## Objective

The objective of this lab is to learn how to use the Windows **FINDSTR** command to search for text patterns within files. This lab demonstrates basic searching, case-insensitive searches, exact phrase matching, multiple keyword searches, line numbering, and regular expression matching.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- A text file for searching (systeminfo.txt)
- Basic understanding of text searching

---

# Theory

The **FINDSTR** command is an advanced command-line utility used to search for text strings and patterns within files. It provides more features than the FIND command by supporting regular expressions, multiple search strings, exact phrase matching, and various search options.

FINDSTR is widely used by system administrators and cybersecurity professionals to analyze log files, configuration files, and command outputs efficiently.

---

# Syntax

```cmd
findstr [options] "string" filename
```

Examples:

```cmd
findstr "Windows" systeminfo.txt

findstr /i "windows" systeminfo.txt

findstr /r "^OS" systeminfo.txt
```

---

# Commands Used

```cmd
findstr /?

findstr "Windows" systeminfo.txt

findstr /i "windows" systeminfo.txt

findstr /n "OS" systeminfo.txt

findstr /b "OS" systeminfo.txt

findstr /c:"Microsoft Windows" systeminfo.txt

findstr "Memory Version" systeminfo.txt

findstr /r "^OS" systeminfo.txt
```

---

# Steps Performed

### Step 1

Displayed the FINDSTR help menu.

```cmd
findstr /?
```

---

### Step 2

Searched for the keyword "Windows" in the system information file.

```cmd
findstr "Windows" systeminfo.txt
```

---

### Step 3

Performed a case-insensitive search.

```cmd
findstr /i "windows" systeminfo.txt
```

---

### Step 4

Displayed matching lines with their line numbers.

```cmd
findstr /n "OS" systeminfo.txt
```

---

### Step 5

Searched only for lines beginning with "OS".

```cmd
findstr /b "OS" systeminfo.txt
```

---

### Step 6

Searched for the exact phrase "Microsoft Windows".

```cmd
findstr /c:"Microsoft Windows" systeminfo.txt
```

---

### Step 7

Searched for multiple keywords.

```cmd
findstr "Memory Version" systeminfo.txt
```

---

### Step 8

Performed a regular expression search.

```cmd
findstr /r "^OS" systeminfo.txt
```

---

# Expected Output

- FINDSTR help information.
- Lines containing the keyword "Windows".
- Case-insensitive search results.
- Matching lines with line numbers.
- Lines beginning with "OS".
- Exact phrase search results.
- Multiple keyword search results.
- Regular expression search results.

---

# Key Findings

- FINDSTR provides advanced text searching capabilities.
- The `/i` option ignores case differences.
- The `/n` option displays line numbers.
- The `/b` option searches only at the beginning of lines.
- The `/c:` option searches for an exact phrase.
- FINDSTR supports multiple keywords in a single command.
- Regular expressions allow pattern-based searching.

---

# Cybersecurity Perspective

FINDSTR is widely used in cybersecurity for searching logs, configuration files, and command outputs.

It can be used to:

- Search Windows event log exports.
- Locate Indicators of Compromise (IOCs).
- Search configuration files for suspicious entries.
- Analyze malware logs.
- Perform threat hunting.
- Filter large forensic datasets.
- Identify suspicious keywords quickly.

FINDSTR is an essential utility for SOC Analysts, Incident Responders, and Digital Forensics professionals.

---

# Challenges

- Understanding the different search options.
- Learning regular expression syntax.
- Selecting the correct option for different search requirements.
- Interpreting search results in large files.

---

# Interview Questions

### 1. What is the purpose of the FINDSTR command?

**Answer:**

FINDSTR searches for text strings and patterns within one or more files.

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

### 4. Which option searches only at the beginning of a line?

**Answer:**

```cmd
/b
```

---

### 5. Which option searches for an exact phrase?

**Answer:**

```cmd
/c:
```

---

### 6. Why is FINDSTR preferred over FIND?

**Answer:**

FINDSTR supports regular expressions, exact phrase matching, multiple search strings, and additional search options, making it more powerful than FIND.

---

# Skills Gained

- Advanced Text Searching
- Regular Expression Basics
- Log Analysis
- Windows Command Line
- Threat Hunting
- Configuration File Analysis
- Digital Forensics
- Incident Response

---

# Lab Summary

In this lab, the **FINDSTR** command was used to perform advanced text searches within a system information file. Various search techniques, including case-insensitive searches, exact phrase matching, multiple keyword searches, line numbering, and regular expression matching, were demonstrated. The lab highlighted the importance of FINDSTR for efficient log analysis, troubleshooting, and cybersecurity investigations.

| 07_multiplewords.png | Multiple keyword search |
| 08_regex.png | Regular expression search |
