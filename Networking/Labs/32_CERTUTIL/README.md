# Lab 32 – CERTUTIL Command

## Objective

To understand the Windows **CERTUTIL** command and learn how to generate file hashes, verify file integrity, and perform Base64 encoding and decoding using Command Prompt.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Basic knowledge of files and cryptographic hash functions

---

## Theory

**CERTUTIL (Certificate Utility)** is a built-in Windows command-line tool primarily designed for managing certificates. It also provides several useful features for cybersecurity, including generating file hashes, encoding and decoding files using Base64, and verifying file integrity.

Security professionals frequently use CERTUTIL during malware analysis, digital forensics, incident response, and integrity verification.

---

## Syntax

```cmd
certutil [options]
```

Examples:

```cmd
certutil -hashfile sample.txt SHA256

certutil -encode sample.txt sample.b64

certutil -decode sample.b64 decoded.txt
```

---

## Commands Used

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

## Steps Performed

1. Displayed the CERTUTIL help menu.
2. Created a test folder.
3. Created a sample text file.
4. Generated the MD5 hash of the file.
5. Generated the SHA1 hash of the file.
6. Generated the SHA256 hash of the file.
7. Encoded the file into Base64 format.
8. Decoded the Base64 file back to its original form.
9. Verified that the decoded file matched the original file.

---

## Key Findings

- CERTUTIL successfully generated MD5, SHA1, and SHA256 hashes.
- Different hashing algorithms produced unique hash values.
- Base64 encoding converted the file into an encoded format.
- Base64 decoding successfully restored the original file.
- CERTUTIL can be used for integrity verification and file validation.

---

## Cybersecurity Perspective

CERTUTIL is useful for:

- File Integrity Verification
- Malware Analysis
- Digital Forensics
- Incident Response
- IOC Verification
- Base64 Encoding & Decoding
- Certificate Management
- Security Investigations

---

## Interview Questions

**Q1. What is CERTUTIL used for?**  
It is used for certificate management, file hashing, integrity verification, and Base64 encoding/decoding.

**Q2. Which command generates a SHA256 hash?**

```cmd
certutil -hashfile filename SHA256
```

**Q3. Why are hashes important in cybersecurity?**  
They verify file integrity and help detect unauthorized modifications.

**Q4. What does the `-encode` option do?**  
It converts a file into Base64 format.

**Q5. What does the `-decode` option do?**  
It restores a Base64-encoded file to its original format.

---

## Skills Gained

- File Integrity Verification
- Cryptographic Hashing
- Base64 Encoding & Decoding
- Windows Command-Line Administration
- Digital Forensics
- Malware Analysis
- Incident Response
