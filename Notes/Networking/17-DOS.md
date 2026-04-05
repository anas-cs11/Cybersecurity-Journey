## Denial of Service (DoS) and Distributed Denial of Service (DDoS)

A **DoS** (**Denial of Service**) attack is a malicious attempt to disrupt the normal operations of a network or server by flooding it with an overwhelming amount of traffic. The goal is to make the system crash or become so slow that "legitimate users" (real people trying to use the service) cannot access it.

## 1. DoS vs. DDoS: Scale and Source

While the goal is the same, the method of delivery differs based on how many devices the attacker uses.

| **Term** | **Full Name** | **Description** |
| --- | --- | --- |
| **DoS** | **Denial of Service** | An attack coming from a single source or device. |
| **DDoS** | **Distributed Denial of Service** | An attack using **multiple devices** or servers in different locations. |

**Why DDoS is dangerous:** By using many devices at once, the attacker can send a much larger volume of traffic, making it harder for the target server to stay online.

---

## 2. Common Network-Level DoS Attacks

These attacks specifically target network **Bandwidth** (the capacity to move data) or the way protocols handle connections.

### A. SYN Flood Attack

This attack exploits the **TCP** (**Transmission Control Protocol**) "handshake" process.

1. **The Handshake:** Normally, a device sends a **SYN** (Synchronize) request, the server replies with a **SYN/ACK** (Acknowledge), and the device sends a final **ACK**.
2. **The Attack:** The attacker floods the server with **SYN** requests but never sends the final **ACK**.
3. **The Result:** The server leaves "half-open" ports waiting for the final step. If the number of requests is larger than the available ports, the server becomes overwhelmed and stops functioning.

``

### B. ICMP Flood Attack

**ICMP** (**Internet Control Message Protocol**) is used by devices to send error messages or status updates.

- **The Attack:** An attacker repeatedly sends **ICMP** packets to a server.
- **The Result:** The server is forced to reply to every single one. This uses up all the bandwidth for incoming and outgoing traffic, causing a crash.

### C. Ping of Death

This attack uses a single, massive request to break a system rather than thousands of small ones.

- **The Attack:** The hacker sends an **Oversized ICMP Packet** larger than **64 Kilobytes** (the maximum legal size).
- **The Result:** Vulnerable systems cannot handle a packet this large and will crash immediately.

> **The Anthill Analogy:**
Think of a server like an anthill. Each ant can carry a small amount of weight (normal data). An **ICMP Flood** is like thousands of tiny grains of sand dropped at once. A **Ping of Death** is like dropping one giant rock on the hill—the system is crushed instantly.
> 

---

## 3. Real-World Context: Processing Overload

**Case Study: The "Careful Packet" Attack**
Sometimes, it isn't about the *amount* of traffic, but the *type* of traffic.

- **The Scenario:** An attacker sends a specifically "crafted" packet.
- **The Impact:** The router doesn't crash from high volume; instead, it spends so much extra time trying to process that one complex request that it ignores everyone else.
- **The Result:** This proves that if an attacker overloads *any* part of the network—even just a single router's processor—they "win" by stopping business
