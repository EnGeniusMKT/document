# Port Settings

Use this screen to view and configure switch port settings. The port settings page allows you change the configuration of the ports on the switch in order to find the best balance of speed and flow control according to your preferences. Configuring Gigabit ports require additional factors to be considered when arranging your preferences for the switch compared to 10/100 ports.

To access the page, click **Port Settings** under the **System** menu.

![](https://lh4.googleusercontent.com/GTDUD7sU5QXirZQNTF69YCAdwDh9IW8Fr4ncGXRur2NCKS5hUuB4zEQHKjgI-c8tLfv6RpuZJsiANF_axr00L-GQV4h34H-jL6QxQKRHPmSobF4nUrtEz2yXIAux5r2HlVe0CqM)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Items</th>
      <th style="text-align:left"><b>Descriptions</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Port</td>
      <td style="text-align:left">Displays the port number.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Link Status</b>
      </td>
      <td style="text-align:left">Indicates whether the link is up or down.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Mode</b>
      </td>
      <td style="text-align:left">
        <p>Select the speed and the duplex mode of the Ethernet connection on this
          port.</p>
        <p>Selecting Auto (auto-negotiation) allows one port to negotiate with a
          peer port automatically to obtain the connection speed and duplex mode
          that both ends support. When auto-negotiation is turned on, a port on the
          switch negotiates with the peer automatically to determine the connection
          speed and duplex mode. If the peer port does not support auto-negotiation
          or turns off this feature, the switch determines the connection speed by
          detecting the signal on the cable and using half duplex mode. When the
          switch&apos;s auto-negotiation is turned off, a port uses the pre-configured
          speed and duplex mode when making a connection, thus requiring you to make
          sure that the settings of the peer port are the same in order to connect.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Flow Control</b>
      </td>
      <td style="text-align:left">
        <p>A concentration of traffic on a port decreases port bandwidth and overflows
          buffer memory causing packet discards and frame losses. Flow Control is
          used to regulate transmission of signals to match the bandwidth of the
          receiving port. The switch uses IEEE 802.3x flow control in full duplex
          mode and backpressure flow control in half duplex mode.</p>
        <p>IEEE 802.3x flow control is used in full duplex mode to send a pause signal
          to the sending port, causing it to temporarily stop sending signals when
          the receiving port memory buffers fill.</p>
        <p>Back Pressure flow control is typically used in half duplex mode to send
          a &quot;collision&quot; signal to the sending port (mimicking a state of
          packet collision) causing the sending port to temporarily stop sending
          signals and resend later.</p>
      </td>
    </tr>
  </tbody>
</table>

  
****Click **Apply** to save settings.

