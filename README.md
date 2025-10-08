# 🔐 Secure Multi-Section Network Design
# -------------------------------------
# Final Project Report
# Author: Tom Maosa Mokua
# Course: Networking and Cyber Security
# Instructor: Mr. Albert Kiprop
# Institution: Eldohub Institute Academy
# Date: October 8, 2025
# -------------------------------------

project:
  name: "Secure Multi-Section Network Design"
  type: "Enterprise Network Security Implementation"
  date: "2025-10-08"

submitted_to:
  institution: "Eldohub Institute Academy"
  motto: "Preparing African youth to benefit from the opportunities the digital economy offers."

certificate_of_originality:
  statement: >
    I hereby declare that this project report is my original work and has not been submitted 
    previously for any other course or qualification. All sources of information have been 
    properly acknowledged and referenced.
  signed_by: "Tom Maosa Mokua"

acknowledgements:
  - name: "Ms. Magdaline Chepkemoi"
    role: "CEO, Eldohub Institute Academy"
    note: "For her vision and leadership in providing quality tech education."
  - name: "Mr. Albert Kiprop"
    role: "Instructor"
    note: "For his guidance and expertise in networking and security."
  - name: "My Family"
    note: "For their constant support and encouragement."

executive_summary:
  description: >
    Implementation of a secure, multi-section enterprise network with VLAN segmentation,
    OSPF dynamic routing, and layered security controls.
  achievements:
    - "Multi-VLAN Architecture (Management, Internal, Guest)"
    - "OSPF Dynamic Routing Between Three Routers"
    - "Port Security and Switch Hardening"
    - "ACL Enforcement for Traffic Policies"
    - "End-to-End Secure Connectivity"

network_implementation:
  vlans:
    - { id: 10, name: "Management", subnet: "192.168.10.0/24" }
    - { id: 20, name: "Internal", subnet: "192.168.110.0/24" }
    - { id: 30, name: "Guests", subnet: "192.168.210.0/24" }
    - { id: 99, name: "Native VLAN", subnet: "Trunking VLAN" }

security_features:
  - "Port Security with Sticky MAC Addresses"
  - "BPDU Guard & PortFast"
  - "DHCP Snooping"
  - "ACLs for Traffic Filtering"
  - "Inter-VLAN Routing with Security Policies"

verification_tests:
  VLAN_Segmentation: "✅ Passed"
  Port_Security: "✅ Passed"
  ACL_Enforcement: "✅ Passed"
  OSPF_Routing: "✅ Passed"
  End_to_End_Connectivity: "✅ Passed"

conclusion: >
  The Secure Multi-Section Network Design successfully meets enterprise-grade requirements,
  ensuring strong security, reliability, and efficient communication between VLANs.

author:
  name: "Tom Maosa Mokua"
  title: "Networking and Cyber Security Student"
  institution: "Eldohub Institute Academy"
  date: "October 8, 2025"
