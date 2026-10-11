# wireshark-network-traffic-analysis
# Network Traffic Analysis Using Wireshark

**Author:** Vaibhavi Singh  
**Tools:** Wireshark, Windows OS  
**Project Type:** Hands-on Networking and Cybersecurity Project

## Overview

This project explores network traffic analysis using Wireshark. I captured live network traffic and applied display filters to investigate DNS queries and responses, TCP connection establishment, retransmission indicators, TLS traffic, and HTTP requests.

The goal was to develop practical skills in packet inspection, protocol analysis, and basic network troubleshooting.

## Objectives

- Examine DNS queries and corresponding responses.
- Understand the TCP three-way handshake: SYN, SYN-ACK, and ACK.
- Investigate TCP retransmission indicators.
- Observe TLS traffic and understand the limitations of inspecting encrypted application data.
- Examine HTTP requests where visible in the capture.

## Tools Used

- Wireshark
- Windows OS
- Wi-Fi network interface

## Display Filters Practiced

| Filter | Purpose |
|---|---|
| `dns` | Inspect DNS queries and responses |
| `dns.flags.response == 1` | Display DNS responses |
| `tcp` | Inspect TCP traffic |
| `tcp.flags.syn == 1 && tcp.flags.ack == 0` | Identify SYN packets |
| `tcp.flags.syn == 1 && tcp.flags.ack == 1` | Identify SYN-ACK packets |
| `tcp.analysis.retransmission` | Investigate retransmission indicators |
| `tls` | Inspect TLS traffic |
| `http` | Inspect HTTP traffic, if present |

## Key Learnings

- How DNS queries and responses support domain-name resolution.
- How TCP establishes connections using a three-way handshake.
- How Wireshark identifies packets that may require retransmission analysis.
- Why TLS application data is generally unreadable without appropriate decryption conditions.
- Why packet-level evidence and context matter when investigating network issues.

## Findings and Limitations

The captured traffic included DNS activity, TCP packets, TLS traffic, and packets identified for retransmission analysis. These observations provided an opportunity to practice protocol inspection and troubleshooting.

Retransmissions alone do not prove packet loss or high latency. Likewise, a complete TCP handshake must be verified using packets from the same connection.

## Report

The public PDF report documents the methodology, filters, analysis, findings, and conclusion.

**Report:** `report/wireshark-analysis-report.pdf`

## Privacy and Security

Detailed screenshots and raw packet captures are intentionally excluded from this public repository to reduce exposure of IP addresses, MAC addresses, DNS history, and other potentially sensitive network information.

A separate private evidence report is retained locally for personal reference and verification.

## Disclaimer

This project was conducted for educational purposes using network traffic available on my device. Findings are limited to the captured traffic and should not be interpreted as conclusive proof of a network fault without further investigation.
