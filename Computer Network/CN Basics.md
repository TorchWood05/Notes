![[1.jpeg]]
### **Switches Overview**

A **network switch** is a device that operates at the Data Link Layer (Layer 2) of the OSI model, and its primary function is to **filter** and **forward** packets between devices within a **Local Area Network (LAN)**. The switch forwards data based on **MAC (Media Access Control) addresses** to ensure that data reaches the correct destination device. Key points about switches:

1. **Functionality**: The switch examines the destination **MAC address** (unique hardware address of the device) to decide which port to forward the packet to.
    
2. **Data Communication Types**: Switches support various forms of communication:
    
    - **Unicast**: One device sends data to another specific device.
    - **Multicast**: One device sends data to multiple devices.
    - **Broadcast**: One device sends data to all devices on the network.
3. **Multilayer Switches**: These switches operate at both Layer 2 (Data Link Layer) and Layer 3 (Network Layer), enabling routing between different subnets or VLANs (Virtual Local Area Networks). They combine the functionality of both a switch and a router.
    
4. **CAM Table**: Switches maintain a **Content Addressable Memory (CAM) table**, mapping MAC addresses to their corresponding ports, allowing the switch to quickly forward packets without broadcasting them to all devices on the network.

---
### **Features of Network Switches**

1. **Layer of Operation**: Switches primarily function at the **Data Link Layer (Layer 2)**, dealing with the physical addressing (MAC addresses) of devices.
    
2. **Error Checking**: Switches perform basic error checking to ensure data integrity, discarding corrupted packets before forwarding.
    
3. **Selective Forwarding**: Unlike hubs (which forward data to all devices), switches forward data **only to the device** it is meant for, reducing unnecessary network traffic.
    
4. **Full-Duplex Communication**: Switches support **full-duplex** mode, meaning they can send and receive data simultaneously, unlike hubs, which only allow one-way communication at a time.
    
5. **Packet-Switching**: Switches use **packet-switching** techniques, breaking data into smaller packets and forwarding them to the correct destination device based on the MAC address table.
    
6. **Multiple Ports**: Switches have more ports than hubs, enabling them to connect multiple devices, allowing network scaling without congestion.

---
### **Types of Switches**

Switches come in different types suited to different network needs:

1. **Virtual Switches**: Used in **virtualized environments** (e.g., VMware or Hyper-V), functioning within virtual machines.
    
2. **Routing Switches**: These perform both **switching** (Layer 2) and **routing** (Layer 3) functions, routing traffic between network segments or VLANs.
    
3. **Unmanaged Switches**: Simple **plug-and-play** devices, typically used in small networks, requiring no configuration. They offer no management features and cannot be monitored or controlled.
    
4. **Managed Switches**: Provide advanced features like:
    
    - **Remote Configuration**: Can be configured and monitored remotely using protocols like **SNMP** or CLI.
    - **VLAN Support**: Enable creation of **Virtual LANs** for better security or performance.
    - **Quality of Service (QoS)**: Prioritize traffic (e.g., voice or video) to ensure network performance.
    - **Security Features**: Monitor and control network access to prevent unauthorized users.
5. **LAN Switches**: General-purpose switches designed for **Local Area Networks (LANs)**, available in Layer 2 or Layer 3 versions.
    
6. **PoE (Power over Ethernet) Switches**: Provide both **data and power** over Ethernet cables to devices like IP cameras and VoIP phones.
    
7. **Smart Switches**: Intermediate between unmanaged and managed switches, offering some basic management features like **VLANs** or **QoS**.
    
8. **Stackable Switches**: Can be physically stacked to function as a single switch, useful for scaling networks without complexity.
    
9. **Modular Switches**: Allow the addition or removal of modules (e.g., extra ports) based on needs, typically used in larger or complex networks.
    
---
### **Layer 2 vs. Layer 3 Switches**

- **Layer 2 Switch**:
    
    - Operates at the **Data Link Layer**.
    - Forwards packets based on **MAC addresses**.
    - Used in **LAN environments** with devices in the same subnet.
    - Helps **reduce collisions** by segmenting the network into different collision domains.
- **Layer 3 Switch**:
    
    - Operates at **Data Link Layer (Layer 2)** and **Network Layer (Layer 3)**.
    - Can **route packets** between different **subnets** or **VLANs** based on **IP addresses**.
    - Combines the **speed of switching** with the **flexibility of routing**.
    - Ideal for larger networks with multiple subnets or VLANs.

---
### **Unmanaged vs. Managed Switches**

- **Unmanaged Switch**:
    
    - Simple **plug-and-play** operation, with no configuration required.
    - Used in small networks with no complex management needs.
    - **Limited functionality**, without options for monitoring, security, or advanced traffic management.
- **Managed Switch**:
    
    - Offers features like **remote configuration**, **traffic management**, and **network monitoring**.
    - Used in **enterprise networks** requiring control and flexibility.
    - Provides features like **VLANs**, **Quality of Service (QoS)**, **Security (e.g., ACLs)**, and **SNMP monitoring**.
    
---
### **How a Network Switch Works**

1. **Data Arrival**: A device sends a packet, which enters the switch through one of its ports.
    
2. **Packet Inspection**: The switch examines the packet’s **header**, focusing on the **destination MAC address**.
    
3. **Forwarding Decision**: The switch checks its **CAM table** for the MAC address. If found, the packet is forwarded to the correct port. If not, the switch broadcasts the packet to all other ports to locate the destination device.
    
4. **Data Transmission**: The packet is forwarded to the appropriate port, where it is received by the destination device.
    

This process ensures efficient data flow and minimizes unnecessary broadcast traffic, optimizing network performance.

---
### **Additional Features and Concepts**

1. **Switch Learning Process (MAC Address Learning)**: The switch learns **MAC addresses** by monitoring incoming frames and adding the **MAC address and port** to its CAM table for future use.
    
2. **Broadcast Storm Prevention**: Managed switches can limit or prevent **broadcast storms** that overwhelm the network, improving performance.
    
3. **Spanning Tree Protocol (STP)**: Prevents network loops in switched environments by ensuring only one active path exists between switches.
    
4. **Port Security**: Managed switches can restrict which devices connect to specific ports, enhancing security by preventing unauthorized access.
    
5. **Quality of Service (QoS)**: Prioritizes time-sensitive traffic (e.g., VoIP or video) to ensure performance and prevent delays in high-traffic networks.
    
6. **VLAN Tagging**: Supports **VLANs** (Virtual Local Area Networks) to segment networks logically. VLANs enhance security and efficiency, with **802.1Q** as the standard for tagging VLANs in Ethernet frames.
    
7. **Redundancy and High Availability**: Supports **Link Aggregation** for increased bandwidth and redundancy. Some switches feature **dual power supplies** and **stacking** for improved reliability.
    
8. **Power over Ethernet (PoE)**: Delivers both **data and power** over Ethernet cables to devices like IP cameras and VoIP phones, reducing the need for separate power supplies.
    
9. **Security Features**: Advanced security options like **Access Control Lists (ACLs)**, **RADIUS authentication**, and **port-based security** help protect the network from unauthorized access.
    
10. **Switch Stacking and Modularity**: **Switch Stacking** allows multiple switches to operate as one, improving manageability. **Modular switches** allow adding or removing modules based on network requirements.