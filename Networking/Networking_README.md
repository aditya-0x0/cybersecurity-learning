# 🌐 Networking

> A comprehensive record of my networking knowledge, from fundamental concepts to advanced networking and cybersecurity concepts.

Networking is one of the core foundations of cybersecurity. Understanding how devices communicate, how packets move across networks, how protocols work, and how network security mechanisms operate is essential for security analysis, reconnaissance, penetration testing, and defensive security.

---

## 🎯 Learning Objectives

Through networking, I developed an understanding of:

- How computer networks work
- How devices communicate
- How data is encapsulated and transmitted
- How addressing and routing work
- How common network protocols operate
- How ports and services are exposed
- How DNS and DHCP work
- How network traffic can be analyzed
- How network security mechanisms protect systems
- How networking concepts are applied in cybersecurity

---

# 1. 🧩 Network Fundamentals

## What is a Network?

A computer network is a collection of interconnected devices that communicate and exchange data using defined protocols.

### Core Concepts

- Client and server
- Hosts
- Nodes
- Network interfaces
- Packets
- Frames
- Segments
- Bandwidth
- Throughput
- Latency
- Jitter
- Network topology
- Communication protocols

---

# 2. 🏗️ Types of Networks

### PAN — Personal Area Network

Small network around an individual.

Examples:

- Bluetooth
- Personal hotspot

### LAN — Local Area Network

Network within a limited geographic area.

Examples:

- Home network
- School network
- Office network

### WLAN — Wireless LAN

LAN implemented using wireless communication.

### MAN — Metropolitan Area Network

Network covering a city or metropolitan area.

### WAN — Wide Area Network

Network covering large geographical areas.

Example:

- The Internet

### Other Network Concepts

- Intranet
- Extranet
- Internet
- VPN
- VLAN

---

# 3. 🕸️ Network Topologies

Studied common network topologies:

- Bus
- Star
- Ring
- Mesh
- Tree
- Hybrid

### Key Considerations

- Scalability
- Fault tolerance
- Cost
- Performance
- Single points of failure

---

# 4. 🔄 OSI Model

The OSI model provides a conceptual framework for understanding network communication.

| Layer | Name | Examples |
|---|---|---|
| 7 | Application | HTTP, DNS, FTP, SMTP |
| 6 | Presentation | Encoding, Encryption, Compression |
| 5 | Session | Session management |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP, ICMP, Routing |
| 2 | Data Link | Ethernet, ARP, MAC |
| 1 | Physical | Cables, Radio, Signals |

### Security Perspective

Understanding OSI layers helps identify where attacks, controls, and monitoring mechanisms operate.

---

# 5. 🌐 TCP/IP Model

The TCP/IP model is the practical networking model used by modern networks.

| Layer | Examples |
|---|---|
| Application | HTTP, DNS, SSH, SMTP |
| Transport | TCP, UDP |
| Internet | IP, ICMP |
| Network Access | Ethernet, Wi-Fi |

### OSI ↔ TCP/IP Mapping

```text
OSI                         TCP/IP

Application ───────┐
Presentation ──────┤───→ Application
Session ───────────┘

Transport ─────────────→ Transport

Network ───────────────→ Internet

Data Link ────────┐
Physical ─────────┴───→ Network Access
```

---

# 6. 📦 Encapsulation & Decapsulation

Data is encapsulated as it moves down the networking stack.

```text
Application Data
       ↓
     Segment
       ↓
      Packet
       ↓
      Frame
       ↓
     Bits
```

At the destination, the process is reversed.

```text
Bits
 ↓
Frame
 ↓
Packet
 ↓
Segment
 ↓
Application Data
```

### Important Terms

- Encapsulation
- Decapsulation
- Header
- Payload
- Trailer
- MTU

---

# 7. 🆔 MAC Addresses

A MAC address identifies a network interface at the Data Link layer.

Example:

```text
00:1A:2B:3C:4D:5E
```

Concepts:

- MAC address
- NIC
- OUI
- Unicast
- Multicast
- Broadcast

---

# 8. 🌍 IP Addressing

An IP address identifies a host/interface at the network layer.

## IPv4

IPv4 uses 32-bit addresses.

Example:

```text
192.168.1.10
```

## IPv6

