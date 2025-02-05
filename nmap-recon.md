<h2> Basic scanning technique</h2>

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
