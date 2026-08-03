# Observations – ICACLS Command

## 1. Help Menu (`icacls /?`)

- Displayed the syntax and available ICACLS options.
- Explained commands for viewing and modifying NTFS permissions.
- Included options for granting, removing, and resetting permissions.
- Useful for understanding command usage.

---

## 2. Create Test Folder (`mkdir C:\ICACLS_Lab`)

- Successfully created the test directory.
- The folder served as the target for permission management.
- Prepared the environment for the experiment.
- Demonstrated directory creation using CMD.

---

## 3. Create Test File (`echo Test File > C:\ICACLS_Lab\test.txt`)

- Created a sample text file inside the test folder.
- Verified that the folder contained data.
- The file was used to examine NTFS permissions.
- Demonstrated file creation using the command line.

---

## 4. View Folder Permissions (`icacls C:\ICACLS_Lab`)

- Displayed the NTFS permissions assigned to the folder.
- Listed user groups and their access rights.
- Showed inherited permissions from the parent directory.
- Confirmed successful retrieval of folder permissions.

---

## 5. View File Permissions (`icacls C:\ICACLS_Lab\test.txt`)

- Displayed the permissions assigned to the file.
- Listed access rights for users and groups.
- Confirmed that file permissions were inherited correctly.
- Useful for verifying file-level security settings.

---

## 6. Grant Read Permission (`/grant Everyone:R`)

- Successfully granted Read permission to the **Everyone** group.
- Updated the Access Control List (ACL) of the folder.
- The command completed without errors.
- Demonstrated permission assignment using ICACLS.

---

## 7. Remove Permission (`/remove Everyone`)

- Successfully removed the permission assigned to **Everyone**.
- Restored the original access control configuration.
- The command completed successfully.
- Verified that permissions can be modified dynamically.

---

## 8. Overall Analysis

- ICACLS successfully displayed and managed NTFS permissions.
- Permission changes were applied immediately.
- The command is useful for access control, security auditing, and Windows administration.
- ICACLS is an essential tool for managing file and folder security.
