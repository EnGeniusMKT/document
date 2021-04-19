# Access Points

{% hint style="info" %}
**This page displays the status of all EnSky access points that your Controller is currently managing as well as all the EnSky access points in the network that the Controller has discovered. Use this page to add EnSky access points to your EWS switch’s Controller access point list.** 

**The EWS switch can manage supported EnSky Series access points. For the discovery procedure to succeed, the EWS switch and the EnSky access point must be connected in the same network. The EWS switch can discover supported EnSky access points with any IP address and Subnet settings.**
{% endhint %}

![](https://lh6.googleusercontent.com/WMSNW4WSP_HgdqdFaOIrv-TV5dI4_E3Ww-H6XaRqUUfZLec8Bh7GhAUht4LEU6bABvT02M3dw_EEeYuq6vCXEKUBnTmlMKVVeRCNFat5F4T7B07Ln_Og4vt5obT6pQG0QhoyB1k)

## **Managing Access Points**

EnSky access points can either be configured individually or configured as a group.

To manage an access point individually, click on the **Device Name** field of the access point you wish to configure, and you will be directed to a screen where you can configure settings for the access point.

To manage access points as a group, go to **Device Management &gt; AP Groups** to create an AP group and add members into the group. Click on the Group field of the AP you wish to configure, and you will be directed to a screen where you can configure settings for the AP group.

Group settings can be overridden by individual AP settings. For example, if you want to set the transmit power to a lower setting for only a few specific APs, leave the Transmit Power at Auto in the Wireless Radio Settings of the AP Group, then click on the **Device Name** field of the access point \(which is already in a group\) you wish to configure and you will be directed to a screen where you can configure override settings for the selected access point.  


## **Refresh Countdown Timer**

|  |  |
| :--- | :--- |
| ![](https://lh5.googleusercontent.com/7eg-CgpJ4Zi7BRPck_mRB7N1Xqi4TaoWqnKSgI14c9ianPNiBcoovHEp8LnVysflzMB5tTBL73lHqs33VdFuHh-71LLLJL_2s0tbM2zZL6s_KejjND_tOZBD8YZlT0dYNRp5kZI) | This is the time left before the page auto-refreshes itself. The countdown is from 15 seconds.  |

## **Dashboard**

![](https://lh5.googleusercontent.com/-kvA8jDbYobX_uB4tWACBHu0DgWxABeAKJ8PROZdtRHBPKEU_wGpRUGr8Avm7IBjOsMlZtOh-4yEOUBDJMstx6VxHxPes7KncAFR26NAsdg7C8YV9VshY1H-Q5KfBNiHYkDqnQs)

| Items     | Descriptions |
| :--- | :--- |
| **Managed**                     | This shows the number of APs in the managed AP database that are configured with the EWS switch. |
| **Active** | This shows the number of managed APs that currently have an active connection with the EWS switch’s controller. |
| **Offline** | This shows the number of managed APs that currently do not have an active connection with the EWS switch’s controller. |

## **AP\(s\) Detected List**

| Items                           | Descriptions |
| :--- | :--- |
| ![](https://lh5.googleusercontent.com/oyRvf-S7iVl7aF-T0xvrwDJBtwtOeTP8EhmBcGfAIrRnICzrQGqPxtJFumxMuYSYx0hts9M8Xqk0PDVodmlKETL_Mv6lG1Lmjh8SzLjfKC6tQhHwLzfpL4YTJLVoVGnGdDjD1D4) | Reveals a list of all APs in the network that the EWS switch automatically discovers. Mouse over the discovered access point to show general information such as the MAC address, IP address, model name, and firmware version. |

## **Remove AP**

| Items                         | Descriptions |
| :--- | :--- |
| ![](https://lh5.googleusercontent.com/FzEFzW2-dpZEUHgtH7xNxOyoQTkioIrDfOAg74RDNnoOe2K6o_jxKbCAnSPp4YB2lIg17FIFDGZyzok7uoqd0jw3xT1BxNMCQMBzdMcv-yE9HSGBEBTUw8zN2OgBQ1XrU1E4PBc) | The Remove button removes selected access point\(s\) from managed AP list. Access points removed will be restored to standalone mode. |

## **Reboot AP**

| Items   | Descriptions |
| :--- | :--- |
| ![](https://lh4.googleusercontent.com/HfbvvCFPFECjoMDnpbkirtxVmtyoNFGgpexJ-PNFCmrfdd1_70U9f8SHJRAYvKO5G-7aixkrO2cY_ttHLOvtFlErOgXpQhNV_imDHM7uTgBnK6sU_DLi142VysFCLU1Go4Fy620)                 | The Reboot button will reboot the selected access point\(s\). |

## **Search Bar** 

| Items                             | Descriptions |
| :--- | :--- |
| ![](https://lh4.googleusercontent.com/4pOSIzarOi9BgknQCrnrRLKPGhyrRn5s_K21Zx3-Weqa3cABLeGISCWdHgFmfTJVid0v6c5vB4Zs8fsZOFcwbp7ufrVhLlF0unknMdbBfpfKa-htzENJ1MXjZitLMaVrE4or_0o) | Use the Search Bar to search for access points managed by the EWS switch using the following criteria: Status, model name, MAC Address, Device name, IP address, Firmware Version, and Group. |

## **Status**

This indicates the current status of the managed access point.

|  **Status**                                       | **Explanation** |
| :--- | :--- |
| **Online** | AP is connected and managed by the EWS switch. |
| **Provisioning** | AP is currently in the process of connecting to the EWS switch. |
| **Applying Change** | AP is currently being applied with system changes. |
| **Connecting** | AP is currently connecting to the EWS switch. |
| **Offline** | AP is currently offline. |
| **Resetting** | AP is resetting. |
| **Firmware Upgrading** | AP is currently undergoing firmware upgrade process. |
| **Invalid IP** | The subnet of managed AP’s IP address is not the same as the EWS switch. Please remove AP and reconfigure AP to the correct IP settings. |
| **Incompatible Version** | AP firmware is not compatible with EWS switch. |
| **Checking Certificate** | EWS switch is checking the SSL Certificate of AP. |

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Model Name                                       </b>
      </td>
      <td style="text-align:left">This shows the model name of the managed access point.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>MAC Address</b>
      </td>
      <td style="text-align:left">This shows the MAC address of the managed access point.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Device Name</b>
      </td>
      <td style="text-align:left">
        <p>This displays the device name of the managed access point.</p>
        <ul>
          <li>When the AP is not a group member, click on this field and you&#x2019;ll
            be redirected to the configuration page where you can edit settings such
            as device name, IP Address, and Wireless Radio settings.</li>
          <li>When the AP is a group member, click on this field to configure settings
            for individual access points by overriding the cluster settings.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>IP Address</b>
      </td>
      <td style="text-align:left">This shows the IP address of the managed access point.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Firmware Version</b>
      </td>
      <td style="text-align:left">This shows the firmware version of the managed access point.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Last Update</b>
      </td>
      <td style="text-align:left">It displays the time the access point was last detected, and the information
        was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Group</b>
      </td>
      <td style="text-align:left">Displays the AP Group the access point is currently assigned to. Click
        on this field and you&apos;ll be redirected to the group configuration
        page.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Column Filter</b>
      </td>
      <td style="text-align:left">
        <img src="https://lh5.googleusercontent.com/6c4hqAx9dzyfrPokMCxl5mFyQLNWqxAGJWKnlM-lzg5rIvO2RVbInHOETXEaPLVaDLl1nEagZ5AmGRxT2rAuXU_tDc5WSlweY_dKW-CZwJJlIzICQtzCS8H3Qr6Ia0pvRgJMsLk"
        alt/>Shows or hides fields in the access point list.</td>
    </tr>
  </tbody>
</table>



