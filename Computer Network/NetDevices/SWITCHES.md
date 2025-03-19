![[1.jpeg]]
### **Switches :**

Switch is a device that operates at Layer 2 , and its primary function is to **filter** and **forward** packets between devices within a LAN. The switch forwards data based on MAC addresses to ensure that data reaches the correct destination device. Key points about switches:

1. **Functionality**: The switch examines the destination **MAC address** (unique hardware address of the device) to decide which port of switch to forward the packet to.
2. **Data Communication Types**: Switches support various forms of communication:
    - **Unicast**: One device sends data to another specific device.
    - **Multicast**: One device sends data to multiple devices.
    - **Broadcast**: One device sends data to all devices on the network.
3. **Multilayer Switches**: These switches operate at both Layer 2 and Layer 3 enabling routing between different subnets or VLANs. They combine the functionality of both a switch and a router.
4. **CAM Table**: Switches maintain a **Content Addressable Memory (CAM) table**, mapping MAC addresses to their corresponding ports, allowing the switch to quickly forward packets without broadcasting them to all devices on the network.
---
### **Features of Network Switches**

1. **Error Checking**: Switches perform basic error checking to ensure data integrity, discarding corrupted packets before forwarding.
2. **Selective Forwarding**: Unlike hubs , switches forward data **only to the device** it is meant for, reducing unnecessary network traffic.
3. **Full-Duplex Communication**: Switches support **full-duplex** mode, meaning they can send and receive data simultaneously, unlike hubs, which only allow one-way communication at a time.
4. **Packet-Switching**: Switches use **packet-switching** techniques, breaking data into smaller packets and forwarding them to the correct destination device based on the MAC address table.
5. **Multiple Ports**: Switches have more ports than hubs, enabling them to connect multiple devices, allowing network scaling without congestion.
6. **MAC Address Learning**: The switch learns **MAC addresses** by monitoring incoming frames and adding the **MAC address and port** to its CAM table for future use.
7. **Spanning Tree Protocol (STP)**: Prevents network loops in switched environments by ensuring only one active path exists between switches.
8. **Port Security**: Managed switches can restrict which devices connect to specific ports, enhancing security by preventing unauthorized access.
9. **Quality of Service (QoS)**: Prioritizes time-sensitive traffic (e.g., VoIP or video) to ensure performance and prevent delays in high-traffic networks.
10. **VLAN Tagging**: Supports **VLANs**  to segment networks logically. VLANs enhance security and efficiency, with **802.1Q** as the standard for tagging VLANs in Ethernet frames.
11. **Redundancy and High Availability**: Supports **Link Aggregation** for increased bandwidth and redundancy..
12. **Security Features**: Advanced security options like **Access Control Lists (ACLs)**, **RADIUS authentication**, and **port-based security** help protect the network from unauthorized access.
13. **Switch Stacking and Modularity**: **Switch Stacking** allows multiple switches to operate as one, improving manageability. **Modular switches** allow adding or removing modules based on network requirements.
---
### **Types of Switches**

1. **Virtual Switches**: Used in **virtualized environments** functioning within virtual machines.
2. **Routing Switches**: These perform both **switching** (Layer 2) and **routing** (Layer 3) functions, routing traffic between network segments or VLANs.
3. **Unmanaged Switches**: Simple **plug-and-play** devices, typically used in small networks, requiring no configuration. They offer no management features and cannot be monitored or controlled. Limited functionality, without options for monitoring, security, or advanced traffic management.
4. **Managed Switches**: Provide advanced features like:
    - **Remote Configuration**: Can be configured and monitored remotely using protocols like **SNMP** or CLI.
    - **VLAN Support**: Enable creation of **Virtual LANs** for better security or performance.
    - **Quality of Service (QoS)**: Prioritize traffic (e.g., voice or video) to ensure network performance.
    - **Security Features**: Monitor and control network access to prevent unauthorized users.
5. **PoE (Power over Ethernet) Switches**: Provide both **data and power** over Ethernet cables to devices like IP cameras and VoIP phones.
6. **Smart Switches**: Intermediate between unmanaged and managed switches, offering some basic management features like **VLANs** or **QoS**.
---
### **Layer 2 vs. Layer 3 Switches**

- **Layer 2 Switch**:
    - Operates at the **Data Link Layer**.
    - Forwards packets based on **MAC addresses**.
    - Used in **LAN environments** with devices in the same subnet.
    - Helps **reduce collisions** by segmenting the network into different collision domains.
- **Layer 3 Switch**:
    - Operates at Layer 2 and Layer 3.
    - Can **route packets** between different **subnets** or **VLANs** based on **IP addresses**.
    - Combines the **speed of switching** with the **flexibility of routing**.
---
### **How a Network Switch Works**

1. **Data Arrival**: A device sends a packet, which enters the switch through one of its ports.
2. **Packet Inspection**: The switch examines the packet’s **header**, focusing on the **destination MAC address**.
3. **Forwarding Decision**: The switch checks its **CAM table** for the MAC address. If found, the packet is forwarded to the correct port. If not, the switch broadcasts the packet to all other ports to locate the destination device.
4. **Data Transmission**: The packet is forwarded to the appropriate port, where it is received by the destination device.
---
