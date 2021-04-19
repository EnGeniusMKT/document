# RMON

Remote Network Monitoring, or RMON is used for support monitoring and protocol analysis of LANs by enabling various network monitors and console systems to exchange network monitoring data through the switch.  


## **Event List**

The Event List defines RMON events on the switch.

![](https://lh5.googleusercontent.com/Fxo_n5Fgd_APv9sEbtscdPkOGCydgZY0Wm4iwhGtCkUkcsYWZIF-ASLgBNm_INZ3W0ES6cG-jDKVF4FVu6u-KoBYJTcwOYtbdwJDQkDKnAdacX6BVpLj5pRd_NVv-3B8mvcGbCk)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Index</td>
      <td style="text-align:left">Enter the entry number for event.</td>
    </tr>
    <tr>
      <td style="text-align:left">Event Type</td>
      <td style="text-align:left">
        <p>Select the event type.</p>
        <p>Log: The event is a log entry.</p>
        <p>SNMP Trap: The event is a trap.</p>
        <p>Log &amp; Trap: The event is both a log entry and a trap.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Community</td>
      <td style="text-align:left">Enter the community to which the event belongs.</td>
    </tr>
    <tr>
      <td style="text-align:left">Description</td>
      <td style="text-align:left">Displays the number of good broadcast packets received on the interface.</td>
    </tr>
    <tr>
      <td style="text-align:left">Last Time Sent</td>
      <td style="text-align:left">Displays the time that event occurred.</td>
    </tr>
    <tr>
      <td style="text-align:left">Owner</td>
      <td style="text-align:left">Enter the switch that defined the event.</td>
    </tr>
  </tbody>
</table>

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


## **Event Log Table**

From here, you can view specific event logs for the switch. Choose an event log you wish to view from the drop-down list.

![](https://lh3.googleusercontent.com/PPZxKb--8DUdd-Qwyo3ssk_umvFmPkCFrUnQw-Rcz7W9pLeEfANrTScY1_BY4EAEZU6zJT4-N_G6ta6YytxgPs5tINZD9sPZ95oYDzE1DfBehEDMMUKcThDCFwTrxW5fpuEBID4)

## **Alarm List**

You can configure network alarms to occur when a network problem is detected. Choose your preferences for the alarm from the drop-down boxes.

![](https://lh4.googleusercontent.com/T90pAaIX3UPRwrJl6YmgAb1kid-Kn6DRcPoMFBWMRezc9c6r2Y02_kAuj1pb6Gi5XoHyW8dECSGrgUKvoAQAnF4Ck-CtZ6tpZ9p-mfQTPZc0ZEKWZaqC8Oq_AUhg7i14d-3MhSI)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Index</th>
      <th style="text-align:left">Enter the entry number for the Alarm List.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Sample Port</td>
      <td style="text-align:left">Select the port from which the alarm samples were taken.</td>
    </tr>
    <tr>
      <td style="text-align:left">Sample Variable</td>
      <td style="text-align:left">Select the variable of samples for the specified alarm sample.</td>
    </tr>
    <tr>
      <td style="text-align:left">Sample Interval</td>
      <td style="text-align:left">Enter the alarm interval time.</td>
    </tr>
    <tr>
      <td style="text-align:left">Sample Type</td>
      <td style="text-align:left">
        <p>Select the sampling method for the selected variable and compare the value
          against the thresholds.</p>
        <p>Absolute: Compares the values with the thresholds at the end of the sampling
          interval.</p>
        <p>Delta: Subtracts the last sampled value from the current value.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Rising Threshold</td>
      <td style="text-align:left">Enter the rising number that triggers the rising threshold alarm.</td>
    </tr>
    <tr>
      <td style="text-align:left">Falling Threshold</td>
      <td style="text-align:left">Enter the falling number that triggers the falling threshold alarm.</td>
    </tr>
    <tr>
      <td style="text-align:left">Rising Event</td>
      <td style="text-align:left">Enter the event number by the falling alarms are reported.</td>
    </tr>
    <tr>
      <td style="text-align:left">Falling Event</td>
      <td style="text-align:left">Enter the event number by the falling alarms are reported.</td>
    </tr>
    <tr>
      <td style="text-align:left">Owner</td>
      <td style="text-align:left">Enter the switch that defined the alarm.</td>
    </tr>
  </tbody>
</table>

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## History List

![](https://lh6.googleusercontent.com/Sl3JjC7H4uO75reL_S_B2EH6ytTWAsW91tylaX2V_2vRnthPcDcWnLNfQpoeHyYEBTqh5lE2dGXRCgzlU4Ep-jtevFo0MSM41D0YW4vBbVDCFJ_OhnnwyaBlMvupUsZibAXw7Fk)

| Index | Enter the entry number for the History List. |
| :--- | :--- |
| Sample Port | Select the port from which the history samples were taken. |
| Bucket Requested | Enter the number of samples to be saved. The range is from 1 to 50. |
| Interval | Enter the time that samples are taken from the ports. The field range is from 1 to 3600. |
| Owner | Enter the RMON user that requested the RMON information. The range is from 0 to 32 characters. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## **History Log Table**

From here, you can view the History Index for history logs on the switch. Select a history index to view from the drop-down box.

![](https://lh3.googleusercontent.com/tshifqLqHCRrFCkpuf46FGjgnUne-lDUD08K2JvF9NYc3J1OOEGPUR-y1n8vDLLNh4EPk2hxtPtoshx92x5po9Y9HbrYBVaMYvW6YNeq5Sy8uPH_nOq7EgpppG6PF-hkb0ZeVaM)

## **Statistics**

From here, you can view all the RMON statistics of the switch.

![](https://lh5.googleusercontent.com/9q0N8bz3xPF1IHSE8yxleiK83P3dScGy3AGK-Bkh93fM3YKRW04eu29Qxuw05y1J4bodUIV_pAslcdIeNGAKgEkoF3nbmo7h5_z8KbVoVu5ipu-cYZMkeVEfJg-axhrHnkve2tc)

| Items | Descriptions |
| :--- | :--- |
| Port | Indicates the specific port for which RMON statistics are displayed. |
| Drop Events | Displays the number of dropped events that have occurred on the port. |
| Octets | Displays the number of octets received on the port. |
| Pkts | Displays the number of packets received on the port. |
| Broadcast Pkts | Displays the number of good broadcast packets received on the port. This number does not include multicast packets. |
| Multicast Pkts | Displays the number of good multicast packets received on the port. |
| CRC & Align Errors | Displays the number of CRC and Align errors that have occurred on the port. |
| Undersize Pkts | Displays the number of undersized packets \(less than 64 octets\) received on the port. |
| Oversize Pkts | Displays the number of oversized packets \(over 1518 octets\) received on the port. |
| Fragments | Displays the number of fragments received on the port. |
| Jabbers | Displays the total number of received packets that were longer than 1518 octets. |
| Collisions | Displays the number of collisions received on the port. |
| Pkts of 64 Octets | Displays the number of 64-byte frames received on the port. |
| Pkts of 65 to 127 Octets | Displays the number of 65- to 127-byte packets received on the port. |
| Pkts of 128 to 255 Octets | Displays the number of 128- to 255-byte packets received on the port. |
| Pkts of 256 to 511 Octets | Displays the number of 256- to 511-byte packets received on the port. |
| Pkts of 512 to 1023 Octets | Displays the number of 512- to 1023-byte packets received on the port. |
| Pkts of 1024 to 1518 Octets | Displays the number of 1024- to 1518-byte packets received on port. |

