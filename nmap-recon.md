<h3> Basic scanning technique</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap target     | Scan a single targets |
| nmap target1 target2      | Scan multiple targets |
| nmap -iL targets.txt | Scan target from list |
| nmap -sn target | Ping scan to determine if host is online |

<h3>Port Spesification</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -p port target | Scan a spesific port |
| nmap -p- target | scan all 65535 port | 
| nmap -F target | Scan most common ports (100) |
| nmap -p 20-100 target | Scan port range of port |

<h3> Service and Version Detection</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -sV target | Service and version detection |
| nmap -A target | Aggressive scan (OS detect, version, scripts) |
| nmap --version-intensity 0-9 target | Adjust version detection intensity |

<h3>Scan Types</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -sS target | SYN scan ( stealth scan) |
| nmap -sT target | Connect scan (TCP) |
| nmap -sU target | UDP scan |
| nmap -sA target | ACK scan |
| nmap -sN target | NULL scan (no flags set) |
| nmap -sF target | FIN scan (fin flag scan) |
| nmap -sX target | XMAS scan ( FIN, URG, and PSH flags are set) |
| nmap -sO target | Protocol scan (Determine supported protocols) |
| nmap -sP target | Ping Scan(no port scan) |

<h3>Scripting Engine</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap --script scriptname target | Run spesific script |
| nmap --script vuln target | Scan for Vulnerabilities using scripts |
| nmap --script help scriptname | Get help for a spesific script |
| nmap --script-updatedb | Update script database |

<h3>Ouput Options</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -oN output.txt target | Save normal output to a file |
| nmap -oX output.xml target | Save ouput in XML format |
| nmap -oG output.grep target | Save output in grepable format |

<h3>Timing & Performance</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -T <0-5> target | Set timing template (0=paranoid, 5=insane) |
| nmap --max-retries 3 target | Set the maximum number of retries |
| nmap --max-scan-delay <time> target | Set maximum delay between probes |
| nmap --min-parallelism <number> target | Set minimum parallelism |

<h3>Timing & Performance</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -f target | Use fragment IP packets |
| nmap --mtu value target | Set MTU to bypass firewall filters |
| nmap --data-length value target | Append random data scan to packets |
| nmap --ip-options options target | Specify IP options to use during scanning |


<h3>Miscellaneous Options</h3>

| Command          | Description                              |
|------------------|------------------------------------------|
| nmap -v target | Increase verbosity ( use multiple times for more ) |
| nmap -d target | Debugging output |
| nmap --stats-every <time> target | Display stats periodically |
| nmap --reason target | Show reason for the port state |
| nmap --traceroute target | Perform traceroute |
| nmap --iflist | List available interfaces |
