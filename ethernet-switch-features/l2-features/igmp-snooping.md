# IGMP Snooping

Internet Group Management Protocol \(IGMP\) Snooping allows a switch to forward multicast traffic intelligently. Multicasting is used to support real-time applications such as video conferencing or streaming audio. A multicast server does not have to establish a separate connection with each client. It merely broadcasts its service to the network, and any host that wishes to receive the multicast register with their local multicast switch.

A multicast group is a group of end nodes that want to receive multicast packets from a multicast application. After joining a multicast group, a host node must continue to periodically issue reports to remain a member. Any multicast packets belonging to that multicast group are then forwarded by the switch from the port.

A switch supporting IGMP Snooping can passively snoop on IGMP Query, Report, and Leave packets transferred between IP Multicast switches and IP Multicast hosts to determine the IP Multicast group membership. IGMP Snooping checks IGMP packets passing through the network and configures multicasting accordingly. Based on the IGMP query and report messages, the switch forwards traffic only to the ports that request the multicast traffic. It enables the switch to forward packets of multicast groups to those ports that have validated host nodes. The switch can also limit flooding of traffic to IGMP designated ports. This improves network performance by restricting the multicast packets only to switch ports where host nodes are located. IGMP Snooping significantly reduces overall Multicast traffic passing through your switch. Without IGMP Snooping, Multicast traffic is treated in the same manner as a broadcast transmission, which forwards packets to all ports on the network.

| IGMPv1 | Defined in RFC 1112. An explicit join message is sent to the switch, but a timeout is used to determine when hosts leave a group. |
| :--- | :--- |
| IGMPv2 | Defined in RFC 2236. Adds an explicit leave message to the join message so that the switch can more easily determine when a group has no interested listeners on a LAN. |
| IGMPv3 | Defined in RFC 3376. Support for a single source of content for a multicast group. |

## **Global Settings**

Click to enable or disable the IGMP Snooping feature for the switch. Next, select whether you wish to use V2 or V3. Finally, select whether you wish to enable or disable the Report Suppression feature for the switch.

