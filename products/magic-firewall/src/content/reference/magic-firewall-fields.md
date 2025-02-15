---
title: Magic Firewall fields
pcx-content-type: reference
---

# Magic Firewall fields

<table>
  <thead>
   <tr>
      <th style="width: 50%;">Field Name</th>
      <th>Description</th>
   </tr>
  </thead>
  <tbody style='vertical-align:top'>
    <tr>
        <td><p><code>cf.colo.name</code><br /><Type>String</Type></p>
        </td>
        <td>
        The data center that is handling this traffic.  <br />
        Example value: <code class="InlineCode"> sfo06 </code>
        </td>
    </tr>
    <tr>
        <td><p><code>cf.colo.region</code><br /><Type>String</Type></p>
        </td>
        <td>
        Region of the data center that is handling this traffic. <br />
        Example value: <code class="InlineCode"> WNAM </code>
        </td>
    </tr>
    <tr>
        <td><p><code>icmp</code><br /><Type>String</Type></p>
        </td>
        <td>
        The raw ICMP packet as a list of bytes. It should be used in conjunction with the bit_slice function when other structured fields are lacking.
        </td>
    </tr>
    <tr>
        <td><p><code>icmp.type</code><br /><Type>Number</Type></p>
        </td>
        <td>
         The <a href="https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol#header_type">ICMP type</a>. Only applies to ICMP packets. <br />
         Example value:
         <code class="InlineCode">8</code>
        </td>
    </tr>
    <tr>
        <td><p><code>icmp.code</code><br /><Type>Number</Type></p>
        </td>
        <td>
         The <a href="https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol#header_code">ICMP code</a>. Only applies to ICMP packets. <br />
         Example value:
         <code class="InlineCode">2</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip</code><br /><Type>String</Type></p>
        </td>
        <td>
        The raw IP packet as a list of bytes. It should be used in conjunction with the bit_slice function when other structured fields are lacking.
        </td>
    </tr>
    <tr>
        <td><p><code>ip.dst</code><br /><Type>IP Address</Type></p>
        </td>
        <td>
         The destination address as specified in the IP packet. <br />
         Example value:
         <code class="InlineCode">192.0.2.2</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.geoip.country</code><br /><Type>String</Type></p>
        </td>
        <td>
         Represents the 2-letter country code associated with the client IP address in <a href="https://www.iso.org/obp/ui/#search/code/">ISO 3166-1 Alpha 2</a> format.<br />
         Example value:
         <code class="InlineCode">GB</code>
         <p>For more information on the ISO 3166-1 Alpha 2 format, see <a href="https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2">ISO 3166-1 Alpha 2</a> on Wikipedia.</p>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.hdr_len</code><br /><Type>Number</Type></p>
        </td>
        <td>
         The length of the IPv4 header in bytes. <br />
         Example value:
         <code class="InlineCode">5</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.len</code><br /><Type>Number</Type></p>
        </td>
        <td>
         The length of the packet including the header. <br />
         Example value:
         <code class="InlineCode">60</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.opt.type</code><br /><Type>Number</Type></p>
        </td>
        <td>
         The first byte of <a href="https://en.wikipedia.org/wiki/IPv4#Options">IP options field</a>, if the options field is set. <br />
         Example value:
         <code class="InlineCode">25</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.proto</code><br /><Type>String</Type></p>
        </td>
        <td>
        The transport layer for the packet, if it can be determined. <br />
        Example values: <code class="InlineCode">icmp</code>, <code class="InlineCode">tcp</code>
        </td>
    </tr>
    <tr>
        <td><p><code>ip.src</code><br /><Type>IP Address</Type></p>
        </td>
        <td>
        The source address of the IP Packet.
        </td>
    </tr>
    <tr>
        <td><p><code>ip.ttl</code><br /><Type>Number</Type></p>
        </td>
        <td>
        The time-to-live of the IP Packet. <br />
        Example values: <code class="InlineCode">54</code>
        </td>
    </tr>
    <tr>
        <td><p><code>tcp</code><br /><Type>String</Type></p>
        </td>
        <td>
        The raw TCP packet as a list of bytes. It should be used in conjunction with the bit_slice function when other structured fields are lacking.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags</code><br /><Type>Number</Type></p>
        </td>
        <td>
        The numeric value of the TCP flags byte.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.ack</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP acknowledgment flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.cwr</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP congestion window reduced flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.ecn</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP ECN-Echo flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.fin</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP flag indicating this is the last packet from sender.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.push</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP push flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.reset</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP reset flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.syn</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP synchronize flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.flags.urg</code><br /><Type>Boolean</Type></p>
        </td>
        <td>
        TCP urgent flag.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.srcport</code><br /><Type>Number</Type></p>
        </td>
        <td>
        Source port number of the IP packet. Only applies to TCP packets.
        </td>
    </tr>
    <tr>
        <td><p><code>tcp.dstport</code><br /><Type>Number</Type></p>
        </td>
        <td>
        Destination port number of the IP packet. Only applies to TCP packets.
        </td>
    </tr>
    <tr>
        <td><p><code>udp</code><br /><Type>String</Type></p>
        </td>
        <td>
        The raw UDP packet as a list of bytes. It should be used in conjunction with the bit_slice function when other structured fields are lacking.
        </td>
    </tr>
    <tr>
        <td><p><code>udp.dstport</code><br /><Type>Number</Type></p>
        </td>
        <td>
        Destination port number of the IP packet. Only applies to UDP packets.
        </td>
    </tr>
    <tr>
        <td><p><code>udp.srcport</code><br /><Type>Number</Type></p>
        </td>
        <td>
        Source port number of the IP packet. Only applies to UDP packets.
        </td>
    </tr>
  </tbody>
</table>
