
# Lab 15 – TASKKILL Observations

---

## 1. Display TASKKILL Help Information

- Executed the `taskkill /?` command.
- Reviewed the syntax, parameters, filters, and examples provided by the built-in help.
- Learned about options such as `/PID`, `/IM`, `/F`, `/T`, and `/FI`.
- Understood that TASKKILL can terminate processes using either their Process ID (PID) or Image Name.
- Learned that the built-in help is useful for understanding advanced command usage.

---

## 2. Identify the Running Process

- Opened the Notepad application.
- Executed the `tasklist` command to display all running processes.
- Located the `Notepad.exe` process and noted its Process ID (PID).
- Learned that each running application is assigned a unique PID by Windows.
- Understood that the correct PID must be identified before terminating a process using the `/PID` option.

---

## 3. Terminate Process Using Process ID (PID)

- Initially attempted to terminate a process using an incorrect PID, which resulted in an error indicating that the process was not found.
- Executed the `tasklist` command again to identify the correct PID of the Notepad process.
- Successfully terminated the process using the `taskkill /PID <PID>` command.
- Learned that Process IDs are dynamic and change each time an application is restarted.
- Verified that Windows displayed a success message after terminating the process.

---

## 4. Terminate Process Using Image Name

- Opened Notepad again for testing.
- Executed the `taskkill /IM notepad.exe` command.
- Successfully terminated the Notepad process using its Image Name.
- Observed that specifying the executable name removes the need to identify the Process ID.
- Learned that terminating by Image Name is useful when the executable name is known.

---

## 5. Forcefully Terminate a Process

- Opened Notepad once again.
- Executed the `taskkill /F /IM notepad.exe` command.
- Successfully forcefully terminated the process.
- Learned that the `/F` option forces Windows to terminate the process immediately.
- Understood that forceful termination should be used carefully, especially with important applications, as unsaved data may be lost.
