RCOMP 2023-2024 Project - Sprint 3 planning
===========================================

On the current document we can find the following elements:
- Sprint Backlog
- Technical Decisions and Coordination
    - Cisco Packet Tracer Version 
    - Devices Naming
    - OSPF Area Ids
    - Voip Prefixes
    - DNS server specifications
      - Dns Building root Domain 
      - Dns Servers Naming
    - New Ipv4 Addressing
    - Static Firewall (ACLs)
- Relevant Models to Follow
    - Telephone
    - Switch
    - Router

**Sprint master:** Bernardo Barbosa - 1220741

# 1. Sprint's backlog #
Considering the previous sprint, the team is now required continue working on the regarding building in order to adapt the **static routing** into a **dynamic routing.**
For this process, the OSPF(Open shortest path first) will be the protocol used.
# Task Descriptions

| Task  | Task description                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T.3.1 | Update the building1.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 1.                                                                                                    |
| T.3.2 | Update the building2.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 2. Final integration of each member’s Packet Tracer simulation into a single simulation (campus.pkt). |
| T.3.3 | Update the building3.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 3.                                                                                                    |
| T.3.4 | Update the building4.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 4.                                                                                                    |


# 2. Technical decisions and coordination #
In this section, all technical decisions taken in the planning meeting are to be mentioned.


**Cisco Packet Tracer Version:** V 8.2.2


### 2.1 Devices Naming


The team followed the same conventions and devices naming rules as defined on the last sprint on the devices Naming Section in [planning.md](../sprint2/planning.md).
However, regarding the situation of having two servers,only these two new rules were to be applied:

*DNS and HTTP Servers*

- **DNS Servers**: `Server<number>_<B>Dns`  
  Example: `Server1_dns` for Building 1
- **HTTP Servers**: `Server<number>_<B>http`  
  Example: `Server1_http` for Building 1

### 2.2 OSPF Area Ids

| Building   | ID  |
|------------|-----|
| Backbone   | 0   |
| Building 1 | 1   |
| Building 2 | 2   |
| Building 3 | 3   |
| Building 4 | 4   |

### 2.3 Voip prefixes

| Building   | Prefix | Numbers       |
|------------|--------|---------------|
| Building 1 | 1...   | 1000 and 1001 |
| Building 2 | 2...   | 2000 and 2001 |
| Building 3 | 3...   | 3000 and 3001 |
| Building 4 | 4...   | 4000 and 4001 |


## 2.4.DNS server specifications

### 2.4.1 - Dns Building root Domain

-	The highest level DNS domain will be part of Building 1, naming **rcomp-23-24-dj-g2**.
     It will be used as if it was the DNS root domain.

-	The other DNS domains will be created locally in each building, naming **building-X.rcomp-23-24-dj-g2**.
     The letter *X* will identify the building's number.

### 2.4.2 - Dns Servers Naming
-	The other DNS domains will be created locally in each building, naming **building-X.rcomp-23-24-dj-g2**.
     The letter *X* will identify the building's number.

-	In each building, all DNS servers will have the unqualified DNA name as **ns**.
     While Building 1 will have **ns.rcomp-23-24-dj-g2**, the others will have **ns.building-X.rcomp-23-24-dj-g2**.

-	The **IPv4 node address** for each DNS name server are:
    - **Building 1 - ns.rcomp-23-24-dj-g2**


## 2.5 - New Ipv4 Addressing:
For the project, the DHCPv4 services were struggling to configure some subinterfaces. In response to the issue, the team decided to change the IP address range for certain VLANs.

However, the IP new addressing still assures the minimum number of nodes required for each VLAN as determined in Sprint 2:


| VLANID | VLAN Name     | Default gateway | Mask             | Network address |
|--------|---------------|-----------------|------------------|-----------------|
| 410    | backbone      | 172.25.0.1      | 255.255.255.0    | 172.25.0.0      |
| 405    | 1_groundFloor | 172.25.1.1      | 255.255.255.128  | 172.25.1.0      |
| 406    | 1_floorOne    | 172.25.1.129    | 255.255.255.128  | 172.25.1.128    |
| 407    | 1_wifi        | 172.25.2.1      | 255.255.255.128  | 172.25.2.0      |
| 408    | 1_dmz         | 172.25.2.129    | 255.255.255.128  | 172.25.2.128    |
| 409    | 1_voip        | 172.25.3.1      | 255.255.255.128  | 172.25.3.0      |
| 411    | 2_groundFloor | 172.25.4.1      | 255.255.255.128  | 172.25.4.0      |
| 412    | 2_floorOne    | 172.25.4.129    | 255.255.255.128  | 172.25.4.128    |
| 413    | 2_wifi        | 172.25.5.1      | 255.255.255.0    | 172.25.5.0      |
| 414    | 2_dmz         | 172.25.6.1      | 255.255.255.128  | 172.25.6.0      |
| 415    | 2_voip        | 172.25.6.129    | 255.255.255.128  | 172.25.6.128    |
| 416    | 3_groundFloor | 172.25.8.1      | 255.255.255.128  | 172.25.8.0      |
| 417    | 3_floorOne    | 172.25.8.129    | 255.255.255.128  | 172.25.8.128    |
| 418    | 3_wifi        | 172.25.9.1      | 255.255.255.0    | 172.25.9.0      |
| 419    | 3_dmz         | 172.25.10.1     | 255.255.255.128  | 172.25.10.0     |
| 420    | 3_voip        | 172.25.10.129   | 255.255.255.128  | 172.25.10.128   |
| 421    | 4_groundFloor | 172.25.12.1     | 255.255.255.128  | 172.25.12.0     |
| 422    | 4_floorOne    | 172.25.12.129   | 255.255.255.128  | 172.25.12.128   |
| 423    | 4_wifi        | 172.25.13.1     | 255.255.255.0    | 172.25.13.0     |
| 424    | 4_dmz         | 172.25.14.1     | 255.255.255.128  | 172.25.14.0     |
| 425    | 4_voip        | 172.25.14.129   | 255.255.255.128  | 172.25.14.128   |



## 2.6 - Subtasks assignment

| Sprint Master | Task  |
|---------------|-------|
| 1190378       | T.3.1 |
| 1211895       | T.3.2 |
| 1220672       | T.3.3 |
| 1220741       | T.3.4 |


**Note:** The team member with building 2 is responsible for putting together all members work into a single Packet Tracer simulation all the simulations created by each team member.
However,he only exports config files of its own building (2).


## 2.7- Static Firewall (ACLs)

Our team configured the access lists for the following VLANs:

| VLAN         | Access List |
|--------------|-------------|
| Backbone     | 100         |
| Ground Floor | 101         |
| Floor One    | 102         |
| WiFi         | 103         |
| DMZ          | 104         |
| VoIP         | 105         |

**Note:** The VLAN number is not relevant, so each building uses these access list numbers uniformly, ensuring consistency across all locations.


## 3- Relevant Network Models to Follow

Telephone module :**7960**

Router module:**2811** 

Swtich module: **PT-Empty**