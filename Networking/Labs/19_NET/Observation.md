# Lab 19 – NET Observations

---

## 1. Display Available NET Subcommands

- Executed the `net` command.
- Displayed the list of available NET subcommands.
- Observed commands related to user management, network shares, services, sessions, and workstation configuration.
- Learned that the NET utility is a collection of administrative commands rather than a single command.

---

## 2. Display NET Help

- Executed the `net help` command.
- Displayed the built-in help menu for the NET utility.
- Reviewed the available subcommands and syntax.
- Learned that help information is available for each individual NET subcommand.

---

## 3. Display Local User Accounts

- Executed the `net user` command.
- Displayed all local user accounts configured on the computer.
- Observed accounts such as **Administrator**, **aksha**, **DefaultAccount**, **Guest**, **WDAGUtilityAccount**, and **WsiAccount**.
- Learned that the command is useful for identifying local user accounts during system administration and security assessments.

---

## 4. Display Local Groups

- Executed the `net localgroup` command.
- Displayed all local security groups available on the system.
- Observed groups including **Administrators**, **Users**, **Guests**, **Hyper-V Administrators**, **OpenSSH Users**, **Performance Log Users**, and **Remote Management Users**.
- Learned that local groups determine the permissions and privileges assigned to users.

---

## 5. Display Shared Resources

- Executed the `net share` command.
- Displayed all shared resources configured on the system.
- Observed administrative shares such as **ADMIN$**, **C$**, **IPC$**, and **A$**.
- Learned that administrative shares are created automatically by Windows for remote management and administrative tasks.

---

## 6. Display Account Policies

- Executed the `net accounts` command.
- Displayed local account and password policy settings.
- Observed password age, minimum password length, account lockout threshold, lockout duration, and computer role.
- Learned that these policies help enforce password security and account protection.

---

## 7. Display Workstation Configuration

- Executed the `net config workstation` command.
- Displayed workstation configuration information.
- Observed the computer name, full computer name, current user, Windows version, workstation domain, and logon domain.
- Learned that this command provides useful system configuration details for troubleshooting and security investigations.
