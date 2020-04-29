<h3>NMAP Commands</h3>
<p>Nmap (“Network Mapper”) is a free and open source utility for network discovery and security auditing. Many systems and network administrators also find it useful for tasks such as network inventory, managing service upgrade schedules, and monitoring host or service uptime. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running, what type of packet filters/firewalls are in use, and dozens of other characteristics. It was designed to rapidly scan large networks, but works fine against single hosts. Nmap runs on all major computer operating systems, and official binary packages are available for Linux, Windows, and Mac OS X.</p>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>nmap -v -sS -A -T4 target</td>
<td>Nmap verbose scan, runs syn stealth, T4 timing (should be ok on LAN), OS and service version info, traceroute and scripts against services</td>
</tr>
<tr>
<td>nmap -v -sS -p–A -T4 target</td>
<td>As above but scans all TCP ports (takes a lot longer)</td>
</tr>
<tr>
<td>nmap -v -sU -sS -p- -A -T4 target</td>
<td>As above but scans all TCP ports and UDP scan (takes even longer)</td>
</tr>
<tr>
<td>nmap -v -p 445 –script=smb-check-vulns<br>
–script-args=unsafe=1 192.168.1.X</td>
<td>Nmap script to scan for vulnerable SMB servers – WARNING: unsafe=1 may cause knockover</td>
</tr>
<tr>
 <td>nmap localhost</td>
 <td>Displays all the ports that are currently in use</td>
 </tr>
 <tr>
<td>ls /usr/share/nmap/scripts/* | grep ftp</td>
<td>Search nmap scripts for keywords</td>
</tr>
</tbody>
</table>
<h2>SMB enumeration</h2>
<p>In computer networking, Server Message Block (SMB), one version of which was also known as Common Internet File System (CIFS, /ˈsɪfs/), operates as an application-layer network protocol mainly used for providing shared access to files, printers, and serial ports and miscellaneous communications between nodes on a network</p>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>nbtscan 192.168.1.0/24</td>
<td>Discover Windows / Samba servers on subnet, finds Windows MAC addresses, netbios name and discover client workgroup / domain</td>
</tr>
<tr>
<td>enum4linux -a target-ip</td>
<td>Do Everything, runs all options (find windows client domain / workgroup) apart from dictionary based share name guessing</td>
</tr>
</tbody>
</table>
<h3>Other Host Discovery</h3>
<p>Other methods of host discovery, that don’t use nmap…</p>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>netdiscover -r 192.168.1.0/24</td>
<td>Discovers IP, MAC Address and MAC vendor on the subnet from ARP, helpful for confirming you’re on the right VLAN at $client site</td>
</tr>
</tbody>
</table>
