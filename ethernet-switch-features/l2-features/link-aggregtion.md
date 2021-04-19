# Link Aggregtion



A Link Aggregation Group \(LAG\) optimizes port usage by linking a group of ports together to form a single, logical, higher-bandwidth link. Aggregating ports multiplies the bandwidth and increases port flexibility for the switch. Link Aggregation is most used to link a bandwidth intensive network device \(or devices\), such as a server, to the backbone of a network.

The participating ports are called members of a port trunk group. Since all ports of the trunk group must be configured to operate in the same manner, the configuration of one port of the trunk group is applied to all ports of the trunk group. Thus, you will only need to configure one of any of the ports in a trunk group. A specific data communication packet will always be transmitted over the same port in a trunk group. This ensures the delivery of individual frames of a data communication packet will be received in the correct order. The traffic load of the LAG will be balanced among the ports according to aggregate arithmetic. If the connections of one or several ports are broken, the traffic of these ports will be transmitted on the normal portsto guarantee reliable connection.

When you aggregate ports, the ports and LAG must fulfill the following conditions:

* All ports within a LAG must be the same media/format type.
* A VLAN is not configured on the port.
* The port is not assigned to another LAG.
* The Auto-negotiation mode is not configured on the port.
* The port is in full-duplex mode.
* All ports in the LAG have the same ingress filtering and tagged modes.
* All ports in the LAG have the same back pressure and flow control modes.
* All ports in the LAG have the same priority.
* All ports in the LAG have the same transceiver type.
* Ports can be configured as LACP ports only if the ports are not part of a previously configured LAG.

LACP is a dynamic protocol which helps to automate the configuration and maintenance of LAGs. The main purpose of LACP is to automatically configure individual links to an aggregate bundle, while adding new links and helping to recover from link failures if the need arises. LACP can monitor to verify if all the links are connected to the authorized group. LACP is a standard in computer networking; hence, LACP should be enabled on the switch's trunk ports initially for both the participating switches/devices that support the standard, to use it.

## **Port Trunking**

Port trunking allows you to assign physical links to one logical link that functions as a single, higher-speed link, providing dramatically increased bandwidth. Use port trunking to bundle multiple connections and use the combined bandwidth as if it were a single larger “pipe.”

{% hint style="info" %}
**Important:  
You must enable Trunk Mode before you can add a port to a trunk group.**
{% endhint %}

![](https://lh5.googleusercontent.com/YQ-kyNp5f031AwNPnrFbm5h2e2jc4PLCI_wTAXBSjQQpu6kWmwtoDYwiQL__1eEmSxWQdF_zEJDVuUyn7Re1-tU0PgdlM_wnV2XIQwh8ejjJ-fdsqvZNhsdSXbz7jM8E0zZyfJk)

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
      <td style="text-align:left">Group</td>
      <td style="text-align:left">Displays the number of the given trunk group. You can utilize up to 8
        link aggregation groups with each group consisting up to 8 ports on the
        switch.</td>
    </tr>
    <tr>
      <td style="text-align:left">Active Ports</td>
      <td style="text-align:left">Displays the active participating members of the trunk group.</td>
    </tr>
    <tr>
      <td style="text-align:left">Member Port</td>
      <td style="text-align:left">
        <p>Select the ports you wish to add to the trunk group. Up to eight ports
          per group can be assigned.</p>
        <p>Static: The Link Aggregation is configured manually for specified trunk
          group.</p>
        <p>LACP: The Link Aggregation is configured dynamically for specified trunk
          group.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Mode</td>
      <td style="text-align:left">LACP allows for the automatic detection of links in a port trunking group
        when connected to a LACP-compliant switch. You will need to ensure that
        both the switch and the device it&#x2019;s connected to are in the same
        mode for them to function; otherwise, they will not work. Static configuration
        is used when connecting to a switch that does not support LACP.</td>
    </tr>
  </tbody>
</table>

**Click the Apply button** ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) **to accept the changes or the Cancel button** ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) **to discard them.**  
Assign a system priority to run with Link Aggregation Control Protocol \(LACP\), which will become a backup link if another link goes down. The lowest system priority can make decisions about which ports it is actively running in case a link goes down. If two or more ports have the same LACP port priority, the port with the lowest physical port number will be selected as the backup port. If a LAG already exists with the maximum number of allowed port members, and LACP is subsequently enabled on another port using a higher priority than an existing member, the newly configured port will replace the existing port member that has a lower priority. A smaller number indicates a higher priority level. The range is from 0-65535 and default is 32768.

