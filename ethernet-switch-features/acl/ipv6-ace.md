# IPv6 ACE

Allows IPv6 Based Access Control Entry \(ACE\) to be defined within a configured ACL.

![](https://lh3.googleusercontent.com/c-W_PvC-FBwt4_jlL6S0tWbkLY7eYkAnJkJwJ6u_6CKOw1B46gov3LqkiQO-zBCNMuKf0OtymjSGhs4aOyOabMZHh08BPHdZ479JMfZbqOwtdUmF63XA8-B7xjmLvQB2OMrtULw)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">ACL Name</td>
      <td style="text-align:left">Select the ACL from the list.</td>
    </tr>
    <tr>
      <td style="text-align:left">Sequence</td>
      <td style="text-align:left">Enter the sequence number which signifies the order of the specified ACL
        relative to other ACLs assigned to the selected interface. The valid range
        is from 1 to 2147483647, 1 being processed first.</td>
    </tr>
    <tr>
      <td style="text-align:left">Action</td>
      <td style="text-align:left">
        <p>Select what action to take if a packet matches the criteria.</p>
        <p>Permit: Forward packets that meet the ACL criteria.</p>
        <p>Deny: Drops packets that meet the ACL criteria.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Protocol</td>
      <td style="text-align:left">
        <p>Select the Any, Protocol ID, or Select from List from drop-down menu.</p>
        <p>Protocol ID: Enter the protocol in the ACE to which the packet is matched.</p>
        <p>Select from List: Select the protocol from the list in the provided field.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Source IP Address Value</td>
      <td style="text-align:left">Enter the source IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Source IP Prefix Length</td>
      <td style="text-align:left">Enter the prefix length of the new source IP address. The range is from
        0 to 128.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination IP Address Value</td>
      <td style="text-align:left">Enter the destination IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination IP Prefix Length</td>
      <td style="text-align:left">Enter the prefix length of the new source IP address. The range is from
        0 to 128.</td>
    </tr>
    <tr>
      <td style="text-align:left">Source Port</td>
      <td style="text-align:left">Select Single or Range from the list. Enter the source port that is matched
        to packets. The range is from 0 to 65535.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination Port</td>
      <td style="text-align:left">Select Single or Range from the list. Enter the destination port that
        is matched to packets. The range is from 0 to 65535.</td>
    </tr>
    <tr>
      <td style="text-align:left">TCP Flags</td>
      <td style="text-align:left">
        <p>Select whether to handle each six TCP control flags; URG (Urgent), ACK
          (Acknowledgment), PSH (Push), RST (Reset), SYN (Synchronize), and FIN (Fin)
          from drop-down menu.</p>
        <p>Don&apos;t Care: The ACE does not treat the TCP control flag.</p>
        <p>Set: The packet with the TCP control flag being set matches the criteria.</p>
        <p>Unset: The packet with the TCP control flag being unset matches the criteria.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Type of Service</td>
      <td style="text-align:left">Select Any or DSCP to match from drop-down list. When DSCP to match is
        selected, enter the DSCP. The range is from 0 to 63.</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.  


