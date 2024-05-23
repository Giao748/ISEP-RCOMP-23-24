# Campus 

## Campus Information

- The Campus has four buildings, each of these buildings has two floors. The buildings are identified by the numbers 1, 2, 3, and 4. 
- The Cable used to connect the Main Cross-Connect (MC) located in building 1 to all the Intermediate Cross-Connect (IC) in each building is **Optical Fiber Multi-Mode**.

### Campus Layout
![Campus](Campus.png)
**Note:** Redundancy measures were implemented using parallel cables for backbone connections, allowing for failover mechanisms and automatic detection of cable failures.

| Buildings | length (m) |
|-----------|------------|
| 1 -> 2    | 650        |
| 1 -> 3    | 650        |
| 1 -> 4    | 650        |
| **Total** | **1950**   |

| Number of Fiber Multi-Mode cables | 
|-----------------------------------|
| 6                                 |

# Building 1

## Building's information

- Width: 20m
- Length: 20m
- Area: 400m²
- Floors: 2

    - **Floor 0:**
        - Height: 4m 

    - **Floor 1:**
        - Height: 3m

### Additional Information

- This building holds the datacenter (room 1.1.4), it will also house the Main Cross-Connect (MC) for the structured cabling system. Both floors have wireless LAN coverage (Wi-Fi)

- The first floor (Floor 0) has an underfloor cable raceway connected to the external technical ditch. Access to the underfloor cable raceway is available at points marked over the plan at the image below. Also, cable passageways to the above floor are available.

- Common areas, like the entrance hall, restrooms, and stairs require no network outlets.

- There’s a removable dropped ceiling in Floor 1, placed 2.5 meters from the ground, covering the entire floor. The space over the dropped ceiling is perfect to install cable raceways and wireless access-points, this floor has no underfloor cable raceways.

- The CAT7 cables used in the horizontal cabling system where installed through cable trays, which are accessible at the points marked over the plan at the images below.

## Floor 0

### Floor 0 Layout

![Building1Floor0](Building1_Floor0.png)

**Note:** The cables are represented by the dashed lines, the orange lines represent the CAT7 cables installed in the horizontal cabling system through cable trays, and the blue lines represent the CAT7 cables installed in the underfloor cable raceway.

### Rooms measurements
| Division | Width (m) | Length (m) | Area (m^2) | Outlets |
|----------|-----------|------------|------------|---------|
| 1.0.1    | 5,9       | 5          | 29,5       | 6       |
| 1.0.2    | 3,7       | 5          | 18,5       | 5       |
| 1.0.3    | 4,8       | 5          | 24         | 5       |
| 1.0.4    | 5         | 7,2        | 36         | 8       |
| 1.0.5    | 5,9       | 4,4        | 25,96      | 6       |
| 1.0.6    | 5,9       | 7,2        | 42,48      | 10      |

| Total Outlets | Number of CAT7 cables | 
|---------------|-----------------------|
| 40            | 43                    |

### Important Notes

- Room 1.0.4 contains celling cable passageway to the floor above and the Horizontal Cross-Connect (HC) for this floor (Floor 0).
- The location of each element is taken into account when calculating the amount of cable needed for the installation.
- **Outlets (RJ45):**
    - The quantity of outlets per room was determined based on a ratio of 2 outlets for every 10 square meters of area.
    - The distribution of outlets in each room was determined based on the room's layout and to ensure that there are outlets available in all areas of the room.
    - All outlets are situated above the footer of the wall, 0.1m from the ground.
- **Cables:**
  - All cables have a maximum length of 90m, respecting the standard.
  - The cables used are CAT7, which is the best choice for horizontal cabling.
  - The cables were installed in the underfloor cable raceway, which is accessible at the points marked over the plan at the image below.
  - The underfloor cable raceway is connected to the external technical ditch, which is used to connect all buildings using Optical Fiber and is located in the room 1.0.4. This room also contains a ceiling cable passageway to the floor above.
- **Access Points (AP):**
  - Each has a range of 50m in diameter, however accounting for the walls and other obstacles, the range considered is 30m.
  - Each Access Point (AP) requires 1 outlet.
  - The rooms 1.0.2 and 1.0.6 have 1 additional outlet each because they contain Access Points (APs) for the wireless network.
  - One Access Point (AP) would cover the area of the whole floor as required by the client, however the reason for the existence of 2 Access Points (APs) in room 1.0.6 and 1.0.2 is due to the number of predictable connections (2 Connections per outlet) which is larger than only one Access Point can support.
- **Consolidation Points (CP):**
  - The consolidation points (CP) improve the cable distribution and makes it look more aesthetically pleasing in each room. 
  - There are 2 Consolidation Points (CP) in the floor, located in the rooms 1.0.2 and 1.0.6. The CPs are used to minimize cabling crossing through walls. 
  - Both Consolidation Points (CP) are connected to the Horizontal Cross-Connect (HC) with a CAT7 cable by the passage ways in the underfloor cable raceway.
