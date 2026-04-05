## **1. Security Logs: The Digital Paper Trail**

A **log** is a record of every event that happens in a network. Analysts use three main sources to spot trouble:

- **Firewall Logs:** Record of connections trying to enter or leave the network from the internet.
    - *Purpose:* Spots hackers trying to "break in" or malware trying to "call home."
- **Network Logs:** Record of every device (phones, laptops, servers) that joins or leaves the network.
    - *Purpose:* Tracks lateral movement (how a threat moves from one computer to another).
- **Server Logs:** Record of specific service activities like websites, emails, or file sharing.
    - *Purpose:* Monitors login attempts, password changes, and file access.

---

## **2. SIEM Tools: The Security Brain**

**SIEM** (Security Information and Event Management) is an application that collects all those logs and makes sense of them.

- **Centralization:** Instead of checking 100 different computers, a SIEM puts all logs in **one place**.
- **Real-Time Visibility:** Shows exactly what is happening *right now* across the entire company.
- **Automated Alerts:** If a log shows something suspicious (like 50 failed logins in 1 minute), the SIEM sends an instant alert to the analyst.
- **Efficiency:** It indexes and filters data so analysts don't have to read millions of lines of code manually.

---

## **3. Maintaining the SIEM**

A SIEM is not "set it and forget it." It requires constant updates:

- **Customization:** Each company has different needs (e.g., a bank's SIEM is set up differently than a school's).
- **Evolution:** As hackers invent new tricks, analysts must update the SIEM's "rules" to detect those new threats.
