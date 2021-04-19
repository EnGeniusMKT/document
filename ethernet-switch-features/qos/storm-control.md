# Storm Control

Storm Control limits the amount of Broadcast, Unknown Multicast, and Unknown Unicast frames accepted and forwarded by the switch. Storm Control can be enabled per port by defining the packet type and the rate that the packets are transmitted at. The switch measures the incoming Broadcast, Unknown Multicast, and Unknown Unicast frames rates separately on each port, and discards the frames when the rate exceeds a user-defined rate.

![](https://lh6.googleusercontent.com/tYSTas7gvyAJ3YXwi3QpkvstBmexQr2-UVOipYa1wL7c77r7-tJ5tPfhzrB2Fz2sKKsoRjzs8xhHCuSoY0XMLuzA6gTX_Exg_6ZRy3akJ__q8XDgvoCpxZ-a4IO4nRJ8qcLdKWQ)

| Items | Descriptions |
| :--- | :--- |
| Port | Displays the ports for which the Storm Control information is displayed. |
| Status | Select whether Storm Control is Enabled or Disabled ingress on the interface. |
| Broadcast | Enter the broadcast rate in kilobits per second. The Gigabit Ethernet ports have a maximum speed of 1000000 kilobits per second. If the rate of broadcast traffic ingress on the interface increases beyond the configured threshold, the traffic is dropped. |

| Items | Descriptions |
| :--- | :--- |
| Unknown Multicast | Enter the Unknown Multicast rate in kilobits per second. The gigabit Ethernet ports have a maximum speed of 1000000 kilobits per second. If the rate of broadcast traffic ingress on the interface increases beyond the configured threshold, the traffic is dropped. |
| Unknown Unicast | Enter the Unknown Unicast rate in kilobits per second. The gigabit Ethernet ports have a maximum speed of 1000000 kilobits per second. If the rate of broadcast traffic ingress on the interface increases beyond the configured threshold, the traffic is dropped. |

Click **Apply** to update the system settings.  


