# MAC Address Table

The MAC address table contains address information that the switch uses to forward traffic between the inbound and outbound ports. All MAC addresses in the address table are associated with one or more ports. When the switch receives traffic on a port, it searches the Ethernet switching table for the MAC address of the destination. If the MAC address is not found, the traffic is flooded out all the other ports associated with the VLAN. All the MAC address that the switch learns by monitoring traffic are stored in the dynamic address. A static address allows you to manually enter a MAC address to configure a specific port and VLAN.

## **Static MAC Address**

The address table lists the destination MAC address, the associated VLAN ID, and port number associated with the address. When you specify a static MAC address, you set the MAC address to a VLAN and a port; thus, it makes an entry into its forwarding table. These entries are then used to forward packets through the switch. Static MAC addresses along with the switch's port security allow only devices in the MAC address table on a port to access the switch.

![](https://lh3.googleusercontent.com/kkzXLL56eZtFL8U-B4DqWgyO6QZ5N_-d0M7zhjSc6ZDKAyWymJL6TS_l-SX4r8LIhiXFo2jpWPzFp2BDS0m-LUrkbkrvI0nGXMjK3iDf52ZteKUuGOdhq98sOSJDQUzE9_I1HXE)

|  |  |
| :--- | :--- |
| Index | Displays the index for the static MAC address table. |
| Port | Select the port where the MAC address entered in the previous field will be automatically forwarded. |
| VID | Enter the VLAN ID on which the IGMP Snooping querier is administratively enabled and for which the VLAN exists in the VLAN database. |
| MAC Address | Enter a unicast MAC address for which the switch has forwarding or filtering information. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## **Dynamic MAC Address**

The switch will automatically learn the device's MAC address and store it to the dynamic MAC address table. If there is no packet received from the device within the aging time, the switch adopts an aging mechanism for updating the tables from which MAC address entries will be removed from related network devices. The dynamic MAC address table shows the MAC addresses and their associated VLANs learned on the selected port.

![](https://lh3.googleusercontent.com/6nJR0SqPDHHPGxmb7gS4Ys9lXC4p02F8gWArtBVXmL7F9Gai_2rcPpwIWHOjw5P7k3lpZb0QFj2CZlLhkifVc7uS5_q5w3_FFjm4vV90qD_z-5Ttv_B6EETy14FWI_gDdHc_i-Q)

| **Items** | **Descriptions** |
| :--- | :--- |
| **Index** | **Displays the index for the dynamic MAC address table.** |
| **Port** | **Select the port to which the entry refers.** |
| **VID** | **Displays the VLAN ID corresponding to the MAC address.** |
| **MAC Address** | **Displays the MAC addresses that the switch learned from a specific port.** |

##  **Search MAC Address**

The function will help user to locate the connected device or the incoming port on the EWS switch for wireless connected clients to managed APs.

![](https://lh6.googleusercontent.com/KAqg5XP12bPGnrhjqjhsqQKXiiquNbZyRzzfrHJDPoBIt4-z8K3MbkwrzAZBlknp3HcZGU5DBdTVeHep4dvx3K1c1Kg2xI8sq_B7YiwOkyt_OY3-6MdD66kJolUz0kZMc7lWaGw)

