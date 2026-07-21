# Lab Report

## Experiment Title

**Using the Netsh Command to View and Analyze Windows Network Configuration**

---

## Objective

The objective of this experiment was to study the Windows **Netsh (Network Shell)** utility and understand its role in network administration. The experiment focused on viewing network interfaces, saved Wi-Fi profiles, wireless connection details, and Windows Defender Firewall configuration using Netsh commands.

---

## Tools Used

- Operating System: Windows 11
- Command Prompt (CMD)
- Netsh (Network Shell)
- Windows Defender Firewall
- Wi-Fi Network Connection

---

## Commands Executed

```cmd
netsh
interface show interface
wlan show profiles
wlan show interfaces
advfirewall show allprofiles
```

---

## Procedure

1. Opened Command Prompt.
2. Entered the Netsh interactive shell using the `netsh` command.
3. Displayed all available network interfaces using the `interface show interface` command.
4. Viewed all saved wireless network profiles using the `wlan show profiles` command.
5. Displayed detailed information about the active Wi-Fi connection using the `wlan show interfaces` command.
6. Examined the Windows Defender Firewall configuration for Domain, Private, and Public profiles using the `advfirewall show allprofiles` command.
7. Recorded observations and captured screenshots for each command.

---

## Results

- Successfully entered the Netsh interactive shell.
- Displayed all available network interfaces and identified active and inactive adapters.
- Verified that the **Wi-Fi** interface was connected while the **Ethernet** interface was disconnected.
- Displayed all saved wireless network profiles stored on the system.
- Verified that the system was connected to the **Jakhmola_5G** wireless network.
- Identified the wireless adapter as **Realtek 8821CE Wireless LAN 802.11ac PCI-E NIC**.
- Confirmed that the wireless connection used the **IEEE 802.11ac (Wi-Fi 5)** standard.
- Verified that the network used **WPA2-Personal** authentication with **CCMP (AES)** encryption.
- Observed a signal strength of **100%** with a receive and transmit rate of **433.3 Mbps**.
- Confirmed that the Domain, Private, and Public firewall profiles were enabled with the **BlockInbound, AllowOutbound** policy.
- Verified that Windows Defender Firewall was actively protecting the system.

---

## Conclusion

The experiment successfully demonstrated the functionality of the Windows **Netsh** utility. It provided detailed information about network interfaces, saved wireless profiles, active Wi-Fi connections, and firewall configurations. The Netsh command proved to be an effective tool for network administration, troubleshooting, and security auditing. Understanding its functionality is valuable for system administrators and cybersecurity professionals when managing Windows networking environments.

---

## Skills Gained

- Learned to use the Windows Netsh utility.
- Entered and navigated the Netsh interactive shell.
- Examined network interface status and connectivity.
- Viewed saved Wi-Fi profiles stored on the system.
- Analyzed wireless network configuration and security settings.
- Examined Windows Defender Firewall configuration.
- Improved Windows networking troubleshooting skills.
- Developed practical knowledge useful for system administration and cybersecurity.
