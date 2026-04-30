# CN_Mininet_Project
# 📡 Broadcast Traffic Control using SDN

📌 Project Overview

This project focuses on controlling excessive broadcast traffic in a network using **Software Defined Networking (SDN)**. Traditional networks flood broadcast packets to all devices, which can lead to congestion and inefficiency.

Using an SDN approach, we implement a Ryu controller that intelligently detects broadcast packets and applies controlled forwarding instead of blind flooding, thereby improving network performance.

---

🎯 Objectives

* Detect broadcast packets in the network
* Reduce unnecessary flooding
* Implement selective forwarding using SDN
* Improve overall network efficiency

---

🛠️ Technologies Used

* Mininet – Network simulation
* Ryu Controller (Python) – SDN control logic
* OpenFlow Protocol – Communication between controller and switch
* Wireshark (optional) – Packet analysis

---

🧠 Key Concepts

* Software Defined Networking (SDN)
* Control Plane vs Data Plane
* Broadcast Traffic & ARP
* MAC Learning
* Flow Rules (Match-Action)

---

⚙️ How It Works

1. A packet arrives at the switch
2. If no rule is found, it is sent to the controller
3. The controller analyzes the packet:
   * If it is a **broadcast packet**, controlled forwarding is applied
   * Otherwise, normal forwarding is performed using learned MAC addresses
4. The controller sends instructions back to the switch
5. The switch forwards the packet accordingly

---

🚀 Setup & Execution

1. Install Requirements

```bash
sudo apt update
sudo apt install mininet
pip install ryu
```

---

2. Run Ryu Controller

```bash
ryu-manager broadcast_control.py
```

---

3. Start Mininet

```bash
sudo mn --topo single,3 --controller remote --switch ovsk,protocols=OpenFlow13
```

---

4. Test Network

```bash
pingall
```

You can also generate broadcast traffic using:

```bash
h1 ping h2
```

---

📊 Expected Output

* Controller logs showing:

  * Broadcast packet detection
  * Controlled forwarding behavior
* Reduced unnecessary flooding compared to traditional networks

---

📈 Results

* Efficient handling of broadcast traffic
* Reduced network congestion
* Improved bandwidth utilization
* Demonstrates advantages of SDN over traditional networking

---

🔍 Future Enhancements

* Broadcast rate limiting
* Intelligent filtering using ML techniques
* Traffic visualization dashboard
* Integration with larger network topologies

---

👩‍💻 Author

Riya H
* AIML Student
* Passionate about networking, systems, and creative tech

---

📎 GitHub Repository

https://github.com/riyaharugop/CN_Mininet_Project

---

---
