
## Day 4-Activity-1

### Understanding the evolution of Ethernet

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

## Day 4-Activity:3
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


