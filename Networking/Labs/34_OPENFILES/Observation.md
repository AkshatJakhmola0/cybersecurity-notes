# Observations – OPENFILES Command

## 1. Help Menu (`openfiles /?`)

- Displayed the syntax and available OPENFILES options.
- Explained commands for querying and managing open files.
- Included options for enabling local object tracking.
- Useful for understanding command usage.

---

## 2. Display Open Files (`openfiles`)

- Displayed information about open files on the system.
- Reported that local object tracking was not enabled.
- Showed that no shared open files were found.
- Demonstrated the default behavior of the OPENFILES command.

---

## 3. Query Open Files (`openfiles /query`)

- Queried the list of currently opened shared files.
- Returned no shared open files.
- Displayed a message indicating that local object tracking was disabled.
- Confirmed that local file monitoring requires additional configuration.

---

## 4. Enable Local Object Tracking (`openfiles /local on`)

- Successfully enabled the **Maintain Objects List** feature.
- Displayed a confirmation message.
- Indicated that the change would take effect after restarting the system.
- Completed without errors.

---

## 5. Query After Enabling (`openfiles /query`)

- Queried open files again after enabling local object tracking.
- The command still displayed the previous message because the computer had not yet been restarted.
- No shared open files were found.
- Verified that a system restart is required before local object tracking becomes active.

---

## 6. Overall Analysis

- OPENFILES successfully displayed shared file information.
- Local object tracking is disabled by default.
- The `/local on` command enables local tracking but requires a restart.
- The command is useful for Windows administration, file monitoring, and security investigations involving shared resources.
