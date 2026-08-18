# Observations – Linux File System Exploration

## 1. Root Directory Listing (`ls /`)

- Displayed the top-level Linux directory structure.
- Observed important directories including:
  - /bin
  - /boot
  - /dev
  - /etc
  - /home
  - /root
  - /tmp
  - /usr
  - /var
- Confirmed successful access to the Linux root directory.
- Useful for understanding Linux file system hierarchy.

---

## 2. Navigate to Root Directory (`cd /`)

- Successfully navigated to the root directory.
- Verified current location as:

```text
/
```

- Demonstrated absolute path navigation.

---

## 3. Home Directory Exploration (`cd /home`)

- Successfully accessed the `/home` directory.
- Verified location:

```text
/home
```

- Confirmed presence of user home directories.
- Useful for locating user data and profiles.

---

## 4. Configuration Directory Exploration (`cd /etc`)

- Successfully accessed the `/etc` directory.
- Verified location:

```text
/etc
```

- Identified this directory as the primary location for Linux configuration files.
- Commonly reviewed during system administration and investigations.

---

## 5. Variable Data Directory Exploration (`cd /var`)

- Successfully accessed the `/var` directory.
- Verified location:

```text
/var
```

- Identified as the storage location for logs and frequently changing data.
- Important during incident response investigations.

---

## 6. Temporary Directory Exploration (`cd /tmp`)

- Successfully accessed the `/tmp` directory.
- Verified location:

```text
/tmp
```

- Identified as temporary storage used by applications and users.
- Frequently reviewed during forensic investigations.

---

## 7. Binary Directory Exploration (`cd /bin`)

- Successfully accessed the `/bin` directory.
- Verified location:

```text
/bin
```

- Identified as a location containing essential Linux commands and executables.
- Important for understanding system operation.

---

## 8. Incorrect Directory Navigation (`cd / etc`)

- Attempted to access `/etc` using incorrect syntax.
- Linux returned an error indicating the directory could not be found.
- Demonstrated that Linux commands require proper spacing and syntax.
- Useful for understanding command-line behavior.

---

## 9. Incorrect Command Execution (`owd`)

- Attempted to execute a non-existent command.
- Linux returned a command-not-found message.
- Suggested similar valid commands.
- Demonstrated Linux command validation mechanisms.

---

## 10. Root Directory Access Attempt (`cd /root`)

- Attempted to access the root user's home directory.
- Linux returned:

```text
Permission denied
```

- Confirmed that the current user lacks permission to access `/root`.
- Demonstrated Linux access control and permissions.

---

## 11. Incorrect Home Navigation (`cd~`)

- Attempted to use `cd~` without a space.
- Linux returned a command-not-found error.
- Demonstrated the importance of proper command syntax.

---

## 12. Return to Home Directory (`cd ~`)

- Successfully returned to the user's home directory.
- Verified location:

```text
/home/kali
```

- Confirmed proper usage of the home directory shortcut.

---

## Overall Analysis

- Successfully explored major Linux directories.
- Identified locations used for user data, configurations, logs, binaries, and temporary files.
- Observed Linux permission restrictions.
- Demonstrated correct and incorrect navigation methods.
- Improved understanding of Linux file system hierarchy.

---
