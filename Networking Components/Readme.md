# Networking Components

## 🌐 2a. Subnetting and IP Addressing

### 🔹 Subnet

A **subnet** (short for subnetwork) is a technique used in computer networking to divide a larger IP network into smaller, more manageable sub-networks or subnets. This helps optimize performance, improve security, and efficiently allocate IP addresses.

Subnets are logical partitions of an IP network into multiple, smaller segments.

#### 🏛 Public Subnet vs Private Subnet

| Feature        | Public Subnet | Private Subnet |
|---------------|--------------|---------------|
| **Accessibility** | Accessible from the internet | Only accessible within the internal network |
| **Use Case**  | Web servers, public-facing applications | Databases, internal applications |
| **Security**  | Requires firewall rules to restrict access | More secure as it is not exposed to the internet |
| **IP Assignment** | Uses public IP addresses | Uses private IP addresses (RFC 1918: 10.x.x.x, 172.16.x.x, 192.168.x.x) |

---

## 🌐 Subnet Mask

A **subnet mask** is a 32-bit number used to divide an IP address into network and host portions. It determines the number of available hosts in a subnet.

### 📌 Example:
- **IP Address:** 192.168.1.10
- **Subnet Mask:** 255.255.255.0
- **Network Portion:** 192.168.1
- **Host Portion:** .10
- **Total Usable Hosts:** 254 (First and last addresses are reserved)

---

## 🌐 IP Addressing

An **IP address** is a unique identifier assigned to each device on a network, enabling communication between devices.

### 📌 Types of IP Addresses:
- **IPv4:** 32-bit address (e.g., 192.168.1.1)
- **IPv6:** 128-bit address (e.g., 2001:db8::ff00:42:8329)

### 📌 Example:
- **IPv4 Example:** 192.168.1.100 (Private IP)
- **IPv6 Example:** fe80::1ff:fe23:4567:890a (Local Link Address)

An IP address consists of **network** and **host** portions, defined by the subnet mask.

---

## 🌐 2b. Domain Name System (DNS)

The **Domain Name System (DNS)** is a hierarchical system that translates human-readable domain names (e.g., example.com) into IP addresses (e.g., 192.168.1.1). It plays a crucial role in internet communication by enabling users to access websites using domain names instead of numerical IP addresses.

### 📌 DNS Record Types

| Record Type | Description | Example |
|------------|-------------|---------|
| **A** | Maps a domain to an IPv4 address | example.com → 192.168.1.1 |
| **AAAA** | Maps a domain to an IPv6 address | example.com → 2001:db8::ff00:42:8329 |
| **CNAME** | Alias record that maps a domain to another domain | www.example.com → example.com |
| **MX** | Specifies mail servers for a domain | example.com → mail.example.com |
| **TXT** | Stores text-based information, often for security and verification | example.com → "v=spf1 include:_spf.google.com ~all" |
| **NS** | Specifies authoritative name servers for a domain | example.com → ns1.example.com, ns2.example.com |
| **PTR** | Reverse lookup record that maps an IP address to a domain | 192.168.1.1 → example.com |
| **SRV** | Defines service-specific records for applications | _sip._tcp.example.com → sipserver.example.com |
| **SOA** | Provides administrative information about a DNS zone | example.com → Primary NS, email, serial number |

---

## 🔥2c. Firewall and Security Principles

A **firewall** is a network security system that monitors and controls incoming and outgoing network traffic based on predefined security rules. It acts as a barrier between a trusted internal network and untrusted external networks like the internet.

### 📌 Firewall Rules Typically Include:
- **Source IP Address:** Specifies where the traffic originates from.
- **Destination IP Address:** Specifies the target of the traffic.
- **Port Number:** Determines the type of service (e.g., HTTP, SSH, FTP) being accessed.
- **Protocol:** Defines whether TCP, UDP, or ICMP is used.
- **Action:** Allows or blocks traffic based on defined rules.

### 📌 Basic and Necessary Port Numbers

| Port Number | Protocol | Description |
|------------|----------|-------------|
| **22**     | TCP      | SSH (Secure Shell) for secure remote access |
| **53**     | UDP/TCP  | DNS (Domain Name System) for resolving domain names |
| **80**     | TCP      | HTTP (Hypertext Transfer Protocol) for web traffic |
| **443**    | TCP      | HTTPS (Secure HTTP) for encrypted web traffic |
| **25**     | TCP      | SMTP (Simple Mail Transfer Protocol) for sending emails |
| **110**    | TCP      | POP3 (Post Office Protocol) for retrieving emails |
| **143**    | TCP      | IMAP (Internet Message Access Protocol) for email retrieval |
| **3389**   | TCP      | RDP (Remote Desktop Protocol) for remote Windows access |
| **3306**   | TCP      | MySQL database communication |
| **27017**   | TCP      | Mongo database communication |
| **8080**   | TCP      | Alternative HTTP port |

### 🔒 Security Principles

