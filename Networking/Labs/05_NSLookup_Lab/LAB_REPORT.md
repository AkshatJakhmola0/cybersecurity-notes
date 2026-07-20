# Lab Report

## Experiment Title

DNS Investigation Using NSLookup

---

## Objective

To understand the working of the Domain Name System (DNS) and use the `nslookup` utility to perform domain name resolution, retrieve DNS records, perform reverse DNS lookups, and investigate DNS information using both standard and Interactive Mode.

---

## Tools Used

- Windows 11
- Command Prompt (CMD)
- NSLookup Utility
- Internet Connection

---

## Commands Executed

```cmd
nslookup google.com

nslookup github.com

nslookup -type=mx google.com

nslookup -type=ns google.com

nslookup 8.8.8.8

nslookup

server 8.8.8.8
google.com
set type=mx
google.com
set type=ns
google.com
exit
```

---

## Procedure

1. Opened Command Prompt.
2. Performed a DNS lookup for `google.com`.
3. Performed a DNS lookup for `github.com`.
4. Retrieved the Mail Exchange (MX) record for `google.com`.
5. Retrieved the Name Server (NS) records for `google.com`.
6. Performed a reverse DNS lookup for the IP address `8.8.8.8`.
7. Entered Interactive Mode and changed the DNS server to Google's Public DNS (`8.8.8.8`).
8. Queried A/AAAA, MX, and NS records using Interactive Mode.

---

## Results

- Successfully resolved `google.com` and `github.com` to their IP addresses.
- Retrieved IPv4 and IPv6 records for Google.
- Retrieved the MX record (`smtp.google.com`) for Google's email service.
- Retrieved Google's authoritative Name Server records (`ns1.google.com` to `ns4.google.com`).
- Successfully performed a reverse DNS lookup for `8.8.8.8`, which resolved to `dns.google`.
- Successfully used Interactive Mode to perform multiple DNS queries using Google Public DNS.

---

## Conclusion

The NSLookup lab provided practical experience with DNS investigation and name resolution. Different DNS record types, including A, AAAA, MX, NS, and PTR records, were successfully queried. Interactive Mode demonstrated an efficient way to perform multiple DNS lookups using a selected DNS server. This lab strengthened the understanding of DNS operations and their importance in networking and cybersecurity.

---

## Skills Gained

- DNS Fundamentals
- Domain Name Resolution
- Reverse DNS Lookup
- MX Record Analysis
- NS Record Analysis
- Interactive Mode in NSLookup
- Windows Command Line
- Network Troubleshooting
- Cybersecurity Reconnaissance
