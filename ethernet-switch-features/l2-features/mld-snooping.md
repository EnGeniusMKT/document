# MLD Snooping

**Multicast Listener Discovery \(MLD\) Snooping operates on the IPv6 traffic level for discovering multicast listeners on a directly attached port and performs a similar function to IGMP Snooping for IPv4. MLD snooping allows the switch to examine MLD packets and make forwarding decisions based on content. MLD Snooping limits IPv6 multicast traffic by dynamically configuring the switch port so that multicast traffic is forwarded only to those ports that wish to receive it. This reduces the flooding of IPv6 multicast packets in the specified VLANs. Both IGMP and MLD Snooping can be active at the same time.**  


## **Global Settings**

![](https://lh6.googleusercontent.com/G4PfLQXyaiKE8zU43BblBQHzBf6kvvV1oe78OPzQyx1fgkttndjoowy29y51TVHLfX8faQTW_EYn_jOqQfvwnRoI8Xrfto7yLsbodDGLeKHJpZuZgL2NS3P8DKHnaZB4HcNhhF8)

<table>
  <thead>
    <tr>
      <th style="text-align:left">&lt;b&gt;&lt;/b&gt;</th>
      <th style="text-align:left">&lt;b&gt;&lt;/b&gt;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">MLD Snooping Status</td>
      <td style="text-align:left">
        <p>Select to Enable or Disable MLD Snooping on the switch. The switch</p>
        <p>snoops all MLD packets it receives to determine which segments should
          receive packets directed to the group address when enabled.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">MLD Snooping Version</td>
      <td style="text-align:left">Select the MLD version you wish to use. If an MLD packet received by the
        interface has a version higher than the specified version, this packet
        will be dropped.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>MLD Snooping Report</p>
        <p>Suppression</p>
      </td>
      <td style="text-align:left">The report suppression feature limits the amount of membership reports
        the member sends to multicast capable routers.</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.

## **VLAN Settings**

If the Fast Leave feature is not used, a multicast querier will send a GS-query message when an MLD group leave message is received. The querier stops forwarding traffic for that group only if no host replies to the query within the specified timeout period. If Fast Leave is enabled, the switch assumes that only one host is connected to the port. Therefore, Fast Leave should only be enabled on a port if it is connected to only one MLD-enabled device.

![](https://lh3.googleusercontent.com/QNyLQeRDvDBQSungh-VDy4MVpmCUMK7TcHJY4-zMhfm4eUJ4sw53Mfic3suazxndfedAa9G1RRvtTI1S_qwQYqXOehPdCWl3bt8i_JepIkfvnbfhsofXK5yc79R5ofPvwU2xcnw)

Fast Leave does not apply to a port if the switch has learned that a multicast querier is attached to it. Fast Leave can improve bandwidth usage for a network which frequently experiences many MLD host add and leave requests.

| \*\*\*\* | \*\*\*\* |
| :--- | :--- |
| VLAN ID | Displays the VLAN ID. |
| MLD Snooping Status | Select to enable or disable the MLD snooping feature for the specified VLAN ID. |
| Fast Leave | Enables or disables the MLD snooping Fast Leave feature for the specified VLAN ID. Enabling this feature allows the switch to immediately remove the Layer 2 LAN port from its forwarding table entry upon receiving an MLD leave message without first sending out an MLD group-specific \(GS\) query to the port. |

Select from the drop-down list whether to enable or disable MLD Snooping. Next, select to enable or disable Fast Leave for the specified VLAN ID.

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## Group List

The Group List displays the VLAN ID, IPv6 address, and members port in the MLD Snooping List.

![](https://lh3.googleusercontent.com/E0rV9VvEtWy2EIo75NaRe33e4mpcp5lVAVEcyuwgdj7ZpvXE3IYNGwCyCwI4jmWo3EvENRgw0OaHzW0C2m9SQOiwhvLXGi4GUeWKvXHfGpLuo6MacK5MhQB5r9ugPF9L9ltWE7M)

## **Router Settings**

The Router Settings feature shows the learned multicast router attached port if the port is active and a member of the VLAN. Select the VLAN ID you would like to configure and enter the static and forbidden ports for the specified VLAN IDs that are utilizing MLD Snooping. All MLD packets snooped by the switch will be forwarded to the multicast router reachable from the port.

![](https://lh5.googleusercontent.com/vDBwKgjP1yueb9IcfYp26pfkxy-MJmpYKBp9MwHVL6-8KuRBfN5wNS3SPH7nDFFGtBEQtsI-a6hHBbBXUXrNKHAUY7umaRfMXKzCQ44lq-RDbXXCmDVcBxj5Pw4BF0NDpv60AvY)

| \*\*\*\* | \*\*\*\* |
| :--- | :--- |
| VLAN ID | Displays the VLAN ID. |
| Router Ports Auto Learned | The switch will automatically detect the presence of a multicast router and forward MLD packets accordingly. |
| Dynamic Port List | Displays router ports that have been dynamically configured. |
| Static Port List | Designates a range of ports as being connected to multicast-enabled routers. Ensure that all the packets will reach the multicast-enabled router. |
| Forbidden Port List | Designates a range of ports as being disconnected to multicast-enabled routers. Ensures that the forbidden router port will not propagate routing packets out. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


