5 UFS ARCHITECTURE OVERVIEW
===
# 5.1 UFS Top level Architecture

Figure 5.1 shows the Universal Flash Storage (UFS) top level architecture.

![Figure 5.1 — UFS Top Level Architecture](Figure 5.1.bmp "Figure 5.1 — UFS Top Level Architecture")  
**Figure 5.1 — UFS Top Level Architecture**

UFS communication is a layered communication architecture. It is based on SCSI SAM architectural model [SAM].

**Application Layer**  

The application layer consists of the UFS command set layer (UCS), the device manager and the Task Manager. The UCS will handle the normal commands like read, write, and so on. UFS may support multiple command sets. UFS is designed to be protocol agnostic. This version UFS standard uses SCSI as the baseline protocol layer. A simplified SCSI command set was selected for UFS. UFS Native command set can be supported when it is needed to extend the UFS functionalities.

The Task Manager handles commands meant for command queue control. The Device Manager will provide device level control like Query Request and lower level link-layer control.

**UFS Device Manager**

The device manager has the following two responsibilities:

* Handling device level operations.

* Managing device level configurations.

Device level operations include functions such as device sleep, device power down, power management and other device specific operations. These mainly involve power management of the device.

Device level configuration is managed by the device manager by maintaining and storing a set of descriptors. The device manager would handle commands like query request which is meant for modifying and retrieving configuration information of the device.

**Service Access Points**

As seen from the diagram the device manager interacts with lower layers using the following two service
access points
* UDM_SAP
* UIO_SAP

UDM_SAP is the service access point exposed by the UTP for the device manager to allow handling of device level operations and configurations. For example the handling of query request for descriptors would be done using this service access point. The following diagram depicts the usage of the service access point.

UIO_SAP is the service access point exposed by the UIC layer for the device manager to trigger the reset of the UIC layer and also to service a reset request from the host. The following diagram depicts the usage of the service access point.

**Figure 5.3 — Usage of UIO_SAP**

**UIO_SAP**

UIO_SAP is the service access point exposed by the UIC layer. In UniPro, UIO_SAP corresponds to DME_SAP. The DME_SAP provides service primitives including one for resetting the entire UniPro protocol stack and one for UFS device reset, etc.

* DME_RESET : It is used when the UniPro stack has to be reset.
* DME_ENDPOINTRESET: It is used when UFS host wants the UFS device to perform a reset.

For the detailed internal mechanism, refer the UniPro specification [MIPI-UniPro] released by MIPI (MIPI is Mobile Industry Processor Interface).

**UDM_SAP**

UDM_SAP is the service access point exposed by the UTP layer to the Device Manager for UFS device level functions. UDM_SAP corresponds to the Query Request and Query Response functions defined by the UFS UTP layer.

For further details refer to the following subclauses: 10.7.9 “Query Function transport protocol services”, 10.5.10 “QUERY REQUEST UPIU”, and 10.5.11 “QUERY RESPONSE UPIU”.

**UFS Transport Protocol Layer**

The UFS Transport Protocol (UTP) layer provides services for the higher layer . UPIU is “UFS Protocol Information Unit” which is exchanged between UTP layers of UFS host and UFS device. For example, if host side UTP receives the request from application layer or Device Manager, UTP generates an UPIU for that request and transports the generated UPIU to the peer UTP in UFS device side. The UTP layer provides the following three access points.

1. UFS Device Manager Service Access Point (UDM_SAP) to perform the device level management like descriptor access.

2. UTP Command Service Access Point (UTP_CMD_SAP) to transport commands.

3. UTP Task Management Service Access Point (UTP_TM_SAP) to transport task-management function like “abort task” function.

**<a name="UFS Interconnect Layer"></a>UFS Interconnect Layer**

The lowest layer is UFS Interconnect Layer (UIC) which handles connection between UFS host and UFS device. UIC consists of MIPI UniPro and MIPI M-PHY. The UIC provides two service access points to upper layer. The UIC Service Access Point (UIC_SAP) to transport UPIU between UFS host and UFS device. The UIC_SAP corresponds to T_SAP in UniPro. The UIC IO control Service Access Point (UIO_SAP) to manage UIC. The UIO_SAP corresponds to DME_SAP in UniPro.

**UFS Topology**

This version of the standard assumes that only one device is connected to an UFS port. Other topologies may be defined in future versions of the standard.