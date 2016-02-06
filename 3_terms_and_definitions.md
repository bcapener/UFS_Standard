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

# 3.3 Keywords
Several keywords are used to differentiate levels of requirements and options, as follow:  
Can - A keyword used for statements of possibility and capability, whether material, physical, or causal
(can equals is able to).
Expected - A keyword used to describe the behavior of the hardware or software in the design models
assumed by this standard. Other hardware and software design models may also be implemented.
Ignored - A keyword that describes bits, bytes, quadlets, or fields whose values are not checked by the
recipient.
Mandatory - A keyword that indicates items required to be implemented as defined by this standard.
May - A keyword that indicates a course of action permissible within the limits of the standard (may
equals is permitted).
Must - The use of the word must is deprecated and shall not be used when stating mandatory
requirements; must is used only to describe unavoidable situations.
Optional - A keyword that describes features which are not required to be implemented by this standard.
However, if any optional feature defined by the standard is implemented, it shall be implemented as
defined by the standard.
Reserved - A keyword used to describe objects—bits, bytes, and fields—or the code values assigned to
these objects in cases where either the object or the code value is set aside for future standardization.
Usage and interpretation may be specified by future extensions to this or other standards. A reserved
object shall be zeroed or, upon development of a future standard, set to a value specified by such a
standard. The recipient of a reserved object shall not check its value. The recipient of a defined object
shall check its value and reject reserved code values.
Shall - A keyword that indicates a mandatory requirement strictly to be followed in order to conform to
the standard and from which no deviation is permitted (shall equals is required to). Designers are required
to implement all such mandatory requirements to assure interoperability with other products conforming
to this standard.
Should - A keyword used to indicate that among several possibilities one is recommended as particularly
suitable, without mentioning or excluding others; or that a certain course of action is preferred but not
necessarily required; or that (in the negative form) a certain course of action is deprecated but not
prohibited (should equals is recommended that).
Will - The use of the word will is deprecated and shall not be used when stating mandatory requirements;
will is only used in statements of fact.