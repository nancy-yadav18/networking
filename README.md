## 🌐 Hybrid Network Topology Lab (Cisco Packet Tracer)

This repository contains a customized **Hybrid Network Topology** designed in Cisco Packet Tracer. The layout combines **Mesh**, **Bus/Linear**, and **Star** sub-topologies connected through a central router to form a multi-departmental network.

---

## 📸 Network Topology Overview

![Hybrid Network Topology](./assets/hybrid_topology.png)

---

## 🛠️ Network Architecture & Design

This hybrid design combines three distinct structural topologies:

1. **Partial Mesh Core Segment:** 
   * Formed by **Router0 (Cisco 2911)**, **core Switch1 (2960-24TT)**, **core Switch2 (2960-24TT)**, and **core Switch3 (2960-24TT)**.
   * Provides redundant interconnectivity and path fault tolerance between core distribution switches.

2. **Linear / Bus Extension (Engineering Department):**
   * Connected sequentially from `core Switch1` $\rightarrow$ `eng Switch1` $\rightarrow$ `eng Switch2`.
   * Serves host endpoints (`PC0` and `PC1`).

3. **Star Topology Extension (HR Department):**
   * Connected directly from `core Switch2` to **HR-Hub1 (Hub-PT)**.
   * Branches out in a physical star formation to multiple endpoints (`PC2`, `PC3`, and `PC4`).

---

## 📑 Device Inventory

| Device Name | Device Model | Quantity | Role / Department |
| :--- | :--- | :--- | :--- |
| **Router0** | Cisco 2911 | 1 | Core Router / Default Gateway |
| **core Switch1** | Catalyst 2960-24TT | 1 | Core Switch (Left) |
| **core Switch2** | Catalyst 2960-24TT | 1 | Core Switch (Right) |
| **core Switch3** | Catalyst 2960-24TT | 1 | Redundant Core Link Switch |
| **eng Switch1** | Catalyst 2960-24TT | 1 | Engineering Access Switch 1 |
| **eng Switch2** | Catalyst 2960-24TT | 1 | Engineering Access Switch 2 |
| **HR-Hub1** | Hub-PT | 1 | HR Department Central Hub |
| **PC0 – PC4** | Generic PC-PT | 5 | End-user PCs |

---

## ⚙️ Key Concepts Implemented

* **Redundancy & Loop Prevention:** Redundant copper crossover links between core switches managed via **Spanning Tree Protocol (STP)**.
* **Hybrid Interconnectivity:** Demonstrates host aggregation across switches and collision-domain sharing across hub-connected star topologies.
* **Routed Trunking & Access:** Direct Gigabit/FastEthernet routing from `Router0` down through core switching modules.

---

## 🚀 How to Open and Run

1. Download or clone this repository:
   ```bash
   git clone [https://github.com/your-username/networking-repo.git](https://github.com/your-username/networking-repo.git)
