# SNMP

Simple Network Management Protocol \(SNMP\) is an application layer protocol designed specifically for managing and monitoring network devices. Simple Network Management Protocol \(SNMP\) is a popular protocol for network management. It is used for collecting information from and configuring network devices such as servers, printers, hubs, switches, and routers on an Internet Protocol \(IP\) network. SNMP is used to exchange management information between a network management system \(NMS\) and a network device. A manager station can manage and monitor the switch through their network via SNMPv1, v2c and v3. An SNMP managed network consists of two components: agents and a manager.

An agent translates the local management information from the managed switch into a form that is compatible with SNMP. SNMP allows a manager and agents to communicate with each other for the purpose of accessing Management Information Bases \(MIBs\). SNMP uses an extensible design, where the available information is defined by MIBs. MIBs describe the structure of the management data of a device subsystem; they use a hierarchical namespace containing Object Identifiers \(OID\). Each OID identifies a variable that can be read or set via SNMP.

The manager is the console through which network administrators perform network management functions.

Several versions of SNMP are supported. They are v1, v2c, and v3. SNMPv1, which is defined in RFC 1157. "A Simple Network Management Protocol \(SNMP\)" is a standard that defines how communication occurs between SNMP-capable devices and specifies the SNMP message types. Version 1 is the simplest and most basic of versions. There may be times when it's required to support older hardware. SNMPv2c is defined in RFC 1901 "Introduction to Community-Based SNMPv2," RFC 1905 "Protocol Operations for Version 2 of the Simple Network Management Protocol \(SNMPv2\)", and RFC 1906 "Transport Mappings for Version 2 of the Simple Network Management Protocol \(SNMPv2\)." SNMPv2c updates protocol operations by introducing a GetBulk request and authentication based on community names. Version 2c adds several enhancements to the protocol such as support for "Informs." Because of this, v2c has become the most widely used version. Unfortunately, a major weakness of v1 and v2c is security. To combat this, SNMP v3 adds security features that overcome the weaknesses in v1 and v2c. If possible, it is recommended that you use v3, especially if you plan to transmit sensitive information across unsecured links. However, the extra security feature makes configuration a little more complex.

In SNMPv3, User-based Security Model \(USM\) authentication is implemented along with encryption, allowing you to configure a secure SNMP environment. The SNMPv3 protocol uses different terminology than SNMPv1 and SNMPv2c as well. In the SNMPv1 and SNMPv2c protocols, the terms agent and manager are used. In the SNMPv3 protocol, agents, and managers are renamed to entities. With the SNMPv3 protocol, you create users and determine the protocol used for message authentication as well as if data transmitted between two SNMP entities is encrypted.

The SNMPv3 protocol supports two authentication protocols: HMAC-MD5-96 \(MD5\) and HMAC-SHA-96 \(SHA\). Both MD5 and SHA use an algorithm to generate a message digest. Each authentication protocol authenticates a user by checking the message digest. In addition, both protocols use keys to perform authentication. The keys for both protocols are generated locally using the Engine ID and the user password to provide even more security.

In SNMPv1 and SNMPv2c, user authentication is accomplished using types of passwords called community strings, which are transmitted in clear text and not supported by authentication. Users can assign views to community strings that specify which MIB objects can be accessed by a remote SNMP manager.

The default community strings for the switch used for SNMPv1 and SNMPv2c management access for the switch are public, which allows authorized management stations to retrieve MIB objects, and private, which allows authorized management stations to retrieve and modify MIB objects.

## **Global Settings**

Simple Network Management Protocol \(SNMP\) is an OSI Layer 7 \(application layer\) protocol designed specifically for managing and monitoring network devices. The SNMP agents maintain a list of variables that are used to manage the device. The variables are defined in the Management Information Base \(MIB\), which provides a standard presentation of the information controlled by the on-board SNMP agent.

