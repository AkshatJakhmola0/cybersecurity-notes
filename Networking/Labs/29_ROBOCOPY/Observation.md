# Observations – ROBOCOPY Command

## 1. Help Menu (`robocopy /?`)

- Displayed the syntax and available options for the ROBOCOPY command.
- Showed advanced switches such as `/S`, `/E`, and `/MIR`.
- Explained features for copying, synchronization, and backup.
- Useful for understanding command capabilities.

---

## 2. Create Source Folder (`mkdir C:\ROBOCOPY_Source`)

- Successfully created the source directory.
- The folder was used for testing copy operations.
- Prepared the environment for the experiment.
- Demonstrated directory creation using CMD.

---

## 3. Create Test File (`echo Test File > C:\ROBOCOPY_Source\test.txt`)

- Created a sample text file inside the source folder.
- Provided data for copy operations.
- Verified that the source directory contained files.
- Demonstrated basic file creation.

---

## 4. Basic Copy (`robocopy Source Destination`)

- Successfully copied the source directory and file.
- Automatically created the destination directory.
- Displayed detailed copy statistics.
- Reported one file copied successfully.

---

## 5. Copy with `/E`

- Copied all directories, including empty directories.
- Existing files were skipped because they were already up to date.
- No errors or failed copies were reported.
- Demonstrated efficient file synchronization.

---

## 6. Copy with `/S`

- Copied only non-empty directories.
- Unchanged files were skipped automatically.
- The operation completed without errors.
- Useful for routine backup operations.

---

## 7. Mirror with `/MIR`

- Mirrored the destination with the source directory.
- Enabled synchronization between both locations.
- Existing files remained unchanged because they were identical.
- Suitable for maintaining identical backup copies.

---

## 8. Copy Statistics

- ROBOCOPY displayed detailed statistics after each operation.
- Statistics included copied, skipped, failed, and mismatched files.
- No failed or mismatched files were reported.
- The summary confirmed successful execution of all copy operations.
