# LLDP

Link Layer Discovery Protocol \(LLDP\) is the IEEE 802.1AB standard for switches to advertise their identity, major capabilities, and neighbors on the 802 LAN. LLDP allows users to view the discovered information to identify system topology and detect faulty configurations on the LAN. LLDP is essentially a neighbor discovery protocol that uses Ethernet connectivity to advertise information to devices on the same LAN and store information about the network. The information transmitted in LLDP advertisements flow in one direction only: from one device to its neighbors. This information allows the device to quickly identify a variety of other devices, resulting in a LAN that interoperates smoothly and efficiently.

LLDP transmits information as packets called LLDP Data Units \(LLDPDUs\). A single LLDPDU is transmitted within a single 802.3 Ethernet frame. A basic LLDPDU consists of a set of Type-Length-Value elements \(TLV\), each of which contains information about the device. A single LLDPDU contains multiple TLVs. TLVs are short information elements that communicate complex data. Each TLV advertises a single type of information.

## **Global Settings**

![](https://lh4.googleusercontent.com/LufQtNT6HYIXCm4fRpjpoZqgoi6HJb-M0umEk-Q6UBdF07SyjnKxfWH4fnLi9TL5imph_9JWkwL4_ZXOosWCo4w6sYa9QwZYKzHeRklHQNC_r2ukcb08IM0vox07H6fwitjSVLs)

Select whether to enable or disable the LLDP feature on the switch. Next, enter the Transmission Interval, Holdtime Multiplier, Reinitialization Delay parameter, and the Transmit Delay parameter. When finished, click Apply to update the system settings.  


| State | Select Enabled or Disabled to activate LLDP for the switch. |
| :--- | :--- |
| Transmission Interval | Enter the interval at which LLDP advertisement updates are sent. The default value is 30. The range is from 5 to 32768. |
| Holdtime Multiplier | Enter the amount of time that LLDP packets are held before packets are discarded and measured in multiples of the Advertised Interval. The default is 4. The range is from 2 to 10. |
| Reinitialization Delay | Enter the amount of time of delay before reinitializing LLDP. The default is 2. The range is from 1 to 10. |
| Transmit Delay | Enter the amount of time that passes between successive LLDP frame transmissions. The default is 2 seconds. The range is from 1 to 8191 seconds. |

## **Local Device**

LLDP devices must support chassis and port ID advertisement, as well as the system name, system ID, system description, and system capability advertisements. Here, you can view detailed LLDP information for the switch.

![](https://lh6.googleusercontent.com/WH_9qoTa5JPzhYLwvZ39cyRWe_OJMseYz50Fbbq7HqW7XZ_shjChJE4pVR7N5ocOlKSEo-uPi7qgm_nwDDi5goJ2zN9EqRS-H2stQOX4tLDnmhxdgn7amGVK0lLhFJCiyEgwu8U)

| **Chassis ID Subtype** | **Displays the chassis ID type.** |
| :--- | :--- |
| **Chassis ID** | **Displays the chassis ID of the device transmitting the LLDP frame.** |
| **System Name** | **Displays the administratively assigned device name.** |
| **System Description** | **Describes the device.** |
| **Capabilities Supported** | **Describes the device functions.** |
| **Capabilities Enabled** | **Describes the device functions.** |
| **Port ID Subtype** | **Displays the port ID type.** |

## **Remote Device**

**LLDP devices must support chassis and port ID advertisement, as well as the system name, system ID, system description, and system capability advertisements. From here you can view detailed LLDP Information for the remote device.**

![](https://lh6.googleusercontent.com/Dj2OTIa-2kVrR5naGD_6oXb1oXYJvcWxQUNjhiSISZvo9GDNeT1u8WzymyVtFdFY5B9RTOE80ZnJctZZBZDIDWzptk1MHH9A0riDxLcLId1aCe45Q8V7dzk7Om2Qaz3q7SlvfcM)

| Items | **Descriptions** |
| :--- | :--- |
| **Port** | **Displays the port.** |
| **Chassis ID Subtype** | **Displays the chassis ID type.** |
| **Chassis ID** | **Displays the chassis ID of the device that is transmitting the LLDP frame.** |
| **Port ID Subtype** | **Displays the port ID type.** |
| **Remote ID** | **Displays the remote ID.** |
| **System Name** | **Displays the administratively assigned device name.** |
| **Time to Live** | **Displays the time to live.** |
| **Auto-Negotiation Supported** | **Displays state for the auto-negotiation supported.** |
| **Auto-Negotiation Enabled** | **Displays state for the auto-negotiation enabled.** |
| **Auto-Negotiation Advertised Capabilities** | **Displays the type of auto-negotiation advertised capabilities.** |
| **Operational MAU Type** | **Displays the type of MAU.** |
| **802.3 Maximum Frame Size** | **Displays the maximum size of 802.3 maximum frame.** |
| **802.3 Link Aggregation Capabilities** | **Displays the 802.3 Link Aggregation capabilities.** |
| **802.3 Link Aggregation Status** | **Displays the status of 802.3 Link Aggregation.** |
| **802.3 Link Aggregation Port ID** | **Displays the port ID of 802.3 Link Aggregation.** |

