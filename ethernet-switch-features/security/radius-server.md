# Radius Server

RADIUS proxy servers are used for centralized administration. Remote Authentication Dial in User Service \(RADIUS\) is a networking protocol that provides centralized Authentication, Authorization, and Accounting \(AAA\) management for users that connect and use a network service for greater convenience. RADIUS is a server protocol that runs in the application layer, using UDP as transport. The Network switch with port-based authentication and all have a RADIUS client component that communicates with the RADIUS server. Clients connected to a port on the switch must be authenticated by the Authentication server before accessing services offered by the switch on the LAN. Use a RADIUS server to authenticate users trying to access a network by relaying Extensible Authentication Protocol over LAN \(EAPOL\) packets between the client and server. The RADIUS server maintains a user database, which contains authentication information. The switch passes information to the configured RADIUS server, which can authenticate a username and password before authorizing use of the network.

![](https://lh3.googleusercontent.com/ACdtWQVvO_n5fEal70k4vhLX-Nwnw_rhfTXTFE5KDpuzL-izCgWh0vcF6__gTwVmDNBtOiQ7_eV3FolRkLA1-sVSH9kwl3mZBATIbSHgd9HeaBxpQxqkHoD8SpvsdPuF3jpZcj4)

| Items | Description |
| :--- | :--- |
| Index | Displays the index for which RADIUS server is displayed. |
| Server IP | Enter the RADIUS server IP address. |
| Authorized Port | Enter the authorized port number. The default port is 1812. |
| Accounting Port | Enter the name you wish to use to identify this switch. |
| Key String | Enter the key string used for encrypting all RADIUS communication between the device and the RADIUS server. |
| Timeout Reply | Enter the amount of time the device waits for an answer from the RADIUS server before switching to the next server. The default value is 3. |
| Retry | Enter the number of transmitted requests sent to the RADIUS server before a failure occurs. The default is 3. |
| Server Priority | Enter the priority for the RADIUS server. |
| Dead Timeout | Enter the amount of time that the RADIUS server is bypassed for service requests. The default value is 0. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


