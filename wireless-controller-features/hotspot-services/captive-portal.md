# Captive Portal

![](https://lh3.googleusercontent.com/E394nQhZgSGcOeQ22v5EO5Ol3wtalx2UxXxc8pRbnn4K_qKBkpbX0dIchs7QY658CaAbi9JrWw3NaJpW0IkQcCqg2I54teL1T_SKA6xodRBVgL-UoSiJHAIyOfOsrZkFXtZwALQ)

* **Login Type:** Defines the mechanism by which a wireless client gains access to the network after the client has associated with the SSID.

| Items | Descriptions |  |
| :--- | :--- | :--- |
| **Splash & Go** | **The wireless client is granted network access without any further authentication as soon as it associates with the SSID.** |  |
| **Local User DB** | **The wireless client is authenticated using the EWS switch's local database \(from Hotspot Service &gt; Guest Account\).** |  |
| **External RADIUS Server** | **The wireless client is authenticated using an external RADIUS server.** |  |
| **Social Login** | **The wireless client is authenticated using his/her social network account.** |  |

* **Network Connection Mode:** Either “Bridged” or “NAT” mode can be chosen: if bridged mode is selected, users will obtain IP addresses from local DHCP server in the same network; on the other hand, if NAT mode is selected, users will get assigned IP addresses from DHCP server of managed AP which his/her wireless client devices connect to. 
* **Login Page:** A splash page is the web page which prompts the user to log in with a username and password or accept a network user policy once the client has associated with the SSID. 

  | **Items** | Descriptions |
  | :--- | :--- |
  | Local Web Page | Use the splash page hosted locally by EWS switch. The local splash page enables administrators to eliminate the need to set up a local web server. Basic customizations like displaying a business logo, custom message, and term of use is available.  |
  | Redirect users to external URL | External splash page enables the administrator to host their own web server for splash page, rather than having it h**osted by the EWS switch.** |

* **Redirect Behavior:** Configure the destination where users will be redirected after successful login. You can redirect them to the page that they want to visit, or you can set a different page where users will be redirected.

| **Items** | Descriptions |
| :--- | :--- |
| Redirect to the URL that the user was trying to visit | Select this option to cache the initial website from the client during the authentication process and then forward it to the originally targeted web server after the user gets successfully authenticated. |
| Redirect to a different URL | Select this option to redirect users to a specific URL after users successfully get authenticated. |

* **User Session:** Configure session timeout and ideal timeout period.

  | **Items** | Descriptions |
  | :--- | :--- |
  | **Enable Session Timeout** | **Specify a time limit after which users will be disconnected and required to log on again.** |
  | **Enable Idle Timeout** | **Specify a time limit for an idle client after which users will be disconnected and required to log on again.** |

* **Walled Garden:** This option allows users to define network destinations that users can access before authentication, for example, your business website.

  


