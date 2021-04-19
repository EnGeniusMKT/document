# Connecting the Switch

## **Discovery with a DHCP Server**

Use the procedures below to set up the switch within a network that uses DHCP.

1. Connect the switch to your network \(DHCP enabled\) and connect the supplied power cord to the switch and plug the other end into an electrical outlet. Verify the power LED indicator is lit on the switch.
2. Wait for the switch to completely boot up, which might take a minute.
3. Connect one end of a Category 5/6 Ethernet cable into the Gigabit \(10/100/1000Mpbs\) Ethernet port on the switch front panel and the other end to the Ethernet port on the computer. Verify that the LED on the Ethernet ports of the switch are **Green**.
4. Once your computer is on, ensure that your TCP/IP is set to **On** or **Enabled**. Open **Network Connections** and then click **Local Area Connection**. Select Internet Protocol Version 4 \(TCP/IPv4\). Click **DHCP** under Auto-Configuration and click **Apply** to save the settings.
5. On the DHCP server, find and write down the IP address allocated to the device. Use this IP address to access the management interface.
6. A login screen will appear. By default, the username is **admin**, and the password is **password**. Enter the current password of the switch and then click **Login**. To make access to the web-based management interface more secure, it's highly recommended that you change the password to something more unique.

## **Discovery without a DHCP Server**

{% hint style="info" %}
This section describes how to set up the switch in a network without a DHCP server. If your network has no DHCP service, you must assign a static IP address to your switch in order to log in to the web-based management interface.
{% endhint %}

1. Connect the supplied power cord to the switch and plug the other end into an electrical outlet. Verify the power LED indicator is lit on the switch.
2. Wait for the switch to completely boot up, which might take a minute.
3. Connect one end of a Category 5/6 Ethernet cable into the gigabit \(10/100/1000Mbps\) Ethernet port on the switch front panel and the other end to the Ethernet port on the computer. Verify that the LED lights on the Ethernet ports of the switch are **Green**.
4. Once your computer is on, ensure that your TCP/IP is set to **On** or **Enabled**. Open **Network Connections** and then click **Local Area Connection**. Select **Internet Protocol Version 4 \(TCP/IPv4\)**.
5. If your computer is already on a network, ensure that you have set it to a static IP address on the interface \(Example: **192.168.0.239** and the subnet mask address as **255.255.255.0**\).
6. Open a web browser on your computer. In the address bar of the web browser, enter **192.168.0.239** and press **Enter**.
7. A login screen will appear. By default, the username is **admin**, and the password is **password**. Enter the current password of the switch and then click **Login**. To make access to the web-based management interface more secure, change the password to something more unique.
8. Click **IP Settings** under the **System Menu** and select **Static IP** to configure the IP settings of the management interface.
9. Enter the IP address, Subnet Mask, and Gateway.
10. Click **Apply** to update the system.



