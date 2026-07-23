# Lab Report

## Experiment Title

**Using the SYSTEMINFO Command to Display and Analyze System Configuration Information**

---

## Objective

The objective of this experiment was to study the Windows **SYSTEMINFO** command and learn how to retrieve detailed information about the operating system, hardware, processor, memory, network configuration, BIOS, and security settings.

---

## Tools Used

- Operating System: Windows 11
- Command Prompt (CMD)
- SYSTEMINFO Utility

---

## Commands Executed

```cmd
systeminfo
systeminfo | more
systeminfo | findstr /B /C:"Host Name"
systeminfo /?
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `systeminfo` command to display complete system information.
3. Executed the `systeminfo | more` command to view the output page by page.
4. Executed the `systeminfo | findstr /B /C:"Host Name"` command to filter only the hostname.
5. Executed the `systeminfo /?` command to view the available options and syntax.
6. Recorded the observations and captured screenshots for documentation.

---

## Results

- Successfully displayed detailed operating system and hardware information.
- Identified the computer hostname, Windows version, BIOS version, processor, memory, and network configuration.
- Verified that the system was a **64-bit Dell Vostro 3420** running **Windows 11 Home Single Language**.
- Confirmed that the system belonged to the **WORKGROUP** workgroup.
- Observed that Virtualization-Based Security was enabled.
- Displayed the system information page by page using the `more` command.
- Filtered the hostname using the `findstr` command.
- Reviewed the available command-line options of the SYSTEMINFO utility.

---

## Conclusion

The experiment successfully demonstrated the capabilities of the Windows **SYSTEMINFO** command. It provided comprehensive information about the computer's operating system, hardware, memory, BIOS, network adapters, and security configuration. The command proved valuable for system administration, troubleshooting, asset inventory, incident response, digital forensics, and cybersecurity investigations.

---

## Skills Gained

- Learned to use the Windows SYSTEMINFO command.
- Retrieved detailed operating system information.
- Identified hardware specifications and memory details.
- Examined BIOS and security configuration.
- Filtered command output using `findstr`.
- Used the `more` command to improve readability.
- Improved Windows administration and troubleshooting skills.
- Developed practical knowledge useful for cybersecurity, digital forensics, and incident response.
