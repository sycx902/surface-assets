===== Subfinder =====
```
subfinder -d target.com -o subfindresult.txt
```

===== Shodanx =====
```
shodanx subdomain -d target.com -ra -o shodanresult.txt
```

===== Amass =====
```
amass enum -active -norecursive -noalts -d target.com -o amassresult.txt
```
=== Gobuster ===
```
gobuster dns -d cengage.co.in -w /usr/share/wordlists/subdomain_megalist.txt -o gobuster.txt
```
=== crt.sh ===
```
curl -s https://crt.sh/\?q\=\%.$1\&output\=json | jq -r '.[].name_value' | sed 's/\*\.//g' | sort -u | tee -a subs_domain.txt
```
=== alienvault ===
```
curl -s "https://otx.alienvault.com/api/v1/indicators/hostname/domain.com/passive_dns" | jq -r '.passive_dns[]?.hostname' | grep -E "^[a-zA-Z0-9.-]+\.domain\.com$" | sort -u | tee alienvault_subs.txt
```
=== urlscan ===
```
curl -s "https://urlscan.io/api/v1/search/?q=domain:domain.com&size=10000" | jq -r '.results[]?.page?.domain' | grep -E "^[a-zA-Z0-9.-]+\.domain\.com$" | sort -u | tee urlscan_subs.txt
```
=== Web Archive ===
```
curl -s "http://web.archive.org/cdx/search/cdx?url=*.domain.com/*&output=json&collapse=urlkey" | jq -r '.[1:][] | .[2]' | grep -Eo '([a-zA-Z0-9._-]+\.)?domain\.com' | sort -u | tee webarcive_subs.txt
```
