# MAC ACE

Use this page to view and add rules to MAC-based ACLs.

![](https://lh5.googleusercontent.com/AarGQSLcPgdfyDuRCc4WcDokCqaCzugO379g6DB4fkhQzVowWCWS5vUIxA8rZBgL8go2Hjt91gu5OGi0SgnUXhPM0dVuNoEvhe3nWaN9LlBgq7mKGoHrDZnwiAesWwfsPgUViXo)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ACL Name</th>
      <th style="text-align:left">Select the ACL from the list.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Sequence</td>
      <td style="text-align:left">Enter the sequence number which signifies the order of the specified ACL
        relative to other ACLs assigned to the selected interface. The valid range
        is from <b>1 to 2147483647</b>, <b>1</b> being processed first.</td>
    </tr>
    <tr>
      <td style="text-align:left">Action</td>
      <td style="text-align:left">
        <p>Select what action to take if a packet matches the criteria.</p>
        <p><b>Permit:</b> Forward packets that meet the ACL criteria.</p>
        <p><b>Deny: </b>Drops packets that meet the ACL criteria.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Destination MAC Value</td>
      <td style="text-align:left">Enter the destination MAC address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination MAC Wildcard Mask</td>
      <td style="text-align:left">Enter a MAC address mask for the destination MAC address. A mask of 00:00:00:00:00:00
        means the bits must be matched exactly;<b> ff:ff:ff:ff:ff:ff</b> means the
        bits are irrelevant. Any combination of 0s and ffs can be used.</td>
    </tr>
    <tr>
      <td style="text-align:left">Source MAC Value</td>
      <td style="text-align:left">Enter the source MAC address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Source MAC Wildcard Mask</td>
      <td style="text-align:left">Enter a MAC address mask for the source MAC address. A mask of 00:00:00:00:00:00
        means the bits must be matched exactly; <b>ff:ff:ff:ff:ff:ff </b>means the
        bits are irrelevant. Any combination of 0s and ffs can be used.</td>
    </tr>
    <tr>
      <td style="text-align:left">VLAN ID</td>
      <td style="text-align:left">Enter the VLAN ID to which the MAC address is attached in MAC ACE. The
        range is from <b>1 to 4094</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left">802.1p Value</td>
      <td style="text-align:left">Enter the 802.1p value. The range is from<b> 0 to 7.</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Ethertype Value</td>
      <td style="text-align:left">Selecting this option instructs the switch to examine the Ethernet type
        value in each frame&apos;s header. This option can only be used to filter
        Ethernet II formatted packets. A detailed listing of Ethernet protocol
        types can be found in RFC 1060. A few of the more common types include
        0800 (IP), 0806 (ARP), and 8137 (IPX).</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.  


