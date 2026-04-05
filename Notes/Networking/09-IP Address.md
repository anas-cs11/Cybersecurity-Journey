This passage explains how devices find each other on a network using two types of "digital addresses": the logical IP address and the physical MAC address.

# What is an IP Address?
An **IP (Internet Protocol)** address is a unique string of characters that identifies the location of a device on the internet.
• **The Mailing Analogy:** Just like every house on a street needs a unique mailing address to receive letters, every device needs an IP address to receive data packets.

**IPv4 vs. IPv6**
Because the internet grew so fast, we ran out of the original style of addresses, leading to a newer, longer version.**FeatureIPv4 (Internet Protocol Version 4)IPv6 (Internet Protocol Version 6)Format**Four sets of 1, 2, or 3-digit numbers.A long string of 32 hexadecimal characters.**Example**192.168.1.12001:0db8:85a3:0000:0000:8a2e:0370:7334**Separated by**Decimal points (.)Colons (:)**Capacity**Limited (nearly used up).Massive (allows for trillions of devices).

**Public vs. Private IP Addresses**
Devices actually use two different IP addresses depending on whether they are talking to the world or talking to other devices in the same room.

• **Public IP Address:** Assigned by your **ISP (Internet Service Provider)**. This is your "global" address. Just like roommates share one physical house address, all devices in your home share one Public IP when talking to the internet.

• **Private IP Address:** These are only seen by devices on your local network (like your phone talking to your printer). The rest of the internet cannot see these addresses.

**The MAC Address: The Permanent ID**
While an IP address can change if you move to a new Wi-Fi network, a **MAC (Media Access Control)** address is permanent.
• **Definition:** A unique alphanumeric identifier assigned to the physical hardware of every network device.
• **The Switch & The MAC Table:** When a **Switch** (a device that connects others on a network) receives data, it looks at the MAC address to see exactly which physical device should get the packet.
• **The "Address Book":** The switch stores these in a **MAC Address Table** so it knows which physical port leads to which device.
