4 INTRODUCTION
======

Universal Flash Storage (UFS) is a simple, high performance, mass storage device with a serial interface. It is primarily for use in mobile systems, between host processing and mass storage memory devices. The following is the summary of the UFS features.

# 4.1 General Features
* Target performance
 * High speed GEARs (1)
   * Support for GEAR1 is mandatory
   * Support for GEAR2 is mandatory
   * Support for GEAR3 is optional
* Target host applications
  * Mobile phone, UMPC, DSC, PMP, MP3 and any other applications that require mass storage, bootable mass storage, and external card
* Target device types
 * External card
   * Micro size for mobile and portable devices
   * Full size or adaptor for DSC and large devices
 * Embedded packages
   * Mass storage and bootable mass storage
 * Future expansion of device class types
   * I/O devices, camera, wireless, … , etc.
* Topology
 * One device per UFS port. A topology to support multiple devices on a single interface is planned for future revision
* UFS Layering
 * UFS Command Set Layer (UCS)
   * Simplified SCSI command set based on SBC and SPC. UFS will not modify these SBC and SPC Compliant commands. Option for defining UFS Native command and future extension exist.
 * UFS Transport Protocol Layer (UTP)
   * JEDEC to define the supported protocol layer, i.e., UTP for SCSI. This does not exclude the support of other protocol in UFS Transport Protocol Layer.
 * UFS Interconnect Layer (UIC)
   * MIPI UniProSM [MIPI-UniPro] is adopted for data link layer
   * MIPI M-PHY SM [MIPI-M-PHY ] is adopted for physical layer  

NOTE 1 See 6.5.1 for details.

