# Log

The Syslog protocol allows devices to send event notification messages in response to events, faults, or errors occurring on the platform as well as changes in configuration or other occurrences across an IP network to syslog servers. It then collects the event messages, providing powerful support for users to monitor network operations and diagnose malfunctions. A Syslog-enabled device can generate a syslog message and send it to a Syslog server.

Syslog is defined in RFC 3164. The RFC defines the packet format, content, and system log related information of Syslog messages. Each Syslog message has a facility and severity level. The Syslog facility identifies a file in the Syslog server. Refer to the documentation of your Syslog program for details. The following table describes the Syslog severity levels.

| Code | Severity | Description | General Description |
| :--- | :--- | :--- | :--- |
| 0 | EMERG | System is unusable. | A "panic" condition usually affecting multiple apps/servers/sites. At this level, all tech staff on call would be notified. |
| 1 | ALERT | Action must be taken immediately. | Should be corrected immediately. Therefore, notify staff who can fix the problem. An example would be the loss of a primary ISP connection. |
| 2 | CRIT | Critical conditions.  | Should be corrected immediately but indicates failure in a secondary system; an example is a loss of a backup ISP connection. |
| 3 | ERROR | Error conditions. | Non-urgent failures, which should be relayed to developers or admins; each item must be resolved within a given time. |
| 4 | WARNING | Warning conditions. | Warning messages, not an error, but indication that an error will occur if action is not taken \(e.g. file system 85% full\). Each item must be resolved within a given time.  |
| 5 | NOTICE | Normal but significant condition. | Events that are unusual but not error conditions - might be summarized in an email to developers or admins to spot potential problems - no immediate action required. |
| 6 | INFO | Informational messages | Normal operational messages - may be harvested for reporting, measuring throughput, etc. - no action required. |

## **Global Settings**

From here, you can Enable or Disable the log settings for the switch.

![](https://lh3.googleusercontent.com/Dqhd7QQ_BIxAQUa54rFW5WX8HQzC8b154TVmPI427qOHbmDl9YLFkmRdUIlNFMvk7JgfS54fx0MFIz_7zxns6MDtaxHRSeExwtHfrPWKPFB_dklIJ5YVjBtPzXITfRiXl9wLe50)

Click **Apply** to update the system settings.

## **Local Logging**

The System Log is designed to monitor the operation of the switch by recording the event messages it generates during normal operation. These events may provide vital information about system activity that can help in the identification and solutions of system problems. 

The switch supports log output in two directions: Flash and RAM. The information stored in the system's RAM log will be lost after the switch is rebooted or powered off, whereas the information stored in the system's flash will be kept effective even if the switch is rebooted or powered off. The log has a fixed capacity; at a certain level, the EWS switch will start deleting the oldest entries to make room for the newest.

![](https://lh6.googleusercontent.com/wMEkBpd24LDyJkWha4yzm7SZIwF8-c-ar8iZbY0dpuJmA_ftorNLVVSDLv5OxGKDrqW872jRHAQM_6I7SvX7IKsuXAofGLyzILqlCL7Iz_76dj1sdFjTH6RPSOCHXwu5cL7f6_g)

  
Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the Cancel button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.

## **Remote Logging**

The internal log of the EWS switch has a fixed capacity; at a certain level, the EWS switch will start deleting the oldest entries to make room for the newest. If you want a permanent record of all logging activities, you can set up your syslog server to receive log content from the EWS switch. Use this page to direct all logging to the syslog server. Click the Add button, define your syslog server, and select the severity level of events you wish to log.

![](https://lh6.googleusercontent.com/_31pfP4R6dG2H3KCPKybzzqT1K-xBM2p6A2iK6h_BDi70VVq88_zZJ8sWSeWcKNHRkjk3nAOSDu6knotDdU1Ft6ZgvcJOVD8cj3ObFkSW-fHkbBs4rqRy-eq_DIYIrTOBMaDgWA)

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


## **Event Logs**

This page displays the most recent records in the switch's internal log. Log entries are listed in reverse chronological order \(with the latest logs at the top of the list\). Click a column header to sort the content by that category.

![](https://lh5.googleusercontent.com/VENUPpx1XG10BffvHQDEVFQxJ6cso6y0KFy1ZOpNJ3TOyG4L3E8t2RvpeiAb-VwaQargzf9riym8aST41h9yq5dBjKL51lBVI3XwsNfZe4IeGErAAePLzFV3V3SgDcoEylO2a9U)

### **Display logs in**

* **RAM:** The information stored in the system’s RAM log will be lost after the switch is rebooted or powered off.
* **Flash:** The information stored in the system’s Flash will be kept effective even if the switch is rebooted or powered off.

### **Type**

* **Controller:** Display controller related logs.
* **Switch:** Display switch related logs.
* **Wireless Client**: Display wireless client related logs.
* **All:** Display all above types of logs .

### **Export**

Click the **Export** button to export the current buffered log to a .txt file.

### **Clear**

Click the **Clear** button to clear the buffered log in the system's memory.  


