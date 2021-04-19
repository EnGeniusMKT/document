# PVID

When an untagged packet enters a switch port, the PVID \(Port VLAN ID\) will be attached to the untagged packet and forward frames to a VLAN specified VID part of the PVID. A packet received on a given port would be assigned that port's PVID and then be forwarded to the port that corresponded to the packet's destination address. If the PVID of the port that received the packet is different from the PVID of the port that is to transmit the packet, the switch will drop the packet. Within the switch, different PVIDs mean different VLANs, so VLAN identification based upon the PVIDs cannot create VLANs that extend outside a given switch. If no VLANs are defined on the switch, all ports are then assigned to a default VLAN with a PVID equal to 1.  


![](https://lh4.googleusercontent.com/PFIgqGXb0QcclBVes7CsScrB0tQjP74Fil5gBeU1tbgW_joEIk9Sb6S6xyIoBpi2CuK6BvpkNDx8SgNNwg5hNSnF33mSJVkB8WZs6nFTRakGqkNK0Tn97rRD9QBbHyrBjOTgevg)

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Port</td>
      <td style="text-align:left">Displays the VLAN ID to which the PVID tag is assigned. Configure the
        PVID to assign untagged or tagged frames received on the selected port.</td>
    </tr>
    <tr>
      <td style="text-align:left">PVID</td>
      <td style="text-align:left">Enter the PVID value. The range is from 1 to 4094.</td>
    </tr>
    <tr>
      <td style="text-align:left">Accept Type</td>
      <td style="text-align:left">
        <p>Select Tagged Only and Untagged Only from the list.</p>
        <p>Tagged Only: The port discards any untagged frames it receives. The port
          only accepts tagged frames.</p>
        <p>Untagged Only: Only untagged frames received on the port are accepted.</p>
        <p>All: The port accepts both tagged and untagged frames.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Ingress Filtering</td>
      <td style="text-align:left">
        <p>Specify how you wish the port to handle tagged frames. Select Enabled
          or Disabled from the list.</p>
        <p>Enabled: Tagged frames are discarded if VID does not match the PVID of
          the port.</p>
        <p>Disabled: All frames are forwarded in accordance with the IEEE 802.1Q
          VLAN.</p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
**NOTE**

**To enable PVID functionality, the following requirements must be met:**

* **All ports must have a defined PVID.**
* **If no other value is specified, the default VLAN PVID is used.**
* **If you wish to change the port's default PVID, you must first create a VLAN that includes the port as a member.**
{% endhint %}

Click **Apply** to update the system settings.