- **Horizontal Cross-Connect (HC):**
  - This floor only has one Horizontal Cross-Connect (HC), as the building has only 400m2, and the standard requires one HC for every 1000m2.
  - The Horizontal Cross-Connect (HC) is located in the room 1.0.4 as it's the closest room possible to the Intermediate Cross-Connect (IC) located at the floor above (Floor 1). This way the amount of fiber optic cable used is minimized.
  - The Horizontal Cross-Connect (HC) is connected to the Intermediate Cross-Connect (IC) located in the floor above (Floor 1) with a CAT7 cable by the passage ways.

### Floor 0 Inventory

| Equipment                        | Quantity | 
|----------------------------------|----------|
| Outlets                          | 40       |
| Access Points (AP)               | 2        |
| Consolidation Points (CP)        | 2        |
| Horizontal Cross-Connect (HC)    | 1        |
| Copper Cable CAT7 (m)            | 450      |
| Fiber Optic Cable (m)            | 5        |
| Copper Patch Panel 1U (24 ports) | 3        |
| Switch 1U (24 ports)             | 3        |
| Telecommunication Enclosure 6U   | 3        |

## Floor 1

### Floor 1 Layout

![Building1Floor1](Building1_Floor1.png)

**Note:** The cables are represented by the dashed lines, the orange lines represent the CAT7 cables installed in the horizontal cabling system through cable trays, and the green lines represent the CAT7 cables installed in the ceiling cable passageway.

### Rooms measurements
| Division | Width (m) | Length (m) | Area (m^2) | Outlets |
|----------|-----------|------------|------------|---------|
| 1.1.1    | 3,7       | 7,2        | 26,64      | 6       |
| 1.1.2    | 3,7       | 7,2        | 26,64      | 6       |
| 1.1.3    | 3,7       | 7,2        | 26,64      | 6       |
| 1.1.4    | 7,8       | 7,2        | 56,16      | 0       |
| 1.1.5    | 5,6       | 4,4        | 24,64      | 5       |
| 1.1.6    | 5,9       | 7,2        | 42,48      | 10      |
| 1.1.7    | 5,9       | 4,8        | 28,32      | 7       |

| Total Outlets | Number of CAT7 cables | Number of Fiber Multi-Mode cables |
|---------------|-----------------------|-----------------------------------|
| 40            | 45                    | 1                                 |


### Important Notes

- Room 1.1.4 is a datacenter (no outlets required) where the Intermediate Cross-connect (IC) for the building is located, as well as a Horizontal Cross-connect (HC) for this floor. This IC will receive the fiber optic cable from the Main Cross-connect (MC) which is also located in this datacenter room. This room also contains cable passageway to the floor below connecting to room 1.0.4.
- The location of each element is taken into account when calculating the amount of cable needed for the installation.
- **Outlets (RJ45):**
  - The quantity of outlets per room was determined based on a ratio of 2 outlets for every 10 square meters of area.
  - The distribution of outlets in each room was determined based on the room's layout and to ensure that there are outlets available in all areas of the room.
  - All outlets are situated above the footer of the wall, 0.1m from the ground.
- **Cables:**
  - All cables have a maximum length of 90m, respecting the standard.
  - The cables used are CAT7, which is the best choice for horizontal cabling and optical fiber Multi-Mode from the Main Cross-Connect (MC) to the outside.
  - The cables were installed above the dropped ceiling cable raceway.
- **Access Points (AP):**
  - Each has a range of 50m in diameter, however accounting for the walls and other obstacles, the range considered is 30m.
  - Each Access Point (AP) requires 1 outlet.
  - The rooms 1.1.7 and 1.1.6 have 1 additional outlet each because they contain Access Points (APs) for the wireless network.
  - One Access Point (AP)  would cover the area of the whole floor as required by the client, however the reason for the existence of 2 Access Points (APs) in room 1.1.6 and 1.1.7 is due to the number of predictable connections (2 Connections per outlet) which is larger than only one Access Point can support.
- **Consolidation Points (CP):**
  - The consolidation points (CP) improve the cable distribution and makes it look more aesthetically pleasing in each room.
  - There are 2 Consolidation Points (CP) in the floor, located in the rooms 1.1.2 and 1.1.6. The CPs are used to minimize cabling crossing through walls.
  - Both Consolidation Points (CP) are connected to the Horizontal Cross-Connect (HC) with a CAT7 cable by the passage ways above the dropped ceiling.
