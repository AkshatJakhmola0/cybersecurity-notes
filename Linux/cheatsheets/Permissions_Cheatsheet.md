# Linux Permissions Cheat Sheet

## View Permissions

```bash
ls -l
```

Example:

```text
-rwxr-xr--
```

---

## Permission Meaning

| Symbol | Meaning |
|----------|----------|
| r | Read |
| w | Write |
| x | Execute |

---

## Permission Groups

| Position | Represents |
|-----------|------------|
| Owner | File owner |
| Group | Group members |
| Others | Everyone else |

---

## Numeric Permissions

| Value | Permission |
|---------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 0 | --- |

---

## Change Permissions

### Numeric Method

```bash
chmod 755 script.sh
```

### Symbolic Method

```bash
chmod u+x script.sh
```

```bash
chmod g-w file.txt
```

---

## Change Ownership

```bash
chown kali file.txt
```

```bash
chown kali:kali file.txt
```

---

## Special Permissions

### SUID

```bash
chmod u+s file
```

### SGID

```bash
chmod g+s file
```

### Sticky Bit

```bash
chmod +t folder
```

---

## SOC Analyst Usage

- Permission auditing
- Detect privilege abuse
- Secure sensitive files
- Incident response

---

## Quick Examples

```bash
ls -l
chmod 755 script.sh
chown kali:kali file.txt
```