A **security principles** denotes the basic guidelines that should be used while developing a secure application systems. Security principles are fundamental guidelines that help protect systems, networks, and data from unauthorized access, attacks, and vulnerabilities.

### 🔹 The Five basic security principles are:

1️⃣ **Confidentiality**
2️⃣ **Integrity**
3️⃣ **Avalibality**
4️⃣ **Authentication**
5️⃣ **Non-Repudiation**

### Best User Practices:

## 🔹 1. Least Privilege

Users and systems should have only the minimum necessary permissions to perform their tasks. This reduces the risk of accidental or intentional misuse.

📌 **Example:** A database administrator has read/write access to databases, while a regular user only has read access.

---

## 🔹 2. Defense in Depth

Multiple layers of security should be used to protect systems, ensuring that if one layer is breached, others remain in place.

📌 **Example:** Using a combination of firewalls, intrusion detection systems (IDS), and endpoint security solutions.

---

## 🔹 3. Zero Trust

Assume that threats exist both inside and outside the network, and verify every request before granting access.

📌 **Example:** Implementing multi-factor authentication (MFA) and continuous user authentication.

---

## 🔹 4. Security by Design

Security should be integrated into the development lifecycle rather than added as an afterthought.

📌 **Example:** Using secure coding practices and conducting regular security assessments.

---

## 🔹 5. Incident Response and Monitoring

Organizations should continuously monitor for threats and have an incident response plan in place to handle security breaches efficiently.

📌 **Example:** Setting up Security Information and Event Management (SIEM) solutions and defining a response plan for cyber incidents.

---

## 🔹 6. Data Encryption

Sensitive data should be encrypted in transit and at rest to prevent unauthorized access.

📌 **Example:** Using TLS for secure web communication and encrypting databases with AES encryption.

---

## 🔹 7. Regular Patching and Updates

Keeping software and systems updated helps protect against known vulnerabilities.

📌 **Example:** Regularly applying security patches to operating systems, applications, and firmware.

---

## 🔹 8. User Awareness and Training

Educating users about security threats and best practices helps reduce human-related security risks.

📌 **Example:** Conducting phishing awareness training and enforcing strong password policies.

---

## 📦 2d. Packet Flow and Routing

A **Packet Flow** and **Routing** determine how data moves across networks from the source to the destination. Understanding these concepts is essential for troubleshooting network issues and optimizing performance.

---

## 🔹 1. Packet Flow
**Packet flow** refers to the journey of data packets from the sender to the receiver across different networking layers.

### 🚀 **Packet Flow Steps:**
1. **Application Layer**: The sender’s application generates data (e.g., HTTP request).
2. **Transport Layer**: Data is segmented into TCP/UDP packets and assigned port numbers.
3. **Network Layer**: The packet is assigned a source and destination IP address for routing.
4. **Data Link Layer**: The packet is encapsulated into frames with MAC addresses.
5. **Physical Layer**: The frame is converted into electrical/optical signals and sent via cables or wireless.
6. **Intermediate Network Devices (Switches, Routers)**:
   - Switches forward frames within the same network.
   - Routers forward packets between different networks.
7. **Destination Device**: The data is received, reassembled, and passed to the appropriate application.

---

## 🔹 2. Routing
Routing is the process of determining the best path for data packets to reach their destination. This is handled by **routers** and follows predefined rules.

### 🛤 **Types of Routing:**
| Routing Type      | Description  | Example |
|------------------|-------------|---------|
| **Static Routing** | Manually configured routes; suitable for small networks. | `ip route add 192.168.1.0/24 via 10.0.0.1` |
| **Dynamic Routing** | Routers learn and update routes automatically using protocols. | OSPF, BGP, RIP |
| **Default Routing** | A single route used when no specific match is found. | `0.0.0.0/0 via 192.168.1.1` |

### 🔀 **Routing Process:**
1. A router receives a packet.
2. It checks the **destination IP** in its routing table.
3. If a route is found, it forwards the packet to the next-hop router.
4. If no route is found, it follows the default route or drops the packet.

---

## 🔹 3. Key Routing Protocols
| Protocol  | Type        | Description |
|-----------|------------|-------------|
| **RIP**   | Distance Vector | Uses hop count as a metric; slow convergence. |
| **OSPF**  | Link-State | Faster, more scalable; uses shortest path first (SPF) algorithm. |
| **BGP**   | Path-Vector | Used for internet routing between ISPs and large networks. |
| **EIGRP** | Hybrid     | Combines features of distance vector and link-state protocols. |

---

## 🔹 4. Packet Forwarding and NAT
- **Packet Forwarding**: The process of passing packets from one network interface to another.
- **Network Address Translation (NAT)**: Translates private IP addresses to public IPs for internet access.
  - **Types of NAT**:
    - **SNAT (Source NAT)**: Changes the source IP (used in outbound traffic).
    - **DNAT (Destination NAT)**: Changes the destination IP (used in port forwarding).

---

🚀 Happy Learning! 🎯