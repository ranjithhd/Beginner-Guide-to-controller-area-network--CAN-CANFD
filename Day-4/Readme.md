
# Day 4-Activity-1

## Understanding the evolution of Ethernet

First developed by Xerox PARC in the 1970s and ratified by IEEE as a standard in 1983, the evolution of Ethernet has taken this LAN technology through dozens of specifications.

For hundreds of years, scientists believed a mysterious substance known as ether served as the medium for light to disperse through space. The notion was ultimately dismissed once physicists discovered that photons act as both particles and waves. But the archaic word lives on in the modern term Ethernet -- the technology by which bits of information travel through complex computer networks.
Created at Xerox Palo Alto Research Center (PARC) in the early 1970s by a team that included Robert Metcalfe and David Boggs and ratified by the Institute of Electrical and Electronics Engineers (IEEE) as a standard in 1983, Ethernet has become the dominant LAN technology. Decades after its initial specification, the evolution of Ethernet continues.

#### Robert Metcalfe invents Ethernet

The evolution of Ethernet officially began in 1973 when engineer Robert Metcalfe introduced the concept in a memo he wrote while working at Xerox PARC. The technology, as Metcalfe described it, linked discrete advanced computing workstations and enabled them to communicate with each other, as well as with devices like high-speed laser printers. Together, these interconnected endpoints became more than the sum of their parts: an environment we now recognize as the world's first high-speed LAN.
Metcalfe based Ethernet on what he learned from the Aloha system -- an earlier networking project that began at the University of Hawaii in 1968. Aloha aimed to connect remote workstations across the Hawaiian Islands to a central computer at the main Oahu campus.

