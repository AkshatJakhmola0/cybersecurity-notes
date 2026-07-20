# NSLookup Lab

## Objective

The objective of this lab is to understand how the Domain Name System (DNS) works and how the `nslookup` utility can be used to query DNS records. This lab demonstrates how to resolve domain names to IP addresses, retrieve different types of DNS records, perform reverse DNS lookups, and investigate DNS information for troubleshooting and cybersecurity purposes.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Active Internet Connection
- Basic understanding of IP addresses and domain names

---

## Theory

The Domain Name System (DNS) is often referred to as the "phonebook of the Internet." Humans use domain names such as **google.com**, while computers communicate using IP addresses. DNS translates human-readable domain names into IP addresses, allowing users to access websites without remembering numerical addresses.

`nslookup` (Name Server Lookup) is a command-line utility used to query DNS servers. It helps administrators, network engineers, and cybersecurity professionals verify DNS records, troubleshoot name resolution issues, and investigate domains.

Common DNS Record Types:

- **A Record** – Maps a domain name to an IPv4 address.
- **AAAA Record** – Maps a domain name to an IPv6 address.
- **MX Record** – Specifies mail servers responsible for receiving emails.
- **NS Record** – Identifies the authoritative name servers for a domain.
- **CNAME Record** – Creates an alias for another domain.
- **PTR Record** – Performs reverse DNS lookups from an IP address to a hostname.

---

## Commands Used

```cmd
nslookup google.com

nslookup github.com

nslookup -type=mx google.com

nslookup -type=ns google.com

nslookup 8.8.8.8

nslookup
```

Interactive Mode:

```text
server 8.8.8.8
google.com
set type=mx
google.com
set type=ns
google.com
exit
```

---

## Steps Performed

1. Opened Command Prompt.
2. Queried the IP address of `google.com`.
3. Queried the IP address of `github.com`.
4. Retrieved Mail Exchange (MX) records for Google.
5. Retrieved Name Server (NS) records for Google.
6. Performed a reverse DNS lookup for the IP address `8.8.8.8`.
7. Entered Interactive Mode and queried multiple DNS record types using the same DNS server.

---

## Expected Output

- Successful resolution of domain names into IP addresses.
- Display of IPv4 and/or IPv6 addresses.
- List of Google's Mail Exchange (MX) servers.
- List of Google's authoritative Name Servers.
- Reverse DNS information for Google's public DNS server.
- Successful execution of DNS queries in Interactive Mode.

---

## Learning Outcome

After completing this lab, I was able to:

- Understand the purpose of DNS.
- Resolve domain names into IP addresses.
- Identify different DNS record types.
- Perform reverse DNS lookups.
- Use Interactive Mode in `nslookup`.
- Troubleshoot basic DNS resolution problems.

---

## Cybersecurity Perspective

DNS plays a critical role in cybersecurity. Security professionals frequently use `nslookup` during incident response, threat hunting, penetration testing, and phishing investigations. By examining DNS records, analysts can identify suspicious domains, verify email infrastructure, investigate malicious servers, and troubleshoot network communication issues.

Understanding DNS is also essential for detecting malware communication, command-and-control (C2) servers, DNS tunneling, and domain impersonation attacks.

---

## Challenge

During the lab, understanding the differences between various DNS record types and interpreting the returned information required careful analysis. Interactive Mode also introduced a different workflow compared to single-command queries.

---

## Interview Questions

1. What is DNS?
2. What is the purpose of the `nslookup` command?
3. What is the difference between A and AAAA records?
4. What are MX records used for?
5. What is an NS record?
6. What is a PTR record?
7. What is reverse DNS lookup?
8. What is the difference between recursive and authoritative DNS servers?
9. How can `nslookup` help during cybersecurity investigations?
10. What is DNS spoofing?

---

## Skills Gained

- DNS Fundamentals
- DNS Troubleshooting
- Domain Resolution
- Reverse DNS Lookup
- DNS Record Analysis
- Windows Command Line
- Network Troubleshooting
- Cybersecurity Investigation

---

## Lab Summary

This lab demonstrated how to use the `nslookup` utility to investigate DNS information. Multiple DNS record types were queried, reverse lookups were performed, and Interactive Mode was explored. The exercises provided practical experience in DNS analysis, an essential skill for network administrators and cybersecurity professionals.

---
