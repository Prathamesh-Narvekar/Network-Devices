# Network-Devices

## SWITCH
<div align="center">
  <img src="https://github.com/user-attachments/assets/c3acf460-736c-4142-92d7-fdd8c0a2b2bb" alt="Switch" width="70%" />
</div>

### What is Switch?
- The Switch is a network device that is used to segment the networks into different subnetworks called subnets or LAN segments. It is responsible for filtering and forwarding the packets between LAN segments based on MAC address. 
- Switches have many ports, and when data arrives at any port, the destination address is examined first and some checks are also done and then it is processed to the devices. Different types of communication are supported here like unicast, multicast, and broadcast communication.
- Its primary function is to enable these devices to communicate with each other efficiently by managing the flow of data traffic.

### How does it work?
A switch is considered an "intelligent" device because it knows which port each connected device is on, unlike an older device like a hub, which simply broadcasts all data out of every port.
- Step-by-step process of how a switch operates:
  - Receiving a Data Packet
    - When a device sends data to another device on the network, the data is broken down into small units called packets. This packet is sent to the switch.
  - Learning MAC Addresses
    - Every device has a unique physical address called the MAC (Media Access Control) address. The switch learns the MAC address of each connected device and records it in an internal table called the MAC Address Table (or Content-Addressable Memory/CAM table), mapping the address to the specific port the device is connected to.
  - Forwarding the Packet
    - The switch reads the destination MAC address contained in the data packet.
    - It looks up this address in its MAC Address Table.
    - If the address is found, the switch forwards the packet only to the specific port connected to the destination device. This is called unicast communication.
  - Handling Unknown Addresses
    - If the destination MAC address is not yet in the table (e.g., the first time this device is communicating), the switch will temporarily send the packet to all ports (a process called flooding or broadcast).
    - The intended device will respond, allowing the switch to learn its MAC address and update its table for future communications.
    - By only sending data to the intended recipient, a switch optimizes network performance, reduces unnecessary traffic, and increases overall security compared to a hub.
   
## ROUTER
<div align="center">
  <img src="https://github.com/user-attachments/assets/991e1093-a7b9-4df3-ba4c-3c178ac1538e" alt="Router" width="70%" />
</div>

### What is a Router?
A router is a network device that connects different networks and determines the best path for data to travel from its source to its destination across those networks. It is the core component that enables communication between your private home/office network and the vast public network known as the Internet.

### How does it work?
Step-by-step process of how a switch operates:
- Receiving a Packet
  - A device on your Local Area Network (LAN) wants to send data (a packet) to a device on another network, like a web server on the Internet.
- Checking the Destination IP
  - The packet contains the destination IP address (e.g., the address of the website). The router reads this address.
- Consulting the Routing Table
  - The router maintains a Routing Table—a map that contains information about other networks it can reach and the best "next hop" (the next router) to send the packet to get it closer to its final destination.
- Packet Forwarding (Routing)
  - Based on the routing table, the router decides which of its ports (interfaces) the packet should be forwarded through.
    - If the destination is on the local network (LAN), it sends it to the device directly (often via a built-in switch).
    - If the destination is on a remote network (like the Internet, or a Wide Area Network/WAN), it forwards the packet to the next router along the calculated best path.
- Network Address Translation (NAT)
  - For home and small office routers, one of the most important jobs is NAT. This allows all the devices on your private network (which have private IP addresses) to share a single public IP address when communicating with the outside world (the Internet). This is essential for conserving IP addresses and providing a basic layer of security.
