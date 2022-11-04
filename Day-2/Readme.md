
## Day-2 Activity-1

#### 1.	What can a node in active error and passive error do?

An Error Active node will transmit Active Error Flags when it detects errors. An Error Passive node will transmit Passive Error Flags when it detects errors. A node which is Bus Off will not transmit anything on the bus at all.

##### a)	If a node is busoff, how can it come out of that state?

Methods to recover from a Node CAN Bus Off state:

1) Automatically after the CAN controller generates an interrupt. 

2) Manually upon User request (ISO11898).  In both the above instances the bus turns back on after 128 occurrences of 11 consecutive Recessive Bits


##### b)  What is CAN inversion priority?

Priority inversion causes a high priority activity to get delayed for a long time, causing missed deadlines, timeouts, and all kinds of consequent faults. It happens when the high priority (and urgent) activity gets stuck behind a low priority (non-urgent) activity and lots of medium priority activities block the low priority activity, which is blocking the high priority activity.

## Day-2 Activity-2

#### 2.	Where can I add bit stuffing and the range, where can I do bit stuffing?
Bit stuffing is the insertion of non information bits into data. Note that stuffed bits should not be confused with overhead bits.
Bit stuffing may be used to synchronize several channels before multiplexing or to rate-match two single channels to each other.

![Bit stuffing](https://user-images.githubusercontent.com/115522470/199957358-2157ea00-a619-495e-b60c-570577cb48fe.jpg)

#### Applications of Bit Stuffing – 

1.	synchronize several channels before multiplexing

2.	rate-match two single channels to each other

3.	run length limited coding

##### Run length limited coding – To limit the number of consecutive bits of the same value(i.e., binary value) in the data to be transmitted. A bit of the opposite value is inserted after the maximum allowed number of consecutive bits.
Bit stuffing technique does not ensure that the sent data is intact at the receiver side (i.e., not corrupted by transmission errors). It is merely a way to ensure that the transmission starts and ends at the correct places.

## Day-2 Activity-3 and 4  is to Decipher the recived CAN frame		

The excel sheet of the solution is uploaded

## Day-2 Activity 5  is to create CAN 2.0A frames with different IDs 

The excel sheet of the solution is uploaded