![evolution of ethernet](https://user-images.githubusercontent.com/115522470/199961608-e258f44d-b61b-4d81-bcd7-8fcdc75cd0a6.jpg)

Using the rudimentary Aloha protocol, a station would transmit a frame over a common data channel and then wait for confirmation it had reached its destination successfully. If the station didn't receive confirmation within a given period, it assumed a collision had occurred with another frame that a different node happened to send simultaneously. That station would continue to blindly resend the data until it achieved successful transmission. But, as nodes and transmissions increased, more collisions would occur, and the network became less efficient. An Aloha variation called slotted Aloha sought to minimize network contention problems by precisely coordinating individual transmissions, assigning them designated time slots via beacon signaling.

##### Metcalfe's Ethernet experiment 
Which he initially referred to as the Alto Aloha Network -- included several revolutionary new features that enabled significantly more efficient use of a network channel. Together, this set of rules -- now codified as the Carrier Sense Multiple Access/Collision Detect protocol -- enabled stations to monitor the availability of a shared path and detect collisions when two devices happened to send data at the same time. When frames did collide, the system would discard them, and each station would wait a randomly assigned length of time before reinitiating its transmission -- pausing and repeating as many times as necessary, in a process known as exponential back-off.

By 1973, Metcalfe felt the technology had outgrown its original name, Alto Aloha Network, and rechristened it Ethernet. Four years later, Metcalfe and Boggs -- along with Charles Thacker and Butler Lampson, also of Xerox -- would successfully patent Ethernet technology.

#### IEEE standardization

Xerox worked with two other vendors -- Digital Equipment Corporation and Intel -- to publish the first 10 Mbps Ethernet specification in 1980. Meanwhile, the Local and Metropolitan Area Networks (LAN/MAN) Standards Committee at the IEEE set out to develop a similar open standard.

The LAN/MAN committee -- which applies the number 802 to all its standards -- formed an Ethernet subcommittee, dubbing it 802.3. In 1983, the IEEE approved the original 802.3 standard for thick Ethernet (10Base-5), with official publication in 1985. Next, it ratified 802.3a (10Base-2), a version of 10 Mbps Ethernet that uses thin coaxial cable, followed by twisted pair (10Base-T) and fiber optic (10Base-FL) standards.

In 1995, 100 Mbps Ethernet -- also known as Fast Ethernet or 100BASE-T -- debuted, introducing autonegotiation. This new feature enabled two network devices to communicate and establish the best shared mode of operation -- i.e., speed and duplex mode.

Three years later, 802.3 hit a new milestone with the introduction of Gigabit Ethernet (1000Base-T) -- first over fiber optic cable and, subsequently, over twisted pair cabling.

##### The evolution of Ethernet continued with 10 Gbps in 2002 
The first over fiber, then twinaxial and, finally, unshielded twisted pair cables. Eight years later, the IEEE approved 40 GbE and 100 GbE, speeds achieved by aggregating 10 Mbps lanes.

In 2016, driven by demand from hyperscale web companies, the IEEE ratified 25 GbE, which promised to be 2.5 times faster than 10 GbE but more cost-effective than 40 GbE. Because it improves throughput by increasing the capacity of a single lane -- rather than aggregating multiple lower-capacity lanes -- 25 GbE requires less cable and power and has higher port density than 40 GbE. In some cases, an upgrade to 25 GbE lets data center operators extend the life of top-of-rack switches and avoid a full rip-and-replace upgrade of cabling infrastructure.

The following year, in late 2017, the networking industry saw the ratification of 200 GbE and 400 GbE, both based on 50 Gbps single lanes. As the appetite for faster bandwidth skyrockets -- especially among cloud providers and other hyperscale data center operators -- the standards committee now turns its attention to 800 Gbps, 1 Tbps and beyond. The evolution of Ethernet continues.

# Day 4-Activity 2
## Introduction to the LIN bus

#### Background

The protocol for the Local Interconnect Network (LIN) is based on the Volcano-Lite technology developed by the Volvo spin-out company Volcano Communications Technology (VCT). Since other car corporations also were interested in a more cost effective alternative to CAN, the LIN syndicate was created. In the middle of 1999 the first LIN protocol (1.0) was released by this syndicate. The protocol was updated twice in 2000. In November 2002 LIN 1.3 was released with changes mainly made in the physical layer. The latest version LIN 2.2A was released in 2010. With LIN 2.0 came some major changes and also some new features like diagnostics. The changes were mainly aimed at simplifying use of off-the-shelves slave nodes.

##### Areas of use

The LIN protocol is a compliment to the CAN and the SAE J1850 protocols for applications that are not time critical or does not need extreme fault tolerance, since LIN is not quite as reliable as CAN. The aim of LIN is to be easy to use and a more cost effective alternative to CAN. Examples of areas where LIN is and can be used in a car: window lift, mirrors, wiper and rain sensors.

##### Quick facts

LIN is an all-embracing concept according to the OSI-model, where the physical-, data link- , network- and application layers are covered by the specification.

•	The LIN physical layer is based on ISO 9141 (the K-line).

•	Master/slave organization

•	Single wire plus ground

•	Time triggered scheduling

•	1-20 kbit/s

•	Dominant/recessive bits

•	Serial, byte oriented communication

•	Max 40 m wire length

•	Standard defined by the LIN organization: http://www.lin-subbus.org

##### Physical Properties

The LIN-bus transceiver is a modified version of the transceiver used by the ISO 9141 standard. The bus is bidirectional and connected to the node transceiver, and also via a termination resistor and a diode to Vbat of the node (Figure).

![LIN Transreiver](https://user-images.githubusercontent.com/115522470/199962631-0384479e-174d-4dd0-8e57-beac1fd54a65.jpg)

On the bus a logical low level (0) is dominant and a logical high level (1) is recessive.

Voltage supply (Vsup) for an ECU should be between 7 V and 18 V. The limits for how the level of the bus is interpreted are shown in figure.

![logic levels](https://user-images.githubusercontent.com/115522470/199962857-e8120c41-05fb-4f82-8c36-e78047dccc90.jpg)

##### Data Transmission

The LIN network is described by a LDF (LIN Description File) which contains information about frames and signals. This file is used for creation of software in both master and slave.

The master node controls and make sure that the data frames are sent with the right interval and periodicity and that every frame gets enough time space on the bus. This scheduling is based on a LCF (LIN Configuration File) which is downloaded to the master node software.

All data is sent in a frame which contains a header, a response and some response space so the slave will have time to answer. Every frame is sent in a frame slot determined by the LCF.

Messages are created when the master node sends a frame containing a header. The slave node(s) then fills the frame with data depending on the header sent from the master.

![LIN FRAME](https://user-images.githubusercontent.com/115522470/199963047-d339ae0f-b31d-4c3c-9f01-ea245b473281.jpg)
-4f82-8c36-e78047dccc90.jpg)

There are three different ways of transmitting frames on the bus: unconditional, event triggered, and sporadic frames.

##### Unconditional Frames

This is the “normal” type of LIN communication. The master sends a frame header in a scheduled frame slot and the designated slave node fills the frame with data.

###### Event Triggered Frames

The purpose of this method is to receive as much information from slave nodes without overloading the bus with frames. An event triggered frame can be filled with data from more than one slave node. A slave only updates the data in an event triggered frame when the value has changed. If more than one slave wants to update data in the frame a collision occurs. The master should then send unconditional frames to each of the slaves starting with the one with the highest priority.

###### Sporadic Frames

This method provides some dynamic behavior to the otherwise static LIN protocol. The header of a sporadic frame is only sent from the master when it knows that a signal has been updated in a slave node. Usually the master fills the data bytes of the frame itself and the slave nodes will be the receivers of the information.

###### Definition of a Byte Field

The protocol is byte oriented which means that data is sent one byte at a time. One byte field contains a start bit (dominant), 8 data bits and a stop bit (recessive). The data bits are sent LSB first (least significant bit first). Data transmission can be divided into a master task and a slave task.

![Byte field](https://user-images.githubusercontent.com/115522470/199963407-8b78e92a-77de-4501-8840-1a0b772e4546.jpg)

##### The Master Task

The frame (header) that is sent by the master contains three parts; synch break, synch byte and an ID-field. Each part begins with a start bit and ends with a stop bit.

Synch break marks the start of a message and has to be at least 13 dominant bits long including start bit. Synch break ends with a “break delimiter” which should be at least one recessive bit.

![BRAKE FIELD](https://user-images.githubusercontent.com/115522470/199963615-fb0182f1-225a-4cce-95d3-000b7f7f04f7.jpg)
8e92a-77de-4501-8840-1a0b772e4546.jpg)

Synch byte is sent to decide the time between two falling edges and thereby determine the transmission rate which the master uses. The bit pattern is 0x55 (01010101, max number of edges). This is especially usable for compatibility with off-the-shelves slave nodes.

![Sync byte field](https://user-images.githubusercontent.com/115522470/199963810-4f0ebb83-4c52-4901-bfcc-48297ec88967.jpg)

The ID field contains a 6 bits long identifier and two parity bits. The 6 bit identifier contains information about sender and receiver and the number of bytes which is expected in the response. The parity bits are calculated as followed: parity P0 is the result of logic “XOR” between ID0, ID1, ID2 and ID4. Parity P1 is the inverted result of logic “XOR” between ID1, ID3, ID4 and ID5.

###### ID field

![id field](https://user-images.githubusercontent.com/115522470/199964072-3dd277cf-52cc-443c-af25-ac046a330721.jpg)

####### Frame length depending on ID
![frame length on id](https://user-images.githubusercontent.com/115522470/199964287-59e6b040-7ede-4239-8701-a100a6e33668.jpg)

The response (data field) from the slave can be 2, 4 or 8 bytes long depending on the two MSB (Most Significant Byte) of the identifier sent by the master. This ability came with LIN 2.0, older versions have a static length of 8 bytes.

###### The response data field

![response field](https://user-images.githubusercontent.com/115522470/199964473-fff48f45-4199-4e27-a1f2-4ba034e33408.jpg)

##### The Slave Task

The slave waits for synch break and then the synchronization between master and slave begins on synch byte. Depending on the identifier sent from the master the slave will either receive or transmit or do nothing at all. A slave that should transmit sends the number of bytes which the master has requested and then ends the transmission with a checksum field.

There are two different kinds of checksum. The classic checksum is used in LIN 1.3 and consists of the inverted eight bit sum of all (8) data bytes in a message. The new checksum used in LIN 2.0 also incorporates the protected identifier in the checksum calculation. The inverted eight bit sum is not the same as modulo-256. Every time the sum is greater than 256, then 255 is subtracted. Ex: 240+32=272 à 272-255=17 and so on…

To save power the slave nodes will be put in a sleep mode after 4 seconds of bus inactivity or if the master has sent a sleep command. Wakeup from sleep mode is done by a dominant level on the bus which all nodes can create.

##### Diagnostics

A new function in LIN 2.0 is the possibility of reading out diagnostic information from master and slave nodes. For this purpose two frame identifiers are used which both expect 8 data bytes: master request frame with id 60 (0x3c) and slave response with id 61 (0x3d). The first byte of a diagnostic frame is a NAD (Node Address for Diagnostic) which is a one byte long diagnostic node address. The value ranges from 1-127, while 0 is reserved and 128-255 are for free usage. There are three methods for diagnostics: signal based diagnostic, user defined diagnostic or use of a diagnostic transport layer.

##### Signal Based Diagnostic

The signal based diagnostics is the simplest method and uses standard signals in ordinary frames which represent:

•	Low overhead in slave nodes.

•	A standardized concept.

•	Static with no flexibility.

###### User Defined Diagnostic

The user defined diagnostic can be designed to fit the needs for a specific device but this also means that it will not be useful for general purposes. This method uses NADs in the range 128-255.

###### Diagnostic Transport Layer

This method is useful for a LIN network which is built on a CAN-based system where ISO diagnostics is used. NADs 1-127 are used. This method represents:

•	Low load on the master device.

•	Provides ISO diagnostics for LIN slaves.

•	Intended for more complex and powerful LIN nodes.

A diagnostic frame is called a PDU (Packet Data Unit) and starts with a NAD which addresses a certain node. Thereafter follows a PCI (Protocol Control Information) which handles the flow control. If the PCI-type is a Single Frame (SF) the whole diagnostic request command will fit into a single PDU. If the PCI-type is First Frame (FF) the next byte (LEN) will describe the number of bytes to come. The data bytes that do not fit into the first frame will be sent in the following frames with the PCI-type of Continuation Frames (CF). 

###### Compatibility with older versions (LIN 1.3)

A LIN 2.0 master is backward compatible with a LIN 1.3 slave (with limitations). Both LIN 2.0 and LIN 1.3 slaves can coexist in a network but some new features like the improved checksum and automatic baud rate detection have to be avoided.


# Day 4-Activity-3

## Advantages and Disadvantages of Different Automotive Protocols 

#### Advantages of LIN protocol:

•	As LIN is single wire-based interface, it reduces the cost and the complexity of implementation. 

•	LIN is self-synchronized and therefore no need of external oscillators.

•	LIN is the best and the most suited alternative to the CAN for applications that do not need high bandwidth and that are of low speed.

#### Disadvantages of LIN protocol:

•	Since LIN is low speed, it is not considered for safety and other important applications.

•	The communication is always initiated by the master and therefore when the master device fails then the whole bus gets failed.

•	There are no strong error checking mechanisms in LIN.

##### Advantages of CAN protocol:

•	CAN is used in different electrical environments which offers noise free transmission.

•	In CAN any node on the bus can initiate the communication and any node can respond. Therefore, failure of one device/node will not lead to the failure of the entire 
system.

•	CAN protocol offers strong error checking mechanisms.

##### Disadvantages of CAN protocol:

•	CAN bus is more expensive than that of LIN

•	Implementing CAN is bit complex than that of LIN due to increased number of nodes.

##### Advantages of FlexRay:

•	FlexRay is deterministic, fault-tolerant, and high-speed protocol than that of CAN protocol and therefore FlexRay is mostly used in safety critical applications.

•	Since FlexRay is a synchronous protocol, it synchronizes its nodes without external synchronous clock.

•	The star topology of the FlexRay reduces the exposed wire for the segment which in turn decreases the noise.

•	It has better error checking mechanism compared to LIN and CAN.

##### Disadvantages of FlexRay:

•	It is expensive compared to LIN and CAN protocols.

•	It is bit complex to implement

•	It has lower operating voltages

##### Advantages of Ethernet :

•	The fastest speed provide by Gigabit ethernet is of 1Gbps. The speed ranges from more than 10 times Fast Ethernet.

•	To form an Ethernet, we don’t need much cost. It is relatively inexpensive. Total cost induced is less.

•	In Ethernet, all the node have an equivalent privileges. It does not follow client-server architecture.

•	It does not require any switches or hubs

•	Maintenance and administration are simple.

•	The cable wont to connect systems in ethernet is strong to noise.

•	As it is strong to the noise, the standard of the info transfer doesn’t degrade. The data transfer quality is good.

•	With latest versions such as gigabit ethernet and wireless ethernet (IEEE 802.11ac/11ad) transfer speeds in data with the speed of 1-100Gbps.

##### Disadvantages of Ethernet :

•	It offers a nondeterministic service.

•	It doesn’t hold good for real-time applications because it requires deterministic service.

•	As priority packets cannot be set, it’s not suitable for a client-server architecture.

•	In an interactive application, data is extremely small and wish quick data transfer. In ethernet, there’s a limit of the minimum size of the frame to 46B. As a 
result, it’s not an honest choice for interactive applications.

•	If you’re using it for interactive applications, you’ve got to feed dummy data to form the frame size 46B which is mandatory.

•	Not suitable for traffic-intensive applications. In case the rate of traffic on the Ethernet goes up the efficiency of the Ethernet goes down.

•	It provides connectionless communication over the network.

•	The receiver cannot able to send any knowledge after receiving the packets.

•	If there’s any problem in ethernet, it’s difficult to troubleshoot what cable or node within the network causing an actual problem.

•	The 100Base-T4 version does not support full-duplex data communication mode.


# Day 4-Activity-4
### Collection of Log files

Collected Log files and uploaded

# Day 4-Activity-5

### Pick 1 log file & decrypt the frame

From the log file 20180820-mimos2home its observed some of the properties of the frame those are the software used in this are ecu manager and the software version  is l.1.14.0	and the Channel used is AFR Difference and the battery voltage.

The di£tierent channel	used in this log sheet are Battery Voltage, Engine Running Time, lignition timing, Current Duty Cycle, Load, Ignition Load, Shift Light1, Air Temp, Coolant Temp, MAP Source, Lambda Sensor 1 Throttle Position, Base Fuel Base Ignition, Target AFR, Fuel Air Temp Correction, Fuel Coolant Temp Correction, Ignition Coolant Temp Correction, Ignition Air Temp Correction, RPM, Transient Throttle Accel Coolant, Transient Throttle Enrich Sensitivity, Transient Throttle Enrich Decay Rate, Transient Throttle Persentage Async, Transient Throttle Percentage Enrich.

The maximum and minim.um valuds of some of the abO\'C parameters are n1entioned beloi.v
•	Maximum and minimw11value of AFR  is +•-150
•	Max.unnm andl  1inimtun value of running time is 10000 sec and O
seconds
•	Maximum m1d mininuun value Battery Voltage is 16000Y and 8000\'
•	Maximum and minimum Ignition Timing is 600 and -200





