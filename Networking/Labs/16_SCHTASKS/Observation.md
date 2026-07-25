# Lab 16 – SCHTASKS Observations

---

## 1. Display SCHTASKS Help Information

- Executed the `schtasks /?` command.
- Reviewed the syntax, parameters, and available operations provided by the built-in help.
- Learned that SCHTASKS supports creating, querying, modifying, running, ending, and deleting scheduled tasks.
- Observed examples demonstrating different command usages.
- Understood that the built-in documentation is useful for learning advanced command options.

---

## 2. View Scheduled Tasks

- Executed the `schtasks /query` command.
- Displayed the list of scheduled tasks configured on the system.
- Observed system, Microsoft, Office, OneDrive, and third-party application tasks.
- Viewed details such as Task Name, Next Run Time, and Status.
- Learned that scheduled tasks automate system maintenance and application-related activities.

---

## 3. Create a Scheduled Task

- Executed the `schtasks /create` command to create a scheduled task named **Notepad Lab**.
- Configured the task to launch Notepad at the specified time.
- Successfully created the scheduled task.
- Learned that SCHTASKS allows users to automate applications and scripts using command-line options.
- Verified that Windows displayed a confirmation message after successful task creation.

---

## 4. Run a Scheduled Task

- Executed the `schtasks /run /tn "Notepad Lab"` command.
- Successfully started the scheduled task manually.
- Observed that the configured application (Notepad) launched as expected.
- Learned that scheduled tasks can be executed on demand without waiting for their scheduled execution time.
- Verified that Windows confirmed the task execution.

---

## 5. Delete a Scheduled Task

- Executed the `schtasks /delete /tn "Notepad Lab" /f` command.
- Successfully removed the scheduled task from the system.
- Observed that the `/F` option deletes the task without requesting confirmation.
- Learned that unnecessary or temporary scheduled tasks should be removed after testing.
- Understood that deleting unused tasks helps maintain a clean and organized Task Scheduler.
