# ACL Binding

When an ACL is bound to an interface, all the rules that have been defined for the ACL are applied to that interface. Whenever an ACL is assigned on a port or LAG, flows from that ingress or egress interface that do not match the ACL are matched to the default rule of dropping unmatched packets. To bind an ACL to an interface, simply select an interface and select the ACL\(s\) you wish to bind.

![](https://lh5.googleusercontent.com/NtLbL1CudzFj2_IWt7vxcCLPnSekhXDIOV8qBcMhFkWixGu3NfbE9R0vTNPoqAfsj3inUokZbM1l2CzcI8CMQE3ibAWSmeiC-XURApylMKOrs9XuUrn3Avg3qUW-EWHJ2JJch7w)

| Port | Select the port to which the ACLs are bound. |
| :--- | :--- |
| MAC ACL | Select the MAC ACL rule to apply to the port. |
| IPv4 ACL | Select the IPv4 ACL rule to apply to the port. |
| IPv6 ACL | Select the IPv6 ACL rule to apply to the port. |

Click **Apply** to update the system settings.  
****

