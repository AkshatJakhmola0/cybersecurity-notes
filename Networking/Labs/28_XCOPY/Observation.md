# Observations – XCOPY Command

## 1. Help Menu (`xcopy /?`)

- Displayed the syntax and available command options.
- Explained switches such as `/S`, `/E`, and `/Y`.
- Helped understand the usage of the XCOPY command.
- Useful for learning command-line options before execution.

---

## 2. Create Test Folder (`mkdir C:\XCOPY_Lab`)

- Successfully created the test directory.
- The folder served as the source location for the experiment.
- Existing folders generated an informational message.
- Prepared the environment for file-copy operations.

---

## 3. Create Test File (`echo Test File > C:\XCOPY_Lab\test.txt`)

- Created a sample text file.
- Verified that the source directory contained data.
- The file was used during copy operations.
- Demonstrated simple file creation using CMD.

---

## 4. Basic Copy (`xcopy C:\XCOPY_Lab "%USERPROFILE%\Desktop\XCOPY_Backup"`)

- Copied the test file to the destination.
- Windows prompted whether the destination was a file or directory because it did not already exist.
- The copy operation completed successfully.
- Demonstrated the default behavior of XCOPY.

---

## 5. Copy with `/S`

- Copied the directory and its subdirectories.
- Existing files generated an overwrite confirmation.
- The copy completed successfully after confirmation.
- Useful for copying directory structures.

---

## 6. Copy with `/E`

- Copied all directories, including empty ones.
- Prompted for overwrite when the destination already existed.
- Successfully copied the source data.
- Suitable for complete directory backups.

---

## 7. Copy with `/Y`

- Copied files without asking for overwrite confirmation.
- Simplified repeated copy operations.
- Successfully replaced existing files automatically.
- Useful for automated scripts and backups.

---

## 8. Verification

- Confirmed that the destination contained the copied file.
- Verified successful execution of all copy operations.
- The source file remained unchanged.
- Demonstrated successful use of the XCOPY command.
