# Secure-Multi-Section-Network-Design
Secure Multi-Section Network Design - Final Project Report
Submitted By: Tom Maosa Mokua
Course: Networking and Cyber Security
Instructor: Mr. Albert Kiprop
Institution: Eldohub Institute Academy
Date: October 8, 2025

Project Submitted to:
Eldohub Institute Academy
Preparing African youth to benefit from the opportunities the digital economy offers.

Certificate of Originality
I hereby declare that this project report is my original work and has not been submitted previously for any other course or qualification. All sources of information have been properly acknowledged and referenced.

Tom Maosa Mokua

Acknowledgements
I wish to express my sincere gratitude to the following for their support throughout this project:

Ms. Magdaline Chepkemoi, CEO of Eldohub Institute Academy, for her vision and leadership in providing quality tech education.

Mr. Albert Kiprop, my instructor, for his guidance and expertise in networking and security.

My family for their constant support and encouragement.

Thank you all for contributing to my learning journey.

Executive Summary
This project successfully implements a secure three-section enterprise network with comprehensive security controls. The network features VLAN segmentation, OSPF dynamic routing, and advanced security policies using access control lists. All verification tests confirm the network operates as designed, providing secure segmentation while maintaining necessary communication paths.

Key Achievements:
✅ Multi-VLAN architecture (Management, Internal, Guests)

✅ OSPF dynamic routing between three routers

✅ Port security and switch hardening

✅ ACL enforcement for traffic policies

✅ End-to-end connectivity with security controls

Network Implementation
VLAN Configuration
VLAN 10: Management (192.168.10.0/24)

VLAN 20: Internal (192.168.110.0/24)

VLAN 30: Guests (192.168.210.0/24)

VLAN 99: Native VLAN for trunking

Security Features Implemented
Port Security with sticky MAC addresses

BPDU Guard & PortFast

DHCP Snooping

ACLs for traffic filtering

Inter-VLAN routing with security policies

Verification Tests Completed
VLAN Segmentation - ✓ Working

Port Security - ✓ Working

ACL Enforcement - ✓ Working

OSPF Routing - ✓ Working

End-to-End Connectivity - ✓ Working

Conclusion
This secure multi-section network design successfully meets all enterprise requirements, demonstrating robust security controls and reliable connectivity. The implementation showcases practical application of advanced networking concepts suitable for real-world deployment.

Tom Maosa Mokua
October 8, 2025