IPv6 uses 128-bit addresses.

Example:

```text
2001:db8::1
```

---

# 9. 🔢 IPv4 Address Classes

Traditional IPv4 classes:

| Class | Range |
|---|---|
| A | 1.0.0.0 – 126.255.255.255 |
| B | 128.0.0.0 – 191.255.255.255 |
| C | 192.0.0.0 – 223.255.255.255 |
| D | 224.0.0.0 – 239.255.255.255 |
| E | 240.0.0.0 – 255.255.255.255 |

Modern networks primarily use CIDR rather than classful addressing.

---

# 10. 🏠 Private & Public IP Addresses

### Private IPv4 Ranges

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

Private addresses are commonly used inside local networks.

### Public IP

A globally routable address used for communication across the Internet.

---

# 11. 🔢 Subnetting & CIDR

Studied:

- Subnet masks
- Network address
- Broadcast address
- Host addresses
- CIDR notation
- Prefix length
- Network segmentation

Examples:

```text
192.168.1.0/24
10.0.0.0/8
172.16.0.0/16
```

### Why Subnetting Matters

- Efficient IP allocation
- Network segmentation
- Routing
- Security boundaries
- Broadcast control

---

# 12. 🚦 Default Gateway

A default gateway is the device that forwards traffic from a local network toward other networks.

Typical example:

```text
Host
 ↓
Switch
 ↓
Router / Gateway
 ↓
Internet
```

---

# 13. 🔀 Switching

A switch connects devices within a LAN.

Important concepts:

- MAC address table
- Frame forwarding
- Broadcast domain
- Collision domain
- VLAN
- Access port
- Trunk port

---

# 14. 🛣️ Routing

Routing determines how packets travel between networks.

### Routing Concepts

- Router
- Routing table
- Next hop
- Default route
- Static routing
- Dynamic routing
- Autonomous systems

### Common Routing Protocols

- RIP
- OSPF
- EIGRP
- BGP

BGP is fundamental to Internet-scale routing.

---

# 15. 🔌 Ports

A port identifies a network service endpoint.

Port ranges:

```text
0–1023       Well-known
1024–49151   Registered
49152–65535  Dynamic / Private
```

### Common Ports

| Port | Protocol / Service |
|---:|---|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 67/68 | DHCP |
| 80 | HTTP |
| 110 | POP3 |
| 123 | NTP |
| 143 | IMAP |
| 161/162 | SNMP |
| 389 | LDAP |
| 443 | HTTPS |
| 445 | SMB |
| 3389 | RDP |

---

# 16. 🚚 TCP

TCP is a connection-oriented transport protocol.

### TCP Characteristics

- Connection-oriented
- Reliable delivery
- Ordered data
- Error detection
- Flow control
- Congestion control

### TCP Three-Way Handshake

```text
Client                  Server

  SYN  ───────────────→
       ←──────── SYN-ACK
  ACK  ───────────────→

       Connection Established
```

### TCP Connection Termination

Commonly involves:

```text
FIN
ACK
FIN
ACK
```

---

# 17. ⚡ UDP

UDP is a connectionless transport protocol.

Characteristics:

- Low overhead
- No connection establishment
- No guaranteed delivery
- No guaranteed ordering
- Useful for latency-sensitive communication

Common uses:

- DNS
- DHCP
- VoIP
- Streaming
- Online gaming

---

# 18. 🧠 ARP

Address Resolution Protocol maps an IPv4 address to a MAC address on a local network.

Basic process:

```text
Who has 192.168.1.10?
        ↓
ARP Request
        ↓
192.168.1.10 replies
        ↓
MAC address returned
```

### Security Relevance

ARP can be abused in attacks such as ARP spoofing / poisoning, which can facilitate man-in-the-middle scenarios.

---

# 19. 🌐 DNS

The Domain Name System translates domain names into IP addresses and provides other DNS information.

Example:

```text
example.com
     ↓
DNS
     ↓
93.184.216.34
```

### Common DNS Records

| Record | Purpose |
|---|---|
| A | IPv4 address |
| AAAA | IPv6 address |
| CNAME | Canonical name |
| MX | Mail server |
| NS | Name server |
| TXT | Text / verification information |
| PTR | Reverse DNS |
| SOA | Zone authority information |

