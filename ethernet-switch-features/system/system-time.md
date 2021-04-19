# System Time

Use the System Time screen to view and adjust date and time settings.The switch supports Simple Network Time Protocol \(SNTP\). SNTP ensures accurate network device clock time synchronization up to the millisecond. Time synchronization is performed by a network SNTP server. This switch operates only as an SNTP client and cannot provide time services to other systems.

![](https://lh5.googleusercontent.com/uE0-LeHPZJANClZv872vlFM-LxLYy8AHcbdXyEA3sXKFznHH4cMjkPTbOYdWqS7fes1eRULXENp_3-tR1Ae6ZV7SIPGxRToui9k0q0Buc8m4dfeVCV4exSp38ItWTtXevgxc3Ec)

| Items | **Descriptions** |
| :--- | :--- |
| Current time | Displays the current system time. |
| Enable SNTP | Select whether to enable or disable system time synchronization with an SNTP server. |
| Time Zone | Configure the time zone setting either by setting GMT difference or by country. |
| Daylight Savings Time | Select from Disabled, Recurring or Non-recurring. |
| Daylight Savings Time Offset | Enter the time of Daylight Savings Time Offset. |
| Recurring From | Select the Day, Week, Month, and Hour from the list. |
| Recurring To | Select the Day, Week, Month, and Hour from the list. |
| SNTP/NTP Server Address | Enter the IP address or hostname of the SNTP/NTP server. |
| Server Port | Enter the server port of the SNTP/NTP server. |

**To configure date/time through SNMP:**

1. Next to the Enable SNTP, select Enable.
2. In the Time Zone Offset list, select by country or by the GMT time zone where the switch is located.
3. Next select Disabled, Recurring, or Non-Recurring for Daylight Savings Time. Daylight saving is a period from late Spring to early Fall when many countries set their clocks forward or backward by one hour to give more daytime light in the evening.
4. In the SNTP/NTP Server Address field, enter the IP address or the host name of the SNTP/NTP server.
5. Finally, enter the port number on the SNTP server to which SNTP requests are sent. The valid range is from 1–65535. The default is: 123.
6. Click Apply to update the system settings.

**To configure date/time manually:**

1. Next to the Enable SNTP, select Disable.
2. In the Manual Time field, use the drop-down boxes to manually select the date and time you wish to set.
3. In the Time Zone Offset list, select by country or by the Coordinated Universal Time \(UTC/GMT\) time zone in which the switch is located.
4. Next select Disabled, Recurring or Non-recurring for Daylight Savings Time. Daylight saving is a period from late Spring to early Fall when many countries set their clocks forward or backward by one hour to give more daytime light in the evening.
5. Click Apply to update the system settings.

