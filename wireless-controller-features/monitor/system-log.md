# System Log

## **Global Settings**

From here, you can Enable or Disable the Log settings for the EWS switch.

![](https://lh4.googleusercontent.com/O79XPquyhJB-OaDZC-z_pI9PXvonKXd0RBwOUb3qjVTcD_SZylhkREyogQOFyD_226T55tCzysK08DjzPI7_fOZoyUGRgdD5SyOG57-XP01QV7cAw0Pcd39A3OXJwv5VhZCKJFY)

## **Local Logging**

The System Log is designed to monitor the operation of the EWS switch by recording the event messages it generates during normal operation. These events may provide vital information about system activity that can assist in the identification and solutions of system problems. 

The EWS switch supports log output to two repositories: Flash and RAM. The information stored in the system’s RAM log will be lost after the switch is rebooted or powered off, whereas the information stored in the system’s Flash will be kept even after the switch is rebooted or powered off. The flash repository has a fixed capacity; at a certain level, the EWS switch will start deleting the oldest entries to make room for the newest.

![](https://lh5.googleusercontent.com/2bQB1fqCnp6KY0ydI8WHn5jgJliLgsgHMynTZ3Jlf4N49kwh8yqaJPR3Ne5BCTfUVcDVsUE-UCbHSYyccOHURW7qOVoAUvzHvYUon5rSd93oMvieoXAYDujMKABnu3eXyiA4v0Y)

**Severity Level**

RFC 5424 defines eight severity levels:

| **Code** | **Severity** | **Description** | **General Description** |
| :--- | :--- | :--- | :--- |
| **0** | **EMERG** | **System is unusable** | **A "panic" condition usually affecting multiple apps/servers/sites. At this level, all tech staff on call would be notified.** |
| **1** | **ALERT** | **Action must be taken immediately** | **This should be corrected immediately; please notify staff who can fix the problem.**  |
| **2** | **CRIT** | **Critical conditions**  | **This should be corrected immediately; please notify staff who can fix the problem.** |
| **3** | **ERROR** | **Error conditions** | **Non-urgent failures, these should be relayed to developers or admins; each item must be resolved within a given time.** |
| **4** | **WARNING** | **Warning conditions** | **Warning messages, not an error, but indication that an error will occur if action is not taken, \(e.g., file system 85% full\). Each item must be resolved within a given time.**  |
| **5** | **NOTICE** | **Normal but significant condition** | **Events that are unusual but not error conditions - might be summarized in an email to developers or admins to spot potential problems - no immediate action required.** |
| **6** | **INFO** | **Informational messages** | **Normal operational messages - may be harvested for reporting, measuring throughput, etc. - no action required.** |

## **Remote Logging**

The internal log of the EWS switch has a fixed capacity; at a certain level, the EWS switch will start deleting the oldest entries to make room for the newest. If you want a permanent record of all logging activities, you can set up your syslog server to receive log contents from the EWS switch. Use this page to direct all logging to the syslog server. Click the Add button, define your syslog server, and select the severity level of events you wish to log.

![](https://lh6.googleusercontent.com/hkJcr9A4oTYwv3D2f4CVs4Q3vgekqJ-cYI3nWIwHuIDLB0H_krod6-F9G3jYNMthBGRp7_QDWEeTmCgDOkbXMngLVwY0S7te5N3Vj5_oLWobWZg2AT0FNJkNs2GR69Va47pThPo)

| Items | Descriptions |
| :--- | :--- |
| **IP/Hostname** | **Specify the IP address or host name of syslog server** |
| **Server Port** | **Specify the port of the syslog server. The default port is 514.** |
| **Severity Level** | **RFC 5424 defines eight severity levels:**   |

![](../../.gitbook/assets/image%20%287%29.png)

|  |  |
| :--- | :--- |
| **Facility** | **The log facility is used to separate out log messages by application or by function, allowing you to send logs to different files in the syslog server. Use the drop-down menu to select local0, local1, local2, local3, local4, local5, local6, or local7.**  |

## **Event Logs**

This page displays the most recent records in the EWS switch's internal log. Log entries are listed in reverse chronological order \(with the latest logs at the top of the list\). Click a column header to sort the contents by that category.

![](https://lh3.googleusercontent.com/MDWUdQny_ECtwuOMF3PlCjwpR_EqI6zT9WSURdSD78M_4983Yttvek_swlUeDwJiOC0Xzk6Wc_3o336ZqtilSWaGWRxv535IbC94vIYq4Gw6iN5srbLt81ooAXRPy8PCGYW1hIk)

#### **Display logs in**　

|  |  |
| :--- | :--- |
| **RAM**                | The information stored in the system’s RAM log will be lost after the switch is rebooted or powered off. |
| **Flash** | The information stored in the system’s Flash will be kept even after the switch is rebooted or powered off. |

#### **Type**

|  |  |
| :--- | :--- |
| **Controller** |  Display controller related logs. |
| **Switch** | Display switch related logs. |
| **Wireless Client** | Display wireless client activities from managed APs. |
| **All** | Display logs from both controller and switch |

**Export**  
Click Export button to export the current buffered log to a .txt file.

**Clear**  
Click Clear button to clear the buffered log in the system's memory.  
  


