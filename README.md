# Wireshark Home Network Analysis
## Executive Summary
A Wireshark packet capture was performed on a home network to analyze protocol usage, encryption trends, and communication behavior. Analysis identified heavy UDP utilization driven by QUIC traffic, widespread encryption through HTTPS/TLS, and significant IPv6 adoption. The investigation established a baseline of normal network activity and demonstrated foundational packet analysis skills used in Security Operation Centers (SOCs).

---
## Table of Contents
- Executive Summary
- Objective
- Tools Used
- Methodology
- Findings
- Security Relevance
- Wireshark Filters Used
- Skills Practiced
- Lessons Learned
- Analyst Assessment
- Key Takeaway

---

## Objective

The goal of this project was to capture and analyze network traffic from a home network environment using Wireshark.

The investigation focused on:

- Identifying common network protocols
- Comparing encrypted and unencrypted traffic
- Examining IPv4 and IPv6 usage
- Understanding TCP and UDP communication patterns
- Practicing basic network traffic analysis techniques used in Security Operations Center (SOC) environments

## Tools Used

- Wireshark
- macOS
- Home network traffic capture

## Methodology

The packet capture was analyzed using:

- Protocol Hierarchy Statistics
- Packet Inspection
- Traffic Filtering
- Protocol Analysis

The objective was to identify traffic patterns and establish a basic understanding of network activity occurring on the host system.

Key findings:
- UDP traffic represented the majority of network traffic
- Most traffic appeared encrypted due to QUIC protocol usage
- IPv6 traffic was more common than IPv4
- Multiple modern web protocols were identified

## Findings

### Protocol Distribution
<img width="1196" height="631" alt="protocol-hierarchy-statistics" src="https://github.com/user-attachments/assets/b549cb18-fbb1-4f4d-96a2-0b9536f86e5e" />

The protocol hierarchy statistics revealed that UDP traffic accounted for approximately 88.9% of captured traffic, while TCP represented a smaller percentage.

This distribution is consistent with modern web activity where services increasingly utilize QUIC over UDP.

---
### DNS Activity
<img width="1195" height="892" alt="dns-traffic-analysis" src="https://github.com/user-attachments/assets/f9c85fad-6560-4a1f-a5d8-2f027ea0f685" />

DNS traffic was observed throughout the capture and demonstrated how devices resolve domain names before establishing network connections.

---
### TCP Communications
<img width="1161" height="662" alt="tcp-conversations" src="https://github.com/user-attachments/assets/a68ecf5a-e648-4173-9cf8-63751cc58adf" />

TCP conversations showed established connections between local devices and external services using reliable transport protocols.

---

### Encryption Observations
<img width="1191" height="893" alt="quic-udp-traffic" src="https://github.com/user-attachments/assets/cb6baf99-2cc3-4518-b902-0c1e4eb9811e" />

Most observed traffic was encrypted.
Protocols and technologies contributing to encrypted communication included:

- HTTPS
- TLS
- QUIC

This limited visibility into application-layer content while still allowing analysis of metadata and traffic behavior.

---
### IP Version Usage
The capture contained both IPv4 and IPv6 traffic.

Observations included:
- IPv6 traffic appeared more frequently than IPv4
- Modern devices and services increasingly favor IPv6 connectivity
- Both protocols were active during normal browsing activity
---

## Security Relevance

Understanding normal network behavior is essential for identifying anomalies and potential security threats.

Skills developed during this project include:

- Establishing network baselines
- Identifying protocol usage patterns
- Investigating encrypted traffic
- Interpreting packet-level information
- Documenting technical findings

## Wireshark Filters Used

- dns
- tcp
- udp
- ipv6
- quic

## Skills Practiced

- Packet analysis
- Protocol identification
- Traffic investigation
- Network traffic interpretation
- Wireshark filtering
- Security analysis documentation

## Lessons Learned
This project improved my understanding of:

- Real-world network behavior
- Encrypted traffic patterns
- Protocol hierarchy analysis
- IPv4 and IPv6 communication
- Basic SOC-style investigation workflows
- Technical documentation practices

## Analyst Assessment
No malicious traffic was identified during this capture.

Traffic patterns appeared consistent with normal web browsing activity.

The dominance of encrypted QUIC traffic demonstrates the increasing importance of metadata analysis when investigating modern network environments.

Future investigations could focus on: 
- DNS tunneling detection
- Suspicious outbound connections
- Beaconing behavior
- Command and control traffic indicators

---
## Key Takeaway
Modern network traffic is predominantly encrypted and UDP-based, requiring analysts to focus on metadata, protocol behavior, and traffic patterns rather than payload inspection.
