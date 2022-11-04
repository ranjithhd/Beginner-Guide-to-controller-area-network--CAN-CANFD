## Day 1: Activity 1
1.	Different types of communication protocols used in automotive

| **Protocol** | **Controller area network – (CAN) **|** Local Interconnect Network-(LIN) **|** Media Oriented systems Transport-(MOST)) **|** Flexray **|** Ethernet** |
| --- | --- | --- | --- | --- | --- |
| **ISO standard** | ISO11898 | ISO17987 | ISO21806-1 | ISO17458 | ISO 8802-3 |
| **Data rate** | 1Mbps | 19.2kbps | 50Mbps | 10Mbps | 10Mbps |
| **Frame size** | 8 bytes | 8 bytes | 11-32 bytes | 254bytes | 64bytes |
| **Physical layer** | Twisted pair, 10v | Single wire, 12v | Fiber optic | 2 or 4 wires | One or more twisted pair |
| **Message Transmission** | Asynchronous | Synchronous | Asynchronous &Synchronous | Asynchronous &Synchronous | Asynchronous |
| **Latency** | Load dependent | Constant | Constant | Load dependent |
| **Reliability** | Reliable | Least Reliable | Reliable | Most Reliable | Reliable |
| **Operating Voltage** | 4.75V-5.25V | 12V | 135V – 230V | +/- 2.5V | 48V |
| **Cable Impedance** | 120ohm | 1Kohm | 50ohm | 80-120ohm | 100ohm |
| **Cost** | Moderately expensive | Least expensive | Expensive | Most Expensive | Expensive |
| **Access Control** | CSMA/CD+AMP | Polling | TDM CSMA/CA | TDMA | CSMA/CD |
| **Architecture** | Multi-Mater typically 10 to 30 nodes | Multi-Mater typically 2 to 10 slaves | Multi-Mater | Multi-Mater | Multi-Mater |
| **Topology** | Bus | Bus | Ring/Star | Bus/star | Bus/star |
| **year** | 1983 | 2001 | 2001 | 2005 | 1980 |
| **Applications** | Transmission airbags, antilock braking, Electric power steering | Steering wheel, seat, engine, Door | Camera and video connections | Steering by wire control, Anti-lock braking system | IP Cameras, Radar, Infotainment |


### CAN arbitration be used for same ID?

Two node on the network are not allowed to send messages with same id. If two nodes try to send messages with same id at the same time arbitration will not work. Instead, one of the transmitting  nodes will detect that his message is distorted outside of the arbitration field. 

## Day 1: Activity-2

2.	What are the different parameters to look in automotive.

### CAN:

•	Airbags

•	ABS

•	Cratie control

•	Transmissions

•	Transmitters

•	Hybrid vehicle charging systems

•	Audio/sound systems

•	Suspension systems

•	Power steering

•	In-vehicle information system

### LIN:

•	Electric windows

•	Door locks

•	Lights

•	Power seat controllers

•	Rear view mirror control

### Flexray

•	Safety components

•	Active suspension system

•	High performance transmission

•	Traction control  system

•	Sensor components

•	Steering wheel control

### Ethernet:

•	Cellular network communication

•	Radios

•	High resolution cameras

•	In vehicle information system

•	Instrument chuster

## Day-1 Activity-3
### Can two frames have same arbitration address? if yes, why? if not why not?

No two nodes may transmit the same arbitration field. There is one exception to this rule, if the message contains no data, then any node can transmit that message. Since the bus is wired and dominant bit is logically 0, it follows that the message with numerically lowest arbitration field will win the arbitration. If two nodes try to send a message with the same ID at the same time, arbitration will not work. Instead one of the transmitting nodes will detect that his message is distorted outside of the arbitration field.

## Day-1 Activity-5

### CAN standard and extended frame format, understand each parameter in the frame.

#### Standard CAN vs Extended CAN

In 1991, Originally Bosch released CAN specification CAN 2.0 for passenger Vehicles which explains 11- bit identifier frame architecture but later on it divided into CAN 2.0(A) which is named as standard CAN be used in passenger cars dealing with 11-bit Identifier while other is CAN2.0(B) which is known as extended CAN be used in heavy vehicles like Buses and Trucks it deals with 29-bit Identifier. So the basic difference in both standard at message Identifier field.
CAN2.0A for Standard Frame Format for Passenger Vehicles
CAN2.0B for Extended Frame Format for Heavy Vehicles

#### Standard or Classical CAN Frame

The standard frame format is specified in can Specification CAN2.0(A) by Robert Bosch. See below table for frame fields,sub-fields and its role in CAN Frame-

Table 1: Frame Format For Standard CAN

![Frame Format For Standard CAN](https://user-images.githubusercontent.com/115522470/199955060-af42087c-4704-4cbc-9611-e68f827aee18.png)

#### Extended CAN Frame Format

The extended Frame of CAN is almost similar to the standard frame except for its arbitration field. See below table for frame fields,sub-fields and its role in CAN Frame –

Table: Frame Format For Extended CAN

![Frame Format For Extended CAN](https://user-images.githubusercontent.com/115522470/199955344-6466e5dd-0143-4e5e-9d38-663bbc6db7b4.png)

So as we can see Arbitration field in the extended frame format only differ from the standard CAN means extended CAN architecture designed in such a way that standard and extended CAN coexist on the same network.

### Day-1 Activity-6

#### CAN standard frame and extended frame used together in same network? if yes, which one has higher priority?

Yes it is possible to have a system with both standard and extended can identifiers. The standard frame always is given priority against extended frame.


