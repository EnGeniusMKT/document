# Jumbo Frame

Ethernet has used the 1500-byte frame size since its inception. Jumbo frames are network-layer PDUs that have a size much larger than the typical 1500-byte Ethernet Maximum Transmission Unit \(MTU\) size. Jumbo frames extend Ethernet to 9000 bytes, making them large enough to carry an 8 KB application datagram plus packet header overhead. If you intend to leave the local area network at high speeds, the dynamics of TCP will require you to use large frame sizes.

The switch supports a jumbo frame size of up to 9216 bytes. Jumbo frames need to be configured to work on the ingress and egress port of each device along the end-to-end transmission path. Furthermore, all devices in the network must also be consistent on the maximum jumbo frame size, so it is important to do a thorough investigation of all your devices in the communication paths to validate their settings.

![](https://lh5.googleusercontent.com/a6s_An63YqbFbtjYDNi_pAkujFSyObttASEFcVMu_Dmd3ccqOcinxodyPxHaS3WdNSeLXrdTZJtxMOSDnYsNHuB3vJX0c4KuuLLeT15yYBrZoJUN8jCmw0jEzJ0ZvUIS2WB9LOM)

| Items |  |
| :--- | :--- |
| Jumbo Frame | Enter the size of jumbo frame. The range is from 1522 to 9216 bytes. |

Click **Apply** to update the system settings.

