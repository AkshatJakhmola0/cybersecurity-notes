# Lab 33 – POWERCFG Command

## Objective

To understand the Windows **POWERCFG** command and learn how to view power plans, generate energy and battery reports, identify power requests, and examine devices capable of waking the system.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Administrator privileges (recommended)

---

## Theory

**POWERCFG** is a built-in Windows command-line utility used to manage and troubleshoot power settings. It allows administrators to view power schemes, analyze energy efficiency, generate battery health reports, identify applications preventing sleep, and determine which devices can wake the computer.

POWERCFG is useful for system administration, troubleshooting, endpoint management, and performance analysis.

---

## Syntax

```cmd
powercfg [options]
```

Examples:

```cmd
powercfg /list

powercfg /batteryreport

powercfg /energy
```

---

## Commands Used

```cmd
powercfg /?

powercfg /list

powercfg /getactivescheme

powercfg /energy

powercfg /batteryreport

powercfg /requests

powercfg /devicequery wake_armed
```

---

## Steps Performed

1. Displayed the POWERCFG help menu.
2. Listed all available power plans.
3. Displayed the active power scheme.
4. Generated an energy efficiency report.
5. Generated a battery health report.
6. Checked for applications preventing sleep.
7. Listed devices capable of waking the computer.
8. Reviewed the generated HTML reports.

---

## Key Findings

- The system was using the **Balanced** power plan.
- POWERCFG generated an energy efficiency report successfully.
- A battery report was generated in HTML format.
- No applications or services were preventing sleep.
- The Realtek network adapter was configured to wake the computer.
- POWERCFG provides detailed reports for troubleshooting power-related issues.

---

## Cybersecurity Perspective

POWERCFG is useful for:

- Endpoint Health Monitoring
- Windows Administration
- Power Configuration Auditing
- System Troubleshooting
- Battery Health Analysis
- Incident Response
- Device Management

---

## Interview Questions

**Q1. What is POWERCFG used for?**  
It is used to manage and troubleshoot Windows power settings.

**Q2. Which command lists all available power plans?**

```cmd
powercfg /list
```

**Q3. Which command generates an energy report?**

```cmd
powercfg /energy
```

**Q4. What does `powercfg /requests` display?**  
It shows applications, drivers, or services currently preventing the system from entering sleep mode.

**Q5. Which command displays devices that can wake the computer?**

```cmd
powercfg /devicequery wake_armed
```

---

## Skills Gained

- Windows Power Management
- Windows Administration
- Endpoint Health Monitoring
- Battery Analysis
- Power Troubleshooting
- Command-Line Administration
- System Diagnostics