### DNS Security Concepts

- DNS spoofing
- DNS cache poisoning
- DNS tunneling
- DNSSEC
- DNS reconnaissance

---

# 20. 📡 DHCP

Dynamic Host Configuration Protocol automatically provides network configuration.

Typically provides:

- IP address
- Subnet mask
- Default gateway
- DNS server

### DHCP Process

```text
Discover
   ↓
Offer
   ↓
Request
   ↓
ACK
```

Known as **DORA**.

---

# 21. 🌍 HTTP & HTTPS

## HTTP

HTTP is an application-layer protocol used for web communication.

Common methods:

```text
GET
POST
PUT
PATCH
DELETE
HEAD
OPTIONS
```

## HTTPS

HTTPS is HTTP protected using TLS.

Provides:

- Confidentiality
- Integrity
- Server authentication

---

# 22. 🔐 TLS

TLS provides cryptographic protection for network communication.

Security properties:

- Encryption
- Integrity
- Authentication

Commonly used with:

- HTTPS
- Secure email
- Secure APIs
- Other encrypted protocols

---

# 23. 📁 File Transfer Protocols

Studied:

### FTP

Traditional file transfer protocol.

### SFTP

File transfer over SSH.

### SCP

Secure file copying over SSH.

Security considerations:

- Authentication
- Encryption
- Credentials
- Access control

---

# 24. 🔑 SSH

SSH provides secure remote administration and communication.

Default port:

```text
22
```

Common uses:

- Remote login
- Secure file transfer
- Port forwarding
- Remote command execution
- Server administration

Authentication methods:

- Password
- SSH keys

---

# 25. ✉️ Email Protocols

Studied:

### SMTP

Used for sending mail.

### POP3

Used for downloading mail from a server.

### IMAP

Used for synchronizing mail with a server.

---

# 26. 📊 Network Monitoring & Management

Studied concepts related to monitoring network infrastructure.

### SNMP

Simple Network Management Protocol.

Used for monitoring and managing network devices.

Concepts:

- Agents
- Managers
- MIB
- Community strings
- Monitoring

---

# 27. 🕰️ NTP

Network Time Protocol synchronizes system clocks over a network.

Accurate time is important for:

- Logs
- Authentication
- Incident investigation
- Distributed systems
- Security monitoring

---

# 28. 🔄 NAT

Network Address Translation translates addresses between network boundaries.

Common types:

- Static NAT
- Dynamic NAT
- PAT / NAT overload

NAT is widely used to allow multiple private hosts to share public IPv4 addresses.

---

# 29. 🧱 Firewalls

A firewall controls network traffic according to defined rules.

Types:

- Packet-filtering firewall
- Stateful firewall
- Proxy firewall
- Next-generation firewall
- Host-based firewall
- Network firewall

Common filtering criteria:

- Source IP
- Destination IP
- Source port
- Destination port
- Protocol
- Connection state

---

# 30. 🛡️ IDS & IPS

### IDS

Intrusion Detection System detects suspicious activity and generates alerts.

### IPS

Intrusion Prevention System detects and can actively block malicious traffic.

---

# 31. 🔒 VPN

A Virtual Private Network creates a protected communication channel across an untrusted network.

Common concepts:

- Tunneling
- Encryption
- Authentication
- Remote access VPN
- Site-to-site VPN

---

# 32. 🧩 VLAN

Virtual LANs logically segment a physical network.

Benefits:

- Segmentation
- Reduced broadcast domains
- Better organization
- Security isolation

Important concepts:

- Access ports
- Trunk ports
- VLAN tagging
- 802.1Q

---

# 33. 📶 Wireless Networking

Studied fundamentals of wireless networking.

Topics:

- Wi-Fi
- SSID
- Access Point
- Wireless channels
- 2.4 GHz / 5 GHz
- Authentication
- Encryption
- WPA2
- WPA3

Security concepts:

- Evil twin
- Rogue access point
- Deauthentication
- Weak authentication
- Wireless traffic analysis

---

# 34. 🧪 Network Troubleshooting

A structured troubleshooting approach:

```text
Identify the problem
        ↓
Gather information
        ↓
Test connectivity
        ↓
Check configuration
        ↓
Isolate the issue
        ↓
Apply a fix
        ↓
Verify
        ↓
Document
```