![](https://lh4.googleusercontent.com/-2dhbu8tPtHplJfcRPFTAJ-r13q5pn6fYfy1CRpuRuGXmTrisj3xomgiuevWGIPYGwKvBs-fwwvc4iRntO2bgT3BuPPqwbPaYfTFsuLU0uFMwlpQI2EK281j4AkE_tQskT2Lpnw)

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Items</b>
      </th>
      <th style="text-align:left">descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SNMP State</td>
      <td style="text-align:left">Enables or disables the SNMP function. The default SNMP global state is:
        Enabled.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Local Engine ID</p>
        <p>(10-64 hex characters)</p>
      </td>
      <td style="text-align:left">Enter the switch&apos;s Engine ID for the remote clients. A SNMPv3 engine
        is an independent SNMP agent that resides on the switch. This engine protects
        against message replay, delay, and redirection issues. The engine ID is
        also used in combination with user passwords to generate security keys
        for authenticating and encrypting SNMPv3 packets. Normally, a local engine
        ID is automatically generated that is unique to the switch. This is referred
        to as the default engine ID. If the local engine ID is deleted or changed,
        all local SNMP users will be cleared, and you will need to reconfigure
        all existing users.</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.

## **View List**

SNMP uses an extensible design, where the available information is defined by Management Information Bases \(MIBs\). MIBs describe the structure of the management data of a device subsystem; they use a hierarchical namespace containing Object Identifiers \(OID\) to organize themselves. Each OID identifies a variable that can be read or set via SNMP. The SNMP View List is created for the SNMP management station to manage MIB objects.

Click the **Add** button to create a new entry.

![](https://lh5.googleusercontent.com/uTivNB0fMreEM-rJ1Wsst6PHbsIIsXxuEUY-oEocf7AOv-iTzNn2_MztHl5pJZnDS-IY8-GWakUnp1cwPxqHQRoS4ilbnOELs-WXQmU7iC6-nEYjDvSbp_kORkaLr-TsmecGT58)

| View Name | Enter the view name. The view name can contain up to 30 alphanumeric characters. |
| :--- | :--- |
| Subtree OID | Enter the Object Identifier \(OID\) Subtree. The OID identifies an object tree \(MIB tree\) that will be included or excluded from access by an SNMP manager. Note that the first character must be a period \(.\). Wild cards can be used to mask a specific portion of the OID string using a period \(.\). |
| Subtree Mask | Select **0** or **1** for Subtree mask. The mask of the Subtree OID 1 means this object number "is concerned", and 0 means "do not concern," |
| View Type | Select whether the defined OID branch within MIB tree will be Included or **Excluded** from the selected SNMP view. Generally, if the view type of an entry is **Excluded**, another entry of view type Included should exist and its OID subtree should overlap the **Excluded** view entry. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


## **Group List**

Configure SNMP groups to control network access on the switch by providing users in various groups with different management rights via the Read View, Write View, and Notify View options.  


![](https://lh4.googleusercontent.com/ZOB6_ZZ8DjxbiRMII9Xg0qprnaNxm8IkQzCLO3W7U-EUldnLLAj73Li8SbfLE7nlbW_pYoNCeqHB_zzi1yu1dTy7jjAv-lbeCwMc0qEEK8qs4RgG0lhOVKNiShRPiIe7XBUaEzQ)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Group Name</th>
      <th style="text-align:left">Enter the group name to which access control rules are applied. The group
        name can contain up to 30 alphanumeric characters.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Security Mode</td>
      <td style="text-align:left">Select the SNMP version (v1, v2c, v3) associated with the group.</td>
    </tr>
    <tr>
      <td style="text-align:left">Security Level</td>
      <td style="text-align:left">
        <p>Select the security level for the group. Security levels apply to SNMPv3
          only.</p>
        <p>No Auth: Neither authentication nor the privacy security levels are assigned
          to the group.</p>
        <p>Auth: Authenticates SNMP messages.</p>
        <p>Priv: Encrypts SNMP messages.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Read View</td>
      <td style="text-align:left">Management access is restricted to read-only.</td>
    </tr>
    <tr>
      <td style="text-align:left">Write View</td>
      <td style="text-align:left">Select an SNMP to allow SNMP write privileges to the switch&apos;s SNMP
        agent.</td>
    </tr>
    <tr>
      <td style="text-align:left">Notify View</td>
      <td style="text-align:left">Select a SNMP group to receive SNMP trap messages generated by the switch&apos;s
        SNMP agent.</td>
    </tr>
  </tbody>
</table>

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


## **Community List**

In SNMPv1 and SNMPv2c, user authentication is accomplished using types of passwords called community strings, which are transmitted in clear text and not supported by authentication. It is important to note that the community name can limit access to the SNMP agent from the SNMP network management station, functioning as a password.

Click **Add** to add a community list to the switch. Next, name the community and choose the level of access that will be granted to the specified list from the drop-down boxes.

![](https://lh4.googleusercontent.com/jhzeWNzFjN-S1KsLbXMvU8peGv4_hPZNIicO6CpV7vBzMJuPFoXBOjFhda9PGRHf-nS3mfWTqYEbN9SSoiVUwSR3FsuRGBqhL0PbxUyuDAI2VQHmewBGwgWeMPb5HU5rfHs-hqE)

| **Items** | **Descriptions** |
| :--- | :--- |
| Community Name | Enter the name of SNMP community string. |
| Community Mode | Selected Basic or Advance from the list. Select the Advance attached to the SNMP group. |
| Group Name | Select the SNMP group from a list. |
| View Name | Select the view name from a list. |
| Access Rights | Specify the level of permission for the MIB objects accessible to the SNMP. Your choices are Read/Write or Read-only. |

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  
****

## **User List**

Use the User List page to create SNMP users for authentication with managers using SNMP v3 to associate them to SNMP groups. Click Add to add a new user.

![](https://lh4.googleusercontent.com/xz8m4YbpRvTVmc5qP6Fnxd6KbX4Gakup3Y_fyBxrMCugQvwClnTtr8YSTkY4P5eQa75ck2lCTaNS58aikg1jTxv-FWdwftIile9QKO343LcTnUH6baGo6cRdQY-lLYf1yjDxRv8)

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Privilege Mode</td>
      <td style="text-align:left">
        <p>Select<b> No Auth, Auth, or Priv</b> security level from the list.</p>
        <p><b>No Auth:</b> Neither authentication nor the privacy security levels
          are assigned to the group.</p>
        <p><b>Auth:</b> Authenticates and ensures that the origin of the SNMP message
          is authenticated.</p>
        <p><b>Priv: </b>Encrypts SNMP messages.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Authentication Protocol</td>
      <td style="text-align:left">
        <p>Select the method used to authenticate users.</p>
        <p><b>MD5:</b> Using the HMAC-MD5 algorithm.</p>
        <p><b>SHA: </b>Using the HMAC-SHA-96 authentication level. Enter the SHA
          password and the HMAC-SHA-96 password to be used for authentication.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Authentication Password</td>
      <td style="text-align:left">Enter MD5 password and the HMAC-MD5-96 password to be used for authentication.</td>
    </tr>
    <tr>
      <td style="text-align:left">Encryption Protocol</td>
      <td style="text-align:left">
        <p>Select the method used to authenticate users.</p>
        <p><b>None:</b> No user authentication is used.</p>
        <p><b>DES: </b>Using the Data Encryption Standard algorithm.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Encryption Key</td>
      <td style="text-align:left">Enter the Data Encryption Standard key.</td>
    </tr>
  </tbody>
</table>

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the Cancel **button** ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them.  


## **Trap Settings**

A trap is a type of SNMP message. The switch can send traps to an SNMP manager when an event occurs.

You can restrict user privileges by specifying which portions of the MIBs that a user can view. In this way, you restrict which MIBs a user can display and modify for better security. In addition, you can restrict the types of traps users can send as well. You can do this by determining where messages are sent and what types of messages can be sent per user. Traps indicating status changes can be issued by the switch to the specified trap manager by sending authentication failure messages and other trap messages.

![](https://lh3.googleusercontent.com/YIKprMOJkuwf9D0n9XJv_alsSnmyYWpw9YPNu7BQ6EXfyWTvzXNk3JD4BYhfVAke3JOolpVBGP33gtzy7fHd6VWx3XSLrY-MRtIQXp6HnIEfUo0Kc2E_J5SxAtfBtQo0zzr07j0)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left">Descriptions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Server IP/Hostname</td>
      <td style="text-align:left">Enter the server IP or Hostname. The Hostname can contain up to 128 alphanumeric
        characters.</td>
    </tr>
    <tr>
      <td style="text-align:left">SNMP Version</td>
      <td style="text-align:left">Select the SNMP version from the list.</td>
    </tr>
    <tr>
      <td style="text-align:left">Notify Type</td>
      <td style="text-align:left">
        <p>Select the type of notification to be sent.</p>
        <p>Traps: Traps are sent.</p>
        <p>Informs: Informs are sent ONLY when v2c is enabled.</p>
        <p><b>Note:</b>
        </p>
        <p><b>The recipient of a trap message does not send a response to the switch. Traps are therefore not as reliable as inform messages, which include a request for acknowledgment of receipt. Inform messages can be used to ensure that critical information is received by the host. However, please note that informs consume more system resources because they must be kept in memory until a response is received. Informs also add to network traffic. You should consider these effects when deciding whether to issue notifications as traps or informs.</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Community Name</td>
      <td style="text-align:left">Select the Community Name from the list.</td>
    </tr>
    <tr>
      <td style="text-align:left">UDP</td>
      <td style="text-align:left">Enter the UDP port used to send notifications.</td>
    </tr>
    <tr>
      <td style="text-align:left">Timeout</td>
      <td style="text-align:left">Configurable only if the notify type is Informs. Enter the amount of time
        the device waits before re-sending. The default is 15 seconds.</td>
    </tr>
    <tr>
      <td style="text-align:left">Retry</td>
      <td style="text-align:left">Configurable only if the notify type is Informs. Enter the amount of time
        the device waits before re-sending an inform request. The default is 3
        seconds.</td>
    </tr>
  </tbody>
</table>

Click the **Apply** button ![](https://lh4.googleusercontent.com/XMTT8fQ_7-ZeiTvPvRukhv4L0AWct-vSxOhJ3FoFWDUz8lDDOjnB8z3TS4i_dfpCcqDBxi9QK4HLZqqmzieIB9UCQ1h53_LAGhePHU3Qf2lhtLDRweUMCw4lAm_zW7gnMjcOFfg) to accept the changes or the **Cancel** button ![](https://lh4.googleusercontent.com/jJmheoNlaq72LJAXVDSIwNSMs0tSJ8vbDx8UOLAI0IBsDdBZIIDh3GYCbel72dhgAeKuBGcf3SZ3GtC3LCTu9yuKIXTWrYmvZ9c6qgWAr1IfYNoN98KfsdWYobvrFEqGe7xpwYo) to discard them**.**  


