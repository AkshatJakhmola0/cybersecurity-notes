# Observations – POWERCFG Command

## 1. Help Menu (`powercfg /?`)

- Displayed the syntax and available POWERCFG options.
- Listed commands for managing power settings and generating reports.
- Explained various power management features.
- Useful for understanding command usage.

---

## 2. List Power Plans (`powercfg /list`)

- Displayed all available power schemes.
- Identified the currently active power plan.
- The system was using the **Balanced** power plan.
- Useful for checking the current power configuration.

---

## 3. Display Active Power Plan (`powercfg /getactivescheme`)

- Displayed the active power scheme.
- Confirmed that the **Balanced** plan was active.
- Returned the Power Scheme GUID.
- Verified the current system power configuration.

---

## 4. Generate Energy Report (`powercfg /energy`)

- Monitored the system for 60 seconds.
- Generated an HTML energy report.
- Reported errors, warnings, and informational messages.
- Useful for diagnosing power efficiency issues.

---

## 5. Generate Battery Report (`powercfg /batteryreport`)

- Successfully generated a battery health report.
- Saved the report as an HTML file.
- Contains battery capacity and usage information.
- Useful for monitoring battery health.

---

## 6. Display Power Requests (`powercfg /requests`)

- Checked for applications and services preventing sleep.
- No active power requests were found.
- Confirmed that no process was blocking sleep mode.
- Indicates normal power management behavior.

---

## 7. Display Wake Devices (`powercfg /devicequery wake_armed`)

- Listed devices capable of waking the computer.
- The **Realtek PCIe GbE Family Controller** was configured to wake the system.
- Useful for troubleshooting unexpected wake events.
- Helps identify wake-enabled hardware.

---

## 8. Overall Analysis

- POWERCFG successfully displayed the system's power configuration.
- Generated both energy and battery reports successfully.
- Verified the active power plan and wake-enabled device.
- The command is valuable for Windows administration, troubleshooting, and endpoint management.
