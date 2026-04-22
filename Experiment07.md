# Experiment 07
________________


## 🧾 Problem Statement

Implement a simulation to demonstrate the sliding window protocol with piggybacking for efficient data transmission and error control. Use Cisco Packet Tracer to simulate data transfer between two nodes and visualize packet flow, acknowledgments, and window behavior.

---

## 🎯 Learning Outcomes

* Understand sliding window protocol for flow control
* Understand piggybacking in bidirectional communication
* Simulate packet transmission using Cisco Packet Tracer
* Analyze packet flow using Simulation Mode
* Evaluate efficiency of data transmission concepts

---

## 🧩 Module 1: Network Topology Design

### 📌 Topology Description

The network consists of:

* PC0 (Sender)
* PC1 (Receiver)
* Switch (2960)

### 🔗 Connections

* PC0 connected to Switch
* PC1 connected to Switch

---

## 🌐 Module 2: Address Configuration

### 📌 IP Addressing Scheme

| Device | IP Address   | Subnet Mask   |
| ------ | ------------ | ------------- |
| PC0    | 192.168.1.10 | 255.255.255.0 |
| PC1    | 192.168.1.20 | 255.255.255.0 |

---

## 🧪 Module 3: Simulation Setup

### Step 1: Connectivity Test

On PC0:

```bash
ping 192.168.1.20
```

✔ Result: Successful communication

---

### Step 2: Switch to Simulation Mode

* Click on **Simulation Mode**
* Open **Event List**

---

### Step 3: Create Data Packets

* Use **Add Simple PDU tool**
* Send multiple packets from:

  * PC0 → PC1 (4–5 times)

---

## 🔁 Module 4: Sliding Window Simulation

### 📌 Concept

Sliding Window Protocol allows multiple frames to be sent before receiving acknowledgments.

### 📊 Observation

* Multiple packets observed moving from PC0 to PC1
* Packets sent continuously without waiting

### ✅ Interpretation

This behavior represents sliding window transmission.

---

## 🔁 Module 5: Piggybacking Simulation

### 📌 Concept

Piggybacking combines acknowledgment with outgoing data frames.

### 📊 Simulation Steps

* Send packets from:

  * PC1 → PC0

### 📊 Observation

* Bidirectional packet flow observed
* Packets moving in both directions

### ✅ Interpretation

Reverse traffic represents piggybacked acknowledgments.

---

## 🔍 Module 6: Packet Analysis

### 📊 Observations from Simulation Mode

* Protocol used: ICMP
* Source and Destination IP visible
* Continuous packet flow

---

## ⚠️ Limitations of Packet Tracer

Cisco Packet Tracer does not provide full implementation of:

* Sliding window size
* Sequence numbers
* Real acknowledgment numbers
* TCP-level piggybacking

👉 Therefore, this experiment demonstrates the concept visually rather than implementing the protocol internally.

---

## 📡 Module 7: Final Output

* Multiple packets transmitted from sender to receiver
* Packets observed in both directions
* Successful communication between nodes
* Simulation mode shows packet movement

---

## 📊 Comparative Understanding

| Concept        | Explanation                                  |
| -------------- | -------------------------------------------- |
| Sliding Window | Multiple frames sent without waiting for ACK |
| Piggybacking   | ACK included in reverse data transmission    |

---

## ⚠️ Challenges Faced

* Understanding limitations of Packet Tracer
* Simulating protocol behavior without real implementation
* Ensuring proper packet visualization

---

## 🚀 Improvements

* Use advanced simulators like NS2/NS3
* Implement real sliding window in programming
* Add more nodes for extended simulation

---

## ▶️ How to Run the Simulation

1. Open Cisco Packet Tracer
2. Load the topology file
3. Switch to Simulation Mode
4. Add multiple PDUs
5. Use Capture/Forward
6. Observe packet flow

---

## Screenshot

<img width="1920" height="1080" alt="Screenshot 2026-04-22 231244" src="https://github.com/user-attachments/assets/7c42f91b-a73a-440f-b630-120598225efa" />
