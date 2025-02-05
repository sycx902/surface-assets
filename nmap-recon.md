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
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
