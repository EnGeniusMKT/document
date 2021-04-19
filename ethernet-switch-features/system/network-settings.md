# Network Settings

The network setting screen contains fields for assigning IP addresses and Management VLAN. IP addresses are either defined as static or are retrieved using the Dynamic Host Configuration Protocol \(DHCP\). DHCP assigns dynamic IP addresses to devices on a network. DHCP ensures that network devices can have a different IP address every time the device connects to the network.

To access the page, click **IP Settings** under the **System** menu.

## **IPv4**

Select whether to you wish to enable Static or DHCP for auto-configuration. Next, enter the information for the IP address, gateway, and DNS servers.

![](https://lh4.googleusercontent.com/4m2bnrrVr5Qja-4Da6wvXFgDmTyARMWy_Uh525fBtUb3CdRvxKl_FI2XfZSLQB45cJAQSjm5RlX9hfsbAz2TuYGUpkl0-fwx3SuBtcT1ibdSR-tqzV_3QM1XL5cimk_viD20aC8)

| Items | Descriptions |
| :--- | :--- |
| ![C:\Users\User\AppData\Local\Microsoft\Windows\INetCache\Content.Word\UM\_important.png](https://lh3.googleusercontent.com/dRNhusbSG4CNasDxY48r3C-fFaMbuowQ7tIhM9fUuS4_vtjv07wwZAjH_iBwShUw9mo1e5Ngz9Hs-y5gLphlewrNj3UzB2OweHK-pyVjutaCJBGsIZ9YFVJiIZO5tLOYfH16EPc) | Important: If the device fails to retrieve an IP address through DHCP, the default IP address is **192.168.0.239** and the factory default subnet mask is **255.255.255.0.** |
| Dynamic IP Address \(DHCP\) | Enables the IP address to be configured automatically by the DHCP server. Select this option if you have a DHCP server that can assign the switch an IP address, subnet mask, default gateway IP address, and a domain name server IP address automatically. Selecting this field disables the IP Address, Subnet Mask, and Gateway fields. |
| Static IP Address | Allows the entry of an IP address, subnet mask, and a default gateway for the switch. Select this option if you don't have a DHCP server or if you wish to assign a static IP address to the switch. |
| IP Address | This field allows the entry of an IPv4 address to be assigned to this IP interface. Enter the IP address of your switch in dotted decimal notation. The factory default value is: 192.168.0.239 |
| Subnet Mask | A subnet mask separates the IP address into the network and host addresses. A bitmask that determines the extent of the subnet that the switch is on. This should be labeled in the form: xxx.xxx.xxx.xxx, where each xxx is a number \(represented in decimals\) between 0 and 255. The value should be 255.0.0.0 for a Class A network, 255.255.0.0 for a Class B network, and 255.255.255.0 for a Class C network, but custom subnet masks are allowed. Enter the IP subnet mask of your switch in dotted decimal notation. The factory default value is: 255.255.255.0 |
| Gateway | Enter an IP address that determines where packets with a destination address outside the current subnet should be sent. This is usually the address of a router or a host acting as an IP gateway your network is not part of an Intranet, or you do not want the switch to be accessible outside your local network, you can leave this field blank. |
| DNS Server \(Domain Name System\) | Used for mapping a domain name to its corresponding IP addresses and vice versa. Enter a DNS IP address in order to be able to use a domain name to access the switch instead of using an IP address. |

Click **Apply** to save settings.

## **IPv6**

IPv6 is an upgraded version to IPv4, providing more available IP addresses as well as other benefits. To access the switch over an IPv6 network you must first configure it with IPv6 information \(IPv6 prefix, prefix length, and default gateway\). To configure IPv6 for the switch, select whether to you wish to enable **Auto-Configuration, Static,** or **DHCPv6 Client**. Next, enter the information for the IP address, range, and gateway.

![](https://lh6.googleusercontent.com/SMYkRnrSLJj1XbvmcGmZmolFa9OsEOKIeo0iw5-fWnz4vM_QgKeFR56Vgj7iD2KbMtuWG0VMzY5etxPHVwKN7aF8e-6NhhKPChtT6iZfLSfS8kbo69r4BIPFCqa1u-kJbG5h8J4)

| Items | **Descriptions** |
| :--- | :--- |
| IPv6 State | Select whether you wish to enable Auto Configuration, DHCPv6 Client, or Static for the IPv6 address. |
| Auto Configuration | Use this option to set the IPv6 address for the IPv6 network interface in Auto Configuration. The switch will automatically generate and use a globally unique IPv6 address based on the network prefix and its Ethernet MAC address. |
| DHCPv6 Client | This enables the IP address to be configured automatically by the DHCP server. Select this option if you have an IPv6 DHCP server that can assign the switch an IPv6 address/prefix and a default gateway IP address. |
| Static | Allows the entry of an IPv6 address/prefix and a default gateway for the switch. Select this option if you wish to assign static IPv6 address information to the switch. |
| IPv6 Address | This field allows the entry of an IPv6 address/prefix to be assigned to this IP interface. |
| Gateway | Set the default gateway IPv6 address for the interface. Enter the default gateway IPv6 address. |

Click **Apply** to save settings.

Users can select the Management VLAN ID from drop-down list and please note all ports connected to APs on the switch should be configured to the same VLAN ID as this EWS switch’s management VLAN ID to let AP management function works properly.

![](https://lh3.googleusercontent.com/gDfUFPdu0PFfNnhM87MzaqfxbLjsqmQEj4bh42AdM9knvP51zG9PtFM-PgoXkdDiLC8TG9a-cDQDP5yh-Q8Kf4sLCCq9gy6oF3LRN5PKqy9tmBQPFDcpkPmEJUIVJPOhyq41bc4)

