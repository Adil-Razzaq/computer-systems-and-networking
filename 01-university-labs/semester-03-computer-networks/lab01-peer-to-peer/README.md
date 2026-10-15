# Lab 01: Peer-to-Peer Static IPv4 Network Configuration

## 📌 Objective
This laboratory demonstrates the direct point-to-point physical and logical connection between two host end-devices without intermediary layer-3 routing devices. The primary goal is to configure static IPv4 addressing, verify Layer-2 physical connectivity, and test Layer-3 ICMP reachability using peer end-hosts.

---

## 🌐 Address Allocation Table

| Host Name | Interface | IP Address | Subnet Mask | Default Gateway | Subnet Network ID |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **PC-A** | `FastEthernet0` | `192.168.1.10` | `255.255.255.0` (`/24`) | `0.0.0.0` | `192.168.1.0` |
| **PC-B** | `FastEthernet0` | `192.168.1.20` | `255.255.255.0` (`/24`) | `0.0.0.0` | `192.168.1.0` |

---

## 🛠️ Configuration & Verification Steps

1. **Physical Layer Setup:**
   * Connected `PC-A` (`FastEthernet0`) directly to `PC-B` (`FastEthernet0`) using a **Copper Crossover Cable** (or connected both via a Layer-2 Switch using **Copper Straight-Through Cables**).

2. **IP Address Configuration:**
   * Configured static IPv4 address `192.168.1.10` with Subnet Mask `255.255.255.0` on `PC-A`.
   * Configured static IPv4 address `192.168.1.20` with Subnet Mask `255.255.255.0` on `PC-B`.

3. **ICMP Reachability & ARP Verification:**
   * Opened Command Prompt on `PC-A` and executed `ping 192.168.1.20`.
   * Verified physical link status and Address Resolution Protocol (ARP) mapping using `arp -a`.

---

## 📸 Verification & Screenshots

* **Packet Tracer File:** [`topology.pkt`](./topology.pkt)

### 1. Topology Layout
![Topology Workspace](./screenshots/topology.png)

### 2. GUI Static IP Assignment (PC-A)
![IP Configuration GUI](./screenshots/ip_config.png)

### 3. ICMP Ping Test (PC-A to PC-B)
![Ping Proof](./screenshots/ping_proof.png)