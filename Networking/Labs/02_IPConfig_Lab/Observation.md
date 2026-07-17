# Observations

## Command 1

```cmd
ipconfig
```

### Observation

- The system displayed all available network adapters.
- The active adapter was the Wi-Fi adapter.
- IPv4 Address: **192.168.0.118**
- Subnet Mask: **255.255.255.0**
- Default Gateway: **192.168.0.1**
- Multiple disconnected adapters were also listed.

---

## Command 2

```cmd
ipconfig /all
```

### Observation

The command displayed detailed information including:

- Host Name
- MAC Address
- DHCP Status
- DNS Server
- Lease Information
- Network Adapter Description
- VirtualBox Host-Only Adapter
- Physical Addresses
- IPv4 and IPv6 Configuration

---

## Command 3

```cmd
ipconfig /displaydns
```

### Observation

The DNS cache contained multiple cached entries, including:

- Google
- GitHub
- ChatGPT
- Microsoft Services
- WhatsApp
- Google Drive
- Cloudflare

Different DNS record types were observed:

- A Records
- CNAME Records
- PTR Records

TTL values were also displayed for each cached entry.

---

## Command 4

```cmd
ipconfig /flushdns
```

### Observation

The Windows DNS Resolver Cache was successfully cleared.

Previously cached DNS entries were removed from the local DNS cache.

Subsequent DNS requests will require fresh resolution from the configured DNS server.

---

## Overall Observation

The lab demonstrated how Windows stores and manages network configuration and DNS cache information. It also showed how DNS cache can be inspected and cleared for troubleshooting or security purposes.
