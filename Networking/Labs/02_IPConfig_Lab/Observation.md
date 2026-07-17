# Observations

## 1. `ipconfig`

- Displayed all network adapters.
- Active adapter: **Wi-Fi**
- Initial IPv4 Address: **192.168.0.118**
- Default Gateway: **192.168.0.1**
- VirtualBox Host-Only adapter: **192.168.56.1**
- Other adapters were disconnected.

---

## 2. `ipconfig /all`

- DHCP was **Enabled**.
- DHCP Server: **192.168.0.1**
- DNS Server: **192.168.0.1**
- Adapter: **Realtek 8821CE Wireless LAN**
- Displayed MAC Address, Lease Time, DNS Servers and other adapter details.
- VirtualBox adapter was configured with a static IP.

---

## 3. `ipconfig /displaydns`

- Displayed cached DNS records.
- Records included domains such as Google, GitHub, ChatGPT and Microsoft.
- Different record types (A, CNAME, PTR) and TTL values were visible.

---

## 4. `ipconfig / flushdns`

- Command failed because of incorrect syntax.
- Windows displayed:
  - **Error: unrecognized or incomplete command line.**
- Correct command:
  ```cmd
  ipconfig /flushdns
  ```

---

## 5. `ipconfig /flushdns`

- Successfully cleared the Windows DNS Resolver Cache.
- Future DNS requests will create new cache entries.

---

## 6. `ipconfig /release`

- Released the DHCP-assigned IPv4 address.
- IPv4 Default Gateway was removed.
- Link-local IPv6 address remained.
- VirtualBox adapter was unaffected.
- Disconnected adapters displayed **"Media disconnected"**.

---

## 7. `ipconfig /renew`

- Successfully obtained a new DHCP lease.
- New IPv4 Address: **192.168.1.34**
- Default Gateway: **192.168.1.1**
- DNS Suffix: **bbrouter**
- VirtualBox adapter remained unchanged.

---

## Overall Observation

This lab demonstrated how to inspect Windows network configuration, analyze the DNS cache, clear cached DNS records, and manage DHCP leases using the `ipconfig` utility. It also highlighted the importance of correct command syntax and the difference between active, disconnected, and virtual network adapters.
