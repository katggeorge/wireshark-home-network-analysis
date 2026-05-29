# Wireshark Home Network Analysis

## Objective

Analyze network traffic using Wireshark to better understand:
- Network protocols
- Encrypted vs unencrypted traffic
- IPv4 and IPv6 usage
- TCP and UDP communication
- Basic traffic investigation techniques

---

## Tools Used

- Wireshark
- macOS
- Home network traffic capture

---

## Investigation Summary

The packet capture was analyzed using:
- Protocol Hierarchy Statistics
- Packet inspection
- Traffic filtering

Key findings:
- UDP traffic represented the majority of network traffic
- Most traffic appeared encrypted due to QUIC protocol usage
- IPv6 traffic was more common than IPv4
- Multiple modern web protocols were identified

---

## Findings

### Protocol Distribution

<img width="1206" height="654" alt="Screenshot 2026-05-28 at 9 40 03 PM" src="https://github.com/user-attachments/assets/c707627a-f0bb-4590-9141-1347ca02e9ee" />

- UDP traffic: approximately 88.9%
- TCP traffic: lower percentage compared to UDP

The protocol hierarchy statistics showed that UDP traffic represented the majority of captured traffic during analysis. 

### Encryption Observations
Most traffic was encrypted, likely due to:
- HTTPS
- QUIC protocol traffic
- Modern browser encryption standards

### IP Version Usage
- Majority IPv6 traffic observed
- Smaller amount of IPv4 traffic detected

---

## Skills Practiced

- Packet analysis
- Protocol identification
- Traffic investigation
- Network traffic interpretation
- Wireshark filtering
- Security analysis documentation

---

## Lessons Learned

This lab improved understanding of:
- Real-world network behavior
- Encrypted traffic patterns
- Common internet protocols
- Basic SOC analyst investigation workflows
