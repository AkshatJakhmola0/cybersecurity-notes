# Lab 18 – WHOAMI Observations

---

## 1. Display Current Logged-in User

- Executed the `whoami` command.
- Displayed the currently logged-in Windows user account.
- Verified that the current user was successfully identified.
- Learned that this command quickly identifies the user under whose security context the current session is running.

---

## 2. Display Complete User Information

- Executed the `whoami /all` command.
- Displayed complete information about the current user.
- Observed the User Name, Security Identifier (SID), Group Memberships, and User Privileges.
- Learned that this command provides a complete view of the current user's security token and access rights.

---

## 3. Display User Information

- Executed the `whoami /user` command.
- Displayed the current user's name and Security Identifier (SID).
- Verified the unique SID assigned to the user account.
- Learned that every Windows user account is identified internally by its SID rather than its username.

---

## 4. Display Group Memberships

- Executed the `whoami /groups` command.
- Displayed all security groups associated with the current user.
- Observed memberships such as **Administrators**, **Users**, **Authenticated Users**, **Interactive**, and other Windows security groups.
- Learned that group memberships determine the permissions and access rights assigned to a user.

---

## 5. Display User Privileges

- Executed the `whoami /priv` command.
- Displayed all privileges assigned to the current user.
- Observed both enabled and disabled privileges, including **SeChangeNotifyPrivilege**, **SeImpersonatePrivilege**, and **SeCreateGlobalPrivilege**.
- Learned that privileges define the operations a user is permitted to perform on the system.

---

## 6. Display User Information in List Format

- Executed the `whoami /user /fo list` command.
- Displayed the username and SID in a list format.
- Observed that the list format provides a cleaner and more readable output than the default table format.
- Learned that different output formats are useful for documentation and reporting.

---

## 7. Display WHOAMI Help

- Executed the `whoami /?` command.
- Displayed the built-in help menu for the WHOAMI utility.
- Reviewed available parameters such as `/USER`, `/GROUPS`, `/PRIV`, `/ALL`, `/UPN`, `/FQDN`, `/LOGONID`, and output formatting options.
- Learned that the help menu provides complete syntax, parameter descriptions, and usage examples for the WHOAMI command.
