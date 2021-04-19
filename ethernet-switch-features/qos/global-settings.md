# Global Settings

There are two options for applying QoS information onto packets: the 802.1p Class of Service \(CoS\) priority field within the VLAN tag of tagged Ethernet frames, and Differentiated Services \(DiffServ\) Code Point \(DSCP\). Each port on the switch can be configured to trust one of the packet fields \(802.1p , DSCP or DSCP+802.1p\). Packets that enter the switch's port may carry no QoS information as well. If so, the switch places such information into the packets before transmitting them to the next node. Thus, QoS information is preserved between nodes within the network and the nodes know which label to give each packet. A trusted field must exist in the packet for the mapping table to be of any use. When a port is configured as untrusted, it does not trust any incoming packet priority designations and uses the port default priority value instead to process the packet.

![](https://lh6.googleusercontent.com/Ix7dcEKT0fGJEeyWE2cPXVXE-9omOsInGjxj-CthHoDFne5T_k-yw7yAfVfEoj5K6Sbnql841CBadyzc8F20KZSFh0w-9PQn3IlqreGQnpy-JHX5pDcUq6o88kuzbJdR9taHkoA)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">State</td>
      <td style="text-align:left">Select whether QoS is enabled or disabled on the switch.</td>
    </tr>
    <tr>
      <td style="text-align:left">Scheduling Method</td>
      <td style="text-align:left">
        <p>Selects the Strict Priority or WRR to specify the traffic scheduling method.</p>
        <p>Strict Priority: Specifies traffic scheduling based strictly on the queue
          priority.</p>
        <p>WRR: Uses the Weighted Round-Robin (WRR) algorithm to handle packets in
          priority classes of service. It assigns WRR weights to queues.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Trust Mode</td>
      <td style="text-align:left">
        <p>Select which packet fields to use for classifying packets entering the
          switch.</p>
        <p>DSCP: Classify traffic based on the DSCP (Differentiated Services Code
          Point) tag value.</p>
        <p>802.1p: Classify traffic based on the 802.1p. The eight priority tags
          that are specified in IEEE 802.1p are from 1 to 8.</p>
      </td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.  


