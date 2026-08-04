# LAB REPORT

## Experiment Title

Study of the POWERCFG Command in Windows Command Prompt

---

## Objective

To understand the working of the **POWERCFG** command and learn how to view power plans, generate energy and battery reports, identify power requests, and examine devices capable of waking the system.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

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

## Procedure

1. Opened Command Prompt.
2. Displayed the POWERCFG help menu.
3. Listed all available power schemes.
4. Displayed the active power plan.
5. Generated an energy efficiency report.
6. Generated a battery health report.
7. Checked for applications and services preventing the system from entering sleep mode.
8. Listed devices configured to wake the computer.
9. Reviewed the generated HTML reports.

---

## Results

- Successfully displayed the available and active power plans.
- Confirmed that the **Balanced** power plan was active.
- Generated an energy report identifying power efficiency issues.
- Successfully generated a battery health report.
- Verified that no active power requests were preventing sleep.
- Identified the **Realtek PCIe GbE Family Controller** as a wake-enabled device.
- All POWERCFG commands executed successfully.

---

## Conclusion

The **POWERCFG** command is a useful Windows utility for managing and troubleshooting system power settings. It provides detailed information about power plans, battery health, energy efficiency, and wake-enabled devices. These features assist administrators in diagnosing power-related issues, monitoring endpoint health, and optimizing system performance.

---

## Skills Gained

- Windows Power Management
- Power Plan Administration
- Battery Health Analysis
- Energy Efficiency Monitoring
- Windows Troubleshooting
- Command-Line Administration
- Endpoint Management
- System Diagnostics
