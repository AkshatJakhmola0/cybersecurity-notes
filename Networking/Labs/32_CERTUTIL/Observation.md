# Observations – CERTUTIL Command

## 1. Help Menu (`certutil -?`)

- Displayed the syntax and available CERTUTIL options.
- Listed commands related to certificates, hashing, encoding, and decoding.
- Helped understand the functionality of the utility.
- Useful before performing file operations.

---

## 2. Create Test Folder (`mkdir C:\CERTUTIL_Lab`)

- Successfully created the test directory.
- The folder was used for the CERTUTIL experiment.
- Prepared the environment for testing.
- Demonstrated directory creation using CMD.

---

## 3. Create Test File (`echo Hello Cyber Security > sample.txt`)

- Created a sample text file.
- Stored the file inside the test directory.
- Used the file for hashing and encoding operations.
- Verified successful file creation.

---

## 4. Generate MD5 Hash (`-hashfile ... MD5`)

- Successfully generated the MD5 hash.
- Produced a unique fingerprint for the file.
- Verified file integrity.
- Demonstrated basic hash generation.

---

## 5. Generate SHA1 Hash (`-hashfile ... SHA1`)

- Successfully generated the SHA1 hash.
- Produced a different hash value from MD5.
- Confirmed successful execution.
- Demonstrated another hashing algorithm.

---

## 6. Generate SHA256 Hash (`-hashfile ... SHA256`)

- Successfully generated the SHA256 hash.
- Produced a stronger cryptographic hash.
- Verified file integrity accurately.
- Commonly used in cybersecurity investigations.

---

## 7. Encode File (`-encode`)

- Converted the text file into Base64 format.
- Created a new encoded output file.
- Displayed input and output file sizes.
- Completed without errors.

---

## 8. Decode File (`-decode`)

- Successfully restored the original file from the Base64 file.
- Created a decoded output file.
- The decoded file matched the original content.
- Verified successful encoding and decoding.

---

## 9. Overall Analysis

- CERTUTIL successfully performed hashing, encoding, and decoding operations.
- Different hashing algorithms produced unique values for the same file.
- Base64 encoding and decoding preserved the original file content.
- The command is valuable for file integrity verification, digital forensics, and cybersecurity investigations.
