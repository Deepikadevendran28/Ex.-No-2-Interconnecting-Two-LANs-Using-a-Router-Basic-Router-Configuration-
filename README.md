# Date :
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram

<img width="1359" height="729" alt="Screenshot 2026-10-22 160807" src="https://github.com/user-attachments/assets/67f4657f-c69b-4fa0-b0e7-3e9333becf85" />



 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)

<img width="1359" height="729" alt="Screenshot 2026-10-22 155835" src="https://github.com/user-attachments/assets/aed1f937-641b-4415-b1ba-5b391ca9535d" />

<img width="1359" height="729" alt="Screenshot 2026-10-22 155843" src="https://github.com/user-attachments/assets/e83e055c-674c-434c-968e-8b4a0cd44bd1" />

<img width="1359" height="729" alt="Screenshot 2026-10-22 155847" src="https://github.com/user-attachments/assets/8c76e8d4-3cc3-4443-8859-0f345f960f61" />

<img width="1359" height="729" alt="Screenshot 2026-10-22 155852" src="https://github.com/user-attachments/assets/d1d28e8e-c355-48a0-beb1-18f21482825c" />

<img width="1359" height="729" alt="Screenshot 2026-10-22 155856" src="https://github.com/user-attachments/assets/eafe5d78-8697-412a-9ecf-c5e6243a6e30" />

<img width="1359" height="729" alt="Screenshot 2026-10-22 155106" src="https://github.com/user-attachments/assets/b80807e9-57aa-49fe-8d2f-5cc2c70e1ba6" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

