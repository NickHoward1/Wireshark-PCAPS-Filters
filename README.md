<h1>Wireshark: PCAP's & Filters</h1>

<h2>Description</h2>
In this lab, I showcase the knowledge I’ve gained from completing various tasks on TryHackMe, focusing on the filters I used to find answers and, more importantly, how those filters can be applied to identify anomalies in network traffic.

<h2>Environment</h2>
<ul>
  <li>Virtual Machine with TryHackMe</li>
</ul>

<h2>Tools used</h2>
<ul>
  <li>Wireshark </li>
</ul>

<h2>Project walkthrough</h2>

Filtering by IP allows me to isolate conversations for deeper analysis of an alert triggered in the SOC. I can then examine the PCAP for anomalies and unusual behavior, such as repeated requests with large payloads, communication with unknown external IPs or domains, and traffic to servers that do not align with normal business activity. I would also look for encoded or obfuscated data, as well as regular beaconing intervals that could indicate malware communicating with a C2 server.

<h3>IP filters</h3>

 <p>
<img src= "https://github.com/NickHoward1/ActiveDirectoryLab/blob/f7afa327640c281a09056154470ec06df3c7d032/Screenshot%202026-05-06%20at%2008.19.40.png" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/ActiveDirectoryLab/blob/0f268f6aea0a68cc5b94ba70bbb887ec3c5e7862/Screenshot%202026-05-06%20at%2008.09.46.png" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/ActiveDirectoryLab/blob/94a10d4acdda1c3cfa7a527920a43a3625cd9c2e/Screenshot%202026-05-06%20at%2007.56.44.png" width="250" height="250" /> 
</p>

<h3>Filter examples:</h3>
<b>ip</b> (Shows all IP packets)<br>
<b>ip.addr == 10.10.10.111</b> (Shows all packets containing IP address 10.10.10.111)<br>
<b>ip.addr == 10.10.10.0/24</b> (Shows all packets containing IP addresses from 10.10.10.0/24 subnet)<br>
<b>ip.src == 10.10.10.111</b> (Show all packets originated from 10.10.10.111)<br>
<b>ip.dst == 10.10.10.111</b> (Show all packets sent to 10.10.10.111)

<h3>TCP and UDP Filters</h3>

 <p>
<img src= "https://github.com/NickHoward1/Wireshark-PCAPS-Filters/blob/e3c33a0a630dc894466d5f939ae79c37e7c7a851/Screenshot%202026-05-06%20at%2011.48.34.png" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Wireshark-PCAPS-Filters/blob/4564bed4406829a41943ea32582104ce2f19d945/Screenshot%202026-05-06%20at%2011.57.22.png" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "" width="250" height="250" /> 
</p>

<h3>Filter examples:</h3>
<b>ip</b> (Shows all IP packets)<br>
<b>ip.addr == 10.10.10.111</b> (Shows all packets containing IP address 10.10.10.111)<br>
<b>ip.addr == 10.10.10.0/24</b> (Shows all packets containing IP addresses from 10.10.10.0/24 subnet)<br>
<b>ip.src == 10.10.10.111</b> (Show all packets originated from 10.10.10.111)<br>
<b>ip.dst == 10.10.10.111</b> (Show all packets sent to 10.10.10.111)

<h3>Application Level Protocol Filters - HTTP and DNS</h3>

 <p>
<img src= "" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "" width="250" height="250"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "" width="250" height="250" /> 
</p>

<h3>Advanced Filtering</h3>

Other filters: 

<h3>Questions & Answer in try hack me</h3>


<h3>Notes: How to spot anomalies in Wireshark</h3>

