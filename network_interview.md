# 🔧 Technical Networking Questions

## Q1: What is the difference between Layer 2 and Layer 3 switches?

A:

Layer 2 switches operate at the data link layer and switch frames based on MAC addresses. They are used for VLAN segmentation and intra-network communication. Layer 3 switches operate at the network layer and route packets based on IP addresses, allowing inter-VLAN communication and routing between different subnets.

## Q2: What is VLAN and why is it used in data centers?

A:

VLAN (Virtual LAN) logically segments a network into different broadcast domains within the same physical switch. It improves security, reduces broadcast traffic, and simplifies network management in data centers by isolating traffic.

## Q3: How does STP (Spanning Tree Protocol) work and why is it important?

A:

STP prevents loops in a Layer 2 network by blocking redundant paths. It elects a root bridge and determines the shortest path from all switches to the root bridge, blocking others. In data centers, it maintains network stability and prevents broadcast storms.

🔌 Infrastructure / Data Center Specific

## Q4: Explain the basic components of a data center network

A:

Core Layer: High-speed backbone, connects distribution layer devices.

Distribution Layer: Aggregates data from access layer and applies policies.

Access Layer: Connects end devices like servers and storage.

Other: Load balancers, firewalls, cabling (fiber/copper), PDUs, and cooling systems.

## Q5: What is VTP and how does it work?

A:

VTP (VLAN Trunking Protocol) allows switches to share VLAN information to maintain consistency across the network. It operates in Server, Client, and Transparent modes. Only server-mode switches can create and modify VLANs.

🛠 Troubleshooting / Real-world Scenarios

## Q6: A server in VLAN 10 cannot reach a server in VLAN 20. What will you check?

A:

Check VLAN configuration on the switch.

Ensure both VLANs exist and are assigned correctly to ports.

Verify trunk ports allow VLAN 10 and 20.

Confirm inter-VLAN routing is enabled on a Layer 3 device.

Ping the gateway IPs for both VLANs.

Check ACLs/firewall rules between VLANs.

## Q7: A user is complaining of intermittent connection to a server. How do you approach it?

A:

Check physical connectivity (cables, ports, LEDs).

Verify switch port statistics for errors or drops.

Use ping and traceroute to diagnose path issues.

Check switch logs and server NIC settings.

Review spanning-tree state for flapping or blocked ports.

🧠 Behavioral / Situational Questions

## Q8: Describe a time you resolved a critical network issue in a data center

A: (Tailor this to your experience)

Example: During a sudden network outage, I identified a failed core switch module. I coordinated with the team to reroute traffic through redundant paths and brought services back within 30 minutes. Post-resolution, I worked on improving our monitoring and failover mechanisms.

## Q9: How do you handle working under pressure during a P1 incident?

A:

I stay calm and follow the incident response process—start with isolation, root cause analysis, and communication. I prioritize critical services and keep stakeholders informed. After resolution, I participate in post-mortem reviews to prevent recurrence.

🔐 Security-Related Networking

## Q10: How do you secure a Layer 2 network in a data center?

A:

Enable Port Security

Use BPDU Guard, Root Guard

Implement Private VLANs

Disable unused ports and use DHCP snooping, Dynamic ARP Inspection (DAI)

Secure management access (SSH, RADIUS/TACACS+)
