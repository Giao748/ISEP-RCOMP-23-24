## Building 4

### Building Area:

- 30m × 30m = 900 m²


### Document Organization:



### Floor 0
- Measurements taken and information calculated
- Schematic Plan of the Floor
- Explanation of outlet distribution
- Explanation of APS distribution
- Explanation of CPS distribution
- Explanation of IC and HC distribution
- Floor Inventory




### Floor 1
- Measurements taken and information calculated
- Schematic Plan of the Floor
- Explanation of outlet distribution
- Explanation of APS distribution
- Explanation of CPS distribution
- Explanation of IC and HC distribution
- Floor Inventory
- Total Inventory

### Tables
- Table with measurements and room type for floor 0
- Table with measurements and room type for floor 1
- Table with meaning of Colors from previous Tables.




# Floor 0


### Measurements taken and information calculated:

-EM FALTA !
### Schematic Plan of the Floor

![Floor 0](Piso%200.png)

### Outlets
- The standard rule of 2 outlets per every 10 square meters was respected.
- However, there are some exceptions such as Bathrooms (WCs), corridors, and respective rooms:



### 4.0.02:
Room contains only 2 outlets per each cable passage on the floor.
### 4.0.12
The room is a warehouse and therefore does not require any outlet.



- The **single outlet model** was defined for this floor (only one cable entry per outlet).
- When positioning the outlets, it was also considered that the maximum distance between them would be **3 meters**, so that in any part of the room where the user's equipment was located, it could be easily connected to an outlet with the provided cable.
- The outlets, contrary to what may seem in the image, are not located on the floor. An average height of **0.5 meters** from the floor was defined for each outlet in the room.

### Access Points (AP)
- The logic of having each Access Point serve between 25-35 devices was respected.
- Each device will represent an outlet since, as referenced above, the outlets are **single**.
- For this building, **3 Access points** were used and their distribution was done as follows:

  - **4.0.1,4.0.2,4.0.3**: with a reach of 26 devices.
  - **4.0.4,4.0.5,4.0.6,4.0.7**: with a reach of 24 devices.
  - **4.0.8,4.0.9,4.0.10,4.0.11**: with a reach of 24 devices.


- The Building has a total of **74 reached outlets**, not exceeding the total wireless capacity (35 devices). However, some margin is left in case some users use more than 1 device per outlet.
- Each Access Point has a Standard diameter of 50 meters which is sufficient for the entire building, but in this context, it does not reach all the devices in the building (>35).
- The Intersection of each access Point is much greater than 15% as seen in the [figure](Piso%200.png). However, this issue was discussed with the client, and it was understood that the overlapping is not so relevant in this case, as these will be subsequently configured with different frequency channels to not intersect.




### Consolidation Points (CP)

- The distribution of CPS was similar to Access Points:
  - In room **4.0.1** which is responsible for controlling room _4.0.1 and 4.0.2_ being responsible for 20 outlets.
  - In room **4.0.5,** which is responsible for controlling rooms _4.0.3, 4.0.4, 4.0.5, 4.0.6_ and _4.0.7_ being responsible for 30 outlets.
  - In room **4.0.10**, which is responsible for controlling rooms _4.0.8, 4.0.9, 4.0.10 and 4.0.11_ and for the outlet for the access point, being responsible for 26 outlets.


- The connection of the Outlets to the CPs is made with CAT 7 copper cable.
- The connection of the HC with the CPs is made underground (underfloor cable raceway), also by CAT7 connection at the customer's request.



###  Horizontal Cross-Connect (HC) and Intermediate Cross-Connect (IC)
- With the building containing 900 m², one HC was defined per floor, respecting the norm of 1 Horizontal cross-connect for every 1000 m².
- The Building contains its only Intermediate cross-connect on floor 0.
- The IC receives the optical fiber connection from the MC and distributes the signal to the two HCs of floor 0 and 1 of this building through Cat 7 copper cables.
- The placement of HC and IC was made in the warehouse (4.0.12) since the room was described as a possible storage area in the floor description.


| Distance from IC to output       | Quantity | 
|----------------------------------|----------|
| Fiber Optic Cable (m)            | 0.32     |



### Floor 0 Inventory


| Equipment                         | Quantity | 
|-----------------------------------|----------|
| Outlets                           | 74       |
| Access Points (AP)                | 3        |
| Consolidation Points (CP)         | 3        |
| Horizontal Cross-Connect (HC)     | 1        |
| Intermediate Cross-Connect (IC)   | 1        |
| Main Cross-Connect (MC)           | 1        |
| Copper CAT7 Cable (m)             | 800      |
| Fiber Optic Cable (m)             | 0.96     |
| Copper Patch Panel 1U (24 ports)  | 3        |
| Fiber Patch Panel 1U (24 ports)   | 1        |

# Floor 1

![Floor 0](Piso%200.png)

### Outlets

- The 10 outlets rule was also used on this floor, following the same logic as Floor 0, with 2 outlets per every 10 square meters. However, the same exceptions were applied for WCs, corridors, and specific rooms.

#### 4.1.19, 4.1.20
The rooms are warehouses and therefore do not require any outlet.
### Access Point (AP)
Four access Points were distributed on this floor, following the same logic as the CPs.
The same concept from Floor 0 also applies here regarding overlapping and configuration of non-intersecting channels.

### Consolidation Points (CP)
**Four** Consolidation Points were distributed as follows:
- In room 4.1.14, responsible for 4.1.14, 4.1.5, 4.1.16, and 4.1.17.
- In room 4.1.13, responsible for 4.1.13, 4.1.14, 4.1.11, and 4.1.12.
- In room 4.1.7, responsible for 4.1.1 and 4.1.2.
- In room 4.1.4, responsible for 4.1.4 and 4.1.3.


### Horizontal cross-connect (HC)
- The horizontal cross-connect is located in room (4.1.20), as the room was described as a warehouse for possible hardware storage.

### Intermediate cross-connect (IC)

- This Floor does not require an Intermediate Cross-Connect, as the only IC is on Floor 0, and no information was provided for such on Floor 1.





### Floor 1 Inventory

| Equipment                         | Quantity | 
|-----------------------------------|----------|
| Outlets                           | 108      |
| Access Points (AP)                | 4        |
| Consolidation Points (CP)         | 4        |
| Horizontal Cross-Connect (HC)     | 1        |
| Intermediate Cross-Connect (IC)   | 1        |
| Main Cross-Connect (MC)           | 0        |
| Copper CAT7 Cable (m)             | 1100     |
| Fiber Optic Cable (m)             | 4.8      |
| Copper Patch Panel 1U (24 ports)  | 4        |
| Fiber Patch Panel 1U (24 ports)   | 1        |

### Building Inventory

| Equipment                        | Quantity | 
|----------------------------------|----------|
| Outlets                          | 182      |
| Access Points (AP)               | 7        |
| Consolidation Points (CP)        | 7        |
| Horizontal Cross-Connect (HC)    | 2        |
| Intermediate Cross-Connect (IC)  | 1        |
| Main Cross-Connect (MC)          | 1        |
| Copper CAT7 Cable (m)            | 2000     |
| Fiber Optic Cable (m)            | 6        |
| Copper Patch Panel 1U (24 ports) | 7        |
| Fiber Patch Panel 1U (24 ports)  | 2        |

## Tables with calculations
### Floor 0
![Table0](piso0-tabela.png)
### Floor 1
![Table1](piso1-tabela.png)
### Colors meaning in Cells

![ColorMeaning](significado-Cores.png)
