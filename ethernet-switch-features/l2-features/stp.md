# STP

The Spanning Tree Algorithm \(STA\) can be used to detect and disable network loops, and to provide backup links between switches. This allows the switch to interact with other bridging devices in your network to ensure that only one route exists between any two stations on the network and provide backup links which automatically take over when a primary link goes down.

**Spanning Tree Protocol \(STP\)** provides a tree topology for the switch. There are different types of Spanning tree versions supported, including Spanning Tree Protocol \(STP\) IEEE 802.1D, Multiple Spanning Tree Protocol \(MSTP\) IEEE 802.1w, and Rapid Spanning Tree Protocol \(RSTP\) IEEE 802.1s. Please note that only one spanning tree can be active on the switch at a time.

## **Global Settings** 

Spanning Tree Protocol \(STP\) is a Layer 2 protocol that runs on switches. Spanning Tree Protocol \(STP\) allows you to ensure that you do not create loops when you have redundant paths in the network. STP provides a single active path between two devices on a network in order to prevent loops from being formed when the switch is interconnected via multiple paths.

STP uses a distributed algorithm to select a bridging device that serves as the root for the spanning tree network. It does this by selecting a root port on each bridging device to incur the lowest path cost when forwarding a packet from that device to the root device. It then selects a designated bridging device from each LAN which incurs the lowest path cost when forwarding a packet from that LAN to the root device. Next, all ports connected to designated bridging devices are assigned as designated ports. After determining the lowest cost spanning tree, it enables all root ports and designated ports, disabling all other ports. Network packets are therefore only forwarded between root ports and designated ports, eliminating any possible network loops. STP provides a single active path between two devices on a network in order to prevent loops from being formed when the switch is interconnected via multiple paths.

Once a stable network topology has been established, all bridges listen for Hello Bridge Protocol Data Units \(BPDUs\) transmitted from the Root Bridge of the Spanning Tree. If a bridge does not receive a Hello BPDU after a predefined interval \(known as the Maximum Age\), the bridge will assume that the link to the Root Bridge is down and unavailable. This bridge then initiates negotiations with other bridges to reconfigure the network to reestablish a valid network topology.

Loops occur when alternate routes exist between hosts. Loops in an extended network can cause the switch to forward traffic indefinitely, resulting in increased traffic and reducing network efficiency. Once the STP is enabled and configured, primary links are established, and duplicated links are blocked automatically. The reactivation of the blocked links is also automatic.

STP provides a tree topology and other Spanning tree versions supported include STP, Multiple Spanning Tree Protocol \(MSTP\), and Rapid Spanning Tree Protocol \(RSTP\). Please note that only one spanning tree can be active on the switch at a time. The default setting is RSTP.

