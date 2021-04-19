# IPv4 ACE



Use this page to view and add rules to IPv4-based ACLs.

![](https://lh3.googleusercontent.com/BhGIJE6tUStgDzf4itljpA2VuNTXlNzB5db2yF5FWU31I6Sbhm9N1hvK6rWgUbya98RhA_oWBLTF_XmQodEQy5WskeH99_Jct3Zjh7MA8oiTyoH0iDbFjyKouCGqdGzf4IdNoIU)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ACL Name</th>
      <th style="text-align:left">Select the ACL from the list for which a rule is being created.</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Sequence</td>
      <td style="text-align:left">Enter the sequence number which signifies the order of the specified ACL
        relative to other ACLs assigned to the selected interface. The valid range
        is from <b>1 to 2147483647</b>, 1 being processed first.</td>
    </tr>
    <tr>
      <td style="text-align:left">Action</td>
      <td style="text-align:left">
        <p>Select what action to take if a packet matches the criteria.</p>
        <p>Permit: Forwards packets that meet the ACL criteria.</p>
        <p><b>Deny:</b> Drops packets that meet the ACL criteria.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Protocol</td>
      <td style="text-align:left">
        <p>Select Any, Protocol ID, or Select from a List in the drop-down menu.</p>
        <p>Any: Check Any to use any protocol.</p>
        <p>Protocol ID: Enter the protocol in the ACE to which the packet is matched.</p>
        <p>Select from List: Selects the protocol from the list in the provided field.</p>
        <ul>
          <li><b>ICMP:</b> Internet Control Message Protocol (ICMP). The ICMP enables
            the gateway or destination host to communicate with the source host.</li>
          <li><b>IPinIP</b>: IP in IP encapsulates IP packets to create tunnels between
            two routers. This ensures that the IP in IP tunnel appears as a single
            interface, rather than several separate interfaces.</li>
          <li><b>TCP: </b>Transmission Control Protocol (TCP). Enables two hosts to
            communicate and exchange data streams. TCP guarantees packet delivery and
            guarantees that packets are transmitted and received in the order they
            are sent. EGP Exterior Gateway Protocol (EGP). Permits exchanging routing
            information between two neighboring gateway hosts in an autonomous systems
            network.</li>
          <li><b>IGP:</b> Interior Gateway Protocol (IGP). Enables a routing information
            exchange between gateways within an autonomous network.</li>
          <li><b>UDP: </b>User Datagram Protocol (UDP). UDP is a communication protocol
            that transmits packets but does not guarantee their delivery.</li>
          <li><b>HMP:</b> The Host Mapping Protocol (HMP) collects network information
            from various network hosts. HMP monitors hosts spread over the Internet
            as well as hosts in a single network.</li>
          <li><b>RDP: </b>Reliable Data Protocol (RDP). Provides a reliable data transport
            service for packet-based applications.</li>
          <li><b>IPv6:</b> Matches the packet to the IPV6 protocol.</li>
          <li><b>IPv6</b>: Rout: Routing Header for IPv6.</li>
          <li><b>IPv6:</b> Frag: Fragment Header for IPv6.</li>
          <li><b>RVSP:</b> Matches the packet to the ReSerVation Protocol(RSVP).</li>
          <li><b>IPv6:</b> ICMP: The Internet Control Message Protocol (ICMP) allows
            the gateway or destination host to communicate with the source host.</li>
          <li><b>OSPF:</b> The Open Shortest Path First (OSPF) protocol is a link-state
            hierarchical interior gateway protocol (IGP) for network routing Layer
            Two (2) tunneling protocols. It is an extension to the PPP protocol that
            enables ISPs to operate Virtual Private Networks (VPNs).</li>
          <li><b>PIM: </b>Matches the packet to Protocol Independent Multicast (PIM).</li>
          <li><b>L2TP: </b>Matches the packet to Internet Protocol (L2IP).</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Source IP Address Value</td>
      <td style="text-align:left">Enter the source IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Source IP Mask</td>
      <td style="text-align:left">Enter the mask of the new source IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination IP Address Value</td>
      <td style="text-align:left">Enter the destination IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination IP Mask</td>
      <td style="text-align:left">Enter the mask of the new source IP address.</td>
    </tr>
    <tr>
      <td style="text-align:left">Type of Service</td>
      <td style="text-align:left">Select<b> Any</b> or<b> DSCP to match</b> from drop-down list. When<b> DSCP to match</b> is
        selected, enter the DSCP. The range is from 0 to 63.</td>
    </tr>
    <tr>
      <td style="text-align:left">ICMP Type</td>
      <td style="text-align:left">
        <p>Select <b>Any, Protocol ID, or Select from List </b>from drop-down menu.</p>
        <p><b>Protocol ID: </b>Enter the protocol in the ACE to which the packet
          is matched. The range is from 0 to 255.</p>
        <p><b>Select from List: </b>Select the ICMP from the list in the provided
          field.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ICMP Code</td>
      <td style="text-align:left">Select Any or User Defined from drop-down menu. When User Defined is selected,
        enter the ICMP code value. The range is from 0 to 255.</td>
    </tr>
  </tbody>
</table>

Click **Apply** to update the system settings.  


