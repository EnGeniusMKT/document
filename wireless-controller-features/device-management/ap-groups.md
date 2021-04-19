# AP Groups

An AP group can be used to define configuration options and apply them to several APs at once. If your wireless network covers a large physical environment and you want to provide wireless services with some common settings and policies to different areas of your environment, you can use AP Groups to do this instead of having to modify the settings of each AP individually. For example, if your wireless network covers two floors and you need to provide wireless access to visitors on the 1st floor, you can simply setup two different AP groups with different settings and policies to suit your application.

![](https://lh6.googleusercontent.com/fxw7E-P1KiLXxGwLrMAg7bPV88fk5SGCmaGqy-M6TlVz0KyBn_9P78n28e2Du8N5yxtlTLdSxyOdayyPcdIeJyOvPAliP3hBfv-Pb0JNjwCagO9HzXIZhDzwb8gasnCCXPkQcmg)

## **Creating a New AP Group** 

**Follow the steps below to create a new AP group.**

1. Click on **Add** button to create a new AP group. 
2. Enter the name and description of the new AP group.
3. In the Member Setting section, all managed access points that are not currently assigned to an AP group will be listed in **Managed APs** list on the left. Users can select the access points from the list and click **Add** to assign to this group. The access points will be moved to the **Group Member** list on the right .
4. Configure Radio, WLAN, and Advanced settings then click on Apply for settings to take effect.
5. Regarding Mesh AP setting in Advanced settings from AP Group, users can enable this feature to let APs in the group to become mesh members.  If this feature is enabled, when mesh AP detects it’s no longer having wired connection to reach other mesh AP, it will then use the mesh link to set up connection to one of the best preferred mesh peer AP for connection.  The RF link of either 2.4GHz or 5GHz can be decided by Mesh Profile settings under controller tab on EWS switch’s web management page.

![](https://lh6.googleusercontent.com/tx4Kq480UrsBm9WWFiXLQaSvzN76cXtJMyvfqe0yCsXSyP5gu-rtvxdbe00BzOujtnfNSNWx6VTUbOO0oGFHs4E9JS62GjIrmuY3Im1-Dq1iwPh5CSpfRPmh367UuAkrJkOhwQo)

![](https://lh4.googleusercontent.com/MzoenbiltqvwpDLuuC-KTD4OdNUmyXUooB9vNRTxhnfeoD_ci3IyiY1cEgsrVkaGDM-9Q13t_h0fsXYOh1h0sNZ7hnUvZSr-7VEv2pSz_T85nvy6yRsj04kJz0-usHJtsXZe82Q)

{% hint style="success" %}
**Note:** As most settings from above step-4 are the same as mentioned in last section of Access Point Settings, these common settings will apply to all AP members in the group.  Depending on your design on applying group settings to APs in deployed WLAN, certain parameters like channel and transmit power may need to be overridden to reduce RF interference or optimize overall WLAN performance. 
{% endhint %}

Please click on the device item to override group settings; the following shows that items like Channel HT Mode, Transmit Power, and Client Limits are eligible to be overridden.

![](https://lh6.googleusercontent.com/ooC_bSFd3JUxQMnzM8bcGu0ln_kTS-ySbpD0SRJ6Zrue3MpUi4H-Ik61L9tSXoHH0CZ9qeBb1lEkn3Z5jKqgHxJ3YckpEVHeOtSMtHMb9d-5XNysf-Dng_oKpgP1sUMkQbbFLDI)

![](https://lh3.googleusercontent.com/m55JOB4NuYFJVWlt8luSLj0aKUX0ZJBV08RB2zoM4ZAAQNd8nKy5-yrIidpotq2vR3cBowxhRew-R6LgcXrjVTUIB30LFzHVzSyYdZmDVVf_pauTeiqOJzKcxgvG3lDNIwM3ZkI)

## **AP Group Management**

Use the following tool or buttons in controller web management page for further configuration or management:  


| Icons | Functions                   | Descriptions |
| :--- | :--- | :--- |
| ![](https://lh6.googleusercontent.com/3slvXY6h3Z-JiAdGbpwdXl911MrkWZiZ0ONjGnb1DXsZXD1S3O_QndM4qgUtFgP_OzCrimXmH2qgg1Wq0eX9Zdxj76XRq5XGxbcWryFm6cB90CdLL4lCQeQvl6HchjuydDNXdio) | Search Bar  | Use the Search Bar to search for keywords in the list using the following criteria: AP Group Name, AP MAC, AP Name, Description. |
| ![](https://lh3.googleusercontent.com/yn2GdRvQED_8flnQWJLF-fADmEWdh53dxUrCDaIlyLZpsk2D8yYi5rdsAdVSnJld5LWFGFRCcvgnUH6_cPz5KmOx7IDXVuBgVgr9xySOwnLaa6aLPywf9dWcL9h1RrUldB2_QWA) | Add Button | Use the Add Button to create a new AP Group. |
| ![](https://lh6.googleusercontent.com/DdUhleYMOR-PKL508OEZYkxrHOIThy9begxUfalwBcAT7wO3CO23P6mjRX-GSe49eCsWL-EFKgYGhfe20-v85oiPvNeLrJVzgJ9AqlXmUnh4w6RpRrLD658dPQ3omOHbopa_C_8) | Edit Button | Use the Edit Button to edit the configurations of the AP Group. |
| ![](https://lh5.googleusercontent.com/oIrX-_V5r3arjtQA7jzv0g8AgwuZ8VYHGEXaCZdOs_EU6wVjamUrftKIhVXty3tuQc4ZfZRD_qLh-uft8wnrK-Z43-L8UD4AxCxh8TzEQli13Jj76UI4LKafVE6WTdyoo7O-bKo) | Delete Button       | Use the Delete Button to remove an AP Group. |

