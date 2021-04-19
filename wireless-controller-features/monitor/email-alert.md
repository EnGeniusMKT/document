# Email Alert

## **Alert Settings**

If an alert is detected, the EWS switch will record it in the event log. The EWS switch can also be configured to send email notifications for selected events.

![](https://lh3.googleusercontent.com/SUtCuiVs6DpMvW3jVy-RAeHB6tvmxAsWl7ZbS8RUdxTc4f5Oo_kdc44Jlqx1WMxPEBcqCAcQ7-waAOYb_CVnfXuqwdDu916VIv4qvcXFWmq92TyE9Z-2rw0qnFhpl4Dln81hy_8)

**Mail Alert State:** Select whether to Enable/Disable email notification.

**Mail Information Setting**

* **SMTP Server:** Enter the name of the mail server.
* **SMTP Port:** Enter the SMTP port.
* **SSL/TSL:** Enable this option if your mail server uses SSL/TLS encryption.
* **Authentication:** Select this option to enable authentication.
* **User Name:** Enter the username required by the mail server.
* **Password:** Enter the password required by the mail server.
* **From Mail Address:** Enter the email address that will appear as the sender of the email alert.
* **To Mail Address:** Enter the email address to which the EWS switch will send alarm messages. You can only send alarm messages to a single email address.
* **Subject:** Enter the subject of the email notification.

**Test:** To verify that the EWS switch can send email notifications using the SMTP settings you just configured, please click the Test button for a quick test.

**Apply:** Click **Apply** to save settings.  


## **Event Binding**

Use this page to choose which types of events will trigger the EWS switch to send an email notification. When any of the selected events occur, the EWS switch sends an email notification to the email address that you specified in the Monitoring &gt; Email Alert &gt; Alert Settings section.

![](https://lh3.googleusercontent.com/jYcR-Wsq7Mk3t351sqW3s4Kqng-4JMsevV8tvUBvfbKNsbdY0-RSOzAzzMOZBWVIPope3fntdwprMxzRGbHky_C02srON8blF9HVCma8XxkdUfvBIZVGN4MmYwJDFQdKWz3kdqg)

The table below provides explanations for EWS controller syslog event messages.

| **Event Type**            | **EWS Syslog Message** | **Severity Level** |
| :--- | :--- | :--- |
| **Status of AP         Controller** | **Controller is enabled** | **INFO** |
| **Status of AP Controller** | **Controller is disabled** | **WARNING** |
| **Certificate Changed** | **SSL certificate updated** | **INFO** |
| **Certificate Changed** | **SSL certificate will expire in {value} days** | **WARNING** |
| **Certificate Changed** | **SSL certificate has expired** | **ERROR** |
| **Certificate Changed** | **\[AP Name\] \[AP MAC\]'s SSL certificate has been updated** | **INFO** |
| **AP Managed** | **\[AP Name\] \[AP MAC\] added to management list** | **INFO** |
| **AP Managed** | **\[AP Name\] \[AP IP\] removed from management list** | **INFO** |
| **Status of AP** | **\[AP Name\] \[AP MAC\] online** | **INFO** |
| **Status of AP** | **\[AP Name\] \[AP MAC\] reset** | **INFO** |
| **Status of AP** | **\[AP Name\] \[AP MAC\] offline** | **WARNING** |
| **Status of AP** | **\[AP Name\] \[AP MAC\] has invalid IP \[IP Address\]** | **WARNING** |
| **Status of AP** | **\[AP Name\] \[AP MAC\]'s active client number reaches client limits {value} of \[2.4/5\]GHz** | **WARNING** |
| **AP Configuration Changed** | **\[AP Name\] \[AP MAC\] configuration updated** | **INFO** |
| **AP Firmware** | **\[AP Name\] \[AP MAC\] firmware version is incompatible** | **WARNING** |
| **AP Firmware** | **\[AP Name\] \[AP MAC\] started to upgrade firmware from \[old-ver\] to \[new-ver\]** | **INFO** |
| **AP Firmware** | **\[AP Name\] \[AP MAC\] firmware upgrade failed** | **ERROR** |

  


  


