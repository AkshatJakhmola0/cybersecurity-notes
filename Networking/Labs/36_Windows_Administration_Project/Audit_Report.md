# Audit Report

# Windows Administration Audit Report

**Project:** Windows Administration Mini Project  
**Audit Date:** August 2026  
**Auditor:** Akshat Jakhmola  
**System Name:** JAKHMOLA_AKSHAT

---

# Executive Summary

A Windows administrative audit was conducted using built-in Command Prompt utilities to assess the operating system, user accounts, network configuration, running services, active processes, storage utilization, installed drivers, and power configuration.

The system was found to be operational and properly configured for daily use. However, the audit identified critically low available disk space on the primary storage volume, which may impact performance and future updates.

---

# 1. System Information

| Parameter | Value |
|------------|---------|
| Operating System | Windows 11 Home Single Language |
| Architecture | 64-bit |
| System Manufacturer | Dell |
| System Model | Dell Vostro 3420 |
| Computer Name | JAKHMOLA_AKSHAT |

### Assessment

The system is running a modern supported Windows operating system suitable for administration, development, and cybersecurity learning activities.

---

# 2. User Information

### Current User

```text
aksha
```

### Local User Accounts

```text
Administrator
aksha
DefaultAccount
Guest
WDAGUtilityAccount
WsiAccount
```

### Assessment

- Standard Windows default accounts are present.
- Primary user account is active.
- No abnormal accounts were observed.

---

# 3. Network Configuration

### Network Status

The system is connected to a local network through Wi-Fi.

### IPv4 Address

```text
192.168.0.103
```

### Assessment

- Network connectivity is operational.
- System successfully obtained an IP address.
- Suitable for internet access and network communication.

---

# 4. Process Analysis

### Command Used

```cmd
tasklist
```

### Findings

- Multiple Windows system processes were active.
- User applications were functioning normally.
- No immediate abnormal process activity was observed.

### Assessment

Normal operating system behavior was detected.

---

# 5. Service Analysis

### Command Used

```cmd
sc query
```

### Findings

- Essential Windows services were running.
- Service states were reported successfully.
- No critical service failures were identified during the audit.

### Assessment

System services appear healthy and operational.

---

# 6. Storage Analysis

### Disk Statistics

| Parameter | Value |
|------------|---------|
| Total Capacity | 258.7 GB |
| Used Space | 250.6 GB |
| Free Space | 4.5 GB |

### Assessment

⚠ Critical Storage Warning

The primary drive contains less than 5 GB of free space.

Potential Impact:

- Reduced system performance
- Failed Windows updates
- Limited virtual memory
- Application installation issues
- Log file storage limitations

### Recommendation

- Remove unused files.
- Empty temporary folders.
- Uninstall unnecessary applications.
- Move large files to external storage.
- Maintain at least 15–20 GB of free space.

---

# 7. Driver Analysis

### Command Used

```cmd
driverquery
```

### Findings

- Installed drivers were successfully enumerated.
- Core hardware drivers were loaded properly.
- No immediate driver-related issues were observed.

### Assessment

Driver configuration appears stable.

---

# 8. Power Configuration

### Active Power Plan

```text
Balanced
```

### Assessment

The Balanced power plan provides a suitable balance between performance and battery efficiency for daily use.

---

# 9. Security Observations

### Positive Findings

✔ System information accessible and auditable

✔ Network configuration functioning correctly

✔ User account enumeration successful

✔ Services running normally

✔ Drivers loaded successfully

✔ Balanced power configuration active

---

### Areas Requiring Attention

⚠ Very low free disk space

⚠ System maintenance recommended

⚠ Storage cleanup required

---

# 10. Risk Assessment

| Area | Risk Level |
|--------|------------|
| Operating System | Low |
| User Accounts | Low |
| Network Configuration | Low |
| Running Services | Low |
| Drivers | Low |
| Power Configuration | Low |
| Storage Capacity | High |

---

# 11. Recommendations

1. Perform immediate disk cleanup.
2. Remove unused applications.
3. Archive old files and downloads.
4. Monitor storage utilization regularly.
5. Review installed software quarterly.
6. Conduct periodic administrative audits.
7. Keep Windows updates current.
8. Maintain backups of important data.

---

# Conclusion

The Windows Administration Audit was completed successfully. The operating system, user accounts, network settings, services, drivers, and power configuration were functioning normally. The primary concern identified during the audit was critically low free disk space on the system drive.

Apart from storage limitations, the system appears stable and suitable for administrative, educational, and cybersecurity-related tasks. Regular maintenance and storage management are recommended to ensure long-term performance and reliability.
