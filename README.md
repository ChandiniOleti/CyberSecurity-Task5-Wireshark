# CyberSecurity-Task5-Wireshark
# Wireshark Network Traffic Analysis

## Objective
To capture live network packets using Wireshark and identify multiple network protocols through practical analysis.

## Tools Used
- Wireshark (Windows version)
- Windows 11
- Active internet connection

## Steps Performed
1. Opened Wireshark and selected the active network interface (Wi-Fi).
2. Started capturing live network packets.
3. Generated traffic by:
   - Browsing websites to capture HTTP and DNS
   - Accessing domains to trigger TCP connections
   - Allowing local network services to generate UDP and ICMPv6 packets
4. Stopped capture after ~2 minutes.
5. Applied protocol filters: `http`, `dns`, `tcp`, `udp`, `icmpv6`.
6. Analyzed packet details including source/destination, protocol role, and payload.

---

## Protocols Identified

### 1. HTTP
- **Purpose:** Transfers web pages and data between web browsers and servers.
- **Example from Capture:** HTTP GET request for `/igd.xml` from local IP `10.10.32.131`.
- **Screenshot:**  
  ![HTTP Packet](screenshots/http_packet.png)

---

### 2. DNS
- **Purpose:** Resolves human-readable domain names into IP addresses.
- **Example from Capture:** Query to `dns.google` (8.8.8.8) for domain resolution.
- **Screenshot:**  
  ![DNS Packet](screenshots/dns_packet.png)

---

### 3. TCP
- **Purpose:** Ensures reliable, ordered communication between devices over the network.
- **Example from Capture:** TCP ACK packet between local IP and remote server, part of a handshake.
- **Screenshot:**  
  ![TCP Packet](screenshots/tcp_packet.png)

---

### 4. UDP
- **Purpose:** Connectionless protocol for fast, lightweight data transfer without reliability overhead.
- **Example from Capture:** Multicast DNS (mDNS) response from a device on the local network.
- **Screenshot:**  
  ![UDP Packet](screenshots/udp_packet.png)

---

### 5. ICMPv6
- **Purpose:** Used for diagnostic messages and neighbor discovery in IPv6 networks.
- **Example from Capture:** Neighbor Solicitation message for IPv6 address resolution.
- **Screenshot:**  
  ![ICMPv6 Packet](screenshots/icmpv6_packet.png)

---

## Key Learnings
- How to start and stop live packet captures in Wireshark.
- Applying filters to isolate specific protocols.
- Differences between TCP (reliable) and UDP (fast but unreliable).
- How DNS works for domain name resolution.
- The role of ICMPv6 in IPv6 networking.

---

## Files in Repository
- `task5_capture.pcapng` — Packet capture file.
- `README.md` — Report of task process and analysis.
- `screenshots/` — Contains protocol screenshots:
  - `http_packet.png`
  - `dns_packet.png`
  - `tcp_packet.png`
  - `udp_packet.png`
  - `icmpv6_packet.png`