![](https://lh5.googleusercontent.com/-YXJjCEGhqJNUzMxaNeX5RgZKEnXELNz-pw3rlbFt22O-M8_vc6D3m1Bmy9zPWGT8_FqdsEF8oWH19jxU32VYCcRahtDh7okWNDQr5YzCNCnOT5DfvR1cdWflj8Sqj13KQLFkrs)

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">STP</td>
      <td style="text-align:left">Select whether to enable or disable the spanning tree operation on the
        switch.</td>
    </tr>
    <tr>
      <td style="text-align:left">Force Version</td>
      <td style="text-align:left">
        <p>Select the Force Protocol Version parameter for the switch.</p>
        <p>STP (Spanning Tree Protocol): IEEE 802.1D</p>
        <p>RSTP (Rapid Spanning Tree Protocol): IEEE 802.1w</p>
        <p>MSTP (Multiple Spanning Tree Protocol): IEEE 802.1s</p>
      </td>
    </tr>
  </tbody>
</table>

Multiple Spanning Tree Protocol \(MSTP\) defined in IEEE 802.1s, enables multiple VLANs to be mapped to reduce the number of spanning-tree instances needed to support many VLANs. If there is only one VLAN in the network, a single STP works fine.

If the network contains more than one VLAN, however, the logical network configured by a single STP would work, but it becomes more efficient to use the alternate paths available by using an alternate spanning tree for different VLANs or groups of VLANs. MSTP \(which is based on RSTP for fast convergence\) is designed to support independent spanning trees based on VLAN groups. MSTP provides multiple forwarding paths for data traffic and enables load balancing.

STP and RSTP prevent loops from forming by ensuring that only one path exists between the end nodes in your network. RSTP is designed as a general replacement for the slower, legacy STP. RSTP is also incorporated into MSTP. With STP, convergence can take up to a minute to complete in a larger network. This can result in the loss of communication between various parts of the network during the convergence process so STP can subsequently lose data packets during transmission.

RSTP on the other hand is much faster than STP. It can complete a convergence in seconds, so it greatly diminishes the possible impact the process can have on your network compared to STP. RSTP reduces the number of state changes before active ports start learning, predefining an alternate route that can be used when a node or port fails and retain the forwarding database for ports insensitive to changes in the tree structure when reconfiguration occurs.

Select whether to enable or disable the Spanning Tree function for the switch. Next, select whether you wish to enable STP, RSTP, or MSTP. Again, please note that only one Spanning tree function can be active at a time.  


Click **Apply** to save settings.  


## **Root Bridge**

The Root Bridge serves as an administrative point for all Spanning Tree calculations to determine which redundant links to block in order to prevent network loops. From here, you can view all the information regarding the Root Bridge within the STP.

All other decisions in a spanning tree network, such as ports being blocked and ports being put in a forwarding mode, are made regarding a root bridge. The root bridge is the “root” of the constructed “tree” within a spanning tree network. Thus, the root bridge is the bridge with the lowest bridge ID in the spanning tree network. The bridge ID includes two parts: the bridge priority \(2 bytes\) and the bridge MAC address \(6 bytes\). The 802.1d default bridge priority is 32768. STP devices exchange Bridge Protocol Data Units \(BPDUs\) periodically. All bridges “listen” for Hello BPDUs \(Bridge Protocol Data Units\) transmitted from the root bridge. If a bridge does not get a Hello BPDU after a predefined interval \(called the Maximum Age\), the bridge assumes that the link to the root bridge is down. The bridge then initiates negotiations with other bridges to reconfigure the network to re-establish a valid network topology.

![](https://lh6.googleusercontent.com/3MvwQ66XpJ--5XBdZdvYWRHiP-qICxm0gjuUbWGBSoANgHlD4dDIgLpbKRyQAkG2ClGwq_wrLf3UW9utUyF6wPo1rSk8LYmB87hgJtI7JUVaOviD4MLeh0JrWR52e9nlx7r8MNc)

| **Items** | **Descriptions** |
| :--- | :--- |
| **Root Address**                     | **Displays the root bridge MAC address. Root in root bridge refers to the base of the spanning tree, which the switch could be configured for.** |
| **Priority** | **Displays the priority for the bridge. When switches are running STP, each is assigned a priority. After exchanging BPDUs, the switch with the lowest priority value becomes the root bridge.** |
| **Forward Delay** | **Displays the Switch Forward Delay Time. This is the time \(in seconds\) the root switch will wait before changing states \(called listening to learning\).** |
| **Maximum Age** | **Displays the bridge Switch Maximum Age Time. This is the amount of time a bridge waits before sending a configuration message. The default is 20 seconds.** |
| **Hello Time** | **Displays the Switch Hello Time. This is the amount of time a bridge remains in a listening and learning state before forwarding packets. The default is 15 seconds.** |

## **CIST Instance Settings**

The Common Instance Spanning Tree \(CIST\) protocol is formed by the spanning tree algorithm running among bridges that support the IEEE 802.1w, IEEE 802.1s, and IEEE 802.1D standards. A Common and Internal Spanning Tree \(CIST\) represents the connectivity of the entire network and it is equivalent to a spanning tree in an STP/RSTP.

The CIST inside a Multiple Spanning Tree instance \(MST\) region is the same as the CST outside a region. All regions are bound together using a CIST, which is responsible for creating loop-free topology across regions, whereas the MSTI controls topology inside regions. CST instances allow different regions to communicate between themselves. CST is also used for traffic within the region for any VLANs not covered by a MSTI. In an MSTP-enabled network, there is only one CIST that runs between MST regions and single spanning tree devices. A network may contain multiple MST regions and other network segments running RSTP. Multiple regions and other STP bridges are interconnected using a single CST.

![](https://lh4.googleusercontent.com/B2NLLa2k7gFDn2d4NvubNTHYckwzyuue2MrOTlQEI-xBquviFDmsu7h54hWeE2dzTfvPt0_bmDbOk7e5JlSPRcvXKKMxhsZsqMqvvMvQCh0EJZ-aMgsGV_qoC4fTMdLJUIAM6ZA)

Enter the information to set up CIST for the switch:  


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Items</b>
      </th>
      <th style="text-align:left"><b>Descriptions</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Priority</td>
      <td style="text-align:left">Select from the list to specify the priority of the switch for comparison
        in the CIST. CIST priority is an important criterion in determining the
        root bridge. Under the same condition, the switch with the highest priority
        will be chosen as the root bridge. A lower value has a higher priority.
        The default value is 32768 and should be an exact divisor of 4096.</td>
    </tr>
    <tr>
      <td style="text-align:left">Maximum Hop</td>
      <td style="text-align:left">Used to set the number of hops between devices in a spanning tree region
        before the BPDU packet sent by the switch is discarded. Each switch on
        the hop count will reduce the hop count by one until the value reaches
        zero. The switch will then discard the BDPU packet and the information
        held for the port will age out. The user may set a hop countfrom 6 to 40.
        The default value is: 20.</td>
    </tr>
    <tr>
      <td style="text-align:left">Forward Delay</td>
      <td style="text-align:left">
        <p>Enter the bridge forward delay time, which indicates the amount of time
          in seconds that a bridge remains in a listening and learning state before
          forwarding packets. The value must be greater or equal to (Bridge Max</p>
        <p>Age/2) + 1. The time range is from 4 seconds to 30 seconds. The default
          value is 15 seconds.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Maximum Age</td>
      <td style="text-align:left">
        <p>The Max Age may be set to ensure that old information does not endlessly
          circulate through redundant paths in the network, preventing the effective
          propagation of new information. Set by the Root Bridge, this value will
          aid in determining that the switch has spanning tree configuration values
          consistent with other devices on the bridged</p>
        <p>LAN. The user may choose a time between 6 and 40 seconds. The default
          value is 20 seconds.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TX Hold Count</td>
      <td style="text-align:left">Enter the maximum number of Hello packets transmitted per interval. The
        count can be specified from 1 to 10. The default is 6.</td>
    </tr>
    <tr>
      <td style="text-align:left">Hello Time</td>
      <td style="text-align:left">Enter the switch&#x2019;s Hello Time. This is the interval between two
        transmissions of BPDU packets sent by the Root Bridge to verify that it
        is the Root Bridge. The Hello Time range is from 1 to 10 seconds. The default
        Hello Time is 2 seconds.</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.

## **CIST Port Settings**

Use the CIST Ports Settings page to configure and view STA attributes for interfaces when the spanning tree mode is set to STP or RSTP. You may use a different priority or path cost for ports of the same media type to indicate a preferred path or edge port to indicate if the attached device can support fast forwarding or link type to indicate a point-to-point connection or shared-media connection.

![](https://lh6.googleusercontent.com/u0ShA1rEaN8JBXjIUCpzwRr98Fy7xHTx4WE-KxblseLs9mlyZbzwqFDUPksPwps0UUr9_9BXGfHzUV07Hc5Aj3xbdGf5ktsJXTpfl6d5vRMbFx45X-0iDPuU2WIlaJ4SEjt2VxA)



| Items | Descriptions |
| :--- | :--- |
| Port | Port or trunked port identifier. |
| Priority | Defines the priority used for this port in the Spanning Tree Algorithm. If the path cost for all ports on a switch is the same, the port with the highest priority \(i.e., lowest value\) will be configured as an active link in the Spanning Tree. This makes a port with higher priority less likely to be blocked if the Spanning Tree Algorithm is detecting network loops. When more than one port is assigned the highest priority, the port with lowest numeric identifier will be enabled. The range is from 0 to 240, in steps of 16; and the default is 128. |
| Internal Path Cost Conf/Oper | The Internal Path Cost setting allows you to specify the relative cost of sending spanning tree traffic through the interface to adjacent bridges within a spanning tree region. |
| External Path Cost Conf/Oper | The External Path Cost setting is used to calculate the cost of sending spanning tree traffic through the interface to reach an adjacent spanning tree region. The spanning tree algorithm tries to minimize the total path cost between each point of the tree and the root bridge. |
| Designated Root Bridge | Displays the root bridge for the CST. It is comprised using the bridge priority and the base MAC address of the bridge. |
| Internal Root Cost | This is the cost to the CIST regional root in a region. |
| External Root Cost | External root cost is the cost to the CIST root. |
| Regional Root Bridge | This is the bridge identifier of the CST regional root. It is made up using the bridge priority and the base MAC address of the bridge. |
| Internal Port Cost | Enter the cost of the port. |
| Edge Port Conf/Oper | Displays the edge port state. |
| Designated Bridge | This is the bridge identifier of the bridge of the designated port. It is made up using the bridge priority and the base MAC address of the bridge. |
| Port Role | Each MST bridge port that is enabled is assigned a port role within each spanning tree. The port role will be one of the following values: Root Port, Designated Port, Alternate Port, Backup Port, Master Port, or Disabled. |
| Port State | The forwarding state of this port. The state parameters are Discarding, Learning, Forwarding, or Disabled. |

Click **Apply** to update the system settings.

## **MST Instance Settings**

Multiple Spanning Tree Protocol, or MSTP enables the grouping of multiple VLANs with the same topology requirements into one Multiple Spanning Tree Instance \(MSTI\). MSTP then builds an Internal Spanning Tree \(IST\) for the region containing commonly configured MSTP bridges. Instances are not supported in STP or RSTP. Instead, they have the same spanning tree in common within the VLAN. MSTP provides the capability to logically divide a Layer 2 network into regions. Every region can contain multiple instances of spanning trees. In MSTP, all the interconnected bridges that have the same MSTP configuration comprise an MST region.

A Common Spanning Tree \(CST\) interconnects all adjacent MST regions and acts as a virtual bridge node for communications between STP or RSTP nodes in the global network. MSTP connects all bridges and LAN segments with a single Common and Internal Spanning Tree \(CIST\). The CIST is formed as a result of the running spanning tree algorithm between switches that support STP, RSTP, and MSTP protocols. Once you specify the VLANs you wish to include in a Multiple Spanning Tree Instance \(MSTI\), the protocol will automatically build an MSTI tree to maintain connectivity among each of the VLANs. MSTP maintains contact with the global network because each instance is treated as an RSTP node in the Common Spanning Tree \(CST\).

Click the Edit button to configure the MST settings. Next, enter information for the VLAN List and choose the priority you wish to use from the drop-down list.

![](https://lh6.googleusercontent.com/z3A8R2XsN0t3mZ3bROsw48WzzlwBYiTodmQLvFXOdfhIiF8XPoNc5ypm8sJu1cM6GyWg3ut-UkmaYqX7xQrnpQAywPz1fJjezJhk6RZx3yyGEhE7BPEH_sfno8H5UCg3xptjoZA)

| MST ID | Displays the ID of the MST group that is created. A maximum of 15 groups can be set for the switch. |
| :--- | :--- |
| VLAN List | Enter the VLAN ID range for the configured VLANs to associate with the MST ID. The VLAN ID number range is from 1 to 4094. |
| Priority | Select the bridge priority value for the MST. When switches or bridges are running STP, each is assigned a priority. After exchanging BPDUs, the switch with the lowest priority value becomes the root bridge. The default value is 32768. The range is from 0 to 61440. The bridge priority is a multiple of 4096. |
| Regional Root Bridge | This is the bridge identifier of the CST regional root. It is made up using the bridge priority and the base MAC address of the bridge. |
| Internal Root Cost | Displays the path cost to the designated root for the MST instance. |
| Designated Bridge | Displays the bridge identifier of the bridge with the designated port. It is made up using the bridge priority and the base MAC address of the bridge. |
| Root Port | Displays the port that accesses the designated root for MST instance. |

  
****Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them**.**

## **MST Port Settings**

This page displays the current MSTI configuration information for the switch. From here you can update the port configuration for an MSTI ID. If a loop occurs, the MSTP function will use the port priority to select an interface to put into the forwarding state. Set a higher priority value for ports you wish to be selected for forwarding first. In instances where the priority value is identical, the MSTP function will implement the lowest MAC address into the forwarding state and other interfaces will be blocked. Note that lower priority values mean higher priorities for forwarding packets.

![](https://lh5.googleusercontent.com/msb1btRRYS865Uqer7nWHX6aDDBkdRbS-Jjae_2LTO24WgQRGQEjlIInBQSyPht_-2UUKjDMmOsBhsCJXBy9axLPt73ZiWjaU-2Zs9AWXQ0v_a3_mjoo9zmWBujFD0Gqp0cKBAY)

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Items</b>
      </th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">MST ID</td>
      <td style="text-align:left">Displays the ID of the MST group that is created. A maximum of 15 groups
        can be set for the switch.</td>
    </tr>
    <tr>
      <td style="text-align:left">Port</td>
      <td style="text-align:left">Displays port or trunked port ID.</td>
    </tr>
    <tr>
      <td style="text-align:left">Priority</td>
      <td style="text-align:left">Select the bridge priority value for the MST. When switches or bridges
        are running STP, each is assigned a priority. After exchanging BPDUs, the
        switch with the lowest priority value becomes the root bridge. The bridge
        priority is a multiple of 4096. If you specify a priority that is not a
        multiple of 4096, the priority is automatically set to the next lowest
        priority that is a multiple of 4096. For example, if you set the priority
        to any value from 0 through 4095, the priority is set to 0. The default
        priority is 32768. The valid range is from 0 to 61440.</td>
    </tr>
    <tr>
      <td style="text-align:left">Internal Path Cost Conf</td>
      <td style="text-align:left">The Internal Path Cost setting allows you to specify the relative cost
        of sending spanning tree traffic through the interface to adjacent bridges
        within a spanning tree region.</td>
    </tr>
    <tr>
      <td style="text-align:left">Internal Path Cost Oper</td>
      <td style="text-align:left">Displays the operation cost of the path from this bridge to the root bridge.</td>
    </tr>
    <tr>
      <td style="text-align:left">Regional Root Bridge</td>
      <td style="text-align:left">This is the bridge identifier of the CST regional root. It is made up
        using the bridge priority and the base MAC address of the bridge.</td>
    </tr>
    <tr>
      <td style="text-align:left">Internal Root Cost</td>
      <td style="text-align:left">Displays the path cost to the designated root for the selected MST instance.</td>
    </tr>
    <tr>
      <td style="text-align:left">Designated Bridge</td>
      <td style="text-align:left">Displays the bridge identifier of the bridge for the designated port.
        It is made up using the bridge priority and the base MAC address of the
        bridge.</td>
    </tr>
    <tr>
      <td style="text-align:left">Internal Port Cost</td>
      <td style="text-align:left">This parameter is set to represent the relative cost of forwarding packets
        to specified ports when an interface is selected within an STP instance.
        Selecting this parameter with a value in the range of 1 to 200000000 will
        set the quickest route when a loop occurs. A lower internal cost represents
        a quicker transmission. Selecting 0 (zero) for this parameter will set
        the quickest optimal route automatically for an interface.</td>
    </tr>
    <tr>
      <td style="text-align:left">Port Role:</td>
      <td style="text-align:left">Each MST bridge port that is enabled is assigned a port role for each
        spanning tree. The port role is one of the following values: Root, Designated,
        Alternate, Backup, Master, or Disabled.</td>
    </tr>
    <tr>
      <td style="text-align:left">Port State</td>
      <td style="text-align:left">
        <p>Indicates the current STP state of a port. If enabled, the port state
          determines what forwarding action is taken regarding traffic. The possible
          port states are:</p>
        <p>Disabled: STP is disabled on the port. The port forwards traffic while
          learning MAC addresses.</p>
        <p>Blocking: The port is blocked and cannot be used to forward traffic or
          learn MAC addresses.</p>
        <p>Listening: The port is in listening mode. The port cannot forward traffic
          or learn MAC addresses in this state.</p>
        <p>Learning: The port is in learning mode. The port cannot forward traffic.
          However, it can learn new MAC addresses.</p>
        <p>Forwarding: The port is in forwarding mode. The port can forward traffic
          and learn new MAC addresses in this state.</p>
      </td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.

  


