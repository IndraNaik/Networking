# Networking Foundations

## 🌐 1a. OSI Model

The **Open Systems Interconnection (OSI) Model** is a standardized framework that defines how computer systems communicate over a network. It consists of seven layers, each with distinct responsibilities to ensure seamless data transfer and network troubleshooting.

### 🔹 The Seven Layers of OSI Model:

1️⃣ **Physical Layer**: Transmits raw bits via cables, radio waves, and other physical mediums.  
   📌 *Examples: Ethernet cables, WiFi signals*

2️⃣ **Data Link Layer**: Handles error detection, MAC addressing, and frame transmission between connected devices.  
   📌 *Examples: Switches, VLANs, ARP*

3️⃣ **Network Layer**: Manages routing, IP addressing, and packet forwarding.  
   📌 *Examples: Routers, Firewalls, ICMP*

4️⃣ **Transport Layer**: Ensures reliable data transfer (TCP) or fast, connectionless transfer (UDP).  
   📌 *Examples: TCP, UDP, Ports, `netstat -tupln`, `telnet <ip> <port>`*

5️⃣ **Session Layer**: Establishes, manages, and terminates communication sessions between applications.

6️⃣ **Presentation Layer**: Handles encryption, compression, and data format translation.  
   📌 *Examples: SSL/TLS, JSON, XML*

7️⃣ **Application Layer**: Provides user interfaces and services for applications.  
   📌 *Examples: HTTP, DNS, FTP, SMTP*
   🔹 Use `dig` or `nslookup` to test DNS.
   🔹 Use `curl` and `wget` to test HTTP endpoints.

---

## 🌐 1b. TCP/IP Model

The **TCP/IP Model** is the fundamental framework for internet communication, built on **Transmission Control Protocol (TCP)** and **Internet Protocol (IP)**. It ensures structured, reliable data exchange across networks.

### 🔹 The Four Layers of TCP/IP Model:

1️⃣ **Link Layer**: Handles MAC addressing, error detection, and frame transfers.  
   📌 *Examples: Switches, VLANs, ARP*

2️⃣ **Internet Layer**: Manages routing, IP addressing, and packet forwarding.  
   📌 *Examples: Routers, Firewalls, ICMP*

3️⃣ **Transport Layer**: Ensures reliable or fast data transmission.  
   📌 *Examples: TCP, UDP, Ports, `netstat -tupln`, `telnet <ip> <port>`*

4️⃣ **Application Layer**: Provides services and user interactions.  
   📌 *Examples: HTTP, DNS, FTP, SMTP*
   🔹 Use `dig` or `nslookup` for DNS testing.
   🔹 Use `curl` and `wget` for HTTP endpoint testing.

---

## 🌐 UDP (User Datagram Protocol)

**UDP** is a lightweight, connectionless transport protocol that prioritizes speed over reliability. It is commonly used for real-time applications where packet loss is acceptable.

---

## 🌐 TCP vs UDP

| Feature           | **TCP (Transmission Control Protocol)** | **UDP (User Datagram Protocol)** |
|------------------|----------------------------------|------------------------------|
| **Connection**   | Connection-oriented             | Connectionless              |
| **Reliability**  | Ensures data delivery, error checking | No guarantee of delivery |
| **Speed**        | Slower due to acknowledgments   | Faster, no acknowledgments required |
| **Usage**        | Used for reliability-focused applications (HTTP, FTP, SMTP) | Used for real-time applications (VoIP, DNS, Streaming) |
| **Error Checking** | Uses checksums, retransmissions | Uses checksums, no retransmissions |
| **Header Size**  | Larger (20 bytes)              | Smaller (8 bytes) |
| **Order**        | Maintains data order           | No guarantee of order |

---

## 🌐 Protocols & Internet Protocol

A **protocol** is a set of rules governing data transmission over networks.

### 🔹 Internet Protocol (IP)

**Internet Protocol (IP)** operates at the **Network Layer** and is responsible for addressing and routing data. Each device on a network has a unique **IP address**, allowing communication across global networks.

📌 **Functionality**:
- Assigns unique IP addresses
- Directs network traffic using routing tables

📌 **Common Uses**:
- Internet communication
- Routing across networks

---

## 🌐 Network & Packet

🔹A**Network** is linked to share resorces over two or more computers.

📌 **Types of Network**
- PAN (Personal Area Network)
- LAN (Local Area Network)
- WAN (Wide Area Network)
- MAN (Metropoltian Area Network)

### 🔹 Packet

Data sent over network is divided into smaller segments called **packets**

---

🚀 **This guide is constantly evolving!** Stay tuned for updates, and feel free to contribute. 🎯

