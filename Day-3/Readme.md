## Day-3 Activity

### Anti-Braking system
#### Different Conditions:
##### Brake Position:
		
    OFF-0001
		
    ON- 0010

##### Speed & ABS Sensor:

Switch 0- ABS is OFF -0101

Switch 1 – Speed less than 20km/h –ABS is OFF (Lower-0110)

Switch 2- Speed greater than 20km/h –ABS is ON (Lower-0111)

Switch 3- Raining ABS activate  (Skidding-0100)

##### Brake Light:

Dim Light-0001

Less Bright Light-0010

Full Bright Light: 0011

##### Identifier:

ID1- 10000100000 (420H)

ID2-10000110000(430H)

ID3-10001000000(440H)

##### Control System Work flow:

![control system work flow](https://user-images.githubusercontent.com/115522470/199960645-e5948a52-460e-4002-b626-a64fc4bab04d.png)

##### Flow Diagram for different sequences:

![Flow Diagram for different sequences](https://user-images.githubusercontent.com/115522470/199960879-2466cf5c-27b5-4cd6-a223-4a4fde9e2168.png)

##### CAN Frame representation for different Identifiers:

![EXCEL FOR brake system with different ID](https://user-images.githubusercontent.com/115522470/199961012-703e67a5-3ebc-4ce8-9158-332cbe8cb650.png)

