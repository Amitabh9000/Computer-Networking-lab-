# Experiment 08
________________

## 🧾 Problem Statement

Create a simulation to demonstrate logical addressing using IPv4 and IPv6. Implement address mapping techniques such as ARP, RARP, BOOTP, and DHCP to show how devices acquire and resolve network addresses using Cisco Packet Tracer.

---

## 🎯 Learning Outcomes

* Understand and apply IPv4 and IPv6 addressing
* Implement ARP, RARP, BOOTP, and DHCP
* Analyze how devices acquire and resolve addresses
* Visualize packet flow using simulation mode
* Compare different address mapping techniques

---

## 🧩 Module 1: Network Topology Design

### 📌 Topology Description

The network consists of:

* 2 PCs (PC0, PC1)
* 1 Switch (2960)
* 1 Router (1941)
* 1 DHCP + RARP Server (Server0)
* 1 BOOTP Server (Server1)

### 🔗 Connections

* PCs and Servers connected to Switch
* Switch connected to Router

---

## 🌐 Module 2: Address Configuration (IPv4 & IPv6)

### 📌 IPv4 Addressing Scheme

* Network: 192.168.1.0/24
* Router: 192.168.1.1
* Server0: 192.168.1.2
* Server1: 192.168.1.3
* PC1: 192.168.1.20
* PC0: Dynamic (DHCP/BOOTP)

### 📌 IPv6 Addressing Scheme

* Network: 2001:DB8:1::/64
* Router: 2001:DB8:1::1
* PC1: 2001:DB8:1::20

---

### ⚙️ Router Configuration

```bash
enable
configure terminal
interface g0/0
ip address 192.168.1.1 255.255.255.0
ipv6 address 2001:DB8:1::1/64
no shutdown
```

---

## 🔁 Module 3: Address Mapping Implementation

### 🔹 ARP (Address Resolution Protocol)

* PC0 sends ARP request (broadcast)
* PC1 replies with MAC address (unicast)

Check ARP table:

```bash
arp -a
```

---

### 🔹 RARP (Reverse Address Resolution Protocol)

* Enabled RARP service on Server0
* MAC to IP mapping configured
* PC0 retrieves IP using MAC address

---

### 🔹 BOOTP (Bootstrap Protocol)

* Enabled BOOTP on Server1
* Static MAC → IP mapping configured
* PC0 receives fixed IP

---

### 🔹 DHCP (Dynamic Host Configuration Protocol)

* Enabled DHCP on Server0
* Configured pool:

  * Start IP: 192.168.1.100
  * Gateway: 192.168.1.1

#### DHCP Process (DORA)

1. Discover
2. Offer
3. Request
4. Acknowledge

---

## 🌍 Module 4: Simulation and Visualization

### 🔎 Steps Performed

* Switched to Simulation Mode
* Used Add Simple PDU
* Used Capture/Forward

### 📊 Observed Protocols

* ARP → MAC resolution
* DHCP → IP assignment
* BOOTP → Static mapping
* ICMP → Ping communication

---

## 📡 Module 5: Testing and Results

### ✔ IPv4 Communication

```bash
ping 192.168.1.20
```

Result: Successful

---

### ✔ IPv6 Communication

```bash
ping 2001:DB8:1::20
```

Result: Successful

---

## 📊 Comparative Analysis

| Protocol | Function      | Type    | Usage               |
| -------- | ------------- | ------- | ------------------- |
| ARP      | IP → MAC      | Dynamic | Local communication |
| RARP     | MAC → IP      | Static  | Legacy systems      |
| BOOTP    | MAC → IP      | Static  | Predefined configs  |
| DHCP     | IP Assignment | Dynamic | Modern networks     |


---


## ▶️ How to Run the Project

1. Open Cisco Packet Tracer
2. Load:

   * `ipv4_ipv6_addressing.pkt`
   * `address_mapping.pkt`
3. Switch to Simulation Mode
4. Use Add Simple PDU
5. Observe packet flow

---

## ScreenShot

<img width="592" height="613" alt="image" src="https://github.com/user-attachments/assets/10ee6e17-017b-49be-bacf-b33c590410f2" />
