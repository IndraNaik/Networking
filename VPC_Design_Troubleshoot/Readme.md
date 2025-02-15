# 🏗️  VPC Design & Troubleshooting

## 📌 Key Topics

### 🎯 3a. Best Practices for VPC Design
- Use **multiple Availability Zones (AZs)** for high availability.
- Implement **private and public subnets** to separate resources securely.
- Enable **VPC Flow Logs** for monitoring traffic.
- Apply **least privilege security groups** and **network ACLs**.
- Use **Elastic IPs** wisely to manage external access.
- Leverage **VPC Peering** or **Transit Gateway** for inter-VPC communication.

---

### 📜 3b. Route Tables & NAT Gateway
- **Route Tables:** Define how traffic is directed within the VPC.
- **Internet Gateway (IGW):** Allows public subnet instances to access the internet.
- **NAT Gateway:** Enables private subnet instances to access the internet while remaining unexposed.
- **VPC Peering & Transit Gateway:** Connect multiple VPCs efficiently.

🖥️ **Example Routing Table:**
| Destination CIDR | Target | Notes |
|-----------------|--------|-------|
| 0.0.0.0/0 | Internet Gateway (IGW) | Public subnet outbound traffic |
| 10.0.1.0/24 | Local | Internal VPC communication |
| 0.0.0.0/0 | NAT Gateway | Private subnet outbound traffic |

---

### 🚨 3c. Common VPC Connectivity Issues & Fixes

| 🛑 Issue | 🔍 Cause | 🛠️ Fix |
|---------|--------|-------|
| No internet access in public subnet | Missing IGW or route table misconfiguration | Attach IGW & update route table |
| Private subnet can't access the internet | No NAT Gateway assigned | Add NAT Gateway & configure routes |
| Inter-VPC communication failure | Missing VPC Peering / Transit Gateway routes | Configure proper routing rules |
| Unable to SSH into EC2 | Security group blocking inbound traffic | Open required ports in security group |

🔍 **Troubleshooting Commands:**
- `ping <destination>` → Check basic network connectivity.
- `traceroute <IP>` → Trace the route packets take to the destination.
- `netstat -r` → View routing table.
- `telnet <IP> <Port>` → Check if a port is open.
- `dig <domain>` → Verify DNS resolution.

---

✅ Following these best practices ensures a **secure, scalable, and resilient** VPC architecture! 🚀

