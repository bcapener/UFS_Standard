3 TERMS AND DEFINITIONS
======

For the purposes of this standard, the terms and definitions given in the document included in clause 2 “Normative Reference” and the following apply.

# 3.1 Acronyms

|Acronym||
|--|--|
|BOOT_ID |Boot Identification Number|
|CDB |Command Descriptor Block|
|CPORT| A CPort is a Service Access Point on the UniPro Transport Layer (L4) within a Device that is used for Connection-oriented data transmission|
|CRB| Command Request Block|
|DEVID| Device ID|
|DID| Device ID|
|DMA| Direct Memory Access|
|DSC| Digital Still Camera|
|EOF| End of Packet|
|GB| Gigabyte|
|HCI| Host Controller Interface|
|HPQ| High Priority Queue|
|KB| Kilobyte|
|LUN| Logical Unit Number|
|MB| Megabyte|
|MIPI| Mobile Industry Processor Interface|
|MP3| MPEG-2 Audio Layer 3|
|Mbps| Mega bit per second|
|NA| Not applicable|
|NU| Not used|
|PDU| Protocol Data Unit|
|PLL| Phase-Locked Loop|
|PMP| Portable media player,|
|PTR| Pointer|
|PWM| Pulse Width Modulation|
|RFU| Reserved for future use|
|RPMB| Replay Protected Memory Block|
|SBC| SCSI Block Commands|
|SID| Segment ID|
|SDU| Service Data Unit|
|SOF| Start of Packet|
|SPC| SCSI Primary Commands|
|SRB| SCSI Request Block|
|TB| Terabyte|
|T_PDU| MIPI Unipro Protocol Data Unit|
|T_SDU| MIPI Unipro protocol Service Data Unit|
|UFS| Universal Flash Storage|
|UMPC| Ultra-Mobile PC|
|UniPro| Unified Protocol|
|UPIU| UFS Protocol Information Unit|
|UTP| UFS Transport Protocol|
|IU| Information Unit|

# 3.2 Terms and Definitions

**Address Nexus**: An address nexus is a combination of parameters that identify a connection between one
bus device to another. For the UFS bus and address nexus consists of a bus device ID for the source, a bus
device ID for the destination and a logical unit number for the destination.  

**Byte**: An 8‐bit data value with most significant bit labeled as bit 7 and least significant bit as bit 0.  

**Command Descriptor Block**: The structure used to communicate commands from an application client to a device server. A CDB may have a fixed length of up to 16 bytes or a variable length of between 12 and 260 bytes.  

**Command Request Block**: The bytes the make up a SCSI command that are encapsulated within a SCSI
Request Block  

**Device**: An addressable device on the UFS bus usually a target that contains at least one LUN  

**Device ID**: The bus address of a UFS device  

**Doubleword**: A 32‐bit data value with most significant bit labeled as bit 31 and least significant bit as bit 0.  

**Dword**: A 32‐bit data value, a Doubleword.  

**Gigabyte**: 1,073,741,824 or 230 Bytes.  

**Host**: An addressable device on the UFS bus which is usually the main CPU that hosts the UFS bus.  
