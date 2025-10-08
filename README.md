<!-- Paste this into your README.md -->
<div style="max-width:900px; margin:12px auto; font-family: 'Courier New', monospace; line-height:1.25;">

  <!-- Header (fixed layout) -->
  <div style="border-top:2px solid #444; border-bottom:2px solid #444; padding:10px 8px; margin-bottom:12px;">
    <table style="width:100%; border-collapse:collapse; font-size:14px;">
      <tr>
        <td style="width:25%;"><strong>Author</strong><br>Tom Maosa Mokua</td>
        <td style="width:25%;"><strong>Instructor</strong><br>Mr. Albert Kiprop</td>
        <td style="width:30%;"><strong>Institution</strong><br>Eldohub Institute Academy</td>
        <td style="width:20%; text-align:right;"><strong>Date</strong><br>October 8, 2025</td>
      </tr>
    </table>
  </div>

  <!-- Project Summary (preserved spacing) -->
  <div style="margin-bottom:12px;">
    <h3 style="margin:6px 0;">📜 Project Summary</h3>
    <pre style="background:#0f172a10; padding:10px; border-radius:6px; white-space:pre; font-size:13px; margin:6px 0;">
A secure enterprise network segmented into three functional sections:

  → VLAN 10: Management    (192.168.10.0/24)
  → VLAN 20: Internal      (192.168.110.0/24)
  → VLAN 30: Guests        (192.168.210.0/24)
  → VLAN 99: Native VLAN   (Trunking)

Implements:
  • OSPF Dynamic Routing
  • Port Security (Sticky MAC)
  • ACL Traffic Filtering
  • DHCP Snooping & BPDU Guard
  • Inter-VLAN Security Policies
    </pre>
  </div>

  <!-- Verification Tests (stable table) -->
  <div style="margin-bottom:12px;">
    <h3 style="margin:6px 0;">🧩 Network Verification Tests</h3>
    <table style="width:100%; border-collapse:collapse; font-size:13px;">
      <tr><td style="padding:6px 8px; border-bottom:1px dashed #ddd;">VLAN Segmentation</td><td style="padding:6px 8px; text-align:right;">✅ PASSED</td></tr>
      <tr><td style="padding:6px 8px; border-bottom:1px dashed #ddd;">Port Security</td><td style="padding:6px 8px; text-align:right;">✅ PASSED</td></tr>
      <tr><td style="padding:6px 8px; border-bottom:1px dashed #ddd;">ACL Enforcement</td><td style="padding:6px 8px; text-align:right;">✅ PASSED</td></tr>
      <tr><td style="padding:6px 8px; border-bottom:1px dashed #ddd;">OSPF Routing</td><td style="padding:6px 8px; text-align:right;">✅ PASSED</td></tr>
      <tr><td style="padding:6px 8px;">End-to-End Connectivity</td><td style="padding:6px 8px; text-align:right;">✅ PASSED</td></tr>
    </table>
  </div>

  <!-- Network overview (stable ASCII-like layout using table) -->
  <div style="margin-bottom:18px;">
    <h3 style="margin:6px 0;">⚙️ Network Overview</h3>
    <table style="width:100%; border-collapse:collapse; font-size:13px; text-align:center;">
      <tr>
        <td style="width:34%; padding:10px; background:#f6f8fa; border-radius:6px;">
          <strong>VLAN 10</strong><br>Management<br><small>192.168.10.0/24</small>
        </td>
        <td style="width:32%; padding:8px; font-size:20px;">➡️ &#8203;OSPF&#8203; ➡️</td>
        <td style="width:34%; padding:10px; background:#f6f8fa; border-radius:6px;">
          <strong>VLAN 20</strong><br>Internal<br><small>192.168.110.0/24</small>
        </td>
      </tr>
      <tr style="height:8px;"><td colspan="3"></td></tr>
      <tr>
        <td style="border-top:1px dashed #eee; padding:8px;">(Mgmt switches)</td>
        <td style="border-top:1px dashed #eee; padding:8px;">(OSPF backbone)</td>
        <td style="border-top:1px dashed #eee; padding:8px;">(Internal switches)</td>
      </tr>
      <tr style="height:12px;"><td colspan="3"></td></tr>
      <tr>
        <td colspan="3" style="padding:10px; background:#fffbe6; border-radius:6px;">
          <strong>Guest VLAN</strong> - VLAN 30 : 192.168.210.0/24 (isolated; controlled by ACLs)
        </td>
      </tr>
    </table>
  </div>

</div>

## 🔐 Security Highlights
Port Security ........... Sticky MAC, single host per port

DHCP Snooping ........... Enabled on all access ports

BPDU Guard .............. Active

ACLs .................... Filtering inter-VLAN traffic

Switch Hardening ........ Default VLANs removed, unused ports disabled


## 🧾 Certificate of Originality
"I hereby declare that this project report is my original work and has not been submitted
previously for any other course or qualification. All sources of information have been
properly acknowledged and referenced."

Signed,
Tom Maosa Mokua


## 🙏 Acknowledgements
• Ms. Magdaline Chepkemoi — CEO, Eldohub Institute Academy
→ For her vision and leadership in providing quality tech education.

• Mr. Albert Kiprop — Instructor
→ For his guidance and expertise in networking and security.

• My Family
→ For their continuous support and encouragement.

## 🧠 Conclusion
The Secure Multi-Section Network Design successfully meets enterprise requirements,
providing robust segmentation, routing efficiency, and layered security policies.

This project demonstrates practical application of advanced networking principles
for real-world secure enterprise environments.
---

**👨🏽‍💻 Author:** *Tom Maosa Mokua*  
**🏫 Institution:** *Eldohub Institute Academy*  
**📅 Date:** *October 8, 2025*  
**🔒 Course:** *Networking and Cyber Security*

