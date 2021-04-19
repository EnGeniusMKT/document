# One-click Update

The EWS switch can be configured to automatically check for new firmware updates for your EnSky devices. The icon below will appear on the upper right corner of the user interface when a new update is available. Simply click on the icon and follow the on-screen instructions to update your devices.

![](https://lh6.googleusercontent.com/t-o7ccm_o6eRJDzmRcIvsk8zg17crylNHC2lDimNspQ05cyO1TbUIzHNHewibeiMKEceWzeiC4YKqo4YLtcMGbie7FN-w8bsN9XekoruSZdckw80eFy8z9M5JC-HYGk1LWXWC58)

{% hint style="success" %}
**Note: An active Internet connection is required for this feature.**
{% endhint %}

## **Update List**

This page displays the devices which has new firmware updates available. A release note states the purpose of the firmware. Click on Check for Updates for the EWS switch to check for the latest firmware. Select the devices you wish to update and click on Update button to begin the updating process.  


![](https://lh6.googleusercontent.com/5wMlw24svRdpf0qSh6Xw_Ugy7quFdOpQNskIHyW0AegpEmaxrg5RyzZa1tA8t59XzRnPMHG_I79lFfB2aU3GE59DG8Ly746iVBgBmvY0XkdP9mLUJfuf7jiYD8o50S5TunRMfTw)

{% hint style="success" %}
**Note: Both the EWS switch and the browser on the PC must be able to access the Internet for this function to work. One Click Update might also not be available if you are using a proxy server for Internet connections.**
{% endhint %}

## **Update Settings**

![](https://lh4.googleusercontent.com/kv2lwkZo4ovhoDuSWQ7eqnNvcW6uHMIp9B_-rf5PnTNGEwaRvcCIXVOCTm7kmqBbGOWbURVL9yz4NFG6RleYNmQQ4kB1O3Wi6KkS_ZHixpEf9Idtd4rxzCl6fZi6jFtwLHqjr2c)

**Automatically Check for Updates**

Enable/disable automatically checks for new updates for your devices.  


**Update Server** 

Choose whether you wish to check for updates from an EnGenius server or specify your own http/ftp server path.  


**Check updates from specific server**

Apart from copying firmware image files into the specific http/ftp path, an index file is required in the same folder.

Follow the instructions below for creating the index file.

1. Create a new .txt file with the name "lastfwlist.txt".
2. In the file, create entries based on the format below and save the file.

&lt;Model Name&gt;,&lt;Firmware Version&gt;,&lt;File Name&gt;,&lt;MD5&gt;,&lt;SKU&gt;

| **Field** | **Description** | **Reference String** |
| :--- | :--- | :--- |
| **Model Name** | **Enter model name.** | **EWS310AP, EWS320AP, EWS660AP** |
| **Firmware Version** | **Enter firmware version.** | **v2.0.129-c1.3.5** |
| **File Name** | **Enter complete filename with extension.** | **ews310ap-fcc-v2.0.132.0-c1.3.5.bin** |
| **MD5** | **Enter MD5 value of the firmware image** | **4959e8d68536227d182b53a719dcdae4** |
| **SKU** | **Enter in device SKU.** | **FCC, ETSI, INT** |

**Examples:**

EWS210AP,v2.0.129-c1.3.5,ews210ap-fcc-v2.0.129.0-c1.3.5.bin,af44f429a5404e2f7bde651921366c33,FCC

EWS210AP,v2.0.129-c1.3.5,ews210ap-etsi-v2.0.129.0-c1.3.5.bin,186cab281b7038e7c9b8909acfd9e63e,ETSI

EWS310AP,v2.0.132-c1.3.5,ews310ap-fcc-v2.0.132.0-c1.3.5.bin,4959e8d68536227d182b53a719dcdae4,FCC

EWS310AP,v2.0.132-c1.3.5,ews310ap-etsi-v2.0.132.0-c1.3.5.bin,0ee6663cc9b6c652b1139214455ed92e,ETSI

EWS320AP,v2.0.132-c1.3.5,ews320ap-fcc-v2.0.132.0-c1.3.5.bin,e584a03d0218a0f1a29a4c5550c99614,FCC

EWS320AP,v2.0.132-c1.3.5,ews320ap-etsi-v2.0.132.0-c1.3.5.bin,967312acc588b6caad7e55a98fc19997,ETSI

EWS360AP,v2.0.130-c1.3.5,ews360ap-fcc-v2.0.130.0-c1.3.5.bin,3bff8f450f171c0f839032124cbe4860,FCC

EWS360AP,v2.0.130-c1.3.5,ews360ap-etsi-v2.0.130.0-c1.3.5.bin,e2483bfc74259263dda18e8d86682183,ETSI

EWS660AP,v2.0.124-c1.3.5,ews660ap-int-v2.0.124.0-c1.3.5.bin,cc00b2871dec668b9a1b82f330a2611e,FCC

EWS660AP,v2.0.124-c1.3.5,ews660ap-etsi-v2.0.124.0-c1.3.5.bin,d67554b30fd98d06093f7da306cb8fd2,ETSI

EWS860AP,v2.0.124-c1.3.5,ews860ap-fcc-v2.0.124.0-c1.3.5.bin,39f5f935f7b83515c4a6c30ef4c61114,FCC  


