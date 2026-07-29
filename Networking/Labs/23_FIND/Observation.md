# Observations

## 1. FIND Help (`find /?`)

- The help menu displayed the syntax and available options for the FIND command.
- Options such as `/i` and `/n` were available for modifying search behavior.
- The command accepts a search string and one or more files.
- The help menu serves as a quick reference for using FIND.

---

## 2. Search in Hosts File (`find "Windows" C:\Windows\System32\drivers\etc\hosts`)

- The command successfully searched the Hosts file.
- The keyword "Windows" was found in the default comment section.
- FIND displayed only the matching line from the file.
- Exact text matching was performed.

---

## 3. Search for Operating System Information (`find "OS" systeminfo.txt`)

- The command displayed operating system-related information.
- OS name, version, manufacturer, configuration, and build type were identified.
- The BIOS version also appeared because it contained the keyword "OS".
- FIND returned only the lines containing the specified text.

---

## 4. Search for Version Information (`find "Version" systeminfo.txt`)

- The command displayed both Windows and BIOS version information.
- Multiple matching lines were returned.
- Version details were extracted without displaying unrelated data.
- This method helps quickly identify software and firmware versions.

---

## 5. Search for Memory Information (`find "Memory" systeminfo.txt`)

- Physical and virtual memory information was displayed.
- Total, available, and in-use memory values were identified.
- Only memory-related entries were shown.
- The command simplified the extraction of hardware information.

---

## 6. Case-Insensitive Search (`find /i "windows" systeminfo.txt`)

- The `/i` option ignored differences in uppercase and lowercase letters.
- The command found matches regardless of text case.
- Windows-related paths and operating system information were displayed.
- Case-insensitive searching improves search flexibility.

---

## 7. Search with Line Numbers (`find /n "OS" systeminfo.txt`)

- The `/n` option displayed line numbers with each matching result.
- Line numbers made it easier to locate matching entries within the file.
- Multiple matching lines were identified.
- This feature is useful during log analysis and troubleshooting.

---

## 8. System Information File (`systeminfo > systeminfo.txt`)

- The `systeminfo` output was successfully redirected to a text file.
- The generated file served as input for subsequent FIND commands.
- Redirecting command output allows repeated analysis without rerunning commands.
- Saving command output simplifies documentation and forensic investigations.