![](https://lh3.googleusercontent.com/wryc4JF_JW0idw-lwE2UUC9KdjC3sIBG77wvIKeH09b3dwRng-ksRhoZvxTuxR6UOPbBMlrPwMOWeea0XcpBlJhlN8m3AX9pYTnkCM_nGydbptKf07lAabW4Xw54iDNX1ScU62w)



| Items | Descriptions |
| :--- | :--- |
| Status | Select to enable or disable IGMP Snooping on the switch. The switch snoops all IGMP packets it receives to determine which segments should receive packets directed to the group address when enabled. The default setting is: Disabled. |
| Version | Select the IGMP version you wish to use. If an IGMP packet received by the interface has a version higher than the specified version, this packet will be dropped. |
| Report Suppression | Select whether Report Suppression is Enabled or Disabled for IGMP Snooping. The Report Suppression feature limits the amount of membership reports the member sends to multicast capable routers. |
| Unregistered IPMCv4 Forward Action | Select either Flood or Drop for IP Multicast forward action. |

Click **Apply** to update the system settings.  


## **VLAN Settings**

Use the IGMP Snooping VLAN Settings to configure IGMP Snooping settings for VLANs on the system. The switch performs IGMP Snooping on VLANs that send IGMP packets. You can specify the VLANs that IGMP Snooping should be performed on. Choose from the drop-down box whether to enable or disable IGMP Snooping. Next, choose to enable or disable Fast Leave for the VLAN ID.

![](https://lh4.googleusercontent.com/Ns1ajN1_sli-rDa_PuxalVHLxSaGUVaH1evf11a4u-qUuLOUsHPbmcegF_VeCPamgXEVZ_PfTyCH7tzQSJTrMIAfd4-6AXEAaRiAz9ZIa807f9oQwa_WH44_b0lV2GDFEz8-6o8)

| Items | Descriptions |
| :--- | :--- |
| VLAN ID | Displays the VLAN ID. |
| IGMP Snooping Status | Enables or disables the IGMP Snooping feature for the specified VLAN ID. |
| Fast Leave | Enables or disables the IGMP Snooping Fast Leave for the specified VLAN ID. Enabling this feature allows the switch to immediately remove the Layer 2 LAN port from its forwarding table entry upon receiving an IGMP leave message without first sending out IGMP group-specific \(GS\) queries to the port. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


If Fast Leave is not used, a multicast querier will send a GS-query message when an IGMPv2/v3 group leave message is received. The querier stops forwarding traffic for that group only if no host replies to the query within the specified timeout period. If Fast Leave is enabled, the switch assumes that only one host is connected to the port. Therefore, Fast Leave should only be enabled on a port if it is connected to only one IGMP-enabled device.

Fast Leave is supported only with IGMPv2 or IGMPv3 Snooping when IGMP Snooping is enabled. Fast Leave does not apply to a port if the switch has learned that a multicast querier is attached to it.

Fast Leave can improve bandwidth usage for a network which frequently experiences many IGMP host add and leave requests.

## Querier Settings

IGMP Snooping requires that one central switch to periodically query all end devices on the network to announce their multicast memberships and this central device is the IGMP querier. The snooping switch sends out periodic queries with a time interval equal to the configured querier query interval. The IGMP query keeps the switch updated with the current multicast group membership information. If the switch does not receive the updated membership information, then it will stop forwarding multicasts to specified VLANs.

![](https://lh3.googleusercontent.com/-_IZU0u68h1Aupuqmbnd50NkvigieogwzfYApqaO-oVsKiQx8Yr_rUA2aBZ2h5Wkg2D7EFIqW4PcSDgwfsO0l-CpWD9PB21F4Gu1wjtPfCOsV6tZozvTCH5ns35MOPBbxPgFfwU)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">VLAN ID</td>
      <td style="text-align:left">Displays the VLAN ID.</td>
    </tr>
    <tr>
      <td style="text-align:left">Querier State</td>
      <td style="text-align:left">
        <p>Select whether to enable or disable the IGMP querier state for the specified
          VLAN ID.</p>
        <p>A querier can periodically ask their hosts if they wish to receive multicast
          traffic. The querier feature will check whether hosts wish to receive multicast
          traffic when enabled. An elected querier will assume the role of querying
          the LAN for group members and then propagate the service requests onto
          any upstream multicast switch to ensure that it will continue to receive
          the multicast service. This feature is only supported for IGMPv1 and v2
          snooping.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Querier Version</td>
      <td style="text-align:left">Enter the version of IGMP packet that will be sent by this port. If an
        IGMP packet received by the port has a version higher than the specified
        version, this packet will be dropped.</td>
    </tr>
    <tr>
      <td style="text-align:left">Robustness</td>
      <td style="text-align:left">Provides fine-tuning to allow for expected packet loss on a subnet. It
        is used in calculating the following IGMP message intervals. The default
        is 2.</td>
    </tr>
    <tr>
      <td style="text-align:left">Interval</td>
      <td style="text-align:left">Enter the amount of time in seconds between general query transmissions.
        The default is 125 seconds.</td>
    </tr>
    <tr>
      <td style="text-align:left">Oper Interval</td>
      <td style="text-align:left">Displays the IGMP Interval of the operational querier.</td>
    </tr>
    <tr>
      <td style="text-align:left">Max Response Interval</td>
      <td style="text-align:left">Enter the maximum response time used in the queries that are sent by the
        snooping querier. The default is 10 seconds.</td>
    </tr>
    <tr>
      <td style="text-align:left">Oper Max Response Interval</td>
      <td style="text-align:left">Displays the maximum response time used in the queries that are sent by
        the snooping querier.</td>
    </tr>
    <tr>
      <td style="text-align:left">Last Member Query Counter</td>
      <td style="text-align:left">Enter the number of the operational last member querier.</td>
    </tr>
    <tr>
      <td style="text-align:left">Oper Last Member Query Counter</td>
      <td style="text-align:left">Enter the number of IGMP group-specific queries sent before the switch
        assumes there are no local members.</td>
    </tr>
    <tr>
      <td style="text-align:left">Last Member Query Interval</td>
      <td style="text-align:left">Enter the time between two consecutive group-specific queries that are
        sent by the querier including those sent in response to leave group messages.
        You might lower this interval to reduce the amount of time it takes a querier
        to detect the loss of the last member of a group.</td>
    </tr>
    <tr>
      <td style="text-align:left">Oper Last Member Query Interval</td>
      <td style="text-align:left">Displays the operational last member query interval sent by the elected
        querier.</td>
    </tr>
  </tbody>
</table>

  
Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## **Group List**

The Group List displays VLAN ID, group IP address, and members port in the IGMP Snooping list.

![](https://lh3.googleusercontent.com/TOq1IrSApmi_XnMMQybqWwbaeNc0bO_ty6_TqYGQZe5OdpWcsruBI833n54GuOIkP63oisfWRnpBdKav7mmB-LzSqUMhELLl3IcUDPbM0tVxfznCAuf6yjo0JBMjti3h3-hM_5I)

## **Router Settings**

The Router Settings shows the learned multicast router attached port if the port is active and a member of the VLAN. Select the VLAN ID you would like to configure and enter the Static and Forbidden ports for the specified VLAN IDs. All IGMP packets snooped by the switch will be forwarded to the multicast router reachable from the port.

![](https://lh5.googleusercontent.com/ULMcRkAaUrHZcoeEtC_-P0SzJbdUencjcMutlSzO7Bp-VS5ZDI5cPYxo3sxwkg1PbIZSViIN3UPrzQHLDYtjFdKBke2aB7COnY2qMSncXRczkXDWmvjUT5mYxJ8rKR9dh95S0jg)

| Items | Descriptions |
| :--- | :--- |
| VLAN ID | Displays the VLAN ID. |
| Router Ports Auto Learned | The switch will auto detect the presence of a multicast router and forward IGMP packets accordingly. |
| Dynamic Port List | Displays router ports that have been dynamically configured. |
| Forbidden Port List | Designates a range of ports as being disconnected to multicast-enabled routers. Ensures that the forbidden router port will not propagate routing packets out. |
| Static Port list | Designates a range of ports as being connected to multicast-enabled routers. Ensures that all the packets will reach the multicast-enabled router. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  
  


