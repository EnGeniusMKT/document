# Access

HTTP\(S\) Settings

The EnGenius Switch provides a built-in browser interface that enables you to configure and manage the switch via Hypertext Transfer Protocol \(HTTP\) and Hypertext Transfer Protocol Secure \(HTTPS\) requests selectively to help prevent security breaches on the network. You can manage your HTTP and HTTPS settings for the switch further by choosing the length of session timeouts for HTTP and HTTPS requests. Select whether to enable or disable the HTTP service and enter the HTTP Timeout session. Next, select whether to enable or disable the HTTPS service and enter the HTTPS timeout session for the switch.

![](https://lh6.googleusercontent.com/dXSXc6FYYLxQJZ7N9daiiL5UKNV5AMAlmSmGVBqzCjyVs604IwX8kR_-aHarFnVik7ltQfDSpnyFD1GxeT2yx_Z8ZAqQOccijPomB6pPG6MIXOuGZwLkSvNpOjKpLiLYGiw7gaI)

| Items | Descriptions |
| :--- | :--- |
| HTTP Service | Select whether HTTP service for the switch is Enabled or Disabled. This is enabled by default. |
| HTTP Session Timeout | Enter the amount of time that elapses before HTTP is timed out. The default is 5 minutes. The range is from 0 to 86400 minutes. |
| HTTPS Service | Select whether the HTTP service is Enabled or Disabled. This is disabled by default. |
| HTTPS Session Timeout | Enter the amount of time that elapses before HTTPS is timed out. The default is 5 minutes. The range is from 0 to 86400 minutes. |

Click **Apply** to update the system settings.

## **Telnet Settings**

From here, you can configure and manage the switch's Telnet protocol settings. The Telnet protocol is a standard Internet protocol which enables terminals and applications to interface over the Internet with remote hosts by providing Command Line Interface \(CLI\) communication using a virtual terminal connection. This protocol provides the basic rules for making it possible to link a client to a command interpreter. The Telnet service for the switch is enabled by default. Please note that for secure communication, it is better to use SSH over Telnet. To enable and configure SSH settings, please refer to SSH settings on the next page.

![](https://lh6.googleusercontent.com/3lx-UpwFQXw0PDebiL2vV4OsPw1ClYBRcdFVRnLBOZDjTUNkY7-zkCJaj24JwOQwHpF7_JePave9cuvhrVyxARC09aOTq7pH7o32U4i9NO8OK6o-yDT9LLjcefcChhYXNqJ0h7k)

| **Items** | **Descriptions** |
| :--- | :--- |
| Telnet Service | Select whether the Telnet service is Enabled or Disabled. It is enabled by default. |
| Session Timeout | Enter the amount of time that elapses before the Telnet service is timed out. The default is 5 minutes. The range is from 0 to 65535 minutes. |
| History Count | Enter the entry number for history of Telnet service. The default is 128. The range is from 0 to 256. |
| Password Retry Count | Enter the number of password requests send to Telnet service. The default is 3. The range is from 0 to 120. |
| Silent Time | Enter the silent time for Telnet service. The range is from 0 to 65535 seconds. |

Click **Apply** to update the system settings.

## **SSH Settings**

Secure Shell \(SSH\) is a cryptographic network protocol for secure data communication network services. SSH is a way of accessing the command line interface on the network switch. The traffic is encrypted, so it is difficult to eavesdrop as it creates a secure connection within an insecure network such as the Internet. Even if an attacker were able to view the traffic, the data would be incomprehensible without the correct encryption key to decode it.

To configure SSH settings for the switch, first select whether you wish to enable or disable the SSH service for the switch. Note that SSH is more secure than the Telnet service when

deciding which service to use. Enter the session timeout you wish to implement for SSH. Next, enter the History Count number you wish. The default count is: 128. Enter the number of passwords requests to be sent across SSH. The default attempts are: 3. Finally, enter the silent time you wish to implement for the SSH service.

![](https://lh3.googleusercontent.com/V_uW-3WiclKZLIAKKhcsZfdz9-LWsX-XWJz-CPQuXDfpfqHfuwNY5vt8shK2yJTjB-Cte9HX24l-woMaa4wBt2Cj-0evdP6fuud0aykNj8kLsSCHuWfuLfkE_4RhC8T3xS1GpQw)

| Items | Descriptions |
| :--- | :--- |
| SSH Service | Select whether the SSH service is Enabled or Disabled. It is disabled by default. |
| Session Timeout | Enter the amount of time that elapses before the SSH Service is timed out. The default is 5 minutes. The range is from 0-65535 minutes. |
| History Count | Enter the entry number for history of SSH service. The default is 128. The range is from 0 to 256. |
| Password Retry Count | Enter the number of password requests send to SSH service. The default is 3. The range is from 0 to 120. |
| Silent Time | Enter the silent time for SSH service. The range is from 0 to 65535 seconds. |

Click **Apply** to update the system settings.

## **Console Settings**

From here, you can configure the Console service settings for the switch.

![](https://lh4.googleusercontent.com/WeJboPiQouiWleH78L7URluzOOo9kez66b1qLr2575zQMeLNfEw5r4z-2F4lR41xSRlTWF3gIRSztwaSua7zxfofahI8DuXpxOTZyRUlt2_hR25I4ytiAJnjPc5zAA-hj7UBJy8)

| Items | Descriptions |
| :--- | :--- |
| Session Timeout | Enter the amount of time that elapses before Console service is timed out. The default is 5 minutes. The range is from 0 to 65535 minutes. |
| History Count | Enter the entry number for the history of Console service. The default is 128. The range is from 0 to 256. |
| Password Retry Count | Enter the number of password requests to send to the Console service. The default is 3. The range is from 0 to 120. |
| Silent Time | Enter the silent time for Console service. The range is from 0 to 65535 seconds. |

Click **Apply** to update the system settings.  
  
  


