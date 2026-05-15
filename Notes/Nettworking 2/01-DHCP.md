# **How Your Devices Automatically Get Network Settings (DHCP)**

When you connect your laptop or phone to a new WiFi (like at a coffee shop), you don’t manually type any IP address, yet it works instantly. This magic is done by **DHCP** — **Dynamic Host Configuration Protocol**.

---

### **Why Do We Need DHCP?**

Every device on a network needs these 3 things to work properly:

1. **IP Address + Subnet Mask**
2. **Default Gateway** (Router)
3. **DNS Server**

Manually setting these is fine for **servers** (which stay in one place), but it’s impractical for laptops, phones, and tablets that move between networks.

**DHCP** automatically assigns these settings, saving time and preventing **IP address conflicts** (two devices having the same IP).

---

### **How DHCP Works: The DORA Process**

DHCP follows a simple 4-step process called **DORA**:

| Step | Message | Who Sends? | What Happens? |
| --- | --- | --- | --- |
| **1. Discover** | DHCPDISCOVER | Client | Client broadcasts: “Is there any DHCP server here?” |
| **2. Offer** | DHCPOFFER | DHCP Server | Server replies: “You can take this IP address” |
| **3. Request** | DHCPREQUEST | Client | Client says: “I accept this IP” |
| **4. Acknowledge** | DHCPACK | DHCP Server | Server confirms: “IP is now yours” |

**Real-life Analogy**:
Imagine going to a restaurant (new network):

- **Discover** → You ask: “Is there anyone who can give me a table?”
- **Offer** → The waiter offers you a table number.
- **Request** → You say “I’ll take that table.”
- **Acknowledge** → The waiter confirms the table is reserved for you.

---

### **Important Details**

- The client starts with **no IP address** (it uses 0.0.0.0).
- It communicates using **broadcast** messages (255.255.255.255) because it doesn’t know the DHCP server’s address yet.
- DHCP uses **UDP** protocol:
    - Server listens on **UDP Port 67**
    - Client sends from **UDP Port 68**

**What DHCP gives your device at the end:**

- A leased IP address
- Subnet mask
- Default Gateway (Router)
- DNS server address

---

### **Quick Summary**

**DHCP** is like an automatic network assistant.
When your device joins a new WiFi:

1. It shouts “Anyone there?” (Discover)
2. The router’s DHCP server offers an IP (Offer)
3. Your device accepts it (Request)
4. The server confirms (Acknowledge)

This whole process usually happens in less than a second — which is why your laptop connects to the coffee shop WiFi instantly without any manual setup.
