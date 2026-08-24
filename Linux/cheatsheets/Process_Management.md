# Linux Process Management Cheat Sheet

## View Running Processes

### Show All Processes

```bash
ps aux
```

### Process Tree

```bash
pstree
```

---

## Real-Time Monitoring

### Top

```bash
top
```

### Htop

```bash
htop
```

---

## Find a Process

```bash
ps aux | grep ssh
```

```bash
pidof sshd
```

---

## Kill Processes

### Normal Kill

```bash
kill PID
```

### Force Kill

```bash
kill -9 PID
```

---

## Background Jobs

### Run in Background

```bash
command &
```

### View Jobs

```bash
jobs
```

### Bring Job to Foreground

```bash
fg
```

---

## Process Priority

### View Priority

```bash
top
```

### Change Priority

```bash
nice -n 10 command
```

```bash
renice 10 PID
```

---

## Service Management

### Check Service Status

```bash
systemctl status ssh
```

### Start Service

```bash
systemctl start ssh
```

### Stop Service

```bash
systemctl stop ssh
```

### Restart Service

```bash
systemctl restart ssh
```

---

## SOC Analyst Usage

- Detect malicious processes
- Resource monitoring
- Incident response
- Threat hunting
- Service investigation

---

## Quick Examples

```bash
ps aux
top
kill -9 1234
systemctl status ssh
```
