# Network Devices

## Definition

Network devices are hardware components used to connect devices, control traffic, and enable communication within a network.

Common network devices include:

- Hub
- Switch
- Router
- Modem
- Access Point (AP)
- Firewall

---

## Why

Without network devices, computers and other devices cannot communicate efficiently.

Network devices help to:

- Connect devices
- Forward data
- Manage network traffic
- Provide Internet access
- Improve network security

---

## Working

```text
Device
   │
   ▼
Switch
   │
   ▼
Router
   │
   ▼
Internet
```

Network devices receive, process, and forward data to the correct destination.

---

## Real-World Example

- **Hub** – Connects multiple computers and broadcasts data to every connected device.
- **Switch** – Connects devices in an office network and forwards data only to the intended device.
- **Router** – Connects your home or office network to the Internet.
- **Modem** – Connects your router to the Internet Service Provider (ISP).
- **Access Point (AP)** – Provides wireless (Wi-Fi) connectivity.
- **Firewall** – Filters and controls incoming and outgoing network traffic.

---

## Cybersecurity Perspective

- **Hub** – Insecure because all traffic is broadcast, making packet sniffing easy.
- **Switch** – More secure than a hub but can still be targeted by attacks such as MAC flooding.
- **Router** – Can be compromised through weak passwords, exposed services, or misconfigurations.
- **Modem** – Usually managed by the ISP; firmware should be kept updated.
- **Access Point (AP)** – Should use strong Wi-Fi encryption (WPA2/WPA3) and secure passwords.
- **Firewall** – Acts as the first line of defense by allowing or blocking traffic based on predefined security rules.

---

## Interview Questions

### Q1. Which device connects a local network to the Internet?

**Answer:** Router

---

### Q2. Which device provides Wi-Fi connectivity?

**Answer:** Access Point (AP)

---

### Q3. Which device forwards data based on MAC addresses?

**Answer:** Switch

---

### Q4. Which device converts ISP signals into usable network signals?

**Answer:** Modem

---

### Q5. Which device is used to filter network traffic?

**Answer:** Firewall

---

### Q6. Which is more secure: Hub or Switch?

**Answer:** Switch

---

## Key Takeaways

- **Hub** = Broadcasts data to all connected devices.
- **Switch** = Forwards data using MAC addresses.
- **Router** = Connects different networks using IP addresses.
- **Modem** = Connects your network to the ISP.
- **Access Point (AP)** = Provides wireless connectivity.
- **Firewall** = Filters and secures network traffic.

---

## Memory Trick

```text
H → S → R → M → AP → F

Hub → Switch → Router → Modem → Access Point → Firewall
```

**Easy to Remember**

- Data inside a network → **Switch**
- Network to Network → **Router**
- Internet Connection → **Modem**
- Wireless Network → **Access Point**
- Security → **Firewall**
