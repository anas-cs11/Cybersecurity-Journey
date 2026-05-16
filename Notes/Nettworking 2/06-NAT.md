# **NAT (Network Address Translation)**

The world is running out of IPv4 addresses (only about 4 billion available). **NAT** is a clever solution that allows **many devices** to share **one public IP address** to access the internet.

---

### **Why Do We Need NAT?**

- Buying a public IP address for every device (laptop, phone, camera, smart TV, etc.) is very expensive and not possible.
- NAT lets a company or home use **private IP addresses** internally, while using **only one (or very few) public IP addresses** to connect to the internet.

**Real-life Analogy**:
Think of your home as an office building.

- Private IPs = Employees’ extension numbers (only used inside the building).
- Public IP = The main office phone number.
NAT is like the receptionist — she translates between internal extensions and the single external phone number so everyone can make calls using just one number.

---

### **How NAT Works**

When a device on your internal network wants to access the internet:

1. The device sends a request using its **private IP** and a **port number**.
2. The **NAT router** (usually your home WiFi router) changes:
    - The **Source IP** from private → public IP
    - The **Source Port** to a new unique port
3. It records this mapping in a **NAT Translation Table**.
4. When the reply comes back, the router uses the table to forward the response to the correct internal device.

**Example from the passage:**

| Device | Internal (Private) | External (Public) after NAT |
| --- | --- | --- |
| Laptop | 192.168.0.129 : 15401 | 212.3.4.5 : 19273 |

From the web server’s point of view, the connection appears to come from the public IP address only.

---

### **Key Benefits of NAT**

- Saves public IP addresses (very important).
- Provides a level of security — external devices cannot directly see or reach internal private IPs.
- Allows many devices to share one internet connection.

---

### **One-Line Summary**

**NAT** is like a translator that lets hundreds of devices with **private IP addresses** share **one public IP address** to access the internet by keeping track of connections using a translation table.
