# Observations – Linux Installation and Navigation

## 1. Present Working Directory (`pwd`)

- Successfully displayed the current working directory.
- The current location was `/home/kali`.
- Confirmed that the logged-in user was operating from the home directory.
- Useful for understanding the current position within the Linux file system.

---

## 2. List Directory Contents (`ls`)

- Displayed the contents of the current directory.
- Standard user directories such as Desktop, Documents, Downloads, Music, Pictures, Public, Templates, and Videos were present.
- Confirmed successful access to the user's home directory.
- Useful for file system exploration and navigation.

---

## 3. Detailed Directory Listing (`ls -l`)

- Displayed detailed information about files and directories.
- Included permissions, ownership, file size, and modification dates.
- Verified that user directories were owned by the user `kali`.
- Useful for file management and permission analysis.

---

## 4. Hidden Files and Directories (`ls -la`)

- Displayed all files, including hidden files and directories.
- Identified important Linux configuration files such as:
  - `.bashrc`
  - `.profile`
  - `.zshrc`
  - `.ssh`
  - `.config`
  - `.local`
- Verified the presence of user-specific configuration files.
- Useful during Linux administration and security investigations.

---

## 5. Home Directory Navigation (`cd`)

- Executed the `cd` command without any arguments.
- Linux returned the user to the home directory.
- Demonstrated default behavior of the `cd` command.
- Useful for quickly navigating back to the home directory.

---

## 6. Incorrect Command Usage (`cd..`)

- Attempted to execute `cd..` without a space.
- Linux returned a "command not found" error.
- Demonstrated that Linux commands require proper spacing and syntax.
- Useful for understanding command-line behavior.

---

## 7. Parent Directory Navigation (`cd ..`)

- Successfully moved one directory level upward.
- Navigation changed from `/home/kali` to `/home`.
- Confirmed correct usage of parent directory traversal.
- Useful for navigating through directory structures.

---

## 8. Return to Home Directory (`cd ~`)

- Successfully returned to the home directory.
- Verified the use of `~` as a shortcut for the current user's home location.
- Simplifies Linux navigation.
- Commonly used during command-line operations.

---

## 9. User Identification (`whoami`)

- Successfully identified the currently logged-in user.
- The active user account was `kali`.
- Useful for access verification and system auditing.
- Commonly used during Linux enumeration activities.

---

## 10. Hostname Command Attempt (`host name`)

- Attempted to execute `host name`.
- Linux interpreted `host` as a DNS lookup utility.
- The command failed because no valid hostname was provided.
- Demonstrated the importance of correct command syntax.
- The correct command should be:

```bash
hostname
