# RCOMP 2023-2024 Project - Sprint 2 planning


On the current document we can find the following elements:
- Sprint Backlog
- Technical Decisions and Coordination
    - Packet Tracer Version 
    - Devices naming
    - VTP Domain Name
    - VTP DataBase
    - Free Vlans
    - IPV4 Address
    - IPV4 Network
    - ISP Address
- Subtasks Assignement
- Relevant Models to Follow
  - Telephone
  - Switch
  - Router


**Sprint master:** Bernardo Barbosa - 1220741

## 1. **Sprint's backlog**

| Task   | Task description                                                                                                                                                                                         |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T.2.1  | Development of a layer two and layer three Packet Tracer simulation for building 1, encompassing the campus backbone. Integration of every member’s Packet Tracer simulation into a single simulation.   |
| T.2.2  | Development of a layer two and layer three Packet Tracer simulation for building 2, encompassing the campus backbone.                                                                                    |
| T.2.3  | Development of a layer two and layer three Packet Tracer simulation for building 3, encompassing the campus backbone.                                                                                    | 
| T.2.4  | Development of a layer two and layer three Packet Tracer simulation for building 4, encompassing the campus backbone.                                                                                    |
                                                                           |

## 2. **Technical decisions and coordination**

- **Packet Tracer Version:** V 8.2.1

## Conventions

- The name of the complete file should be `campus.pkt`.
- There should be a file for each building.
- Each building file should be named `buildingN.pkt`", where **N** means the letter of the building.

**Devices naming**



**Access-Point:** `[AP][Access Point Number][AP Number]_Prefix_Room Number` (Example: `AP1_1.0.1`)

**MC:** `[MC][Example: MC1]`

**IC:** `[IC]_[Building]Prefix_Room Number` (Example: `IC_Building4`)

**HC:** `[HC]Horizontal Cross-Connect numbers` (Example:`HC_1.0.1`)

**Routers:** `[R][Router Number]/[B]Router/[Building][Building Number]` (Example: `Router_Building4`)

**Switches:** `[Cross Connect Type][Switch Number]_[B]Prefix_Room Number` (Example: `CP1_1.0.1`)

**PCs or Laptops:** `PC[Laptop Number]` (Example: `PC1_1.04`)

**IP-phones:** `IP[phone number]_[B]Prefix_Room Number` (Example: `ipPhone1_1.0.1`)


**The Server** does not have a predefined rule , however, therefore only to be one , a suggestion  Name  could be **(Server_Building4)** for building 4 server.


**VTP domain name**

- **r2324djg2**



**VLAN database**

- Range of VLAN IDs used: **404 - 425**

| Vlan Id | Vlan Name     |
|---------|---------------|
| 404     | default       |
|         |               |
| 405     | 1_groundFloor |
| 406     | 1_floorOne    |
| 407     | 1_wifi        |
| 408     | 1_dmz         |
| 409     | 1_voip        |
|         |               |
| 411     | 2_groundFloor |
| 412     | 2_floorOne    |
| 413     | 2_wifi        |
| 414     | 2_dmz         |
| 415     | 2_voip        |
|         |               |
| 416     | 3_groundFloor |
| 417     | 3_floorOne    |
| 418     | 3_wifi        |
| 419     | 3_dmz         |
| 420     | 3_voip        |
|         |               |
| 421     | 4_groundFloor |
| 422     | 4_floorOne    |
| 423     | 4_wifi        |
| 424     | 4_dmz         |
| 425     | 4_voip        |



**Free VLANS:**

| Vlan Id |
|---------|
| 410     |

**IPv4 address**

| IP Address | Subnet Mask |
|------------|-------------|
| 172.25.0.0 | /20         |

**IPv4 network**

| Building | Nodes | Network address | Broadcast address | Address range                                         | VLAN range |
|----------|-------|-----------------|-------------------|-------------------------------------------------------|------------|
| BackBone | 200   | 172.25.2.0/24   | 172.25.2.255      | 172.25.2.0                                            | 404        |
| 1        | 347   | 172.25.0.0/22   | 172.25.3.255      | 172.25.0.1 - 172.25.3.254 (exlcuding backbone adress) | 405 - 409  |
| 2        | 590   | 172.25.4.0/22   | 172.25.7.255      | 172.25.4.1 - 172.25.7.254                             | 411 - 415  |
| 3        | 665   | 172.25.8.0/22   | 172.25.11.255     | 172.25.8.1 - 172.25.11.254                            | 416 - 420  |
| 4        | 670   | 172.25.12.0/22  | 172.25.15.255     | 172.25.12.1 - 172.25.15.254                           | 421 - 425  |



**ISP address**

| IP Address | Subnet Mask |
|------------|-------------|
| 5.60.38.38 | /30         |

## 3 - Subtasks assignment

| Sprint Master | Task  |
|---------------|-------|
| 1190378       | T.2.1 |
| 1211895       | T.2.2 |
| 1220672       | T.2.3 |
| 1220741       | T.2.4 |


**Note:** The team member with building 2 is responsible for putting together into a single Packet Tracer simulation all the simulations created by each team member. 

## 4- Relevant Network Models to follow:

Telephone module :**7960**
Switch Module: **PT-Empty**
Router module:**2811** 










