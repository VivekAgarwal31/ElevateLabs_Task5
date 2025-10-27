# 🌐 Network Traffic Analysis – Task 5  
**By:** Vivek Agrawal  
**Date:** October 27, 2025  
**Tool Used:** Wireshark  
**Environment:** Kali Linux  

---

## 🎯 Objective
The objective of this task was to **capture and analyze live network packets using Wireshark** to identify commonly used network protocols and understand their roles in data communication.  
This activity enhanced packet inspection, protocol identification, and troubleshooting skills through real-time traffic analysis.

---

## 🧰 Tools and Resources
- **Wireshark** — for live packet capture and protocol analysis.  
- **Active network interface (Wi-Fi)** — to generate and monitor network traffic.  
- **Browser and Ping utilities** — to generate DNS, HTTP, HTTPS, and ICMP traffic.  

---

## 🧪 Methodology
1. Installed and opened **Wireshark** on the assessment system.  
2. Selected the **active Wi-Fi network interface** for capturing packets.  
3. Initiated the capture and generated traffic by:  
   - Visiting websites (e.g., *google.com*, *youtube.com*).  
   - Sending ping requests to external servers.  
4. Stopped the capture after approximately **one minute**.  
5. Applied protocol filters: `dns`, `http`, `tcp`, `tls`, `icmp`, `arp`, `quic`, and `igmp`.  
6. Saved the capture file as **networkTraffic.pcapng** for detailed inspection.  

---

## 📡 Protocols Observed

| Protocol | Layer | Function | Example Observation |
|:--|:--|:--|:--|
| **DNS (Domain Name System)** | Application | Resolves domain names to IP addresses | Queries for *google.com* and *amazon.in* |
| **TCP (Transmission Control Protocol)** | Transport | Ensures reliable data transfer between devices | Three-way handshake (SYN, SYN-ACK, ACK) |
| **HTTP (Hypertext Transfer Protocol)** | Application | Transfers unencrypted web content | HTTP GET requests |
| **TLS (Transport Layer Security)** | Application/Session | Encrypts HTTPS communication | TLS handshake and encrypted packets |
| **QUIC (Quick UDP Internet Connections)** | Application/Transport | Combines transport and encryption (used in HTTP/3) | QUIC packets replacing TCP+TLS |
| **ICMP (Internet Control Message Protocol)** | Network | Used for diagnostics and connectivity testing | Echo request and reply packets |
| **ARP (Address Resolution Protocol)** | Data Link | Maps IP addresses to MAC addresses | ARP requests between local devices |
| **IGMP (Internet Group Management Protocol)** | Network | Manages multicast group memberships | IGMP Membership Reports for 224.0.0.1 and 224.0.0.22 |

---

## 🔍 Key Observations
- DNS lookups occurred **before** HTTP and QUIC communications, resolving domain names first.  
- Modern browsers predominantly used **QUIC (HTTP/3)**, replacing TCP/TLS layers for efficiency.  
- **TLS and QUIC** packets were encrypted — only handshake and metadata were visible.  
- **ICMP packets** confirmed network connectivity through echo requests and replies.  
- **IGMP and ARP** traffic highlighted local device communication and multicast group exchanges.  

---

## 📊 Summary of Findings

| Category | Observation |
|:--|:--|
| **Total Packets Captured** | 52,581 packets |
| **Most Active Protocols** | QUIC, TCP, DNS, TLS |
| **Encryption Present** | TLS and QUIC |
| **Local Network Activity** | ARP and IGMP packets |
| **Transport Layer Trend** | QUIC replaced TCP/UDP for HTTP/3 |
| **Web Traffic** | Primarily encrypted HTTPS and HTTP/3 packets |
| **Ping Activity** | ICMP Echo Request and Reply observed |

---

## 🧠 Learnings and Insights
- Learned how to **capture and filter live packets** effectively.  
- Understood how various protocols interact across different layers of the **TCP/IP model**.  
- Observed the dominance of **QUIC/HTTP3** in modern encrypted web traffic.  
- Distinguished between **encrypted** (TLS/QUIC) and **unencrypted** (HTTP/DNS) communications.  
- Gained practical skills in **network troubleshooting and traffic behavior analysis**.  

---

## 💬 Interview Preparation – Quick Answers

| Question | Answer |
|:--|:--|
| **What is Wireshark used for?** | It captures and analyzes network packets to understand traffic flow and protocol behavior. |
| **What is a packet?** | A packet is a formatted unit of data transmitted across a network. |
| **How to filter packets in Wireshark?** | By using display filters such as `http`, `dns`, `tcp`, or `icmp` in the filter bar. |
| **Difference between TCP and UDP?** | TCP is connection-oriented and reliable, while UDP is connectionless and faster. |
| **What is a DNS query packet?** | A packet that requests IP address resolution for a domain name. |
| **How does packet capture help troubleshooting?** | It identifies network delays, misconfigurations, or packet losses. |
| **What is a protocol?** | A standardized rule set that governs communication between network devices. |
| **Can Wireshark decrypt encrypted traffic?** | Only if provided with decryption keys; otherwise, encrypted payloads remain unreadable. |

---

## 📁 Deliverables
- `networkTraffic.pcapng` — raw packet capture file.  
- `Network Traffic Analysis Report.pdf` — detailed analysis and summary.  
- `task5_README.md` — this documentation file.  

---

## 🏁 Outcome
The network traffic analysis task successfully demonstrated how **data travels through multiple network layers** and how different protocols operate together.  
By analyzing live packets, a deeper understanding of **encrypted communications**, **protocol interactions**, and **network behavior** was achieved.  
This exercise strengthened analytical and diagnostic capabilities essential for cybersecurity and network forensics.

---

> ✨ *Prepared by Vivek Agrawal as part of the Cybersecurity Internship — Network Traffic Analysis Task 5 (October 2025).*
