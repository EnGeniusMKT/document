# Voice VLAN

Enhance your Voice over IP \(VoIP\) service by configuring ports to carry IP voice traffic from IP phones on a specific VLAN. Voice VLAN provides QoS to VoIP, ensuring that the quality of the call does not deteriorate if the IP traffic is received erratically or unevenly.

## **Global Settings**

![](https://lh3.googleusercontent.com/7-K97r75zeTxRysYD0_JIyQLxXEo6IVs9y4jlZ-GtT1UrG--5IDGb5x1LJnCVLZPAVd6yYlIdpk4xnVvDtL1s4xCiaJiPwUL6wq1FIvgPqHUC4XX3vXp9DsS3-7ezbb8-uEg_IA)

| Items | Descriptions |
| :--- | :--- |
| Voice VLAN State                     | Select Enabled or Disabled for Voice VLAN on the switch. |
| Voice VLAN ID | Sets the Voice VLAN ID for the network. Only one Voice VLAN is supported on the switch. |
| 802.1p Remark | Enable this function to have outgoing voice traffic to be marked with the selected CoS value. |
| Remark CoS/802.1p | Defines a service priority for traffic on the Voice VLAN. The priority of any received VoIP packet is overwritten with the new priority when the Voice VLAN feature is active on a port. \(Range: 0 to 7; Default: 6\) |
| Aging Time | The aging time is used to remove a port from voice VLAN if the port is an automatic VLAN member. When the last voice device stops sending traffic and the MAC address of this voice device is aged out, the voice VLAN aging timer will be started. The port will be removed from the voice VLAN after expiration of the voice VLAN aging timer. If the voice traffic resumes during the aging time, the aging timer will be reset and stop. The range for aging time is from 1 to 65535 minutes. The default is 1440 minutes. |

Click **Apply** to update the system settings.

## **OUI Settings**

The switches determine whether a received packet is a voice packet by checking its source MAC address. VoIP traffic has a pre-configured Organizationally Unique Identifiers \(OUI\) prefix in the source MAC address. You can manually add specific manufacturer's MAC addresses and description to the OUI table. All traffic received on the Voice VLAN ports from the specific IP phone with a listed OUI is forwarded on the voice VLAN.

![](https://lh6.googleusercontent.com/iYNiPYMZrMczmv5IKYVTdpuyEqopjje4BmRgPfhaRdtHLlkhCkdxWuwxqgBRnmNGHOgaDY1X6wDsgtj5Tn5I39UyuN0X_Y72lDiqobmWqwdXy5AfDqTh-Wo-4pt_PEqDTfi3WmE)

| Items | Descriptions |
| :--- | :--- |
| Index | Displays the VoIP sequence ID. |
| OUI Address | Globally unique ID assigned to a vendor by the IEEE to identify VoIP equipment. |
| Description | Displays the ID of the VoIP equipment vendor. |

To configure the OUI settings, click the **Edit** button to re-configure the specific entry. Click the Delete button to remove the specific entry and click the Add button to create a new OUI entry. Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## **Port Settings**

Enhance your VoIP service further by configuring ports to carry IP voice traffic from IP phones on a specific VLAN. Voice VLAN provides QoS to VoIP, ensuring that the quality of voice does not deteriorate if the IP traffic is received unevenly. 

![](https://lh3.googleusercontent.com/I4DZC6WH-oOJyoRsriiR9IAnuOZevauoK6SJA8oo_VR_BE34---Znn_oPBHBX-aOb5E8IYLqv3_nV2JIpR7p8YQmTbsZ7SBRFNEq8XxalCccMlqrPsUPIT3EZcImEYUE1_WTkcs)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Port</th>
      <th style="text-align:left">Displays the port to which the voice VLAN settings are applied.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">State</td>
      <td style="text-align:left">Select Enabled to enhance VoIP quality on the selected port. The default
        is Disabled.</td>
    </tr>
    <tr>
      <td style="text-align:left">CoS Mode</td>
      <td style="text-align:left">
        <p>Select Src or All from the list.</p>
        <p>Src: Src QoS attributes are applied to packets with OUIs in the source
          MAC address.</p>
        <p>All: All QoS attributes are applied to packets that are classified to
          the Voice VLAN.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Operate Status</td>
      <td style="text-align:left">Displays the operating status for the Voice VLAN on the selected port.</td>
    </tr>
  </tbody>
</table>

  
Click **Apply** to update the system settings.  


##  

