# Linux Log Analysis Cheat Sheet

## Common Log Locations

| Log File | Purpose |
|-----------|---------|
| /var/log/auth.log | Authentication events |
| /var/log/syslog | General system logs |
| /var/log/kern.log | Kernel logs |
| /var/log/dpkg.log | Package activity |
| /var/log/apache2/access.log | Web access logs |

---

## Useful Commands

### View Logs

```bash
cat /var/log/auth.log