- **Horizontal Cross-Connect (HC):**
  - The Horizontal Cross-Connect (HC) is located in the room 1.1.4 as it's the closest room possible to the Main Cross-Connect (HC) located at the floor above (Floor 1). This way the amount of fiber optic cable used is minimized.
  - This floor only has one Horizontal Cross-Connect (HC), as the building has only 400m2, and the standard requires one HC for every 1000m2.
  - The Horizontal Cross-Connect (HC) is connected to the Intermediate Cross-Connect (IC) with a CAT7 cable.
- **Intermediate Cross-Connect (IC):**
  - The Intermediate Cross-Connect (IC) is located in the room 1.1.4 as close as possible to the Main Cross-Connect (MC) in order to minimize the amount of fiber optic cable used.
  - The Intermediate Cross-Connect (IC) is connected to the Main Cross-Connect (MC) with an optical fiber Multi-Mode cable.
- **Main Cross-Connect (MC):**
  - The Main Cross-Connect (MC) is located in the room 1.1.4 as it is the datacenter room.
  - The Main Cross-Connect (MC) is connected to the Intermediate Cross-Connect (IC) with an optical fiber Multi-Mode cable.
  - The Main Cross-Connect (MC) distributes the signal to all the Intermediate Cross-Connect (IC) in the campus, one in each building, through fiber optic cables.

### Floor 1 Inventory

| Equipment                        | Quantity | 
|----------------------------------|----------|
| Outlets                          | 40       |
| Access Points (AP)               | 2        |
| Consolidation Points (CP)        | 2        |
| Horizontal Cross-Connect (HC)    | 1        |
| Intermediate Cross-Connect (IC)  | 1        |
| Main Cross-Connect (MC)          | 1        |
| Copper Cable CAT7 (m)            | 550      |
| Fiber Optic Cable (m)            | 5        |
| Copper Patch Panel 1U (24 ports) | 4        |
| Fiber Patch Panel 1U (24 ports)  | 1        |
| Switch 1U (24 ports)             | 5        |
| Telecommunication Enclosure 12U  | 1        |
| Telecommunication Enclosure 6U   | 2        |

# Total Building 1 Inventory

| Total number of CAT7 cables | Total Number of Fiber Multi-Mode cables |
|-----------------------------|-----------------------------------------|
| 88                          | 7                                       |

| Equipment                        | Quantity | 
|----------------------------------|----------|
| Outlets                          | 80       |
| Access Points (AP)               | 4        |
| Consolidation Points (CP)        | 4        |
| Horizontal Cross-Connect (HC)    | 2        |
| Intermediate Cross-Connect (IC)  | 1        |
| Main Cross-Connect (MC)          | 1        |
| Copper Cable CAT7 (m)            | 1000     |
| Fiber Optic Cable (m)            | 1960     |
| Copper Patch Panel 1U (24 ports) | 7        |
| Fiber Patch Panel 1U (24 ports)  | 1        |
| Switch 1U (24 ports)             | 8        |
| Telecommunication Enclosure 12U  | 1        |
| Telecommunication Enclosure 6U   | 5        |

The **Telecommunication Enclosure** is a cabinet used to accommodate the equipment. The enclosure also provides space for the expansion of additional racks if necessary, thus adhering to structured cabling recommendations.

# Further Explanations

## Cable Explanation

### Optical Fiber Multi-Mode

The choice to use Multi-Mode fiber over Single-Mode fiber for a distance of 1960 meters is advisable due to its cost-effectiveness and suitability for shorter transmission distances. Multi-Mode fiber is more economical and easier to install for distances under 2 kilometers, making it the practical choice for this scenario. Additionally, if the bandwidth requirements are not exceptionally high, Multi-Mode fiber can adequately fulfill the data transmission needs over this relatively short distance without the need for the precision and higher costs associated with Single-Mode fiber.

### Copper Cable CAT7

The choice to use Copper Cables - CAT7 was its capability to support high data transmission speeds and a superior level of protection against electromagnetic interference compared to CAT5 and CAT6 cables. In this manner, it is possible to ensure the quality of data transmission while minimizing the risk of network interruptions or failures.

### Cable Lengths

To achieving a good estimate of total cables lengths required some common-sense approximations were used:

- When a high number of cables share the same segment of a pathway, measure the segment pathway length and multiply by the number of cables.

- When a high number of cables irradiates from the same point, we can estimate the average cable length and multiply by the number of cables. This will be accurate if the cables length distribution is symmetrical. For instance, we can estimate the average cable length based on the two longest cables and two shortest cables.

## Telecommunication Enclosure Size

In order to choose the right size for a Telecommunication Enclosure these are the rules followed.

- If the Telecommunication Enclosure is housing a single 1U patch panel, then we should add another 1U for the expected corresponding switch
- An additional 100% increment is wise for future reasons
- The minimum size for a Telecommunications Enclosure is 6U