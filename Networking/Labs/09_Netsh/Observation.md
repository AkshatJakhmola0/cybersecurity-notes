# Observations

## 1. Netsh Interactive Shell

- Executed the `netsh` command to launch the Windows Network Shell.
- Successfully entered the interactive Netsh environment, indicated by the `netsh>` prompt.
- Verified that the utility was ready to accept networking commands directly without requiring the `netsh` prefix.
- Confirmed that the interactive shell can be used to configure, manage, and troubleshoot various Windows networking components.

---

## 2. Network Interfaces

- Executed the `interface show interface` command to display all available network interfaces.
- Observed three network interfaces: **Ethernet**, **Ethernet 2**, and **Wi-Fi**.
- Verified that the **Wi-Fi** interface was enabled and connected, serving as the primary network connection.
- Observed that the **Ethernet** interface was enabled but disconnected, indicating that no wired network cable was connected.
- Observed that **Ethernet 2** was enabled and connected, representing an additional active network interface.
- Verified that all listed interfaces were of the **Dedicated** type.

---

## 3. Saved Wi-Fi Profiles

- Executed the `wlan show profiles` command to display all saved wireless network profiles.
- Verified that no Group Policy Wi-Fi profiles were configured on the system.
- Observed multiple user-created Wi-Fi profiles representing previously connected wireless networks.
- Confirmed that Windows stores wireless network profiles for automatic reconnection.
- Learned that saved Wi-Fi profiles contain network configuration details such as the SSID, authentication method, and encryption settings.
- Understood that reviewing saved Wi-Fi profiles is useful for network administration, troubleshooting, and cybersecurity investigations.

---

## 4. Connected Wi-Fi Interface

- Executed the `wlan show interfaces` command to display detailed information about the active wireless network interface.
- Verified that the system was connected through the **Wi-Fi** interface using the **Realtek 8821CE Wireless LAN 802.11ac PCI-E NIC** adapter.
- Confirmed that the connected wireless network (SSID) was **Jakhmola_5G**.
- Observed that the connection was operating on the **5 GHz** frequency band using **Channel 36**.
- Identified the network type as **Infrastructure**, indicating communication through a wireless access point.
- Verified that the wireless standard in use was **IEEE 802.11ac (Wi-Fi 5)**.
- Observed that the network used **WPA2-Personal** authentication with **CCMP (AES)** encryption.
- Measured a receive and transmit link speed of **433.3 Mbps**.
- Recorded a signal strength of **100%** with an RSSI value of **-42 dBm**, indicating an excellent wireless connection.
- Confirmed that the connection mode was set to **Auto Connect**, allowing Windows to reconnect automatically to the saved network.

---

## 5. Windows Firewall Configuration

- Executed the `advfirewall show allprofiles` command to display the configuration of Windows Defender Firewall.
- Verified that the **Domain**, **Private**, and **Public** firewall profiles were enabled.
- Observed that the firewall policy for all profiles was configured as **BlockInbound, AllowOutbound**, blocking unsolicited incoming traffic while allowing outgoing connections.
- Confirmed that inbound user notifications were enabled for all firewall profiles.
- Observed that **Remote Management** was disabled across all firewall profiles, improving system security.
- Verified that **Unicast Response to Multicast** was enabled.
- Reviewed the firewall logging configuration and observed that logging for both allowed and dropped connections was disabled.
- Identified the default firewall log file location as `%systemroot%\system32\LogFiles\Firewall\pfirewall.log` with a maximum log file size of **4096 KB**.
- Confirmed that Windows Defender Firewall was actively protecting the system across all network profiles.

---

## Summary

- Successfully launched and used the Windows Netsh interactive shell.
- Examined the available network interfaces and identified active and inactive adapters.
- Reviewed all saved Wi-Fi profiles stored on the system.
- Analyzed the active wireless connection, including SSID, frequency band, wireless standard, authentication, encryption, signal strength, and connection speed.
- Examined Windows Defender Firewall settings for Domain, Private, and Public network profiles.
- Learned how the Netsh utility is used for network administration, troubleshooting, firewall management, and cybersecurity tasks.
