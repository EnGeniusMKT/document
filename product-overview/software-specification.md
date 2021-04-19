# Technical Specification

### **Wireless Management** 

* Access Point Auto Discovery and Provisioning
* Access Point Auto IP Assignment
* Access Point Group Management
* Visual Topology View
* Floor Plan View
* Map View
* Access Point Status Monitoring
* Wireless Client Monitoring
* Wireless Traffic & Usage Statistics
* Real-time Throughput Monitoring
* Bulk Firmware Upgrade Capability
* Remote Access Point Rebooting
* Fast Roaming
* Band Steering
* Traffic Shaping
* Intelligent Diagnostics
* Access Point Device Name Editing
* Access Point Radio Settings
* RSSI Threshold
* Access Point Client Limiting
* Wireless Security \(WEP, WPA/WPA2 Enterprise, WPA/WPA2 PSK\)
* VLANs for Access Point- Multiple SSIDs
* Guest Network
* Secure Control Messaging \(SSL Certificate\)
* Local MAC Address Database
* Remote MAC Address Database \(RADIUS\)
* Configuration Import / Export



### **L2 Features**

* 802.3ad Link Aggregation
  *  Maximum of 8 groups/8 ports per group
* Port Mirroring
  * One-to-One
  * Many-to-One
* Spanning Tree Protocol
* * 802.1D Spanning Tree Protocol \(STP\)
  * 802.1w Rapid Spanning Tree Protocol \(RSTP\)
  * 802.1s Multiple Spanning Tree Protocol \(MSTP\)
* MAC Address Table
  * 8K entries
* Static MAC Address
  * 256 entries
* 802.1ab Link Layer Discovery Protocol
* IGMP Snooping
  * IGMP v1/v2/v3 Snooping
  * Supports 256 IGMP groups
  * IGMP per VLAN
  * IGMP Snooping Querier
  * IGMP Snooping Fast Leave
* MLD Snooping
  * MDL Snooping v1/v2
  * Supports 256 MLD groups
  * IGMP per VLAN
* Jumbo Frame
  * Up to 9216 bytes
* 802.3x Flow Control
* 802.3az Energy Efficient Ethernet



### **VLAN**

* 802.1Q support
* VLAN Group
  * Max 4094 static VLAN groups
* Voice VLAN

### **QoS**

* 802.1p Quality of Service
  * 8 queues per port
* Queue Handling
  * Strict
  * Weighted Round Robin \(WRR\)
* QoS based on:
  * 802.1p Priority
  * DSCP 
* Bandwidth Control
  * Port-based \(Ingress/Egress, 64 Kbps~1000 Mbps\)
* Broadcast/Unknown Multicast/ Unknown Unicast Storm Control 



### **Access Control List \(ACL\)**

* Layer 2/3
  * Support maximum 32 entries \(ACL\)
  * Support maximum 256 entries \(ACE\)
* ACL based on:
  * MAC address
  * VLAN ID
  * 802.1p priority
  * Ethertype
  * IP address
  * Protocol type
  * DSCP

### **Security**

* 802.1X
  * Guest VLAN
  * Port-based Access Control
* Supports RADIUS Authentication
* Port Security
  * Up to 256 MAC Addresses per port
* Port Isolation
* DoS Attack Prevention
* BPDU Attack Prevention

### **Monitoring**

* Port Statistics
* System Log
* RMON

### **Management**

* Web Graphical User Interface \(GUI\)
* Command Line Interface \(CLI\)
* BootP/DHCP Client/DHCPv6 Client
* SSH Server
* Telnet Server
* TFTP Client
* HTTPS
* SNMP
  * Supports v1/v2c/v3
* SNMP Trap
* SNTP
* Configuration restore/backup

\*\*\*\*

### **Diagnostic**

* Cable Diagnostic
* Ping Test
* Trace Route

### **MIB/RFC Standards**

* RFC1213
* RFC1493
* RFC1757
* RFC2674
* RFC 2863

### **Operating Temperature**

* 0 to 40°C \(EWS2910P, EWS2908P\)
* 0 to 50°C \(EWS5912FP, EWS7928P, EWS1200-28TFP, EWS7926EFP, EWS7952P, EWS7952FP\)

### **Storage Temperature**

* -40°C to 70°C

### **Humidity \(Non-condensing\)**

* 5% - 95%

### **Dimensions \(W x D x H\)**

* EWS2908P: 240x105x27mm
* EWS2910P: 240x105x27mm
* EWS5912FP: 330x230x44mm
* EWS7928P: 440x260x44mm
* EWS1200-28TFP: 440x260x44mm
* EWS7926EFP: 440x260x44mm
* EWS7952P: 440x310x44mm
* EWS7952FP: 440x310x44mm





