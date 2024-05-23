## RCOMP 2023-2024 Project - Sprint 2 - Member 1220672 folder

# Building 3

  | Network address | 	Broadcast       | address           | 	Address range               | VLAN range|
  |-----------------|------------------|-------------------|------------------------------|-------------|
  | Building 3	     | 172.25.8.0/22    | 	172.25.11.255    | 	172.25.8.1 - 172.25.11.254	 |416 - 420|
  
### Schematic Vlan Ip distribution:

| ID da VLAN | Nome da VLAN  | Total de nodes | IP da rede       | Primeiro host | Último host   | Broadcast     | Máscara de sub-rede |
|------------|---------------|----------------|------------------|---------------|---------------|---------------|---------------------|
| 418        | 3_Wifi        | 200            | 172.25.8.0/24    | 172.25.8.1    | 172.25.8.254  | 172.25.8.255  | 255.255.255.0       |
| 420        | 3_Voip        | 180            | 172.25.9.0/24    | 172.25.9.1    | 172.25.9.254  | 172.25.9.255  | 255.255.255.0       |
| 417        | 3_FloorOne    | 130            | 172.25.10.0/24   | 172.25.10.1   | 172.25.10.254 | 172.25.10.255 | 255.255.255.0       |
| 416        | 3_GroundFloor | 110            | 172.25.11.0/25   | 172.25.11.1   | 172.25.11.127 | 172.25.11.128 | 255.255.255.128     |
| 419        | 3_DMZ         | 45             | 172.25.11.128/26 | 172.25.11.129 | 172.25.11.191 | 172.25.11.192 | 255.255.255.192     |

## Equipment Used

| Hardware                   | Packet Tracer   |
|----------------------------|-----------------|
| Intermediate Cross-connect | Switch-PT-Empty |
| Horizontal Cross-connect   | Switch-PT-Empty |
| Consolidation Point        | Switch-PT-Empty |
| Access Point               | AccessPoint-PT  |
| Router                     | 2811            |
| PC                         | PC-PT           |
| Laptop                     | Laptop-PT       |
| Server                     | Server-PT       |
| Phone                      | 7960            |