# Experiment 05
________________

## 🧾 Problem Statement

Design and simulate flow control and error control protocols such as Stop and Wait, Go-Back-N ARQ, and Selective Repeat ARQ using Cisco Packet Tracer. Compare their performance in terms of throughput and efficiency under varying network conditions.

---

## 🎯 Learning Outcomes

* Understand flow control and error control mechanisms
* Analyze Stop and Wait, Go-Back-N, and Selective Repeat ARQ
* Simulate packet transmission using Cisco Packet Tracer
* Compare efficiency and throughput of protocols
* Evaluate performance under network conditions

---

## 🧩 Module 1: Network Topology Design

### 📌 Topology Description

The network consists of:

* PC0 (Sender)
* PC1 (Receiver)
* Router (to simulate network conditions)

### 🔗 Connections

* PC0 connected to Router
* PC1 connected to Router

---

## 🌐 Module 2: Address Configuration

### 📌 IP Addressing Scheme

| Device      | IP Address   | Subnet Mask   | Gateway     |
| ----------- | ------------ | ------------- | ----------- |
| PC0         | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| Router G0/0 | 192.168.1.1  | 255.255.255.0 | -           |
| Router G0/1 | 192.168.2.1  | 255.255.255.0 | -           |
| PC1         | 192.168.2.10 | 255.255.255.0 | 192.168.2.1 |

---

### ⚙️ Router Configuration

```bash id="r1cfg"
enable
configure terminal

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown

interface g0/1
ip address 192.168.2.1 255.255.255.0
no shutdown
```

---

## 🧪 Module 3: Simulation Setup

### Step 1: Connectivity Test

On PC0:

```bash id="pingtest"
ping 192.168.2.10
```

✔ Result: Successful communication

---

### Step 2: Switch to Simulation Mode

* Enable **Simulation Mode**
* Open **Event List**

---

## 🔁 Module 4: Stop and Wait Protocol

### 📌 Concept

Stop and Wait allows only one frame to be sent at a time. The sender waits for acknowledgment before sending the next frame.

### 📊 Simulation

* Send one PDU at a time from PC0 → PC1
* Wait for reply before sending next

### 👀 Observation

* One packet sent → reply received → next packet

### ✅ Interpretation

This represents Stop and Wait protocol behavior.

---

## 🔁 Module 5: Go-Back-N ARQ

### 📌 Concept

Go-Back-N allows multiple frames to be sent without waiting, but retransmits all frames from the error point onward.

### 📊 Simulation

* Send multiple PDUs (4–5) from PC0 → PC1
* Introduce error by deleting one packet

### 👀 Observation

* Communication disrupted after packet loss
* Conceptually, all frames from the lost one must be resent

### ✅ Interpretation

This demonstrates Go-Back-N ARQ behavior.

---

## 🔁 Module 6: Selective Repeat ARQ

### 📌 Concept

Selective Repeat retransmits only the lost frames instead of all frames.

### 📊 Simulation

* Send multiple PDUs
* Delete only one packet

### 👀 Observation

* Other packets still reach destination
* Only missing packet affects communication

### ✅ Interpretation

This represents Selective Repeat ARQ.

---

## 🔍 Module 7: Packet Analysis

### 📊 Observations

* Protocol used: ICMP
* Packets visible in Simulation Mode
* Packet drops simulated manually

---

## ⚠️ Limitations of Packet Tracer

Cisco Packet Tracer does not provide full implementation of:

* Sequence numbers
* Sliding window size
* Actual retransmission logic
* Real ARQ mechanisms

👉 Therefore, the experiment demonstrates conceptual behavior using ICMP packets.

---

## 📊 Module 8: Performance Comparison

| Protocol         | Throughput | Efficiency | Behavior                 |
| ---------------- | ---------- | ---------- | ------------------------ |
| Stop & Wait      | Low        | Low        | One frame at a time      |
| Go-Back-N        | Medium     | Moderate   | Resends multiple frames  |
| Selective Repeat | High       | High       | Resends only lost frames |

---

## 📈 Analysis

* Stop and Wait has low efficiency due to waiting time
* Go-Back-N improves throughput but wastes bandwidth during retransmission
* Selective Repeat is most efficient as it retransmits only lost frames

---

## ⚠️ Challenges Faced

* Packet Tracer limitations
* Manual simulation of errors
* Conceptual understanding required

---

## 🚀 Improvements

* Use NS2/NS3 for real protocol simulation
* Add more nodes for complex scenarios
* Introduce delay and packet loss conditions

---

## ▶️ How to Run the Simulation

1. Open Cisco Packet Tracer
2. Load the topology
3. Switch to Simulation Mode
4. Add multiple PDUs
5. Delete packets to simulate errors
6. Use Capture/Forward
7. Observe packet flow

---

## Screenshot 
go_back_n 
<img width="1920" height="1080" alt="Screenshot 2026-04-23 001112" src="https://github.com/user-attachments/assets/52064b47-bbf4-4f6f-a15c-e9cc9fe3499b" />

selective_repeat_arq
<img width="1920" height="1080" alt="Screenshot 2026-04-23 002758" src="https://github.com/user-attachments/assets/eaa51249-dc36-4540-9219-6436b5e9f8a1" />

Stop_and_wait
<img width="1920" height="1080" alt="Screenshot 2026-04-23 004133" src="https://github.com/user-attachments/assets/2e32d032-85d9-4fb4-ba09-b12cbac06ffb" />


