This passage introduces the **OSI (Open Systems Interconnection)** model, which is the industry-standard "map" used by security professionals to pinpoint where problems or attacks are happening across seven different layers.

## The 7 Layers of the OSI Model

The **OSI (Open Systems Interconnection)** model breaks down network communication from the physical hardware all the way to the software on your screen.

**Layer 7: Application Layer**

- **Focus:** User interaction and network requests.
- **Function:** This is the only layer the user actually "sees." It uses protocols to connect software to the internet.
- **Examples:**
    - **HTTP/HTTPS (Hypertext Transfer Protocol/Secure):** For web browsing.
    - **SMTP (Simple Mail Transfer Protocol):** For sending emails.
    - **DNS (Domain Name System):** Translating website names (like google.com) into **IP (Internet Protocol)** addresses.

**Layer 6: Presentation Layer**

- **Focus:** Data translation and formatting.
- **Function:** It ensures that the data sent by one system can be understood by the other. It handles **Encryption**, **Compression**, and character sets.
- **Example:** **SSL (Secure Sockets Layer)** encrypts data between your browser and a web server.

**Layer 5: Session Layer**

- **Focus:** Connection management.
- **Function:** It starts (opens), manages, and ends (terminates) the conversation between two devices.
- **Key Tasks:** **Authentication** (checking who you are) and **Checkpoints** (if the connection drops, it picks up where it left off).

**Layer 4: Transport Layer**

- **Focus:** End-to-end delivery and flow control.
- **Function:** It breaks large data into smaller pieces called **Segmentation** and manages the speed of the transfer to match the receiver.
- **Protocols:** **TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)**.

**Layer 3: Network Layer**

- **Focus:** Routing between different networks.
- **Function:** It uses **IP (Internet Protocol)** addresses to decide the best path for data packets to travel from the sender's network to the receiver's network.
- **Hardware:** Routers live at this layer.

**Layer 2: Data Link Layer**

- **Focus:** Communication within a *single* network.
- **Function:** It organizes data into "frames" and handles physical addressing.
- **Hardware:** **Switches** and **NICs (Network Interface Cards)**.
- **Protocols:** **HDLC (High-level Data Link Control)** and **SDLC (Synchronous Data Link Control)**.

**Layer 1: Physical Layer**

- **Focus:** Physical hardware and raw bitstreams.
- **Function:** Translates data packets into a stream of **0s and 1s** (electrical or light signals) to travel across cables.
- **Hardware:** Hubs, modems, Ethernet cables, and fiber optics.
