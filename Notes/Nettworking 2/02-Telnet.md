# **TELNET Protocol – Simple Explanation**

**Telnet** (Teletype Network) is an old but still useful protocol that lets you connect to a remote computer or service and communicate with it using **text commands**.

In simple terms:
Telnet allows you to **manually talk** to any service running on a TCP port, just like having a direct text conversation with that service.

> **Note**: Telnet is **not secure** (it sends everything in plain text), so it is rarely used for real administration today. However, it is excellent for learning and testing.
> 

---

### **Services Tested Using Telnet**

The passage demonstrates how to use Telnet to connect to three different services on a target machine:

| Service | Port | What it does | Behavior |
| --- | --- | --- | --- |
| **Echo Server** | 7 | Repeats everything you type | Stays connected until you close it |
| **Daytime Server** | 13 | Returns the current date and time | Sends response and immediately closes |
| **Web (HTTP) Server** | 80 | Serves web pages (you can request manually) | Allows manual HTTP commands |

---

### **Practical Examples**

### 1. Connecting to Echo Server (Port 7)

Shell

`telnet MACHINE_IP 7`

- You type anything → the server sends back the exact same text.
- Real-life example: Like talking to someone who repeats everything you say.

### 2. Connecting to Daytime Server (Port 13)

Shell

`telnet MACHINE_IP 13`

- The server immediately replies with the current date and time and closes the connection.

### 3. Connecting to Web Server (Port 80)

Shell

`telnet MACHINE_IP 80`

After connecting, you manually type:

text

`GET / HTTP/1.1
Host: telnet.thm`

(Then press **Enter** twice)

This sends a basic HTTP request to fetch the homepage, just like a web browser would do behind the scenes.

---

### **How to Close Telnet Connection**

- Press Ctrl + ] to get the telnet prompt
- Then type quit and press Enter

---

### **Key Takeaways**

- Telnet is a simple tool to **test and communicate** with services on any TCP port.
- It helps you understand how different services (Echo, Daytime, HTTP, etc.) work at a very basic level.
- Even though Echo and Daytime servers are insecure and not used in real environments, they are great for learning.

**Real-life Analogy**:
Telnet is like calling a service hotline and talking directly to the system using raw commands, instead of using a polished app or browser.
