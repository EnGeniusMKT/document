# PoE

The PoE Management screen contains system PoE information for monitoring the current power usage and assigns the total amount of power the switch can provide to all its PoE ports. To access the page, click PoE under the System menu.

## **Power Budget**

![](https://lh4.googleusercontent.com/D1ZPRFmCPbOVrj6LK1LaR-RYxAFqLLbOsBQ3KTI6FtDOgGTgX0OZTDJZWEJugX2SemJ3eF1pteroRbIGNK_h9L1zbVQcbpoWdYzUCzto_SiSmHTfOnhglT4t07V_R-mMFwFH1L8)

**Total Power Budget:** Enter the amount of power the switch can provide to all ports.

**Consumed Power:** Displays the total amount of power \(in watts\) currently being delivered to all PoE ports.  


## **PoE Port Settings**

![](https://lh6.googleusercontent.com/klhqfhzyRZl6nFQulgjkvN033y762zjX-5TvgxQSpS0UkH-PqPpEDTwyicfkxWUiuD72AXle4XzbcC6Ovm4bgXihEc73AO7Aj2NQlZnBmrF_JWFgeDFLO-XgUqSjJP-sIdPSY2A)



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
      <td style="text-align:left">Displays the specific port for which PoE parameters are defined. PoE parameters
        are assigned to the powered device that is connected to the selected port.</td>
    </tr>
    <tr>
      <td style="text-align:left">State</td>
      <td style="text-align:left">Displays the active participating members of the trunk group.</td>
    </tr>
    <tr>
      <td style="text-align:left">Member Port</td>
      <td style="text-align:left">
        <p>Enable: Enables the Device Discovery protocol and provides power to the
          device using the PoE module. The Device Discovery protocol lets the device
          discover powered devices attached to device interfaces and learn their
          classification.</p>
        <p>Disable: Disables the Device Discovery protocol and halts the power supply
          delivering power to the device using the PoE module.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Priority</td>
      <td style="text-align:left">
        <p>Select the port priority if the power supply is low. The field default
          is low. For example, if the power supply is running at 99% usage, and port
          1 is prioritized as high, but port 6 is prioritized as low, port 1 is prioritized
          to receive power and port 6 may be denied power.</p>
        <p>Low: Sets the PoE priority level as low.</p>
        <p>Medium: Sets the PoE priority level as medium.</p>
        <p>High: Sets the PoE priority level as high.</p>
        <p>Critical: Sets the PoE priority level as critical.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Class (Auto)</td>
      <td style="text-align:left">
        <p>Shows the classification of the powered device. The class defines the
          maximum power that can be provided to the powered device. The possible
          field values are:</p>
        <p>Class 0: The maximum power level at the Power Sourcing Equipment is 15.4
          Watts.</p>
        <p>Class 1: The maximum power level at the Power Sourcing Equipment is 4.0
          Watts.</p>
        <p>Class 2: The maximum power level at the Power Sourcing Equipment is 7.0
          Watts.</p>
        <p>Class 3: The maximum power level at the Power Sourcing Equipment is 15.4
          Watts.</p>
        <p>Class 4: The maximum power level at the Power Sourcing Equipment is 30
          Watts.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Class (User Defined)</td>
      <td style="text-align:left">Select this option to base the power limit on the value configured in
        the User Power Limit field.</td>
    </tr>
    <tr>
      <td style="text-align:left">User Power Limit</td>
      <td style="text-align:left">
        <p>Set the maximum amount of power that can be delivered by a port.</p>
        <p>Note: The User Power Limit can only be implemented when the Class value
          is set to User-Defined.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Status</td>
      <td style="text-align:left">
        <p>Shows the port&apos;s PoE status. The possible field values are:</p>
        <p>Delivering Power: The device is enabled to deliver power via the port.</p>
        <p>Disabled: The device is disabled from delivering power via the port.</p>
        <p>Test Fail: The powered device test has failed. For example, a port could
          not be enabled and cannot be used to deliver power to the powered device.</p>
        <p>Testing: The powered device is being tested. For example, a powered device
          is tested to confirm it is receiving power from the power supply.</p>
        <p>Searching: The device is currently searching for a powered device. Searching
          is the default PoE operational status.</p>
        <p>Fault: The device has detected a fault on the powered device when the
          port is forced on. For example, the power supply voltage is out of range,
          a short occurs, there is a communication error with PoE devices, or an
          unknown error occurs.</p>
      </td>
    </tr>
  </tbody>
</table>

Click **Apply** to save settings.

