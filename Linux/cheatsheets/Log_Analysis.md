# Linux Log Analysis Cheat Sheet

## Common Log Locations

| Log File | Purpose |
|-----------|---------|
| /var/log/auth.log | Authentication logs |
| /var/log/syslog | General system logs |
| /var/log/kern.log | Kernel logs |
| /var/log/dpkg.log | Package installation logs |
| /var/log/apache2/access.log | Apache access logs |
| /var/log/apache2/error.log | Apache error logs |

---

## View Logs

```bash
cat /var/log/auth.log
```

```bash
less /var/log/syslog
```

---

## Monitor Logs in Real Time

```bash
tail -f /var/log/auth.log
```

```bash
tail -f /var/log/syslog
```

---

## Search Logs

### Failed Logins

```bash
grep "Failed" /var/log/auth.log
```

### SSH Events

```bash
grep ssh /var/log/auth.log
```

### Sudo Activity

```bash
grep sudo /var/log/auth.log
```

---

## Journalctl

### View All Logs

```bash
journalctl
```

### SSH Logs

```bash
journalctl -u ssh
```

### Today's Logs

```bash
journalctl --since today
```

---

## SOC Analyst Usage

- Detect brute-force attacks
- Investigate failed logins
- Review user activity
- Threat hunting
- Incident response

---

## Quick Examples

```bash
tail -f /var/log/auth.log
grep "Failed" /var/log/auth.log
journalctl -u ssh
```
