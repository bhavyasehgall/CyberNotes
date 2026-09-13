# 🌐 Networking Notes

A practical guide to **computer networking fundamentals, protocols, addressing, network devices, and cybersecurity concepts**.

---

# 📚 Table of Contents

* [What is Networking?](#what-is-networking)
* [Network Types](#network-types)
* [Network Components](#network-components)
* [Network Devices](#network-devices)
* [MAC Address](#mac-address)
* [IP Address](#ip-address)
* [IPv4](#ipv4)
* [IPv4 Address Classes](#ipv4-address-classes)
* [Private and Public IP](#private-and-public-ip)
* [Loopback Address](#loopback-address)
* [Subnet Mask](#subnet-mask)
* [CIDR](#cidr)
* [Default Gateway](#default-gateway)
* [DNS](#dns)
* [DHCP](#dhcp)
* [ARP](#arp)
* [Ports](#ports)
* [TCP and UDP](#tcp-and-udp)
* [TCP Three-Way Handshake](#tcp-three-way-handshake)
* [OSI Model](#osi-model)
* [TCP/IP Model](#tcpip-model)
* [Common Protocols](#common-protocols)
* [HTTP and HTTPS](#http-and-https)
* [FTP and SFTP](#ftp-and-sftp)
* [SSH](#ssh)
* [ICMP](#icmp)
* [NAT](#nat)
* [Firewall](#firewall)
* [VPN](#vpn)
* [Proxy](#proxy)
* [Packet](#packet)
* [LAN Communication Example](#lan-communication-example)
* [Internet Communication Example](#internet-communication-example)
* [Linux Networking Commands](#linux-networking-commands)
* [Networking and Cybersecurity](#networking-and-cybersecurity)
* [Quick Reference](#quick-reference)

---

# What is Networking?

**Computer networking** is the process of connecting computers and other devices so they can communicate and share resources.

For example:

```text
Laptop ─── Wi-Fi ─── Router ─── Internet
```

A network allows devices to exchange:

* Data
* Files
* Messages
* Web requests
* Services
* Network resources

### Simple Example

When you open:

```text
https://example.com
```

your computer communicates with a remote server through several networking technologies and protocols.

---

# Network Types

## LAN

**LAN = Local Area Network**

A network covering a small geographical area.

Examples:

* Home network
* School network
* Office network
* Computer lab

```text
PC ──┐
PC ──┼── Switch ── Router
PC ──┘
```

---

## WAN

**WAN = Wide Area Network**

A network covering a large geographical area.

The Internet is the largest example of a WAN.

---

## WLAN

**WLAN = Wireless Local Area Network**

A LAN using wireless communication such as Wi-Fi.

---

## MAN

**MAN = Metropolitan Area Network**

A network covering a city or large campus.

---

# Network Components

A basic network can contain:

```text
Device
  ↓
NIC
  ↓
Switch / Access Point
  ↓
Router
  ↓
Internet
```

Important components include:

* NIC
* Switch
* Router
* Access Point
* Firewall
* Modem
* Servers
* Clients

---

# Network Devices

## NIC

**NIC = Network Interface Card**

It allows a device to connect to a network.

A NIC can provide:

* MAC address
* Ethernet connectivity
* Wireless connectivity

Modern laptops commonly have both:

```text
Ethernet NIC
Wi-Fi NIC
```

---

## Switch

A switch connects devices within a LAN.

Example:

```text
PC1 ──┐
PC2 ──┼── Switch
PC3 ──┘
```

A switch primarily uses **MAC addresses** to forward Ethernet frames.

---

## Router

A router connects different networks.

Example:

```text
Home LAN
192.168.1.0/24
      |
    Router
      |
   Internet
```

A router makes forwarding decisions using **IP addresses** and routing information.

---

## Access Point

An access point provides wireless network connectivity.

Example:

```text
Laptop ))))
        Wi-Fi
         ↓
    Access Point
         ↓
       LAN
```

---

## Modem

A modem connects a local network to an ISP's access service.

In many home setups, modem and router functionality may be combined into one device.

---

## Firewall

A firewall controls network traffic according to security rules.

Example:

```text
Internet
   |
Firewall
   |
Internal Network
```

A firewall can allow or block traffic based on factors such as:

* Source IP
* Destination IP
* Port
* Protocol
* Connection state
* Application, depending on firewall type

---

# MAC Address

A **MAC address** is a Layer 2 hardware/network-interface address used for local network communication.

Example:

```text
00:1A:2B:3C:4D:5E
```

MAC addresses are typically represented as six hexadecimal pairs.

### MAC vs IP

| MAC Address                                         | IP Address                                              |
| --------------------------------------------------- | ------------------------------------------------------- |
| Mainly used at Layer 2                              | Mainly used at Layer 3                                  |
| Identifies a network interface on the local network | Identifies a network endpoint/interface at the IP layer |
| Used by Ethernet/Wi-Fi frames                       | Used for IP packet delivery                             |
| Usually associated with a NIC                       | Can change depending on the network                     |

---

# IP Address

An **IP address** identifies an interface/endpoint in an IP network.

Example IPv4 address:

```text
192.168.1.10
```

IP addresses allow devices to communicate across networks.

---

# IPv4

IPv4 uses **32 bits**.

It is commonly written as four decimal octets:

```text
192.168.1.10
```

Each octet ranges from:

```text
0 - 255
```

Therefore:

```text
192.168.1.10
```

contains:

```text
192
168
1
10
```

---

# IPv4 Address Classes

Traditional IPv4 classful addressing divided addresses into Classes A, B, C, D, and E.

| Class | Range   | Traditional Use       |
| ----- | ------- | --------------------- |
| A     | 1–126   | Large networks        |
| B     | 128–191 | Medium networks       |
| C     | 192–223 | Smaller networks      |
| D     | 224–239 | Multicast             |
| E     | 240–255 | Experimental/reserved |

Modern networks generally use **CIDR** rather than classful addressing.

---

# Private and Public IP

## Private IP

Private IP addresses are used inside private networks.

IPv4 private ranges are:

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

Example:

```text
192.168.1.20
```

A private IP is not directly routable across the public Internet.

---

## Public IP

A public IP is used for communication across the public Internet.

Example:

```text
203.0.113.10
```

The address above is from a documentation range and is used here only as an example.

---

# Loopback Address

The loopback address refers to the local system itself.

IPv4:

```text
127.0.0.1
```

Hostname:

```text
localhost
```

Example:

```bash
ping 127.0.0.1
```

This tests communication with the local TCP/IP stack.

The entire:

```text
127.0.0.0/8
```

range is reserved for IPv4 loopback.

---

# Subnet Mask

A subnet mask determines which portion of an IPv4 address represents the network and which portion represents hosts.

Example:

```text
IP:          192.168.1.10
Subnet Mask: 255.255.255.0
```

This is commonly written as:

```text
192.168.1.10/24
```

With `/24`:

```text
Network portion = 24 bits
Host portion    = 8 bits
```

---

# CIDR

**CIDR = Classless Inter-Domain Routing**

CIDR represents the network prefix using `/number`.

Examples:

```text
192.168.1.0/24
10.0.0.0/8
172.16.0.0/16
```

The number represents how many bits belong to the network prefix.

### Common CIDR Values

| CIDR  | Subnet Mask     |  Addresses |
| ----- | --------------- | ---------: |
| `/8`  | 255.0.0.0       | 16,777,216 |
| `/16` | 255.255.0.0     |     65,536 |
| `/24` | 255.255.255.0   |        256 |
| `/30` | 255.255.255.252 |          4 |

For a typical IPv4 subnet, some addresses have special purposes, so the number of usable host addresses may be smaller than the total number of addresses.

---

# Default Gateway

A **default gateway** is the router a device uses when the destination is outside its local network.

Example:

```text
Laptop
192.168.1.10
     |
     | 192.168.1.1
     ↓
Router
     |
Internet
```

The laptop can use:

```text
192.168.1.1
```

as its default gateway.

---

# DNS

**DNS = Domain Name System**

DNS translates domain names into IP addresses and also supports other types of records.

Example:

```text
example.com
     ↓
93.184.216.34
```

Without DNS, users would have to remember IP addresses instead of domain names.

### Common DNS Records

| Record  | Purpose                        |
| ------- | ------------------------------ |
| `A`     | Domain → IPv4                  |
| `AAAA`  | Domain → IPv6                  |
| `CNAME` | Alias                          |
| `MX`    | Mail server                    |
| `NS`    | Authoritative name server      |
| `TXT`   | Text/configuration information |
| `PTR`   | Reverse DNS                    |

### Cybersecurity Relevance

DNS is important in:

* Reconnaissance
* Phishing analysis
* Malware analysis
* Incident response
* Domain investigation

---

# DHCP

**DHCP = Dynamic Host Configuration Protocol**

DHCP automatically provides network configuration to clients.

It can provide:

* IP address
* Subnet mask
* Default gateway
* DNS server

### DHCP Process

A common DHCP exchange is:

```text
DORA

Discover
   ↓
Offer
   ↓
Request
   ↓
ACK
```

### Example

When a laptop connects to Wi-Fi, it may request an IP address from the DHCP server.

---

# ARP

**ARP = Address Resolution Protocol**

ARP maps an IPv4 address to a MAC address on a local network.

Example:

```text
IP Address
192.168.1.1
     ↓
   ARP
     ↓
MAC Address
AA:BB:CC:DD:EE:FF
```

A host may ask:

```text
Who has 192.168.1.1?
```

The device owning that IP responds with its MAC address.

### Important

ARP operates within the local network and is associated with IPv4.

IPv6 uses **Neighbor Discovery Protocol (NDP)** instead of ARP.

---

# Ports

A **port number** identifies a service/application endpoint associated with a network connection.

TCP and UDP ports range from:

```text
0 - 65535
```

### Port Ranges

| Range         | Name            |
| ------------- | --------------- |
| `0–1023`      | Well-known      |
| `1024–49151`  | Registered      |
| `49152–65535` | Dynamic/private |

### Common Ports

|  Port | Protocol/Service |
| ----: | ---------------- |
| 20/21 | FTP              |
|    22 | SSH              |
|    23 | Telnet           |
|    25 | SMTP             |
|    53 | DNS              |
|    80 | HTTP             |
|   110 | POP3             |
|   143 | IMAP             |
|   443 | HTTPS            |
|   445 | SMB              |
|  3306 | MySQL            |
|  3389 | RDP              |
|  5432 | PostgreSQL       |

A port number alone does not guarantee that a particular service is actually running there.

---

# TCP and UDP

## TCP

**TCP = Transmission Control Protocol**

TCP is connection-oriented and provides reliable, ordered delivery.

Features include:

* Connection establishment
* Reliability
* Ordering
* Retransmission
* Flow control
* Congestion control

Examples:

* HTTPS
* SSH
* FTP

---

## UDP

**UDP = User Datagram Protocol**

UDP is connectionless and does not provide TCP-style reliable, ordered delivery.

It has lower protocol overhead and is useful where speed or application-controlled reliability is important.

Examples:

* DNS queries
* DHCP
* VoIP
* Streaming
* Online gaming

---

# TCP Three-Way Handshake

TCP establishes a connection using a three-way handshake.

```text
Client                         Server

   SYN  -------------------->
        <-------------------- SYN-ACK
   ACK  -------------------->
```

### Step 1 — SYN

The client sends:

```text
SYN
```

It requests to establish a TCP connection.

### Step 2 — SYN-ACK

The server responds:

```text
SYN + ACK
```

### Step 3 — ACK

The client responds:

```text
ACK
```

The TCP connection can now proceed.

---

# OSI Model

The **OSI model** divides network communication into seven conceptual layers.

```text
7  Application
6  Presentation
5  Session
4  Transport
3  Network
2  Data Link
1  Physical
```

---

## Layer 7 — Application

Provides network services to applications.

Examples:

* HTTP
* DNS
* FTP
* SMTP

---

## Layer 6 — Presentation

Concerned with data representation, encoding, and related transformations.

Examples include:

* Encryption
* Compression
* Data formatting

---

## Layer 5 — Session

Manages communication sessions between applications.

---

## Layer 4 — Transport

Provides end-to-end transport.

Main protocols:

```text
TCP
UDP
```

---

## Layer 3 — Network

Responsible for logical addressing and routing.

Main protocol:

```text
IP
```

Routers primarily operate at this layer.

---

## Layer 2 — Data Link

Handles local network communication using frames and MAC addresses.

Examples:

* Ethernet
* Wi-Fi

Switches primarily operate at this layer.

---

## Layer 1 — Physical

Deals with physical transmission.

Examples:

* Cables
* Radio signals
* Electrical signals
* Fiber optics

---

# OSI Model Memory Trick

From Layer 7 to Layer 1:

```text
All
People
Seem
To
Need
Data
Processing
```

Application → Presentation → Session → Transport → Network → Data Link → Physical

---

# TCP/IP Model

The TCP/IP model is commonly represented using four layers.

```text
Application
Transport
Internet
Link
```

### Mapping

| TCP/IP      | OSI     |
| ----------- | ------- |
| Application | 5, 6, 7 |
| Transport   | 4       |
| Internet    | 3       |
| Link        | 1, 2    |

The exact terminology can vary between references, but the models describe similar networking concepts.

---

# Common Protocols

| Protocol | Purpose                             |
| -------- | ----------------------------------- |
| HTTP     | Web communication                   |
| HTTPS    | Secure web communication            |
| DNS      | Name resolution                     |
| DHCP     | Automatic network configuration     |
| ARP      | IPv4-to-MAC resolution on LAN       |
| TCP      | Reliable transport                  |
| UDP      | Connectionless transport            |
| ICMP     | Network control/diagnostic messages |
| SSH      | Secure remote administration        |
| FTP      | File transfer                       |
| SMTP     | Sending email                       |
| IMAP     | Accessing email                     |
| POP3     | Downloading email                   |
| SMB      | File/printer sharing                |
| SNMP     | Network management                  |

---

# HTTP and HTTPS

## HTTP

**HTTP = Hypertext Transfer Protocol**

Commonly uses:

```text
TCP port 80
```

Example:

```text
GET /index.html HTTP/1.1
```

---

## HTTPS

HTTPS is HTTP protected using **TLS**.

Commonly uses:

```text
TCP port 443
```

HTTPS provides protections such as:

* Encryption
* Server authentication
* Integrity protection

---

# FTP and SFTP

## FTP

**FTP = File Transfer Protocol**

Commonly uses:

```text
TCP 21
```

FTP does not provide encryption by itself.

---

## SFTP

**SFTP = SSH File Transfer Protocol**

It operates over SSH.

Commonly uses:

```text
TCP 22
```

SFTP provides encrypted file transfer through SSH.

---

# SSH

**SSH = Secure Shell**

SSH provides secure remote administration.

Commonly:

```text
TCP port 22
```

Example:

```bash
ssh user@192.168.1.10
```

SSH can also be used for:

* Remote command execution
* Secure file transfer
* Port forwarding
* Tunneling

---

# ICMP

**ICMP = Internet Control Message Protocol**

ICMP is used for network control and diagnostic messages.

`ping` commonly uses ICMP Echo Request and Echo Reply.

Example:

```bash
ping 8.8.8.8
```

ICMP is not a TCP or UDP transport protocol.

---

# NAT

**NAT = Network Address Translation**

NAT translates IP addresses between network contexts.

A common home setup is:

```text
Laptop
192.168.1.10
     |
Router
     |
Public IP
     |
Internet
```

The private address is translated when communicating through the public Internet.

### Why NAT is Common

Private IPv4 addresses are not globally routable, while public IPv4 addresses are limited.

NAT allows multiple private devices to share a public IPv4 address.

---

# Firewall

A firewall controls network traffic according to defined rules.

Example:

```text
Internet
    |
 Firewall
    |
Server
```

A firewall rule might conceptually say:

```text
Allow TCP 443
Block TCP 23
```

This could allow HTTPS while blocking Telnet.

### Firewall Types

Common categories include:

* Network firewall
* Host-based firewall
* Stateful firewall
* Next-generation firewall

---

# VPN

**VPN = Virtual Private Network**

A VPN creates a protected communication path over an underlying network.

Example:

```text
Laptop
   |
Encrypted VPN Tunnel
   |
VPN Server
   |
Internal Network
```

VPNs are commonly used for:

* Remote access
* Site-to-site connectivity
* Protecting traffic over untrusted networks

---

# Proxy

A proxy acts as an intermediary between a client and another server.

```text
Client
  |
Proxy
  |
Server
```

Instead of connecting directly to the destination, the client communicates through the proxy.

Proxies can be used for:

* Web filtering
* Monitoring
* Caching
* Access control
* Security testing

Tools such as Burp Suite can act as an HTTP proxy during authorized web application testing.

---

# Packet

A **packet** is a unit of data carried by a network-layer protocol such as IP.

Simplified:

```text
+----------------------+
| IP Header            |
+----------------------+
| TCP/UDP Header       |
+----------------------+
| Application Data     |
+----------------------+
```

At different layers, data has different names:

```text
Application → Data
Transport   → Segment / Datagram
Network     → Packet
Data Link   → Frame
```

The exact terminology can vary by protocol and context.

---

# LAN Communication Example

Suppose:

```text
PC1 = 192.168.1.10
PC2 = 192.168.1.20
```

Both belong to:

```text
192.168.1.0/24
```

PC1 wants to communicate with PC2.

### Step 1

PC1 determines that PC2 is on the local network.

### Step 2

PC1 needs PC2's MAC address.

It uses ARP.

### Step 3

PC1 sends an Ethernet frame to PC2's MAC address.

```text
PC1
 |
Switch
 |
PC2
```

The router is not required for this local communication.

---

# Internet Communication Example

Suppose your laptop:

```text
192.168.1.10
```

wants to access:

```text
https://example.com
```

A simplified flow is:

```text
Laptop
  |
DNS lookup
  |
IP address
  |
Router
  |
ISP
  |
Internet
  |
Web Server
```

### Simplified Process

```text
1. Laptop needs the server's IP.
2. DNS resolves the domain.
3. Laptop determines the destination is remote.
4. Traffic is sent to the default gateway.
5. Routers forward the packets.
6. A TCP connection may be established.
7. TLS is negotiated for HTTPS.
8. HTTP requests/responses are exchanged.
```

This is simplified; actual communication can involve additional steps and protocols.

---

# Linux Networking Commands

## `ip`

Display network interfaces:

```bash
ip addr
```

Short form:

```bash
ip a
```

Display routes:

```bash
ip route
```

Display neighbor/ARP information:

```bash
ip neigh
```

---

## `ping`

Test connectivity:

```bash
ping 8.8.8.8
```

Test a hostname:

```bash
ping example.com
```

---

## `ss`

View network sockets:

```bash
ss
```

Show listening TCP ports:

```bash
ss -ltn
```

Show listening TCP and UDP ports with processes:

```bash
sudo ss -lntup
```

---

## `ip route`

View routing information:

```bash
ip route
```

Example:

```text
default via 192.168.1.1 dev eth0
```

This indicates that:

```text
default gateway = 192.168.1.1
interface = eth0
```

---

## `dig`

Perform DNS queries:

```bash
dig example.com
```

Short result:

```bash
dig +short example.com
```

Query an MX record:

```bash
dig example.com MX
```

---

## `nslookup`

Basic DNS lookup:

```bash
nslookup example.com
```

---

## `curl`

Test HTTP/HTTPS:

```bash
curl https://example.com
```

View HTTP headers:

```bash
curl -I https://example.com
```

---

## `traceroute`

Trace the path toward a destination:

```bash
traceroute example.com
```

---

## `nmap`

Discover hosts and services on authorized systems.

Basic scan:

```bash
nmap 192.168.1.10
```

Service detection:

```bash
nmap -sV 192.168.1.10
```

Specific ports:

```bash
nmap -p 22,80,443 192.168.1.10
```

Network scan:

```bash
nmap 192.168.1.0/24
```

Only scan systems you own or have explicit permission to test.

---

# Networking and Cybersecurity

Networking knowledge is fundamental to cybersecurity.

A security analyst needs to understand:

```text
IP Address
     ↓
Port
     ↓
Protocol
     ↓
Service
     ↓
Application
```

For example:

```text
192.168.1.10:443
```

can be interpreted as:

```text
IP       = 192.168.1.10
Port     = 443
Protocol = TCP
Service  = HTTPS
```

This information is useful during:

* Vulnerability assessment
* Network monitoring
* Incident response
* Threat hunting
* Penetration testing
* SOC analysis

---

# Network Reconnaissance

During an authorized assessment, reconnaissance may involve identifying:

* Live hosts
* IP addresses
* Open ports
* Running services
* Service versions
* DNS information
* Network routes

Example:

```bash
nmap -sV 192.168.1.10
```

Possible output:

```text
PORT    STATE SERVICE VERSION
22/tcp  open  ssh
80/tcp  open  http
443/tcp open  https
```

This tells us that the host has services listening on ports 22, 80, and 443.

The next step in an assessment is understanding whether those services are expected, properly configured, and vulnerable.

---

# Network Traffic Analysis

Tools such as **Wireshark** can capture and analyze network traffic.

A simplified packet might show:

```text
Source      → 192.168.1.10
Destination → 192.168.1.20
Protocol    → TCP
Source Port → 51542
Dest Port   → 443
```

This allows analysts to investigate:

* Connections
* Protocols
* DNS requests
* HTTP traffic
* Suspicious destinations
* Network anomalies

---

# Important Concepts to Understand

Before moving into advanced cybersecurity networking, make sure you understand:

```text
MAC Address
      ↓
IP Address
      ↓
Subnet
      ↓
Gateway
      ↓
Routing
      ↓
DNS
      ↓
Ports
      ↓
TCP / UDP
      ↓
Protocols
      ↓
Services
```

These concepts form the foundation for understanding network attacks, monitoring, and defense.

---

# Quick Reference

## Addresses

| Concept      | Example             |
| ------------ | ------------------- |
| IPv4         | `192.168.1.10`      |
| Private IPv4 | `192.168.1.10`      |
| Loopback     | `127.0.0.1`         |
| CIDR         | `192.168.1.0/24`    |
| MAC          | `00:1A:2B:3C:4D:5E` |

---

## Common Ports

|   Port | Service    |
| -----: | ---------- |
|   `21` | FTP        |
|   `22` | SSH        |
|   `23` | Telnet     |
|   `25` | SMTP       |
|   `53` | DNS        |
|   `80` | HTTP       |
|  `110` | POP3       |
|  `143` | IMAP       |
|  `443` | HTTPS      |
|  `445` | SMB        |
| `3306` | MySQL      |
| `3389` | RDP        |
| `5432` | PostgreSQL |

---

## Networking Commands

| Command      | Purpose                       |
| ------------ | ----------------------------- |
| `ip a`       | Show interfaces/IP addresses  |
| `ip route`   | Show routing table            |
| `ip neigh`   | Show neighbor/ARP information |
| `ping`       | Test connectivity             |
| `ss`         | Show sockets/connections      |
| `dig`        | DNS queries                   |
| `nslookup`   | DNS lookup                    |
| `traceroute` | Trace network path            |
| `curl`       | Test HTTP/HTTPS               |
| `nmap`       | Network/service discovery     |

---

# Final Concept

Networking is easier to understand when you follow the path of data:

```text
Application
     ↓
Protocol
     ↓
Port
     ↓
IP Address
     ↓
Router
     ↓
Network
     ↓
Destination
```

For example, when accessing a website:

```text
Domain
  ↓
DNS
  ↓
IP Address
  ↓
TCP
  ↓
TLS
  ↓
HTTPS
  ↓
Web Server
```

Understanding this flow gives you the foundation required for **network security, SOC analysis, VAPT, penetration testing, and troubleshooting**.
