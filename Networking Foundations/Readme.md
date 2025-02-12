# Networking Foundations

## 1a. OSI Model

Open Systems Interconnection Model is a 7-layer model which is a set of rules that explains how different computer systems communicate over a network.
OSI Model provides a clean structure for data transmission and managing network issues. OSI Model has 7 layers as follows:

1. **Physical Layer**: Transmission of raw data (bits) through cables, hardware, or wireless media. `Example: Ethernet cables, WiFi signals`
2. **Data Link Layer**: Transfers frames between internet, Framing, MAC addressing, error detection. `Example: Switches, VLAN, ARP`
3. **Network Layer**: Packet forwarding, IP addressing, and routing. `Example: Routers, Firewalls, ICMP`
4. **Transport Layer**: Reliable data transfer (TCP) or faster transfer (UDP). `Example: TCP, UDP, Ports, netstat-tupln, telnet <ip> <port>`
5. **Session Layer**: Manages sessions between apps (APIs). Session of communicating.
6. **Presentation Layer**: Data formatting, Encryption, Compression. `Example: SSL/TLS, Data Serialization (JSON, XML)`
7. **Application Layer**: Interface for user applications and services. `Example: HTTP, DNS, FTP, SMTP`
   - Test DNS with `dig` or `nslookup`
   - Use `curl` or `wget` to test HTTP endpoints.
---

## 1b. TCP/IP Model

This is a fundamental framework for computer networking and operates at the Transport Layer of the OSI Model. TCP/IP are the core protocol components of the internet and define how data is transmitted over the network. This ensures reliable communication between devices before data exchange.

**Functionality**: It breaks data into packets, assigns sequence numbers.

This model has 4 layers as follows:

1. **Link Layer**: Transfers frames between internet, Framing, MAC addressing, error detection. `Example: Switches, VLAN, ARP`
2. **Internet Layer**: Packet forwarding, IP addressing, and routing. `Example: Routers, Firewalls, ICMP`
3. **Transport Layer**: Reliable data transfer (TCP) or faster transfer (UDP). `Example: TCP, UDP, Ports, netstat-tupln, telnet <ip> <port>`
4. **Application Layer**: Interface for user applications and services. `Example: HTTP, DNS, FTP, SMTP`
   - Test DNS with `dig` or `nslookup`
   - Use `curl` or `wget` to test HTTP endpoints.
---

## UDP

User Datagram Protocol also operates at the transmission layer. This is a connectionless protocol that offers minimal services.

---

## TCP vs UDP

| Feature           | TCP (Transmission Control Protocol) | UDP (User Datagram Protocol) |
|------------------|----------------------------------|------------------------------|
| **Connection**   | Connection-oriented             | Connectionless              |
| **Reliability**  | Reliable, ensures data delivery | Unreliable, no delivery guarantee |
| **Speed**        | Slower due to error checking & acknowledgment | Faster, no acknowledgment required |
| **Usage**        | Used for applications needing reliability (e.g., HTTP, FTP, SMTP) | Used for real-time applications (e.g., VoIP, DNS, Streaming) |
| **Error Checking** | Uses checksums, acknowledgments, and retransmissions | Uses checksums but no retransmissions |
| **Header Size**  | Larger header (20 bytes)        | Smaller header (8 bytes)    |
| **Order**        | Ensures data is received in order | No guarantee of ordered delivery |

---

## Protocol

A protocol is a set of rules that define how data is transmitted and received between devices in a network.

---

## Internet Protocol

Internet Protocol functions at the Network layer. It is a fundamental part of the TCP/IP protocol suite. Internet Protocol is a set of standards for addressing and routing data on the internet.

**Functionality**: IP assigns unique IP addresses to devices and uses routing tables to direct data across networks.

---
