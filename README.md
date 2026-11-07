Simple VLAN Configuration Using Cisco Packet Tracer

📌 Project Overview

This project demonstrates the configuration of Virtual Local Area Networks (VLANs) on a Cisco Layer 2 switch using Cisco Packet Tracer.
The main objective is to divide a single physical network into multiple logical networks using VLANs. This improves network segmentation, security, and traffic management.
Four VLANs are created to separate Students, Faculty, Management, and unused switch ports.

🎯 Project Objectives

•	Create and configure multiple VLANs.
•	Assign switch ports to specific VLANs.
•	Configure access ports on a Cisco switch.
•	Assign IP addresses to end devices.
•	Configure a management VLAN interface.
•	Disable unused switch ports.
•	Verify VLAN configuration using Cisco IOS commands.

🖥️ Network Devices Used

•	1 × Cisco 2960 Switch (S1)
•	6 × End Devices (PCs)
•	Cisco Packet Tracer

🌐 VLAN Configuration

VLAN ID	VLAN Name	Assigned Ports	Network
10	Students	Fa0/1–Fa0/8	192.168.10.0/24
20	Faculty	Fa0/9–Fa0/16	192.168.20.0/24
30	Management	Fa0/17–Fa0/24	192.168.30.0/24
40	Unused	Gi0/1–Gi0/2	Not assigned

⚙️ Switch Configuration

1. Basic Switch Configuration
enable
configure terminal
hostname S1
2. Create VLANs
vlan 10
name Students

vlan 20
name Faculty

vlan 30
name Management

vlan 40
name Unused

end

3. Verify VLANs
show vlan brief

5. Assign Access Ports to VLANs
   
Students VLAN – VLAN 10
configure terminal
interface range fa0/1-8
switchport mode access
switchport access vlan 10
Faculty VLAN – VLAN 20
interface range fa0/9-16
switchport mode access
switchport access vlan 20
Management VLAN – VLAN 30
interface range fa0/17-24
switchport mode access
switchport access vlan 30
Unused Ports – VLAN 40
interface range g0/1-2
switchport mode access
switchport access vlan 40
shutdown
end

7. Verify Interface Status
show interfaces status

9. Configure Management VLAN Interface
configure terminal

interface vlan 30
ip address 192.168.30.254 255.255.255.0
no shutdown
end

💻 IP Address Configuration

Assign the following static IP addresses to the end devices.
Device	VLAN	IPv4 Address	Subnet Mask
Student1	10	192.168.10.10	255.255.255.0
Student2	10	192.168.10.11	255.255.255.0
Faculty1	20	192.168.20.10	255.255.255.0
Faculty2	20	192.168.20.11	255.255.255.0
Management1	30	192.168.30.10	255.255.255.0
Management2	30	192.168.30.11	255.255.255.0

🔍 Verification Commands

Use the following Cisco IOS commands to verify the configuration.
show vlan brief
show interfaces status
show ip interface brief
show running-config

📚 Key Learning Outcomes

Through this project, I learned:
•	How to create and configure VLANs.
•	How to assign switch ports to different VLANs.
•	How to configure access mode on switch interfaces.
•	How to configure a Switch Virtual Interface (SVI).
•	How to assign static IP addresses to end devices.
•	How to disable unused switch ports.
•	How to verify VLAN and interface configurations.

🛠️ Technologies Used

•	Cisco Packet Tracer
•	Cisco IOS CLI
•	VLAN Configuration
•	IPv4 Addressing
•	Layer 2 Switching

👨‍💻 Project Conclusion

This project demonstrates the fundamentals of VLAN configuration and network segmentation using a Cisco switch. It provides practical experience with Cisco IOS commands, port assignments, IP addressing, and basic network administration.
This project is part of my learning journey toward an entry-level Computer Networking / Network Support Engineer role.

