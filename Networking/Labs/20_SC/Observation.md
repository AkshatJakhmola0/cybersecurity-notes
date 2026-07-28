# Observations

## 1. SC Command Overview (`sc`)

- The `sc` command displayed all available Service Controller operations.
- It provides commands for querying, creating, deleting, starting, and stopping Windows services.
- The utility communicates directly with the Windows Service Control Manager (SCM).
- This command serves as the primary reference for Windows service management.

---

## 2. Display Running Services (`sc query`)

- The command listed all currently running Windows services.
- Each service displayed its Service Name, Display Name, Type, and Current State.
- Most essential Windows services were shown in the **RUNNING** state.
- Running services represent background processes required by Windows and installed applications.

---

## 3. Display All Services (`sc query state= all`)

- The command displayed both running and stopped Windows services.
- Services appeared with different states such as **RUNNING** and **STOPPED**.
- The output provided a complete inventory of services available on the system.
- This command is useful for auditing service availability and troubleshooting. 

---

## 4. Query Service Configuration (`sc qc EventLog`)

- The configuration of the Windows Event Log service was displayed.
- Information such as startup type, executable path, dependencies, and service account was shown.
- Configuration details help administrators verify service settings.
- Analysts can identify unusual configurations during security investigations.

---

## 5. Retrieve Service Key Name (`sc GetKeyName "Windows Event Log"`)

- The command converted the Display Name into its internal Service Name.
- Windows uses the Service Name for service management commands.
- This helps when only the Display Name is known.
- Accurate Service Names are required for most SC operations.

---

## 6. Retrieve Display Name (`sc GetDisplayName EventLog`)

- The command displayed the user-friendly Display Name of the service.
- It confirmed the relationship between the Service Name and Display Name.
- Display Names are commonly shown in the Windows Services console.
- This command assists administrators when identifying services.

---

## 7. Display Help Information (`sc /?`)

- The help command displayed detailed syntax and available options.
- Examples for common SC commands were provided.
- It serves as a quick reference during service management.
- Help documentation reduces syntax-related errors while using SC.
