# Experimen 01
_______________


## 🧾 Problem Statement

Design and simulate a simple computer network using various connection topologies: **Bus, Star, Ring, and Mesh**. Compare the advantages and disadvantages of each topology in terms of data flow and network efficiency and analyze their performance under different network conditions.

---

## 🎯 Learning Outcomes

* Apply networking concepts to analyze different topologies
* Design efficient network architectures
* Compare performance of Bus, Star, Ring, and Mesh
* Use Cisco Packet Tracer for simulation and analysis
* Evaluate impact on real-time communication

---

## 🧩 Logical Structure of Simulation

### 📌 Network Devices

* PCs (End devices)
* Switches
* Routers (optional)

### 🔗 Network Connections

* Twisted Pair Cable (Copper Straight-Through)
* Coaxial Cable (conceptual for bus)
* Fiber Optic Cable (optional)

### 📡 Data Flow Simulation

* Packet generation using **Add Simple PDU**
* Packet transmission analysis in Simulation Mode

---

# 🛠 Step 1: Setting Up Cisco Packet Tracer

1. Download from Cisco Networking Academy
2. Install and launch Packet Tracer
3. Create a new workspace (**File → New**)

---

# 🧩 Module 1: Bus Topology

## 📌 Design

* Devices connected in a linear structure

## ⚙️ Configuration

Assign IP addresses:

* PC0: 192.168.1.1
* PC1: 192.168.1.2
* Subnet: 255.255.255.0

## 🧪 Testing

```bash id="busping"
ping 192.168.1.2
```

## 📊 Observation

* Data flows along a single path
* Entire network affected if main link fails

## ✅ Advantages

* Low cost
* Simple setup

## ❌ Disadvantages

* Poor scalability
* Low reliability

---

# ⭐ Module 2: Star Topology

## 📌 Design

* All devices connected to a central switch

## ⚙️ Configuration

* PC0: 192.168.2.1
* PC1: 192.168.2.2

## 🧪 Testing

```bash id="starping"
ping 192.168.2.2
```

## 📊 Observation

* Centralized communication
* Easy fault detection

## ✅ Advantages

* Easy management
* High performance

## ❌ Disadvantages

* Switch failure affects entire network

---

# 🔄 Module 3: Ring Topology

## 📌 Design

* Devices connected in circular form

## ⚙️ Configuration

* Assign IPs in same network

## 🧪 Testing

```bash id="ringping"
ping next device IP
```

## 📊 Observation

* Data flows in a circular path
* Delay increases with number of nodes

## ✅ Advantages

* Organized data transmission

## ❌ Disadvantages

* One failure disrupts entire network

---

# 🕸️ Module 4: Mesh Topology

## 📌 Design

* Every device connected to every other device

## ⚙️ Configuration

* Assign IPs within same network

## 🧪 Testing

```bash id="meshping"
ping all connected devices
```

## 📊 Observation

* Multiple paths available
* High reliability

## ✅ Advantages

* Fault tolerant
* High efficiency

## ❌ Disadvantages

* Expensive
* Complex configuration

---

# 🔍 Module 5: Data Flow Simulation

## Steps:

1. Switch to **Simulation Mode**
2. Use **Add Simple PDU tool**
3. Send packets between devices
4. Use **Capture/Forward**

## 📊 Observations

* Packet flow between nodes
* Delay differences across topologies
* Packet success/failure

---

# 📊 Performance Comparison

| Topology | Cost   | Reliability | Efficiency | Complexity |
| -------- | ------ | ----------- | ---------- | ---------- |
| Bus      | Low    | Low         | Low        | Low        |
| Star     | Medium | Medium      | High       | Low        |
| Ring     | Medium | Low         | Medium     | Medium     |
| Mesh     | High   | Very High   | Very High  | High       |

---

# 📈 Analysis

* **Bus** is cost-effective but unreliable
* **Star** is widely used due to ease of management
* **Ring** is less preferred due to failure risks
* **Mesh** provides best performance but is costly

---

# ⚠️ Challenges Faced

* Difficulty in simulating Bus and Ring in Packet Tracer
* Managing multiple connections in Mesh topology
* IP configuration errors

---

# 🚀 Improvements

* Add hybrid or tree topology
* Simulate network failures
* Introduce traffic load testing

---

# ▶️ How to Run the Simulation

1. Open Cisco Packet Tracer
2. Load topology file
3. Assign IP addresses
4. Test connectivity using ping
5. Switch to Simulation Mode
6. Observe packet flow

---
## Screenshot  Star topology  
<img width="1920" height="1080" alt="Screenshot 2026-04-23 103754" src="https://github.com/user-attachments/assets/d032d55e-479b-4f2b-b387-2631ddf7c283" />

## Screenshot Mesh topology 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/128d1e48-d140-4cc7-a74b-21e2b4f6e0cc" />

## Screenshot bus toplogy 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/edaca365-d572-4d0b-aa54-0940d5009de9" />

## Screenshot ring topology 
<img width="1920" height="1080" alt="Screenshot 2026-04-23 105102" src="https://github.com/user-attachments/assets/f8386e37-5225-46bd-af31-747d7058cf7c" />



