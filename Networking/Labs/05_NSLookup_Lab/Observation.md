# Observations

## Commands Executed

The following DNS queries were performed during this lab:

- `nslookup google.com`
- `nslookup github.com`
- `nslookup -type=mx google.com`
- `nslookup -type=ns google.com`
- `nslookup 8.8.8.8`
- Interactive Mode using Google Public DNS (`8.8.8.8`)

---

## DNS Server Information

- The default DNS server configured on the system was **192.168.0.1**, which is the local router.
- The server name appeared as **UnKnown** because the router does not have a configured PTR (reverse DNS) record.
- During Interactive Mode, the DNS server was changed to **Google Public DNS (8.8.8.8)**, which was successfully recognized as **dns.google**.

---

## Basic DNS Resolution

### Google

- Successfully resolved **google.com**.
- Multiple IPv4 (A) and IPv6 (AAAA) addresses were returned.
- The response was **Non-authoritative**, indicating that the answer came from a recursive DNS server rather than Google's authoritative name servers.
- Multiple IP addresses demonstrate Google's use of load balancing, redundancy, and globally distributed infrastructure.

### GitHub

- Successfully resolved **github.com**.
- Returned a single IPv4 address (`20.207.73.82`) during the query.
- The response was also **Non-authoritative**.

---

## Mail Exchange (MX) Record

- Successfully retrieved Google's Mail Exchange (MX) record.
- MX Preference: **10**
- Mail Exchanger: **smtp.google.com**
- MX records identify the mail servers responsible for receiving emails for a domain.

---

## Name Server (NS) Records

The following authoritative Name Servers were retrieved:

- ns1.google.com
- ns2.google.com
- ns3.google.com
- ns4.google.com

These servers are responsible for maintaining Google's official DNS records and provide redundancy, fault tolerance, and high availability.

---

## Reverse DNS Lookup

A reverse DNS lookup was performed on **8.8.8.8**.

Result:

- Hostname: **dns.google**
- IP Address: **8.8.8.8**

This confirmed that Google's public DNS server has a valid PTR (Pointer) record.

---

## Interactive Mode

Interactive Mode was used to perform multiple DNS queries without restarting the `nslookup` utility.

The following tasks were completed:

- Changed the DNS server to Google Public DNS (`8.8.8.8`)
- Queried A and AAAA records
- Queried MX records
- Queried NS records

This demonstrated how Interactive Mode improves efficiency when performing multiple DNS investigations.

---

## Security Observations

- DNS is one of the first services involved in almost every internet communication.
- `nslookup` is useful for verifying domain resolution and identifying DNS records.
- Reverse DNS lookups help identify the hostname associated with an IP address.
- MX records provide insight into a domain's email infrastructure.
- NS records identify the authoritative DNS servers for a domain.
- DNS information is valuable during network troubleshooting, threat hunting, phishing investigations, and penetration testing.

---

## Learning Outcome

After completing this lab, I gained practical experience in:

- Resolving domain names to IP addresses.
- Performing reverse DNS lookups.
- Retrieving MX and NS records.
- Using Google Public DNS for queries.
- Working with Interactive Mode in `nslookup`.
- Understanding the role of DNS in networking and cybersecurity.
