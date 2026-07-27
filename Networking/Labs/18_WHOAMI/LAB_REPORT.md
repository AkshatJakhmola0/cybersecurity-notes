# Lab Report

## Experiment Title

Study of the WHOAMI Command in Windows

---

## Objective

To study and understand the WHOAMI command in Windows for identifying the currently logged-in user, viewing the Security Identifier (SID), examining group memberships, inspecting user privileges, and understanding the security context of the current user account.

---

## Tools Used

- Windows 11
- Command Prompt
- WHOAMI Utility

---

## Commands Executed

```cmd
whoami

whoami /all

whoami /user

whoami /groups

whoami /priv

whoami /user /fo list

whoami /?
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `whoami` command to display the currently logged-in user.
3. Used `whoami /all` to display complete security information, including user details, groups, and privileges.
4. Executed `whoami /user` to display the user's Security Identifier (SID).
5. Used `whoami /groups` to view all group memberships associated with the current user.
6. Executed `whoami /priv` to display the privileges assigned to the current user.
7. Used `whoami /user /fo list` to display the user information in list format.
8. Executed `whoami /?` to view the built-in help menu and available command options.
9. Recorded the observations and captured screenshots for each command.

---

## Results

Successfully identified the currently logged-in user, displayed the user's Security Identifier (SID), viewed group memberships and assigned privileges, examined the complete user security token, and explored the available command-line options. The experiment demonstrated how the WHOAMI command provides valuable security information about the current user session and access permissions.

---

## Conclusion

The WHOAMI command is an essential Windows command-line utility for identifying the current user and examining the associated security context. It provides information about user identities, Security Identifiers (SIDs), group memberships, and user privileges, making it highly valuable for Windows administration, Active Directory environments, cybersecurity investigations, penetration testing, and incident response. Understanding the WHOAMI command helps administrators and security professionals verify user permissions and assess system security.

---

## Skills Gained

- User Enumeration
- Security Identifier (SID) Analysis
- Group Membership Analysis
- User Privilege Analysis
- Windows Security Administration
- Access Control Understanding
- Incident Response Fundamentals
- Windows Command Line Proficiency
