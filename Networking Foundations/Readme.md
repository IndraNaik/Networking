# Networking Foundations

## 1a. OSI Model

Open Systems Interconnection Model is a 7 layer collection of guidelines that describes how various computer systems interact with one another via a network.
The OSI Model offers a clear framework for handling network problems and data transfer. The seven layers of the OSI Model are as follows:

1. **Physical Layer**:  Raw data (bits) are transmitted by wireless media, wires, or hardware. `Example: Ethernet cables and WiFi signals`
2. **Data Link Layer**: Responsible for error detection, MAC addressing, framing, and frame transfers between the internet.
 `Example: switches, VLANs, and ARP`
3. **Network Layer**:  Routing, IP addressing, and packet forwarding. 
`Example: Routers, Firewalls, ICMP`
4. **Transport Layer**: Reliable data transfer (TCP) or faster transfer (UDP). 
`Example: TCP, UDP, Ports, netstat-tupln, telnet <ip> <port>`
5. **Session Layer**: Controls app (API) sessions. communication session.
6. **Presentation Layer**: Compression, encryption, and data formatting. 
`Example: SSL/TLS, Data Serialization (JSON, XML)`
7. **Application Layer**: User interface for services and applications. 
`Example: HTTP, DNS, FTP, SMTP`
   -  Use `dig` or `nslookup` to test DNS.
   - The `curl` and `wget` commands are used to test HTTP endpoints.
---

## 1b. TCP/IP Model

This is a key computer networking framework that runs at the OSI Model's Transport Layer. TCP/IP are the main protocol components of the internet, defining how data is transported across the network. This ensures reliable communication between devices prior to data sharing.

**Functionality**: It breaks data into packets, assigns sequence numbers.

This model has 4 layers as follows:

1. **Link Layer**: Responsible for error detection, MAC addressing, framing, and frame transfers between the internet. 
`Example: switches, VLANs, and ARP`
2. **Internet Layer**: Routing, IP addressing, and packet forwarding. 
`Example: Routers, Firewalls, ICMP`
3. **Transport Layer**:Reliable data transfer (TCP) or faster transfer (UDP). 
`Example: TCP, UDP, Ports, netstat-tupln, telnet <ip> <port>`
4. **Application Layer**: User interface for services and applications. 
`Example: HTTP, DNS, FTP, SMTP`
   -  Use `dig` or `nslookup` to test DNS.
   - The `curl` and `wget` commands are used to test HTTP endpoints.
---

## UDP

The User Datagram Protocol also works at the transmission layer. This is a connectionless protocol that provides few services.

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

A protocol is a set of rules that control how data is sent and received over a network.

---

## Internet Protocol

The Internet Protocol operates at the Network layer. It is a core component of the TCP/IP protocol system. Internet Protocol (IP) is a set of standards for addressing and routing data over the internet.

**Functionality**: IP assigns each device a unique IP address and directs traffic across networks using routing tables.

---
