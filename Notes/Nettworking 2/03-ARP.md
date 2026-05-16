# **ARP (Address Resolution Protocol)**

When two devices want to communicate on the **same local network** (Ethernet or WiFi), they need each other’s **MAC address** (hardware address).

They usually know the **IP address**, but not the MAC address. **ARP** is the protocol that helps them **translate** (resolve) an IP address into the correct MAC address.

---

### **Why Do We Need ARP?**

- **IP Address** = Logical address (used for routing across networks)
- **MAC Address** = Physical address (used for delivery inside the local network)

Even if your device knows the destination IP, it still needs the MAC address to create the **Ethernet frame** (Layer 2).

**Real-life Analogy**:
Imagine you want to send a letter to your neighbor in the same apartment building.
You know their **apartment number** (IP address), but to hand over the letter, the security guard needs their **exact door nameplate** (MAC address). ARP is like asking loudly in the building: “Who lives in apartment 101?”

---

### **How ARP Works**

1. **ARP Request**
    - A device sends a broadcast message to **all devices** on the local network.
    - It asks: “Who has IP address 192.168.66.1? Please tell me your MAC address.”
    - This is sent to the broadcast MAC address: ff:ff:ff:ff:ff:ff
2. **ARP Reply**
    - The device that owns that IP address replies directly to the requester.
    - It says: “I have IP 192.168.66.1 and my MAC address is 44:df:65:d8:fe:6c”

Once the MAC address is known, both devices can communicate directly using Ethernet frames.

---

### **Example from Packet Capture**

**ARP Request:**

> Who has 192.168.66.1? Tell 192.168.66.89
> 

**ARP Reply:**

> 192.168.66.1 is at 44:df:65:d8:fe:6c
> 

---

### **Key Features of ARP**

| Feature | Description |
| --- | --- |
| Layer | Primarily Layer 2 (Data Link) |
| Protocol Type | Not carried inside IP or UDP. It is directly inside Ethernet frame |
| Broadcast | ARP Request is broadcasted |
| Unicast | ARP Reply is sent directly to the requester |
| Purpose | Maps IP address → MAC address |

---

### **Important Points**

- ARP is only used for devices on the **same local network** (same subnet).
- Once a device gets a MAC address, it usually stores it temporarily in its **ARP cache** (to avoid asking again and again).
- ARP is essential for local communication — without it, devices on the same WiFi/Ethernet cannot talk to each other even if they have each other’s IP addresses.

---

**One-Line Summary**:

**ARP** is the translator that converts a known **IP address** into the required **MAC address** so devices on the same local network can communicate at the data link layer.
