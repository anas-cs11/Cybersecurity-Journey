## IP Spoofing and Associated Attacks

**IP Spoofing** is a network attack where an attacker changes the **Source IP** of a data packet to impersonate a trusted system. By "pretending" to be an authorized user, the hacker can bypass firewall rules that usually block outside traffic.

| **Attack Type** | **Description** | **Goal** |
| --- | --- | --- |
| **On-path Attack** | The attacker places themselves between two devices (like a browser and a server). | To intercept, read, or change data in transit. |
| **Replay Attack** | An attacker captures a valid data packet and "plays it back" or delays it later. | To impersonate a user and gain unauthorized access to a session. |
| **Smurf Attack** | A mix of **DDoS** (**Distributed Denial of Service**) and spoofing. | To flood a target with traffic using a spoofed IP, crashing the network. |

## 2. Deep Dive: On-path and Replay Attacks

- **On-path Attack:** The attacker "sniffs" the packet to learn the **IP** and **MAC** (**Media Access Control**) addresses of both sides. Once they have these, they can pretend to be either device to trick the other.
- **Replay Attack:** Imagine a user sends a "Login Successful" packet. An attacker captures that specific packet and sends it again an hour later. Even if the attacker doesn't know the password, the system might see the "valid" packet and let them in.

---

## 3. How to Prevent IP Spoofing

While spoofing is a clever trick, there are strong technical defenses to stop it.

- **Encryption:** Always encrypt data so that even if a packet is caught or replayed, the attacker cannot read or use the information inside.
- **Firewall Configuration (Ingress Filtering):** You can set a rule to catch "impossible" traffic.
    - **The Logic:** If a packet arrives from the **Internet** (outside), but its **Source IP** says it is from your **Local Network** (inside), the firewall knows it is a lie.
    - **The Rule:** Configure the firewall to **deny/reject** any incoming traffic that claims to have an internal IP address.

---

## 4. Real-World Context: The Smurf Attack

**Case Study: The Overwhelmed Server**
Imagine a university in **Chennai** with a student server.

1. **The Spoof:** An attacker sends a request to thousands of devices, but they "spoof" the **Source IP** to be the university's main server.
2. **The Flood:** All those thousands of devices send a response at the same time back to the university server (the "Smurf" effect).
3. **The Result:** The university server is hit with a massive **DDoS** attack it didn't even ask for, causing the website to crash during exam registration.
