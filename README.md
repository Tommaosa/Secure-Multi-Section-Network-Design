

<h1>🛡️ Secure Multi-Section Network Design</h1>

<h3>Final Project Report</h3>
<p><b>Submitted by:</b> Tom Maosa Mokua<br>
<b>Course:</b> Networking and Cyber Security<br>
<b>Instructor:</b> Mr. Albert Kiprop<br>
<b>Institution:</b> Eldohub Institute Academy<br>
<b>Date:</b> October 8, 2025</p>

<hr>

<h2>📘 Overview</h2>
<p>
The <b>Secure Multi-Section Network Design</b> project implements a three-section enterprise network featuring
<b>VLAN segmentation</b>, <b>OSPF dynamic routing</b>, and <b>multi-layer security controls</b>.
It demonstrates a complete, secure enterprise topology suitable for small to medium-sized businesses.
</p>

<hr>

<h2>🧠 Key Features</h2>

<p>✅ <b>Multi-VLAN Architecture</b></p>
<table>
  <tr><th>VLAN</th><th>Purpose</th><th>Network</th></tr>
  <tr><td>10</td><td>Management</td><td>192.168.10.0/24</td></tr>
  <tr><td>20</td><td>Internal</td><td>192.168.110.0/24</td></tr>
  <tr><td>30</td><td>Guests</td><td>192.168.210.0/24</td></tr>
  <tr><td>99</td><td>Native VLAN</td><td>Trunk</td></tr>
</table>

<p>✅ <b>OSPF Dynamic Routing</b> between routers<br>
✅ <b>Access Control Lists (ACLs)</b> for inter-VLAN security<br>
✅ <b>Port Security</b> & Switch Hardening<br>
✅ <b>DHCP Snooping</b> + <b>BPDU Guard</b><br>
✅ <b>End-to-End Secure Connectivity</b></p>

<hr>

<h2>🧩 Network Topology</h2>
<pre>
+---------------------+         +---------------------+         +---------------------+
|   Router R1         |---------|   Router R2         |---------|   Router R3         |
| VLAN 10, 99         |         | VLAN 20, 99         |         | VLAN 30, 99         |
+---------------------+         +---------------------+         +---------------------+
       |                            |                             |
    [Switch 1]                 [Switch 2]                   [Switch 3]
   (Mgmt VLAN)                (Internal VLAN)              (Guest VLAN)
</pre>
<p><i>(Replace this diagram with your actual network image if available)</i></p>
<p><b>Example:</b><br>
<img src="https://raw.githubusercontent.com/Tommaosa/Secure-Multi-Section-Network-Design/894254aaea1fd454b8746fffde24c1fbff9402f4/secure%20network.png" width="700">
</p>

<hr>

<h2>⚙️ Cisco Configuration Samples</h2>

<h3>1️⃣ VLAN Configuration (Switch)</h3>
<pre>
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
</pre>

<h3>2️⃣ Trunk Configuration</h3>
<pre>
Switch(config)# interface gig0/1
Switch(config-if)# switchport trunk encapsulation dot1q
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk native vlan 99
Switch(config-if)# switchport trunk allowed vlan 10,20,30,99
</pre>

<h3>3️⃣ OSPF Configuration (Router)</h3>
<pre>
Router(config)# router ospf 1
Router(config-router)# network 192.168.10.0 0.0.0.255 area 0
Router(config-router)# network 192.168.110.0 0.0.0.255 area 0
Router(config-router)# network 192.168.210.0 0.0.0.255 area 0
Router(config-router)# passive-interface default
Router(config-router)# no passive-interface g0/0
Router(config-router)# no passive-interface g0/1
</pre>

<h3>4️⃣ ACL Example (Restrict Guest Access)</h3>
<pre>
Router(config)# access-list 110 deny ip 192.168.210.0 0.0.0.255 192.168.10.0 0.0.0.255
Router(config)# access-list 110 permit ip any any
Router(config)# interface g0/1
Router(config-if)# ip access-group 110 in
</pre>

<h3>5️⃣ Security Features</h3>
<pre>
Switch(config)# interface range fa0/1 - 12
Switch(config-if-range)# switchport port-security
Switch(config-if-range)# switchport port-security maximum 2
Switch(config-if-range)# switchport port-security mac-address sticky
Switch(config-if-range)# switchport port-security violation restrict
Switch(config)# spanning-tree portfast default
Switch(config)# spanning-tree bpduguard enable
Switch(config)# ip dhcp snooping
Switch(config)# ip dhcp snooping vlan 10,20,30
</pre>

<hr>

<h2>🧾 Verification & Testing</h2>

<table>
  <tr><th>Test</th><th>Result</th></tr>
  <tr><td>VLAN Segmentation</td><td>✅ Working</td></tr>
  <tr><td>Port Security</td><td>✅ Working</td></tr>
  <tr><td>ACL Enforcement</td><td>✅ Working</td></tr>
  <tr><td>OSPF Routing</td><td>✅ Working</td></tr>
  <tr><td>End-to-End Connectivity</td><td>✅ Working</td></tr>
</table>

<hr>

<h2>🏁 Conclusion</h2>
<p>
The <b>Secure Multi-Section Network Design</b> achieves robust enterprise-level security with segmented VLANs,
secure routing, and traffic control mechanisms.
This project demonstrates deep understanding of <b>network security principles</b> and practical <b>Cisco IOS configuration</b>
for real-world deployments.
</p>

<hr>

<h2>🙏 Acknowledgements</h2>
<ul>
  <li><b>Ms. Magdaline Chepkemoi</b>, CEO → For visionary leadership</li>
  <li><b>Mr. Albert Kiprop</b>, Instructor → For expert mentorship</li>
  <li><b>My Family</b> → For endless support and encouragement</li>
</ul>

<hr>

<h2>🧾 Certificate of Originality</h2>
<blockquote>
I, <b>Tom Maosa Mokua</b>, declare that this project is my original work and has not been submitted previously
for any other qualification. All sources have been properly cited.
</blockquote>

<hr>

<h2>🏫 Institution</h2>
<p><b>Eldohub Institute Academy</b><br>
<i>Preparing African youth to benefit from the opportunities the digital economy offers.</i></p>

</body>
</html>
