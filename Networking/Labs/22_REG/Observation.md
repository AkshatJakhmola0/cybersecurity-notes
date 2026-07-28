# Observations

## 1. REG Command (`reg`)

- The `reg` command displayed all available Registry operations.
- Operations such as Query, Add, Delete, Export, and Import were available.
- The command acts as the primary command-line utility for Registry management.
- It provides access to Windows Registry functions without opening Registry Editor.

---

## 2. REG Help (`reg /?`)

- The help menu displayed the syntax for all supported REG operations.
- Separate help is available for each Registry operation.
- Return codes for successful and failed operations were shown.
- The help command serves as a quick reference for Registry management.

---

## 3. Windows Version (`reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion"`)

- The Registry displayed detailed Windows operating system information.
- Details such as product name, build number, edition, and installation information were available.
- Multiple subkeys related to Windows configuration were listed.
- This Registry location is useful for operating system identification during investigations.

---

## 4. Desktop Settings (`reg query "HKCU\Control Panel\Desktop"`)

- The Registry contained desktop customization and user interface settings.
- Wallpaper, cursor, display, and visual preference values were stored here.
- Settings were specific to the currently logged-in user.
- These values can be used to verify user-specific configurations.

---

## 5. Installed Programs (`reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall"`)

- Installed applications were listed under the Uninstall Registry key.
- Each application had its own Registry subkey.
- The Registry provides information used by Windows to manage installed software.
- This location is commonly checked during software inventory and forensic investigations.

---

## 6. Environment Variables (`reg query "HKCU\Environment"`)

- User-specific environment variables were displayed.
- Variables such as `PATH`, `TEMP`, and `TMP` were stored in this Registry key.
- These values define application execution paths and user environment settings.
- Incorrect or malicious modifications may affect system behavior.

---

## 7. Startup Programs (`reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Run"`)

- Startup applications configured for the current user were listed.
- Programs in this Registry key execute automatically during user logon.
- This location is frequently abused by malware for persistence.
- Monitoring this key is important during security assessments.

---

## 8. Computer Name (`reg query "HKLM\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName"`)

- The active computer name stored in the Registry was displayed.
- The Registry provides system identification information.
- This key helps administrators verify system configuration.
- Computer name information is useful during asset inventory and incident response.
