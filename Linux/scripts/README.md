# Linux Scripts

## Overview

This folder contains simple Linux automation and security scripts used for learning Linux administration, system monitoring, log analysis, and cybersecurity fundamentals.

These scripts help automate common tasks performed by Linux administrators, SOC Analysts, Incident Responders, and Security Engineers.

---

## Scripts Included

### system_info.sh

Collects basic system information.

Features:

- Hostname
- Current User
- Kernel Version
- Uptime
- IP Address Information
- Disk Usage

Useful for system enumeration and incident response.

---

### user_audit.sh

Performs a basic user account audit.

Features:

- Lists local users
- Displays privileged accounts
- Reviews login-related information

Useful for security audits and account reviews.

---

### process_monitor.sh

Monitors running processes.

Features:

- Lists active processes
- Displays CPU usage
- Displays Memory usage
- Helps identify resource-intensive processes

Useful for system monitoring and threat hunting.

---

### log_parser.sh

Parses Linux log files.

Features:

- Reads log entries
- Filters specific events
- Searches for suspicious activity
- Simplifies log analysis

Useful for SOC operations and incident response investigations.

---

## Skills Gained

- Linux Administration
- Bash Scripting
- Process Monitoring
- User Auditing
- Log Analysis
- Security Operations
- Incident Response
- System Enumeration

---

## Cybersecurity Relevance

These scripts demonstrate practical Linux skills used by:

- SOC Analysts
- Blue Team Analysts
- Security Engineers
- Incident Responders
- Linux Administrators
- Threat Hunters

---

## Usage

Make scripts executable:

```bash
chmod +x script_name.sh
```

Run a script:

```bash
./script_name.sh
```

Example:

```bash
./system_info.sh
```

---

## Disclaimer

These scripts are created for educational and learning purposes and should be tested in a lab environment before being used on production systems.
