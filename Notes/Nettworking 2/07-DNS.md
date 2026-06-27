# What is DNS?

* **Definition:** A system responsible for properly mapping a human-readable domain name (like `example.com`) to a numerical **IP (Internet Protocol)** address.
* **Network Placement:** Operates at the **Application Layer** (Layer 7) of the **ISO (International Organization for Standardization) OSI (Open Systems Interconnection)** model.
* **Network Ports:** Uses **UDP (User Datagram Protocol) Port 53** by default for speed, and **TCP (Transmission Control Protocol) Port 53** as a fallback.

---

**Four Essential DNS Record Types**

Different types of internet requests require different kinds of maps. The four most common types are:

| Record Type | What it Stands For | Purpose | Real-World Example |
| --- | --- | --- | --- |
| **A** | Address | Maps a hostname to an **IPv4 (Internet Protocol Version 4)** address. | `example.com` $\to$ `172.17.2.172` |
| **AAAA** | Quad-A | Maps a hostname to an **IPv6 (Internet Protocol Version 6)** address. | `example.com` $\to$ `2606:2800:21f:cb07:6820:80da:af6b:8b2c` |
| **CNAME** | Canonical Name | Maps a domain name to another domain name (an alias). | `www.example.com` $\to$ `example.com` |
| **MX** | Mail Exchange | Specifies the server responsible for handling emails for that domain. | Sending an email to `test@example.com` triggers an MX lookup. |

> **Security Note:** Do not confuse the **AAAA** DNS record with the cybersecurity acronym **AAA**, which stands for **Authentication, Authorization, and Accounting**.

---

**Command-Line Tools for DNS Analysis**

Security analysts use command-line tools to verify how domains resolve and to inspect network traffic for malicious activity.

### **1. nslookup (Name Server Lookup)**

Used to look up the IP address of a domain directly from the terminal.

```bash
user@TryHackMe$ nslookup www.example.com
Server:         127.0.0.53
Address:        127.0.0.53#53

Non-authoritative answer:
Name:   www.example.com
Address: 93.184.215.14
Name:   www.example.com
Address: 2606:2800:21f:cb07:6820:80da:af6b:8b2c

```

* **Analysis:** The output shows that `www.example.com` resolves to both an IPv4 address (`93.184.215.14`) and an IPv6 address (`2606:2800...`).

### **2. tshark (Terminal Wireshark)**

A command-line network packet analyzer used to read packet capture files (**PCAPNG - Packet Capture Next Generation**).

```bash
user@TryHackMe$ tshark -r dns-query.pcapng -Nn
    1  192.168.66.89 → 192.168.66.1  DNS  Standard query A www.example.com
    2  192.168.66.1  → 192.168.66.89  DNS  Standard query response A 93.184.215.14
    3  192.168.66.89 → 192.168.66.1  DNS  Standard query AAAA www.example.com
    4  192.168.66.1  → 192.168.66.89  DNS  Standard query response AAAA 2606:2800...

```

* **Packet 1:** The client (`192.168.66.89`) asks the local router (`192.168.66.1`) for the **A record** (IPv4).
* **Packet 2:** The router responds with the IPv4 address `93.184.215.14`.
* **Packet 3:** The client asks for the **AAAA record** (IPv6).
* **Packet 4:** The router responds with the long IPv6 string.

---

