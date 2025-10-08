# 🧠 Secure Multi-Section Network Design
**Final Project Report — Networking & Cyber Security**

───────────────────────────────────────────────
Author : Tom Maosa Mokua
Instructor : Mr. Albert Kiprop
Institution : Eldohub Institute Academy
Date : October 8, 2025
───────────────────────────────────────────────

shell
Copy code

## 📜 Project Summary
A secure enterprise network segmented into three functional sections:
→ VLAN 10: Management (192.168.10.0/24)
→ VLAN 20: Internal (192.168.110.0/24)
→ VLAN 30: Guests (192.168.210.0/24)
→ VLAN 99: Native VLAN for trunking

Implements:
• OSPF Dynamic Routing
• Port Security with Sticky MAC
• ACL Traffic Filtering
• DHCP Snooping & BPDU Guard
• Inter-VLAN Security Policies

shell
Copy code

## 🧩 Network Verification Tests
[✔] VLAN Segmentation ........... PASSED
[✔] Port Security ............... PASSED
[✔] ACL Enforcement ............. PASSED
[✔] OSPF Routing ................ PASSED
[✔] End-to-End Connectivity ..... PASSED

shell
Copy code

## ⚙️ Network Overview
+-----------------------+ +-----------------------+ +-----------------------+
| VLAN 10 - Management | ---> | VLAN 20 - Internal | ---> | VLAN 30 - Guests |
| Subnet: 192.168.10.0 | | Subnet: 192.168.110.0 | | Subnet: 192.168.210.0 |
+-----------------------+ +-----------------------+ +-----------------------+
| | |
+------------ OSPF Dynamic Routing Enabled ---------------+

shell
Copy code

## 🔐 Security Highlights
Port Security ........... Sticky MAC, single host per port

DHCP Snooping ........... Enabled on all access ports

BPDU Guard .............. Active

ACLs .................... Filtering inter-VLAN traffic

Switch Hardening ........ Default VLANs removed, unused ports disabled

shell
Copy code

## 🧾 Certificate of Originality
"I hereby declare that this project report is my original work and has not been submitted
previously for any other course or qualification. All sources of information have been
properly acknowledged and referenced."

Signed,
Tom Maosa Mokua

shell
Copy code

## 🙏 Acknowledgements
• Ms. Magdaline Chepkemoi — CEO, Eldohub Institute Academy
→ For her vision and leadership in providing quality tech education.

• Mr. Albert Kiprop — Instructor
→ For his guidance and expertise in networking and security.

• My Family
→ For their continuous support and encouragement.

shell
Copy code

## 🧠 Conclusion
The Secure Multi-Section Network Design successfully meets enterprise requirements,
providing robust segmentation, routing efficiency, and layered security policies.

This project demonstrates practical application of advanced networking principles
for real-world secure enterprise environments.

yaml
Copy code

---

**👨🏽‍💻 Author:** *Tom Maosa Mokua*  
**🏫 Institution:** *Eldohub Institute Academy*  
**📅 Date:** *October 8, 2025*  
**🔒 Course:** *Networking and Cyber Security*

