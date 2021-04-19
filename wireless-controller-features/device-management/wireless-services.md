# Wireless Services



![](https://lh4.googleusercontent.com/MiXyfoArYXUgjwTsNQXfR_SM2_SDhR9RqbHhkpueb1eO59-y-Jj9UFjsubhI8DKUSl-u7N99FnuFtsCFAWkGM36JS6l-Z8UNtAkQ2W77Yxpy41zeFUUmbTVq6cOs1HJ4yruu4OE)

## **Background Scanning**

With Background Scanning enabled, the controller periodically samples RF activity of all surrounding access points including channel utilization and nearby devices in all available channels. Background scanning is the basis for Auto Tx Power and Rogue AP detection, and must be enabled for these features to operate. If you prefer, you may disable it if you feel it's not helpful, or adjust the scanning frequency, if you prefer scanning at greater or fewer intervals.

{% hint style="info" %}
**Note:** For latency-sensitive applications such as VoIP, it is recommended to set the background scan interval to a higher value, e.g. 5 or 10 minutes. For regular applications, the recommended value is 30 seconds. This value will also be directly related to how long it takes the AP to scan for rogue devices.
{% endhint %}

## **Auto TX Power**

Using the information collected by Background Scanning, APs can automatically adjust their transmit power to optimize coverage. When enabled, APs will optimize their transmit power based on the time interval configured for Background Scanning.

{% hint style="success" %}
**Note:** Background Scanning must be enabled, and Tx Power of APs must be set to Auto \(under Wireless Radio Settings\) for this feature to operate.
{% endhint %}

