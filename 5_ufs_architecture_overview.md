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
