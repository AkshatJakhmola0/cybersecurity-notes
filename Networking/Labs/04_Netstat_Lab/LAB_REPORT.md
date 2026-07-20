# Lab Report

# Experiment Title

Windows Network Connection Analysis using Netstat

---

## Objective

To study active network connections, listening ports, TCP connection states, UDP endpoints, and identify the processes responsible for network communication using Windows command-line tools.

---

## Tools Used

- Windows Command Prompt
- netstat
- tasklist

---

## Commands Executed

```cmd
netstat

netstat -a

netstat -ano

tasklist
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `netstat` command to view active TCP connections.
3. Used `netstat -a` to display all active and listening TCP/UDP connections.
4. Executed `netstat -ano` to obtain Process IDs (PIDs) associated with each network connection.
5. Used `tasklist` to identify the processes corresponding to the observed PIDs.
6. Analyzed the relationship between network ports and running applications.

---

## Results

- Active TCP and UDP connections were successfully identified.
- Listening ports for Windows services and installed applications were observed.
- TCP connection states such as LISTENING, ESTABLISHED, TIME_WAIT, and CLOSE_WAIT were examined.
- Process IDs were successfully mapped to their corresponding applications.
- µTorrent Web, Google Chrome, Windows System services, OneDrive, and Dell services were identified as sources of network activity.

---

## Conclusion

The lab demonstrated how Windows manages network communication and how the `netstat` utility can be used to investigate network activity. By combining `netstat -ano` with `tasklist`, it was possible to identify which applications owned specific network connections. This process forms a fundamental part of network troubleshooting, security monitoring, malware analysis, and incident response.

---

## Skills Gained

- Network connection analysis
- TCP/IP troubleshooting
- Port identification
- Process identification using PID
- Basic host-based network investigation
- Windows command-line networking
- Security analysis using native Windows tools
