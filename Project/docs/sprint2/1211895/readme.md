## Building 1 and Campus Network

# Network Configuration and Details

## VLAN and Network Segment Details

| VlanID | VlanName      | IPv4 Nodes | Network Prefix | Network Address  | First Node      | Broadcast       | Network Mask        |
|--------|---------------|------------|----------------|------------------|-----------------|-----------------|---------------------|
| 405    | 1_GroundFloor | 50         | /26            | 172.25.1.128/26  | 172.25.1.129    | 172.25.1.191    | 255.255.255.192     |
| 406    | 1_FloorOne    | 50         | /26            | 172.25.1.192/26  | 172.25.1.193    | 172.25.1.255    | 255.255.255.192     |
| 407    | 1_Wifi        | 80         | /25            | 172.25.0.128/25  | 172.25.0.129    | 172.25.0.255    | 255.255.255.128     |
| 408    | 1_DMZ         | 100        | /25            | 172.25.0.0/25    | 172.25.0.1      | 172.25.0.127    | 255.255.255.128     |
| 409    | 1_VoIP        | 67         | /25            | 172.25.1.0/25    | 172.25.1.1      | 172.25.1.127    | 255.255.255.128     |
| 410    | 1_BackBone    | 200        | /24            | 172.25.2.0/24    | 172.25.2.1      | 172.25.2.255    | 255.255.255.0       |

## VLAN Gateway Addresses

| VlanID | VlanName      | Gateway Address |
|--------|---------------|-----------------|
| 405    | 1_GroundFloor | 172.25.1.129    | 
| 406    | 1_FloorOne    | 172.25.1.193    |
| 407    | 1_Wifi        | 172.25.0.129    |
| 408    | 1_DMZ         | 172.25.0.1      |
| 409    | 1_VoIP        | 172.25.1.1      |
| 410    | 1_BackBone    | 172.25.2.1      |

## Devices Used

| Device  | Name          | IPv4 Address     |
|---------|---------------|------------------|
| PC      | PC1_1.1.6     | 172.25.1.195     |
| PC      | PC2_1.1.1     | 172.25.1.194     |
| PC      | PC3_1.0.1     | 172.25.1.131     |
| PC      | PC4_1.0.3     | 172.25.1.130     |
| PC      | PC5_1.0.6     | 172.25.1.132     |
| Laptop  | Laptop1_1.0.2 | 172.25.0.133     |
| Laptop  | Laptop2_1.0.6 | 172.25.0.132     |
| Laptop  | Laptop3_1.1.6 | 172.25.0.130     |
| Laptop  | Laptop4_1.1.7 | 172.25.0.131     |
| Server  | Server1       | 172.25.0.2       |

## Equipment Used

| Hardware                   | Packet Tracer   |
|----------------------------|-----------------|
| Intermediate Cross-connect | Switch-PT-Empty |
| Horizontal Cross-connect   | Switch-PT-Empty |
| Consolidation Point        | Switch-PT-Empty |
| Access Point               | AccessPoint-PT  |
| Router                     | 2811            |
| ISP Router                 | 2811            |
| PC                         | PC-PT           |
| Laptop                     | Laptop-PT       |
| Server                     | Server-PT       |
| Phone                      | 7960            |