Useful commands:

```bash
ping
ip
ifconfig
traceroute
tracert
nslookup
dig
arp
route
ss
netstat
curl
wget
```

---

# 35. 🔎 Network Reconnaissance

Networking knowledge is essential for reconnaissance.

Important concepts:

- Host discovery
- Port discovery
- Service discovery
- Version detection
- DNS enumeration
- Network mapping
- Banner grabbing

Common tool:

```text
Nmap
```

Example:

```bash
nmap -sV <authorized-target>
```

All scanning should only be performed against systems where I have explicit authorization.

---

# 36. 🕵️ Packet Analysis

Packet analysis involves inspecting network traffic to understand communication.

Important concepts:

- Packet capture
- Protocol analysis
- Headers
- Payloads
- Source / destination
- TCP streams
- DNS traffic
- HTTP traffic

Tool:

```text
Wireshark
```

---

# 37. ⚠️ Network Security Concepts

Studied common network security threats and concepts:

- Eavesdropping
- Sniffing
- Spoofing
- ARP poisoning
- DNS spoofing
- Man-in-the-middle
- DoS
- DDoS
- Port scanning
- Session interception
- Rogue devices
- Network-based reconnaissance

The focus is understanding these concepts for authorized security testing and defensive security.

---

# 38. 🛡️ Network Defense

Defensive concepts studied:

- Firewalls
- IDS / IPS
- Network segmentation
- VLANs
- Access control
- Secure protocols
- Encryption
- VPNs
- Monitoring
- Logging
- Least privilege
- Network hardening

---

# 39. 🧰 Networking Commands Reference

| Purpose | Commands |
|---|---|
| Interface information | `ip`, `ifconfig` |
| Connectivity | `ping` |
| Route tracing | `traceroute`, `tracert` |
| DNS | `nslookup`, `dig` |
| Connections | `ss`, `netstat` |
| ARP | `arp` |
| Routing | `route` |
| HTTP requests | `curl` |
| Downloads | `wget` |
| Network scanning | `nmap` |

---

# 40. 🛠️ Networking Tools

Tools explored during networking and cybersecurity learning:

- Nmap
- Wireshark
- Netcat
- Burp Suite
- cURL
- DNS utilities
- Linux networking utilities

---

# 41. 🔐 Networking in Cybersecurity

Networking knowledge directly supports cybersecurity domains such as:

```text
Networking
    │
    ├── Reconnaissance
    │
    ├── Vulnerability Assessment
    │
    ├── Penetration Testing
    │
    ├── Web Security
    │
    ├── SOC / Blue Team
    │
    ├── Incident Response
    │
    ├── Digital Forensics
    │
    └── Network Security
```

Understanding networking makes it easier to understand:

- How attackers discover services
- How systems communicate
- How vulnerabilities are exposed over networks
- How security controls detect attacks
- How network traffic can reveal suspicious activity

---

# 🧠 Key Takeaways

After completing networking, I understand:

1. How computer networks are structured
2. How the OSI and TCP/IP models work
3. How data is encapsulated and transmitted
4. How MAC and IP addressing work
5. How subnetting and CIDR work
6. How switching and routing work
7. How TCP and UDP differ
8. How ports and services work
9. How DNS and DHCP operate
10. How HTTP/HTTPS and TLS work
11. How SSH and file-transfer protocols work
12. How NAT and VPNs work
13. How VLANs provide segmentation
14. How firewalls, IDS, and IPS protect networks
15. How to troubleshoot basic network problems
16. How network reconnaissance works
17. How packet analysis works
18. How networking concepts apply to cybersecurity

---

# 📈 Networking → Cybersecurity

Networking is not a separate skill from cybersecurity.

It is one of the foundations on which many cybersecurity concepts are built.

```text
Networking Fundamentals
        ↓
Protocols & Services
        ↓
Network Security
        ↓
Reconnaissance
        ↓
Enumeration
        ↓
Vulnerability Assessment
        ↓
Security Testing
        ↓
Detection & Defense
```

---

# ✅ Completion Status

**Networking — Completed ✅**

The networking foundation is now complete and will be used as a base for further cybersecurity learning.

---

### 🌐 Learn → Understand → Practice → Analyze → Secure
