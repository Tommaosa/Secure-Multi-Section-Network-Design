# Secure-Multi-Section-Network-Design
🛡️ Secure Multi-Section Network Design

Final Project Report
Submitted by: Tom Maosa Mokua
Course: Networking and Cyber Security
Instructor: Mr. Albert Kiprop
Institution: Eldohub Institute Academy
Date: October 8, 2025

📘 Overview

The Secure Multi-Section Network Design project implements a three-section enterprise network featuring VLAN segmentation, OSPF dynamic routing, and multi-layer security controls.
It demonstrates a complete, secure enterprise topology suitable for small to medium-sized businesses.

🧠 Key Features

✅ Multi-VLAN Architecture

VLAN 10 – Management (192.168.10.0/24)

VLAN 20 – Internal (192.168.110.0/24)

VLAN 30 – Guests (192.168.210.0/24)

VLAN 99 – Native VLAN (Trunk)

✅ OSPF Dynamic Routing between routers
✅ Access Control Lists (ACLs) for inter-VLAN security
✅ Port Security & Switch Hardening
✅ DHCP Snooping + BPDU Guard
✅ End-to-End Secure Connectivity

🧩 Network Topology
+---------------------+         +---------------------+         +---------------------+
|   Router R1         |---------|   Router R2         |---------|   Router R3         |
| VLAN 10, 99         |         | VLAN 20, 99         |         | VLAN 30, 99         |
+---------------------+         +---------------------+         +---------------------+
       |                            |                             |
    [Switch 1]                 [Switch 2]                   [Switch 3]
   (Mgmt VLAN)                (Internal VLAN)              (Guest VLAN)


(Replace this with your actual network diagram image if available)
Example:

![Network Topology](./topology-diagram.png)

⚙️ Cisco Configuration Samples
1️⃣ VLAN Configuration (Switch)
Switch(config)# vlan 10
Switch(config-vlan)# name Management
Switch(config)# vlan 20
Switch(config-vlan)# name Internal
Switch(config)# vlan 30
Switch(config-vlan)# name Guests
Switch(config)# vlan 99
Switch(config-vlan)# name Native
Switch(config)# interface range fa0/1 - 24
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 20

2️⃣ Trunk Configuration
Switch(config)# interface gig0/1
Switch(config-if)# switchport trunk encapsulation dot1q
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk native vlan 99
Switch(config-if)# switchport trunk allowed vlan 10,20,30,99

3️⃣ OSPF Configuration (Router)
Router(config)# router ospf 1
Router(config-router)# network 192.168.10.0 0.0.0.255 area 0
Router(config-router)# network 192.168.110.0 0.0.0.255 area 0
Router(config-router)# network 192.168.210.0 0.0.0.255 area 0
Router(config-router)# passive-interface default
Router(config-router)# no passive-interface g0/0
Router(config-router)# no passive-interface g0/1

4️⃣ ACL Example (Restrict Guest Access)
Router(config)# access-list 110 deny ip 192.168.210.0 0.0.0.255 192.168.10.0 0.0.0.255
Router(config)# access-list 110 permit ip any any
Router(config)# interface g0/1
Router(config-if)# ip access-group 110 in

5️⃣ Security Features
Switch(config)# interface range fa0/1 - 12
Switch(config-if-range)# switchport port-security
Switch(config-if-range)# switchport port-security maximum 2
Switch(config-if-range)# switchport port-security mac-address sticky
Switch(config-if-range)# switchport port-security violation restrict
Switch(config)# spanning-tree portfast default
Switch(config)# spanning-tree bpduguard enable
Switch(config)# ip dhcp snooping
Switch(config)# ip dhcp snooping vlan 10,20,30

🧾 Verification & Testing
Test	Result
VLAN Segmentation	✅ Working
Port Security	✅ Working
ACL Enforcement	✅ Working
OSPF Routing	✅ Working
End-to-End Connectivity	✅ Working
🏁 Conclusion

The Secure Multi-Section Network Design achieves robust enterprise-level security with segmented VLANs, secure routing, and traffic control mechanisms.
This project demonstrates deep understanding of network security principles and practical Cisco IOS configuration for real-world deployments.

🙏 Acknowledgements

Ms. Magdaline Chepkemoi, CEO – for visionary leadership

Mr. Albert Kiprop, Instructor – for expert mentorship

My Family – for endless support and encouragement

🧾 Certificate of Originality

I, Tom Maosa Mokua, declare that this project is my original work and has not been submitted previously for any other qualification. All sources have been properly cited.

🏫 Institution

Eldohub Institute Academy

Preparing African youth to benefit from the opportunities the digital economy offers.
