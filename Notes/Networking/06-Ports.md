## The TCP/IP ModelTCP/IP (Transmission Control Protocol/Internet Protocol) is the universal standard for network communication. 
### It is made of two distinct parts working together:

**1. TCP (Transmission Control Protocol)**

- **Role:** The "Connection Manager."
- **Function:** It establishes a stable connection between two devices and ensures that every data packet arrives in the right order. It organizes the data stream so nothing gets lost or scrambled.

**2. IP (Internet Protocol)**

- **Role:** The "Address and Route Map."
- **Function:** It provides the set of standards for addressing and routing. The **IP (Internet Protocol) Address** acts as a specific digital destination for every private network or device.

---

**What are Network Ports?**
Once a data packet reaches the correct building (the IP address), it needs to know which room to go to. This is where **Ports** come in.

- **Definition:** A port is a software-based location within an operating system that organizes the sending and receiving of data.
- **The Apartment Analogy:** If the **IP (Internet Protocol)** is the street address of an apartment building, the **Port Number** is the specific apartment number (e.g., Apt 20 or Apt 443).
- **The Goal:** Ports allow a computer to run multiple services at once (like browsing the web and checking email) without the data getting mixed up.

---

**Common Port Numbers to Know**
Security analysts memorize these common ports because seeing unusual activity on them can signal an attack: 

| **Port Number** | **Service / Use Case** |
| --- | --- |
| **Port 20** | **FTP (File Transfer Protocol)**: Used for sending and receiving large files. |
| **Port 25** | **SMTP (Simple Mail Transfer Protocol)**: Used for sending emails. |
| **Port 443** | **HTTPS (Hypertext Transfer Protocol Secure)**: Used for secure internet browsing and encrypted communication. |

