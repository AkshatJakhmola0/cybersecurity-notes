# Ping Lab

## Objective

The objective of this lab is to understand how the `ping` command works and how it is used to test network connectivity between devices.

---

## Prerequisites

- Windows 10/11
- Command Prompt
- Active Internet Connection

---

## What is Ping?

The `ping` command is a network diagnostic tool used to verify whether a remote host is reachable over an IP network.

It uses the **ICMP (Internet Control Message Protocol)** to send Echo Request packets and waits for Echo Reply packets.

---

## Commands Used

```cmd
ping google.com

ping 8.8.8.8

ping localhost

ping 127.0.0.1
```

---

## Steps Performed

### Step 1

Open **Command Prompt**.

---

### Step 2

Run:

```cmd
ping google.com
```

Observe:

- IP Address
- Reply
- Time
- TTL

Take a screenshot.

---

### Step 3

Run:

```cmd
ping 8.8.8.8
```

Observe:

- Packet Loss
- Latency
- Reply

Take a screenshot.

---

### Step 4

Run:

```cmd
ping localhost
```

Observe:

- Local host response

Take a screenshot.

---

### Step 5

Run:

```cmd
ping 127.0.0.1
```

Observe:

- Loopback interface response

Take a screenshot.

---

## Expected Output

- Packets Sent
- Packets Received
- Lost Packets
- Minimum Time
- Maximum Time
- Average Time
- TTL Value

---

## Learning Outcome

After completing this lab, I learned:

- How Ping works
- What ICMP is
- How to test connectivity
- Difference between Domain Name and IP Address
- Purpose of the Loopback Address
- Basic network troubleshooting

---

## Cybersecurity Perspective

Ping is widely used by:

- Network Administrators
- SOC Analysts
- Penetration Testers
- Incident Responders

Attackers may also use Ping for host discovery during reconnaissance.

Some organizations block ICMP requests to reduce network reconnaissance.
