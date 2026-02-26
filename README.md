# Enterprise Campus Network Design (CCNA-Level Simulation)

## 📌 Project Overview

This project simulates a small-to-medium enterprise campus network using Cisco Packet Tracer.  
The design integrates routing, switching, VLAN segmentation, centralized services, and WAN connectivity between multiple departments.

The goal of this project is to demonstrate practical CCNA-level networking skills by implementing real-world enterprise network concepts in a structured and scalable topology.

---

## 🏗 Network Architecture

The topology follows a hierarchical enterprise design model:

- **Core Layer** – Central router interconnecting all departmental routers
- **Distribution Layer** – Multilayer switch (Layer 3 switch) performing inter-VLAN routing
- **Access Layer** – Access switches connecting end devices (PCs, printers, servers)

### Departments Implemented

- HR Department  
- Finance Department  
- Sales & Marketing Department  
- Server Network  

Each department operates within its own subnet and is connected through routed WAN links.

---

## 🌐 Technologies Implemented

- VLAN Segmentation  
- Inter-VLAN Routing using Multilayer Switch (SVIs)  
- OSPF (Single Area – Area 0)  
- EtherChannel (Link Aggregation)  
- DHCP (Centralized Server)  
- DNS (Internal Name Resolution)  
- VLSM Subnetting  
- /30 Point-to-Point WAN Links 

---

## 🧠 IP Addressing & Subnetting Strategy

This project uses **VLSM (Variable Length Subnet Masking)** to efficiently allocate IP space.

### Departmental Networks
- 192.168.10.0/24 
- 192.168.20.0/24  
- 192.168.30.0/24  

### Server Network
- 192.168.1.0/24  

### WAN Links
- 203.113.X.X /30 networks used for router-to-router connections  

Using /30 subnets for WAN links minimizes IP waste while maintaining full connectivity.

---

## 🔄 Dynamic Routing – OSPF

- OSPF configured on all routers  
- Single Area (Area 0) backbone design  
- Automatic route advertisement between departments  
- Ensures scalable and dynamic routing across the enterprise network  

OSPF allows the network to adapt automatically to topology changes without manual static route configuration.

---

## 🔗 EtherChannel Implementation

EtherChannel is configured between switches to:

- Increase available bandwidth  
- Provide link redundancy  
- Prevent spanning-tree blocking on parallel links  
- Improve network reliability  

---

## 🖥 Network Services

### DHCP
- Centralized DHCP server located in the server network  
- Routers configured with `ip helper-address`  
- Automatic IP assignment per VLAN  

### DNS
- Internal DNS server deployed  
- End devices can resolve internal domain names  

---

## 🧪 Network Testing & Validation

The following tests were successfully performed:

- Inter-VLAN communication  
- End-to-end connectivity between departments  
- DHCP IP address assignment 
- OSPF route propagation verification  

---

## 🎯 Key Skills Demonstrated

- Enterprise network topology design  
- Hierarchical network modeling  
- Advanced subnetting with VLSM  
- Dynamic routing protocol configuration (OSPF)  
- Layer 2 & Layer 3 switching concepts  
- Centralized service deployment (DHCP & DNS)  
- Redundancy implementation with EtherChannel  

---

## 🚀 Future Improvements

- Implement ACLs to restrict inter-department traffic  
- Add Port Security on access switches  
- Implement HSRP for gateway redundancy  
- Expand to multi-area OSPF design  
- Introduce network monitoring (SNMP / Syslog)

---

## 👨‍💻 Author

Mohamed  
Junior Network Engineer | CCNA Candidate  
Focused on enterprise network infrastructure and routing & switching technologies.
