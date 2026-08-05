# Observations – Windows Administration Mini Project

## 1. System Information (`systeminfo`)

- The operating system was identified as **Microsoft Windows 11 Home Single Language**.
- System architecture was 64-bit.
- The device model was **Dell Vostro 3420**.
- System information included BIOS, memory, processor, and OS details.
- Useful for system inventory and asset management.

---

## 2. Computer Name (`hostname`)

- The computer hostname was displayed successfully.
- Hostname identified the system as **JAKHMOLA_AKSHAT**.
- Useful for device identification in enterprise environments.
- Assists in network and asset management.

---

## 3. Current User (`whoami`)

- Displayed the currently logged-in user account.
- Confirmed the active user session.
- Useful for access verification and auditing.
- Helps identify the security context of the current session.

---

## 4. Network Configuration (`ipconfig /all`)

- Displayed complete network adapter information.
- Included IPv4 address, subnet mask, gateway, and DNS configuration.
- Confirmed active network connectivity.
- Useful for network troubleshooting and auditing.

---

## 5. Local User Accounts (`net user`)

- Listed all local user accounts present on the system.
- Included default Windows accounts and custom user accounts.
- Useful for account management and security reviews.
- Helps identify potentially unused or unauthorized accounts.

---

## 6. Running Processes (`tasklist`)

- Displayed active processes running on the system.
- Included system and user applications.
- Useful for monitoring system activity.
- Helps identify resource-intensive or suspicious processes.

---

## 7. Running Services (`sc query`)

- Displayed currently running Windows services.
- Included service names, states, and configurations.
- Useful for service management and troubleshooting.
- Helps verify essential services are operational.

---

## 8. Storage Information (`fsutil volume diskfree C:`)

- Displayed total disk size and available free space.
- The primary drive had limited free storage remaining.
- Storage utilization was significantly high.
- Useful for capacity planning and system maintenance.

---

## 9. Driver Information (`driverquery`)

- Listed installed device drivers.
- Included driver names, types, and installation details.
- Useful for hardware management and troubleshooting.
- Helps identify outdated or unnecessary drivers.

---

## 10. Power Configuration (`powercfg /getactivescheme`)

- Displayed the active power scheme.
- Confirmed that the **Balanced** power plan was active.
- Useful for performance and power management.
- Helps verify system power settings.

---

## 11. Security and Administrative Findings

### Positive Findings

- System information was successfully collected.
- Network configuration was functioning correctly.
- User accounts were properly enumerated.
- Drivers and services were accessible for auditing.
- Power management configuration was available.

### Areas of Attention

- Available disk space on the C: drive was critically low.
- High storage utilization may affect system performance.
- Periodic cleanup and storage management are recommended.
- Regular audits should be performed to maintain system health.

---

## 12. Overall Analysis

- The administrative audit was completed successfully.
- System, network, user, storage, process, service, and driver information were collected.
- The machine was operating under the Balanced power plan.
- Storage utilization was identified as the primary concern requiring attention.
- The project demonstrated practical Windows administration and auditing techniques.
