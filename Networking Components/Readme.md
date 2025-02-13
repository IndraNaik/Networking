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

🚀 Happy Learning! 🎯