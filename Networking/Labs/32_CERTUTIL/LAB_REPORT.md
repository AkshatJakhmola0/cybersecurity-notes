# LAB REPORT

## Experiment Title

Study of the CERTUTIL Command in Windows Command Prompt

---

## Objective

To understand the working of the **CERTUTIL** command and learn how to generate cryptographic hashes, verify file integrity, and perform Base64 encoding and decoding using Command Prompt.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)

---

## Commands Executed

```cmd
certutil -?

mkdir C:\CERTUTIL_Lab

echo Hello Cyber Security > C:\CERTUTIL_Lab\sample.txt

certutil -hashfile C:\CERTUTIL_Lab\sample.txt MD5

certutil -hashfile C:\CERTUTIL_Lab\sample.txt SHA1

certutil -hashfile C:\CERTUTIL_Lab\sample.txt SHA256

certutil -encode C:\CERTUTIL_Lab\sample.txt C:\CERTUTIL_Lab\sample.b64

certutil -decode C:\CERTUTIL_Lab\sample.b64 C:\CERTUTIL_Lab\decoded.txt
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the CERTUTIL help menu.
3. Created a test folder named `CERTUTIL_Lab`.
4. Created a sample text file inside the folder.
5. Generated the MD5 hash of the sample file.
6. Generated the SHA1 hash of the sample file.
7. Generated the SHA256 hash of the sample file.
8. Encoded the file into Base64 format.
9. Decoded the Base64 file back to its original format.
10. Verified that the decoded file matched the original file.

---

## Results

- Successfully generated MD5, SHA1, and SHA256 hashes for the sample file.
- Verified that each hashing algorithm produced a unique hash value.
- Successfully encoded the file into Base64 format.
- Successfully decoded the Base64 file back to its original content.
- Confirmed that the decoded file matched the original file.
- All CERTUTIL operations completed successfully without errors.

---

## Conclusion

The **CERTUTIL** command is a powerful Windows utility for certificate management, file integrity verification, and Base64 encoding and decoding. It enables security professionals to generate cryptographic hashes, verify file authenticity, and perform encoding operations that are commonly encountered during malware analysis, digital forensics, and incident response. These capabilities make CERTUTIL an essential command-line tool for Windows administration and cybersecurity.

---

## Skills Gained

- Cryptographic Hash Generation
- File Integrity Verification
- Base64 Encoding and Decoding
- Windows Command-Line Administration
- Digital Forensics
- Malware Analysis
- Incident Response
- Security Investigation
