# The 4 Layers of the TCP/IP Model

The model organizes network activities into a "stack." Data starts at the top (Application) when you send it and moves down to the bottom (Network Access) to be physically transmitted.

**Layer 1: Network Access Layer**

- **Focus:** Physical hardware and the creation of data packets.
- **Components:** This involves physical cables, network interface cards, and **Switches** (devices that connect others on a network).
- **Security Role:** Ensuring the physical hardware is secure and that packets are correctly formed for transmission.

**Layer 2: Internet Layer**

- **Focus:** Addressing and Routing.
- **Components:** This is where **IP (Internet Protocol)** addresses are attached to packets.
- **Function:** It decides if a packet stays on the **LAN (Local Area Network)** or needs to be sent to a remote network like the internet.
- **Security Role:** Monitoring where traffic is coming from and going to (Source and Destination IP).

**Layer 3: Transport Layer**

- **Focus:** Flow control and Connection status.
- **Components:** Protocols that permit or deny communication between devices.
- **Function:** It handles **Error Control**, making sure data flows smoothly without getting "clogged" or lost.
- **Security Role:** Managing which devices are allowed to talk to each other.

**Layer 4: Application Layer**

- **Focus:** User interaction and services.
- **Components:** The protocols that your apps use to function.
- **Examples:** Email services (like **SMTP - Simple Mail Transfer Protocol**) and file transfers (like **FTP - File Transfer Protocol**).
- **Security Role:** Ensuring the software and services themselves aren't being exploited by hackers.

---

**Case Study: Sending an Email**

1. **Application Layer:** You hit "Send" in your email app.
2. **Transport Layer:** The system checks the connection to the email server and prepares to flow the data.
3. **Internet Layer:** The "To" and "From" **IP (Internet Protocol)** addresses are stamped onto the packets.
4. **Network Access Layer:** The data is turned into electrical or light signals and sent through your Ethernet cable or Wi-Fi.
