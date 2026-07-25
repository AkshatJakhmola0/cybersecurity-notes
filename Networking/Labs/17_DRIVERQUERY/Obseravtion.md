# Lab 17 – DRIVERQUERY Observations

---

## 1. Display Installed Device Drivers

- Executed the `driverquery` command.
- Displayed the list of installed device drivers on the system.
- Observed details such as the Module Name, Display Name, Driver Type, and Link Date.
- Verified that Windows, Intel, Dell, Realtek, VirtualBox, and other hardware drivers were installed.
- Learned that the command provides a quick inventory of all installed drivers.

---

## 2. Display Verbose Driver Information

- Executed the `driverquery /v` command.
- Displayed detailed information for each installed driver.
- Observed additional details including Description, Start Mode, Current State, Status, Driver Path, Memory Usage, and Link Date.
- Learned how to determine whether a driver is currently running or stopped.
- Understood that verbose output is useful for troubleshooting and forensic analysis.

---

## 3. Display Driver Information in CSV Format

- Executed the `driverquery /fo csv` command.
- Displayed driver information in Comma-Separated Values (CSV) format.
- Learned that CSV output can be copied into spreadsheet applications for sorting, filtering, and reporting.
- Understood that this format is useful for documentation, audits, and automated analysis.

---

## 4. Display Signed Drivers

- Executed the `driverquery /si` command.
- Displayed information about digitally signed device drivers.
- Observed the Device Name, INF File, Signature Status, and Manufacturer.
- Verified that most installed drivers were digitally signed by trusted vendors such as Microsoft, Intel, Dell, and Realtek.
- Learned that checking digital signatures helps identify trusted drivers and detect potentially suspicious or unsigned drivers.

---

## 5. Display DRIVERQUERY Help

- Executed the `driverquery /?` command.
- Displayed the built-in help menu for the DRIVERQUERY utility.
- Reviewed the available command-line parameters and output formats.
- Learned how to query remote computers, display verbose information, verify signed drivers, and export output in different formats.
- Understood that the built-in help is useful for learning command syntax and available options.
