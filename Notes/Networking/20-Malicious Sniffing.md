## Packet Sniffing: Passive vs. Active Attacks

**Packet sniffing** is the practice of using software or hardware tools to observe data as it moves across a network. While security analysts use it to debug issues, **Malicious Actors** use it like "opening someone else's mail" to steal sensitive info.

---

## 1. Anatomy of a Data Packet

To understand sniffing, you must remember what is inside a packet:

- **Header:** Contains the "to" and "from" **IP** (**Internet Protocol**) addresses.
- **Body:** Contains the actual data, such as names, dates of birth, personal messages, and credit card numbers.

``

---

## 2. Types of Packet Sniffing Attacks

Attackers "insert themselves in the middle" of a connection to spy on or change these packets.

| **Type** | **How it Works** | **Analogy** |
| --- | --- | --- |
| **Passive Sniffing** | The attacker simply **reads** the data as it passes by. They do not change anything. | A mail carrier reading your postcards while delivering them. |
| **Active Sniffing** | The attacker **manipulates** the data. They might change the info or redirect it to a different port. | A neighbor offering to take your mail, opening it, changing the letter, and then putting it in your box. |

## 3. How to Prevent Packet Sniffing

The good news is that these attacks can be blocked or made useless by using **Encryption**.

- **Use a VPN (Virtual Private Network):** A **VPN** wraps your data in a secure tunnel. Even if a hacker "sniffs" the packet, they cannot **decode** it to read your private information.
- **Check for HTTPS:** Always ensure websites use **HTTPS** (**Hypertext Transfer Protocol Secure**). This uses **SSL/TLS** (**Secure Sockets Layer/Transport Layer Security**) to scramble the data so eavesdroppers can't understand it.
- **Avoid Unprotected Wi-Fi:** Public networks in coffee shops or airports often have **no encryption**. This means *anyone* on that network can see your data.

> **Safety Tip:** Never use free public Wi-Fi unless you have a **VPN** service turned on first.
> 

---

## 4. Real-World Context: The "Middleman" in the Cafe

**Case Study: The Unsecured Hotspot**
Imagine you are at an airport in **Chennai** and connect to "Free Airport Wi-Fi."

1. **The Setup:** A hacker nearby is also on the network using a **Packet Sniffer**.
2. **The Passive Attack:** You log into a site that only uses HTTP (not secure). The hacker sees your username and password pop up on their screen in "plain text."
3. **The Active Attack:** The hacker intercepts your request to go to your bank and "injects" a new protocol that redirects you to a fake version of the bank's site to steal even more data.
4. **The Fix:** If you had turned on your **VPN**, the hacker would only see a scrambled mess of gibberish, protecting your bank account.