![](https://lh5.googleusercontent.com/evueiMgsTlLzbTwWitQDBmRQ0SmjdJbIEKMaLlUoZhn8aUTtkhI9za5_ARDCW0cQsr7g0STXkzqYeJkaVd91Swj096NaOOslRczLH-rFcDL5gTpdzpsoCsBR9VZaEjjnKr9OQXs)

Click **Apply** to save settings.  


|  | \*\*\*\* |
| :--- | :--- |
| **System Priority** | **Enter the LACP priority value to the system. The default is 32768 and the range is from 1 to 65535.** |

## **LACP Settings**

Link Aggregation Control Protocol \(LACP\) allows the exchange of information regarding the link aggregation between two members of the aggregation. The LACP Time Out value is measured in a periodic interval. Check first whether the port in the trunk group is up. When the interval expires, it will be removed from the trunk. Set a Short Timeout \(one second\) for busy trunked links to ensure that disabled ports are removed from the trunk group as soon as possible. The default value for LACP time out is Long Timeout.



![](https://lh5.googleusercontent.com/kQpHB1JCKnUGTpmkCgFYPWr10W0YIW8Ge9Miolov-i5UHhl6bQUmhe7hTpz3CbYRo-i3uLNyO66dghgJTIW_mjf68XaUqwtnp_HZAOdt87fwrquYp2dFo04mnUhDI6D7jcFK2Zs)



<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Timeout</td>
      <td style="text-align:left">
        <p>Select the administrative LACP timeout.</p>
        <p><b>Long Timeout:</b> The LACP PDU will be sent for every 30 seconds. The
          LACP timeout value is 90 seconds.
          <br /><b>Short Timeout:</b> The LACP PDU will be sent every second. The timeout
          value is 3 seconds.</p>
      </td>
    </tr>
  </tbody>
</table>

Click **Apply** to save settings.  


## **Mirror Settings**

Mirror settings mirror network traffic by forwarding copies of incoming and outgoing packets from specific ports to a monitoring port. The packet that is copied to the monitoring port will be the same format as the original packet.

Port mirroring is useful for network monitoring and can be used as a diagnostic tool. Use port mirroring to send traffic to applications that analyze traffic for purposes such as monitoring compliance, detecting intrusions, monitoring, and predicting traffic patterns, and other correlating events. Port mirroring is needed for traffic analysis on a switch because a switch normally sends packets only to the port to which the destination device is connected. The analyzer captures and evaluates the data without affecting the client on the original port. Port mirroring can consume significant CPU resources while active, so be cautious of such usage when configuring the switch.

![](https://lh3.googleusercontent.com/2Vu6qdQ4n6MYnbDZYf3ciyBhtUN36mPlF3MjoW4QyZF3NRb_kEI4T9aeID08xbTYpTcZRyUbJUGrC1zHmSYk-HixOA02wbGh65lELh0V4n-n9vwVSZpacNKO5wZNrPMrqKWvz3g)

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
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Session ID</b>
      </td>
      <td style="text-align:left"><b>A number identifying the mirror session. This switch only supports up to 4 mirror sessions.</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Destination Port</b>
      </td>
      <td style="text-align:left"><b>Select the port for traffic purposes from source ports mirrored to this port.</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Source TX/RX Port</b>
      </td>
      <td style="text-align:left">
        <p><b>Sets the source port from which traffic will be mirrored.</b>
        </p>
        <p><b>TX Port: Only frames transmitted from this port are mirrored to the destination port.</b>
        </p>
        <p><b>RX Port: Only frames received on this port are mirrored to the destination port.</b>
        </p>
        <p><b>Both: Frames received and transmitted on this port are mirrored to the specified destination port.</b>
        </p>
        <p><b>None: Disables mirroring for this port.</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Ingress State</b>
      </td>
      <td style="text-align:left"><b>Select whether to enable or disable ingress traffic forwarding.</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Session State</b>
      </td>
      <td style="text-align:left"><b>Select whether to enable or disable port mirroring.</b>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
**Note**

**You cannot mirror a faster port onto a slower port. For example, if you try to mirror the traffic from a 100Mbps port onto a 10Mbps port, this can cause throughput problems. The port you are copying frames from should always support an equal or lower speed than the port to which you are sending the copies. Please note a target port and a source port cannot be the same port.**
{% endhint %}

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


