# LAB REPORT

## Experiment Title

Study of the ICACLS Command in Windows Command Prompt

---

## Objective

To understand the working of the **ICACLS** command and learn how to view, grant, and remove NTFS file and folder permissions using Command Prompt.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

```cmd
icacls /?

mkdir C:\ICACLS_Lab

echo Test File > C:\ICACLS_Lab\test.txt

icacls C:\ICACLS_Lab

icacls C:\ICACLS_Lab\test.txt

icacls C:\ICACLS_Lab /grant Everyone:R

icacls C:\ICACLS_Lab /remove Everyone
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the ICACLS help menu.
3. Created a test folder named `ICACLS_Lab`.
4. Created a sample text file inside the folder.
5. Displayed the NTFS permissions of the folder.
6. Displayed the NTFS permissions of the file.
7. Granted **Read** permission to the **Everyone** group.
8. Removed the permission from the **Everyone** group.
9. Verified the updated permissions.

---

## Results

- Successfully created the test folder and sample file.
- Displayed the NTFS permissions of both the folder and file.
- Granted **Read** permission to the **Everyone** group successfully.
- Removed the **Everyone** permission successfully.
- All permission changes were applied without errors.
- Verified that ICACLS can efficiently manage NTFS access permissions.

---

## Conclusion

The **ICACLS** command is a powerful Windows utility for viewing and managing NTFS file and folder permissions. It enables administrators to control user access, grant or remove permissions, and audit security settings. These capabilities make ICACLS an essential tool for Windows administration, access control management, cybersecurity, and digital forensic investigations.

---

## Skills Gained

- NTFS Permission Management
- Windows Access Control
- Windows Administration
- Command-Line Administration
- Security Auditing
- Access Control Management
- Digital Forensics
- Windows Security
```
