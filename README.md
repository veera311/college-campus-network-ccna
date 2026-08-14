# college-campus-network-ccna
# College Campus Network — CCNA Project

## 📌 Project Overview

This project demonstrates the design and configuration of a small **College Campus Network** using **Cisco Packet Tracer**.

The network is divided into multiple VLANs representing different college departments. Inter-VLAN communication, automatic IP address assignment, Layer 2 redundancy and basic network security were implemented using Cisco networking technologies.

## 🖥️ Network Topology

The topology consists of:

* 1 Router
* 3 Cisco Switches
* 4 PCs
* Multiple VLANs
* Router-on-a-Stick inter-VLAN routing

## 🏢 VLAN Design

| VLAN | Department     | Network         | Gateway      |
| ---- | -------------- | --------------- | ------------ |
| 10   | Administration | 192.168.10.0/24 | 192.168.10.1 |
| 20   | CSE            | 192.168.20.0/24 | 192.168.20.1 |
| 30   | Staff          | 192.168.30.0/24 | 192.168.30.1 |
| 40   | Students       | 192.168.40.0/24 | 192.168.40.1 |

## 🔧 Technologies Implemented

### VLANs

Created separate VLANs for Administration, CSE, Staff and Students to provide logical network segmentation.

### Trunking

Configured 802.1Q trunk links between switches and the router to carry multiple VLANs.

### Router-on-a-Stick

Configured router subinterfaces for inter-VLAN routing:

```text
G0/0/0.10 → 192.168.10.1
G0/0/0.20 → 192.168.20.1
G0/0/0.30 → 192.168.30.1
G0/0/0.40 → 192.168.40.1
```

### DHCP

Configured Cisco IOS DHCP pools for automatic IP address assignment to clients.

### STP

Configured Spanning Tree Protocol and selected the central switch as the root bridge to help prevent Layer 2 switching loops.

### OSPF

Practiced OSPF configuration and dynamic routing concepts for communication between routers and remote networks.

### ACL

Implemented an extended ACL to restrict traffic from the Students VLAN to the Administration VLAN while permitting other traffic.

## 🧪 Verification & Testing

The following commands were used to verify the network:

```text
show vlan brief
show interfaces trunk
show ip interface brief
show ip dhcp binding
show spanning-tree
show ip route
show access-lists
```

Connectivity was tested using ICMP `ping` between different VLANs.

## 🎯 Project Objectives

* Understand VLAN segmentation
* Configure Cisco switch ports
* Configure 802.1Q trunking
* Implement inter-VLAN routing
* Configure DHCP
* Understand STP operation
* Practice OSPF dynamic routing
* Implement basic traffic filtering using ACLs
* Troubleshoot network connectivity

## 🛠️ Tools Used

* Cisco Packet Tracer
* Cisco IOS CLI

## 📚 Skills Demonstrated

**Networking:** VLAN, Trunking, STP, Inter-VLAN Routing, OSPF, ACL, DHCP

**Cisco:** Cisco IOS CLI, Router Configuration, Switch Configuration, Network Troubleshooting

## 📌 Future Improvements

Possible future enhancements include:

* EtherChannel
* SSH remote management
* NAT/PAT
* ISP/Internet connectivity
* Additional campus routers
* More departments and end devices
* Network redundancy

## 👨‍💻 Author

**Veera**

BCA Cloud Computing Graduate | CCNA/Networking Learner

Interested in opportunities in Networking, NOC, IT Support and Cloud/Network roles.
